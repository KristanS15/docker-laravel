# docker-laravel

-----

After installing Docker Desktop from https://www.docker.com/products/docker-desktop

-----

Setup

```
# clone the repo
$ git clone https://github.com/KristanS15/docker-laravel.git docker-laravel

# go into app's directory
$ cd docker-laravel

# create env file
$ cp .env.example .env

# create docker images and containers
$ docker-compose up

# check docker containers are running
$ docker-compose ps

# check the database ip and potentially set the .env host 
$ docker inspect docker-laravel_db --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}'

# connect to the docker container bash terminal
$ docker exec -it docker-laravel_web /bin/bash

# run migrations
$ php artisan migrate
```

-----

Go to http://localhost:9000 to view the site.
