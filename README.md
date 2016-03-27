## Django Starter Project using Docker Compose, Nginx, and Gunicorn

Based on this [RealPython repo](https://github.com/realpython/dockerizing-django)
This uses [django/alang](https://hub.docker.com/r/alang/django/) docker image instead of python-onbuild

Tested With:

- Docker v1.10.3
- Docker Compose v1.6.2
- Docker Machine v0.6.0
- Python 3.5

### OS X Instructions

1. Start new machine - `docker-machine create -d virtualbox dev;`
1. Build images - `docker-compose build`
1. Start services - `docker-compose up -d`
1. Grab IP - `docker-machine ip dev` - and view in your browser