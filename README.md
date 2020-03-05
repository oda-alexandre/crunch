# CRUNCH

## INDEX

- [CRUNCH](#crunch)
  - [INDEX](#index)
  - [BADGES](#badges)
  - [INTRODUCTION](#introduction)
  - [PREREQUISITES](#prerequisites)
  - [INSTALL](#install)
    - [DOCKER RUN](#docker-run)
    - [DOCKER COMPOSE](#docker-compose)
  - [LICENSE](#license)

## BADGES

[![pipeline status](https://gitlab.com/oda-alexandre/crunch/badges/master/pipeline.svg)](https://gitlab.com/oda-alexandre/crunch/commits/master)

## INTRODUCTION

Docker image of :

- [crunch](https://tools.kali.org/password-attacks/crunch)

Continuous integration on :

- [gitlab pipelines](https://gitlab.com/oda-alexandre/crunch/pipelines)

Automatically updated on :

- [docker hub public](https://hub.docker.com/r/alexandreoda/crunch)

## PREREQUISITES

Use [docker](https://www.docker.com)

## INSTALL

### DOCKER RUN

```\
docker  run -ti --rm --name crunch -v ${HOME}:/home/crunch alexandreoda/crunch
```

### DOCKER COMPOSE

```yml
version: "3.7"

services:
  crunch:
    container_name: crunch
    image: alexandreoda/crunch
    restart: "no"
    network_mode: none
    privileged: false
    volumes:
      - "${HOME}:/home/crunch"
```

## LICENSE

[![GPLv3+](http://gplv3.fsf.org/gplv3-127x51.png)](https://gitlab.com/oda-alexandre/crunch/blob/master/LICENSE)
