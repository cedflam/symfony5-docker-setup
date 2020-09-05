# symfony5-docker-setup

### This set of files makes it possible to obtain a functional configuration (without doubt improving) of Docker containers embedding PHP7.4, Mysql 8.0, PHPMyAdmin, Nginx.
### You also have the option of installing Node.js. To do this, once your Symfony project is created, install the Encore pack.

1) Build the containers:
        -> docker-compose up -d --build

2) Start a PHP bash:
        -> docker exec -it php74-container bash

3) Create the project:
        -> composer create-project symfony / website-skeleton project-name

4) Install the dependencies necessary for the project
        -> composer require dependance-name

5) Check that the environment is ok for Symfony
        -> symfony check: req

6) Edit the file. env to configure the database
        -> DATABASE_URL = mysql: // root: secret @ mysql8-service: 3306 / dbname? ServerVersion = 8

7) Create the database
        -> docker-compose run --rm php74-service php bin / console doctrine: database: create

* Load view in browser -> localhost:80
* Load phpMyAdmin -> localhost:8080
        
### All contributions are welcome :-)

### Good Dev ;-)

