# mini-aspire API (Docker setup)

Repository contains configuration to run project using docker.
Follow below steps

### System required

[Install Docker Engine](https://docs.docker.com/engine/install/)

## Project Installation

Use the docker-compose package manager [composer]() to install application.

```bash
docker-compose run --rm composer install
```

## Environment setup

1. Make copy .env.example as .env

```bash
.env
.env.example
```

2. Set values for environment variables

EXAMPLE

```bash
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=mini_aspire_db
DB_USERNAME=dummyuser
DB_PASSWORD=secret
```

## Start Docker

```bash
docker-compose up server php mysql phpmyadmin
```

## Preusage commands

```bash
docker-compose run artisan migrate
```

## Create Admin(User)

```bash
docker-compose run artisan db:seed
```

## Running The Scheduler Locally

Typically, you would not add a scheduler cron entry to your local development machine. Instead, you may use the schedule:work Artisan command. This command will run in the foreground and invoke the scheduler every minute until you terminate the container.

```bash
docker-compose run artisan schedule:work
```

## Running Tests

```bash
docker-compose run artisan test
```

## Credentials

Admin

`email` admin@application.com

`password` admin@appp

PHPMyAdmin

`Username` dummyuser

`Password` secret

## Documentation

[API](https://documenter.getpostman.com/view/998100/2s93m8xKp3)

## Author

[Sudhir Dhawle](https://www.linkedin.com/in/sudhirdhawle/)
