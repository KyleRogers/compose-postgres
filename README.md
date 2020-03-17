# Postgresql & PgAdmin powered by compose

This is a fork of https://github.com/khezen/compose-postgres currently primarily maintained at https://github.com/KyleRogers/compose-postgres

## Requirements:
* docker >= 17.12.0+
* docker-compose

## Quick Start
* Clone or download this repository
* Go inside the project directory,  e.g. `cd pg-local`
* Create an empty file `.env` and add your own configuration (see Environments) inside
* Run docker compose up command: `docker-compose up -d`


## Environments
This Compose file contains the following environment variables:

* `POSTGRES_USER` the default value is **postgres**
* `POSTGRES_PASSWORD` the default value is **changeme**
* `PGADMIN_PORT` the default value is **5050**
* `PGADMIN_DEFAULT_EMAIL` the default value is **pgadmin4@pgadmin.org**
* `PGADMIN_DEFAULT_PASSWORD` the default value is **admin**

### Using `.env` file
Docker Compose has a feature which allows you to store environment variables inside an environment file called `.env`.
This file is intentionally added to `.gitignore` because it will contain your personal configuration and passwords.

You can create an `.env` file with the following contents:

```shell
POSTGRES_USER=postgres
POSTGRES_PASSWORD=changeme
PGADMIN_PORT=5050
PGADMIN_DEFAULT_EMAIL=pgadmin4@pgadmin.org
PGADMIN_DEFAULT_PASSWORD=admin
```

This allows you to visit pgadmin under http://localhost:5050 and login with the given email and password above.


## Access to postgres: 
* `localhost:5432`
* **Username:** postgres (as a default)
* **Password:** changeme (as a default)

## Access to PgAdmin: 
* **URL:** `http://localhost:5050`
* **Username:** pgadmin4@pgadmin.org (as a default)
* **Password:** admin (as a default)

## Add a new server in PgAdmin:
* **Host name/address** `postgres`
* **Port** `5432`
* **Username** as `POSTGRES_USER`, by default: `postgres`
* **Password** as `POSTGRES_PASSWORD`, by default `changeme`
