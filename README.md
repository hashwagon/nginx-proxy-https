# General
The implementation of nginx reverse proxy is based off of this project: https://hub.docker.com/r/jwilder/nginx-proxy/ and the incorporation of Let's Encrypt from https://github.com/buchdag/letsencrypt-nginx-proxy-companion-compose.
## Prerequisites
### Docker
docker must be installed, please follow [https://docs.docker.com/engine/install/](this documentation).
### Docker Compose
docker-compose must be installed, please follow [https://docs.docker.com/compose/install/](this documentation).
## Getting Started
Create the following network
```
docker network create nginx-proxy
```
Start nginx-proxy and nginx-proxy-le containers
```
docker-compose up -d
```
## Other
Passing proxy_set_header parameters can be done in the optional proxy.conf file. To enable this, uncomment the following line in the `docker-compose.yml` file.
```
# - ./proxy.conf:/etc/nginx/proxy.conf
```
