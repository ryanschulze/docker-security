# docker-security
Security focused docker images


## RIPS: ![Docker Automated build](https://img.shields.io/docker/automated/ryanschulze/security-rips.svg?style=flat-square)-![Docker Build Status](https://img.shields.io/docker/build/ryanschulze/security-rips.svg?style=flat-square)

**Details**

The old (free) branch of [RIPS](https://github.com/robocoder/rips-scanner) for conducting static analysis scans of PHP code.

**Usage**

For easy use, the following function maps the current directory to /code/ inside the container

    docker-rips() {
      docker run --rm -d -e WEBSERVER_UID=$(id -u) -p 80:80 -v ${PWD}:/code ryanschulze/security-rips
      return $?
    }

