# docker-kata
Some katas for docker

## Prerequisites

* Ubuntu 14.04
* wget installed

## Installation

### Kata: Install docker on Ubuntu 14.04

Solution:

```shell
wget -qO- https://get.docker.com/ | sh
```

Bonus:

1. Test
2. Add user to docker group (logout/login)
3. Test again

```shell
sudo docker run hello-world
sudo usermod -aG docker ubuntu
docker run hello-world
```

### Kata: Find the docker client and server version

Solution:

```shell
docker version
```

## Basic Images and Containers

### Kata: Run the latest Node.js REPL

Solution:

```shell
docker run -it node
```

i: interactive, t: terminal (psuedo)

### Kata: List all Images

Solution:

```shell
docker images
```

### Kata: List all Containers

Solution:

```shell
docker ps -a
```

### Kata: Remove a container

Solution:

```shell
docker ps -a
docker rm <id> or <name>
```

### Kata: Remove an image

Solution:

```shell
docker images
docker rmi <id> or <repo-name>
```


### Kata: Run ping 10 times against localhost on latest centos in detached mode

Solution:

```shell
docker run -d centos ping 127.0.0.1 -c 10
```


### Kata: Show logs for docker container

Solution:

```shell
docker ps -a
docker logs <name> or <container-id>
```

### Kata: Tail logs on docker container

Solution:

```shell
docker ps -a
docker logs -f <name> or <container-id>
```

### Kata: Run tomcat v7 in detached mode and map ports

Solution:

```shell
docker run -d -P tomcat:7
```

### Kata: Run and use bash inside latest Ubuntu. Exit container without stopping it.

Solution:

```shell
docker run -it ubuntu bash
CTRL + P + Q
```

### Kata: Open a new bash session in a running Linux container.

Solution:

```shell
docker ps
docker exec -it <id> or <name> bash
```
