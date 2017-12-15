## Ubuntu Dockerfile to reproduce Schedulix / Zope issues (https://mail.google.com/mail/u/0/#inbox/16059981ebe6c784)


This repository contains **Dockerfile** of [Ubuntu](http://www.ubuntu.com/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/dockerfile/ubuntu/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [ubuntu:14.04](https://registry.hub.docker.com/u/library/ubuntu/)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Build Ubuntu 14.04 container from Dockerfile: `docker build -t schedulix/ubuntu - < Dockerfile`)


### Usage

    docker run -it --rm schedulix/ubuntu
    
docker>virtualenv --no-site-packages Zope
docker>easy_install -U pip
docker>pip install -r https://raw.githubusercontent.com/zopefoundation/Zope/2.13.26/requirements.txt
