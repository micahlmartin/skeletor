# README

## Dependencies

It may be possible to run this with older versions of these dependencies but the listed versions are the one that this has been tested with and built for.

- Ruby >= 2.2.2
- Docker Compose >= 1.1.0
- Boot2Docker >= 1.5.0
- IOJS >= 2.5.0

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

Make sure boot2docker is running:

```boot2docker up```

Start up the database and other services in the background.

```docker-compose up -d```

To run all of the processes:

```npm start```

If you only want to run the rails server:

```./bin/rails s```
