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
2. Build images - `docker-compose build`
3. Start services - `docker-compose up -d`
4. Grab IP - `docker-machine ip dev` - and view in your browser

### EC2 Instructions
1. `docker-machine create --driver amazonec2 --amazonec2-region eu-central-1 prod`
2. `eval "$(docker-machine env prod)"`
3. `docker-compose --file docker-compose.prod.yml build`
4. `docker-compose --file docker-compose.prod.yml up -d`
5. `docker-machine ip prod`