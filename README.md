# docker-scripts

Templates for developers to easily create and remove various services within their local development environment, such as postgres and mongodb.

## Pre-requisites

1. **Install** Docker via [https://docs.docker.com/desktop/install/](https://docs.docker.com/desktop/install/)

## Usage

1. **Navigate** to the sub-folder of the service you wish to create:

```
cd mongo
```

2. **Copy** `.env.example` to `.env` and change values if needed:

```
cp .env.example .env
```

3. **Run** docker compose. The `-d` flag runs is a detached-state so that the command-line window can be closed without impacting the service.

```
docker compose up -d
```

4. To stop the container **and destroy the data within**, run from the same folder:

```
docker compose down
```

## Mac Users

Mac users may need to install the following tools to interact with the various services:

### Redis

To gain access to the Redis CLI:
```
brew tap ringohub/redis-cli
brew update && brew doctor
brew install redis-cli
```

### Mongo

To gain access to the MongoDB CLI:
```
brew install mongodb/brew/mongodb-database-tools
```

### Other

The following *might* be needed for Postgres' `psql` to work on some systems:
```
brew install libpq
```
