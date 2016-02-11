This repo contains source for [ficusio/redis-commander] automated Docker Hub build.

This is a lightweight (~52 MB) Docker image for [redis-commander], a web GUI for
viewing and managing Redis data.

[ficusio/redis-commander]: https://hub.docker.com/r/ficusio/redis-commander/
[redis-commander]: http://joeferner.github.io/redis-commander/

## Usage example

```sh
# Start Redis
$ docker run -d --name redis -p 6379:6379 redis

# Start Redis Commander
$ docker run -it --name redis-commander -p 8081:8081 --link redis \
  ficusio/redis-commander --redis-host redis --redis-port 6379

# Navigate to localhost:8081, or DOCKER_MACHINE_IP:8081 if using Docker Toolbox
# on a Mac/Windows (run "docker-machine ip default" to get DOCKER_MACHINE_IP)
```
