# SOURCE

[Docker for JS Devs](https://dev.to/alexeagleson/docker-for-javascript-developers-41me)

## Start Deamon

systemctl --user start docker-desktop

## Pull image

sudo docker pull hello-world

## Browse images

sudo docker image ls

## Search Docker images online

node: https://hub.docker.com/_/node

Alpine is a popular small distro for docker containers

## pull image in advance

sudo docker pull node:14-alpine3.12

## or allow dockerfile to do so

https://docs.docker.com/engine/reference/builder/

## COPY allows layers to be created to save time

https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

## add dockerignore file

## build app

sudo docker build . -t my-node-app

## access image

sudo docker image ls

sudo docker run -p 3000:8080 --name my-node-app-container my-node-app

# connect app using docker volumes to persist data btwn runnning volumes

https://docs.docker.com/storage/volumes/

# stop container, remove it add run again with volume

docker container stop my-node-app-container

docker container rm my-node-app-container

docker run -p 3000:8080 --name my-node-app-container --volume ${PWD}:/usr/src/app my-node-app

# Docker-Compose

Dockerfile not needded to run installation script
