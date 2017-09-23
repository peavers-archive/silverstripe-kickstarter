# Silverstripe Kickstarter
A rapid development environment for working with Silverstripe 4 using docker-compose, requires nothing to be installed
on your local development box other than [docker-compose](https://docs.docker.com/compose/install/).

## Get started

#### Clone the project
```bash
git clone https://github.com/peavers/silverstripe-kickstarter.git
```

#### Start the servers
```bash
cd silverstripe-kickstarter && \
docker-compose up -d
```

#### Install/Update Silverstripe
```bash
docker exec -it php.development /bin/bash

sudo -u www-data /usr/local/bin/composer update -d /var/www/html/

exit
```

Access the site at `http://localhost/` (admin:admin to login)

## Why git ignore everything but? 
When `composer update` runs it will load the project directory with the complete Silverstripe
CMS and framework. These things shouldn't be committed to your project. Remember to specificly include files 
you want to keep.

## Variables
Check the .env for database credentials. 

## Warning
Don't use this in production! 
