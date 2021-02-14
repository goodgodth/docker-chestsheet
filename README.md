# Docker Cheatsheet

## Docker Basic Command
  - [`docker`](https://docs.docker.com/engine/reference/commandline/docker) - show help docker command
  - [`docker version`](https://docs.docker.com/engine/reference/commandline/version/) - show version docker
  - [`docker info`](https://docs.docker.com/engine/reference/commandline/version/) - show information docker

## Docker All Environment
  - [`docker system prune`](https://docs.docker.com/engine/reference/commandline/docker) - clear all container and images in enviroment

## Docker Image Command
  - [`docker images ls`](https://docs.docker.com/engine/reference/commandline/docker) - show all images
  - [`docker pull [IMAGENAME]:[VERSION]`](https://docs.docker.com/engine/reference/commandline/version/) - download docker images from hub.docker.com which imagename and version
  - [`docker build -t [ASSIGNNAME] .`](https://docs.docker.com/engine/reference/commandline/version/) - build images from dockerfile in current directory
  - [`docker rmi [IMAGE NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - delete docker images
  - [`docker rmi $(docker images -aq)`](https://docs.docker.com/engine/reference/commandline/version/) - delete all docker images
  - [`docker tag [IMAGENAME] [IMAGENEWNAME]`](https://docs.docker.com/engine/reference/commandline/version/) - assign tag for new docker images  
  - [`docker image prune --filter="dangling=true"`](https://docs.docker.com/engine/reference/commandline/version/) - remove images with none tag

## Docker Container Command
  - [`docker ps -a`](https://docs.docker.com/engine/reference/commandline/docker) - show docker container with all status
  - [`docker run --name [CONTAINER NAME] -it [IMAGENAME] --rm(Automatically remove the container when it exits) -d(daemon) -p(Publish or expose port) -e(Set environment variables)`](https://docs.docker.com/engine/reference/commandline/run/) - run docker container
  - [`docker [start | stop | restart] [CONTAINER NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - operation docker container
  - [`docker container prune`](https://docs.docker.com/engine/reference/commandline/docker) - remove all stopped containers  
  

## Docker Edit Container
  - [`docker exec -it [CONTAINER NAME or ID] [bash or sh or /bin/bash or /bin/sh]`](https://docs.docker.com/engine/reference/commandline/version/) - enter to docker container with ssh
  - [`docker stop $(docker ps -aq) && docker rm $(docker ps -aq)`](https://docs.docker.com/engine/reference/commandline/version/) - stop and remove all docker container
  - [`docker commit [CONTAINER was edited] [IMAGEwithNewName]`](https://docs.docker.com/engine/reference/commandline/version/) - Commit for get new container after enter ssh edit something in docker container
  - [`docker cp [CONTAINER]:[DIRECTORYINCONTAINER] [LOCALDIRECTORY]`](https://docs.docker.com/engine/reference/commandline/version/) - copy file in container
  - [`docker cp [FILEINLOCAL] [CONTAINER]:[DIRECTORYINCONTAINER]`](https://docs.docker.com/engine/reference/commandline/version/) - copy file from local to container
  - [`docker cp -L [SHORTCUTINLOCAL] [CONTAINER]:[DIRECTORYINCONTAINER]`](https://docs.docker.com/engine/reference/commandline/version/) - copy file local via shotcut
  
## Docker info Container
  - [`docker logs [CONTAINER NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - show logs container
  - [`docker logs -f [CONTAINER NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - show realtime logs container
  - [`docker inspect [CONTAINER NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - show inspect configure docker container
  - [`docker stats [CONTAINER NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - show CPU, MEM, I/O
  - [`docker top [CONTAINER NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - Display the running processes of a container
  - [`docker port [CONTAINER NAME or ID]`](https://docs.docker.com/engine/reference/commandline/version/) - List port mappings or a specific mapping for the container
  
## Docker Edit Image
  - [`docker save [IMAGE] > [OUTPUT.tar]`](https://docs.docker.com/engine/reference/commandline/version/) - Save Image to file.tar
  - [`docker save [ --output | -o ] [OUTPUT.tar] [IMAGE]`](https://docs.docker.com/engine/reference/commandline/version/) - Save Image to file.tar
  - [`docker save myimage:latest | gzip > myimage_latest.tar.gz`](https://docs.docker.com/engine/reference/commandline/version/) - Save Image to file.tar.gz
  - [`docker load < IMAGE.tar.gz`](https://docs.docker.com/engine/reference/commandline/version/) - import Images file
  - [`docker load --input FILE.tar`](https://docs.docker.com/engine/reference/commandline/version/) - import Images file
