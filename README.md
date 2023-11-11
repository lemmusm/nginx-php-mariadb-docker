# Docker project with nginx, php and mariadb

## Prerequisites

- Docker desktop
- A project directory
- Terminal or an IDE with integrated CLI (e.g. Visual Code)

## Checklist

- Create folder structure
- Create the /docker-compose.yml
- Create the /nginx/Dockerfile
- Create the /nginx/default.conf
- Create the /php/Dockerfile
- Run containers
- Check if containers are running

## Create folder structure

<img width="239" alt="Screenshot 2023-11-09 at 12 24 42 a m" src="https://github.com/lemmusm/nginx-php-mariadb-docker/assets/17265234/315a1b23-d64d-4529-a9fe-34224c0588ba">

## Run containers

`docker-compose up -d`

## Check if containers are running

`docker ps -f name=container_name`

## Check if containers are running

Visit [http://localhost:8888](http://localhost:8080) — You should see the PHP info page.

Visit [http://localhost:8889](http://localhost:8081) — You should see the PMA login page, logon with the MySQL credentials you provided in the docker-composer.yml file.

## Connect via database manager

```
    hostname: 0.0.0.0
    user: root
    password: ****
```

Visit [http://localhost:8888](http://localhost:8080) — You should see the PHP info page.

Visit [http://localhost:8889](http://localhost:8081) — You should see the PMA login page, logon with the MySQL credentials you provided in the docker-composer.yml file.

## Stop containers

In the terminal where executed the command to run the containers now execute `CTRL-C` to stop them

## Display running containers

`docker ps`

## Inspect containers

`docker inspect container_name`

## Recreate containers

`docker compose up -d --force-recreate`

## Turn off containers

`docker-compose down`

## Delete container

`docker volume rm container_name`
