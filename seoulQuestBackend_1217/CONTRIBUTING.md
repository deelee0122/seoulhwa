# Contributing

Note that if you're not using WSL on Windows, you should be. Also note that while IntelliJ is awesome, it's sometimes a little funky with WSL. You may need to do some configuration and plugin installation to get IntelliJ to work with WSL properly.

## Setup

1. Run `./gradlew` to get everything set up.
2. Copy `.env.template` to `.env` (`cp .env.template .env`) and fill in the environment variable values in `.env`.

## Running

Make sure you have Docker Desktop or Rancher Desktop installed. Note that Docker Desktop requires payment if your organization has more than some number of people, but it is free to use for personal or very small projects. Rancher Desktop has no such requirements.

1. Run `docker compose up -d` to run a local database and a local database UI at [http://localhost:8000](http://localhost:8000).
2. Run with `source && ./gradlew bootRun`.

## Teardown

1. Run `docker compose down` to stop and remove all the local development Docker containers.

Note that the database contents will be persisted because they're in a volume. If you want to completely clean out the database contents, you'll need to delete the Docker volume. See Docker CLI help on how to do this.
