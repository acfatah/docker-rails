# Containerized Ruby On Rails

Simple image to enable running rails command using docker.

## Building The Image

```bash
docker build -t rails:latest ruby-3.x
```

To build image for rails 6,

```bash
docker build -t rails:6 ruby-2.x
```

## Running A Command

```bash
docker run --rm -it -v $PWD:/usr/src/app rails:latest rails new example-app
```

## Starting a Rails Server

We should use `docker-compose` to start a rails server.

## Links

* https://hub.docker.com/_/ruby

## License

MIT

