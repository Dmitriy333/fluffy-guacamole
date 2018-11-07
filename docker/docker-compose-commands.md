- [Docker Compose Commands](#docker-compose-commands)
  * [NOTE: env variables are adding once the container is started. The data is written into a volume](#note-env-variables-are-adding-once-the-container-is-started-the-data-is-written-into-a-volume)
  * [Lists containers specific to the Docker compose file](#lists-containers-specific-to-the-docker-compose-file)
  * [Start Compose file](#start-compose-file)
  * [Destroy services running configured in Compose file !NOTE: configured volumes are not removed](#destroy-services-running-configured-in-compose-file-note-configured-volumes-are-not-removed)
  * [Start and down docker containers without removing it from disk space](#start-and-down-docker-containers-without-removing-it-from-disk-space)
  * [Exec command is executed against the container that is already started. It is also executed started from "working_directory"](#exec-command-is-executed-against-the-container-that-is-already-started-it-is-also-executed-started-from-working_directory)
  * [Exec command is executed against the container that is already started. It is also executed started from "working_directory" if it is specified](#exec-command-is-executed-against-the-container-that-is-already-started-it-is-also-executed-started-from-working_directory-if-it-is-specified)
  * [Run command is executed against a brand new started container. It is also executed started from "working_directory" if it is specified](#run-command-is-executed-against-a-brand-new-started-container-it-is-also-executed-started-from-working_directory-if-it-is-specified)

# Docker Compose Commands

## NOTE: env variables are adding once the container is started. The data is written into a volume

## Lists containers specific to the Docker compose file

```docker
docker-compose ps
```

## Start Compose file

```docker
docker-compose up -d
```

## Destroy services running configured in Compose file !NOTE: configured volumes are not removed

```docker
docker-compose down
```

## Start and down docker containers without removing it from disk space

```docker
docker-compose start/down
```

## Exec command is executed against the container that is already started. It is also executed started from "working_directory"

```bash
docker exec -it app bash -c "cd /var/www/html && php artisan list"
```

## Exec command is executed against the container that is already started. It is also executed started from "working_directory" if it is specified

```docker
docker-compose exec -it app bash -c "cd /var/www/html && php artisan list"
```

## Run command is executed against a brand new started container. It is also executed started from "working_directory" if it is specified

```docker
docker-compose run -it app bash -c "cd /var/www/html && php artisan list"
```