# httpbin
Dockerfile for httpbin(with gevent and Gunicorn).

# Quickstart

`docker run -d -p 8000:8000 --name httpbin strahe/httpbin`

## Exposing the other port

`docker run -d -p 80:8000 --name httpbin strahe/httpbin`

## Use Gunicorn workers

`docker run -d -p 8000:8000 -e "GUNICORN_WORKERS=4" --name httpbin strahe/httpbin`

## Other Gunicorn configuration

You can specify `-e "GUNICORN_${GUNICORN_CONFIG_NAME}=VALUE"` with `docker run` options to config Gunicorn.

`docker run -d -p 8000:8000 -e "GUNICORN_WORKERS=4" -e "GUNICORN_MAX_REQUESTS=100" -e "GUNICORN_TIMEOUT=30" --name httpbin strahe/httpbin`

For more about Gunicorn configuration,
see:http://docs.gunicorn.org/en/stable/settings.html
