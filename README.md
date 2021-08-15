# Jenkins server with Docker setup

## Create Jenkins with Docker container image

```
docker build -t {docker user}/jenkins-with-docker:{tag}} .
```

Like:
```
docker build -t strategdk/jenkins-with-docker:1.1 .
```

## Push container image to Docker Hub

(Optional)

```
docker push {docker user}/jenkins-with-docker:{tag}
```

Like:
```
docker push strategdk/jenkins-with-docker:1.1
```

## Pre-build Docker image

https://hub.docker.com/r/strategdk/jenkins-with-docker

## Bind Mounts

For bind mounts change the volumes section.

For jenkins_home

```
- {containing host directory}/docker_jenkins_home:/var/jenkins_home
```

Like:
```
- /Users/klaus/DockerVol/jenkins/jenkins_home:/var/jenkins_home
```

## Access
Access Jenkins through browser after bringing up the Docker Compose setup.
```
http://localhost:9080
```

## Refences
* https://www.jenkins.io/doc/book/installing/docker/
* https://docs.docker.com/compose/




