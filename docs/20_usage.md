# Usage

## Run with Docker Compose

The Dashboard can be integrated directly into the [Geo Collector Bot](https://github.com/opengeolab/geocollectorbot) architecture thanks to [Docker](https://www.docker.com/)'s modularity and [Docker Compose](https://docs.docker.com/compose/) integration.

### Configuration 

Edit the file `.env` and change the environment variables according to the [Geo Collector Bot](https://github.com/opengeolab/geocollectorbot) configuration.

```bash
# Database setup
pg_hostname=<host name of PostgreSQL container>
pg_port=<PostgreSQL container port>
# This optional environment variable is used in conjunction with POSTGRES_PASSWORD to set a user and its password.
# This variable will create the specified user with superuser power and a database with the same name.
# If it is not specified, then the default user of postgres will be used.
pg_username=<PostgreSQL username>
# This environment variable is required to use the PostgreSQL image. It must not be empty or undefined.
# This variable sets the superuser password for PostgreSQL. The default superuser is defined by the POSTGRES_USER environment variable.
pg_password=<PostgreSQL password>
# This optional environment variable can be used to define a different name for the default database that is created when the image is first started.
# If it is not specified, then the value of POSTGRES_USER will be used.
app_database=<PostgreSQL database>
# The username and password of the user to create for managing the <app_database>
app_username=<app_database username>
app_password=<app_database password>
# The exposed port of the PostgreSQL container
exposed_pg_port=5432

#Dashboard setup
# The home path of the Dashboard. It's used to set the path where the media files (photo, videos, ...) are uploaded (<data_dir>/uploads).
data_dir=/home/InsubriParks
# The port where the Dashboard is exposed
exposed_dashboard_port=8080

# host name of the container that exposes the API to send messages to the users
api_url=bot_server
```



### Run

```bash
docker-compose up -d
```

The Dashboard run on http://localhost:8080/InsubriParks_Dashboard
