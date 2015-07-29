# README

## Dependencies

- Ruby >= 2.2.2
- Docker Compose >= 1.1.0
- Boot2Docker >= 1.5.0

## Environment setup

Add an environment variable to your bash profile with the boot2docker ip:

```export DOCKER_IP=$(boot2docker ip)```

Install all the gems:

```bundle install```

Install npm packages:

```npm install```

Make a copy of the database configuration:

```cp config/database.yml.sample config/database.yml```

Create the database:

```./bin/rake db:setup```

Run the migrations:

```./bin/rake db:migrate```


## Startup

Make sure boot2docker is running and then start up the database and other services.

```docker-compose up -d```

You can then run your rails server and any other processes:

```npm start```
