# Docker_Ingestion

## Introduction

- This project creates a postgresql database, downloads data, transforms it and uploads it into the database. The database will be accessed with PgAdmin.
- We'd be making use of docker containers.

## Docker Containers
- The postgresql database container was created using the official Postresql docker image.
- The [Pgadmin webserver](https://www.pgadmin.org/) (for interactig with the postgresql database) is created from the official pgadmin docker image.
- Docker-compose file was used to create the containers in the same network to ensure communication between containers.
- The postgresql database in the container was bound to a persistent ocal volume to preserve data even after the container is restarted.

## Download and Transformation of Data
The [NYC taxi trip data](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page) was used for this project.
- Downloaded the data using `wget`.
- Data was transformed using the `pandas` library.

## Uploading Data
- The `sqlalchemy` library was used to make connection with the database to upload data.
