# Docker _privileged_ Jenkins Docker inside Docker Container
_maintained by MarvAmBass_

[FAQ - All you need to know about the marvambass Containers](https://marvin.im/docker-faq-all-you-need-to-know-about-the-marvambass-containers/)

## What is it

This Dockerfile (available as ___marvambass/jenkins-docker__) is based on __\_/jenkins:latest__ and runs Docker besides Jenkins.
So you'll be able to build Docker Containers and push them somewhere or something like that.

View in Docker Registry [marvambass/jenkins-docker](https://registry.hub.docker.com/u/marvambass/jenkins-docker/)

View in GitHub [MarvAmBass/jenkins-docker](https://github.com/MarvAmBass/jenkins-docker)

## Run it

You can run it like the original __\_/jenkins__ container. But you need to run it privileged to be able to use Docker inside of it!

    docker run -d --name jenkins \
    --privileged \
    -p 8080:8080 \
    -v /your/jenkins/home:/var/jenkins_home \
    marvambass/jenkins-docker \
    --prefix=/jenkins/
