# Helpful docker commands

## Images

Show all downloaded images:

`docker images`

[Detail](https://docs.docker.com/engine/reference/commandline/images/)

---

Create a new image from a container’s changes:

`docker commit <container_name> <docker_id>/<image_name>[:<tag>]`


[Detail](https://docs.docker.com/engine/reference/commandline/commit/)

---

Build the image **`<image_name>`** from a *Dockerfile*. *Dockerfile* should be located in current directory:

`docker build -t <image_name> .`


[Detail](https://docs.docker.com/engine/reference/commandline/build/)


## Containers

Run new container from **`image_name`** with interactive mode and tty terminal using some **`command`** (for example, bash):

`$ docker run -it <image_name> <command>`

[Detail](https://docs.docker.com/engine/reference/commandline/run/)

---

Run new container from **`image_name`** in background mode and print container id:

`$ docker run -d <image_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/run/#options)

---

Run new container from **`image_name`** and remove it after exit:

`$ docker run -it -rm <image_name> <command>`

[Detail](https://docs.docker.com/engine/reference/commandline/run/#options)

---

Start container **`container_name`**:

`$ docker start <container_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/start/)

---

Stop container **`container_name`**:

`$ docker stop <container_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/stop/)

---

Reload container **`container_name`**:

`$ docker restart <container_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/restart/)

---

Set **`hostname`** for new container from image **`image_name`** and run it:

`$ docker run -h <hostname> -it <image_name> <command>`

[Detail](https://docs.docker.com/engine/reference/commandline/run/#options)

---

Forward port from host to new container from image **`image_name`** and run it:

`$ docker run -p <host_port>:<container_port> -d <image_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/run/#options)

---

Set name **`container_name`** for new container from image **`image_name`** and run it:

`$ docker run --name <container_name> -it <image_name> <command>`

[Detail](https://docs.docker.com/engine/reference/commandline/run/#options)

---

Show detail information about container **`container_name`**

`$ docker inspect <container_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/inspect/)

---

Remove container **`container_name`**

`$ docker rm <container_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/rm/)

---

Remove all stopped containers

`$ docker rm -v $(docker ps -aq -f status=exited)`

[Detail](https://docs.docker.com/engine/reference/commandline/rm/#options)

---

## States

Show running containers:

`$ docker ps`

[Detail](https://docs.docker.com/engine/reference/commandline/ps/)

---

Show all containers:

`$ docker ps -a`

[Detail](https://docs.docker.com/engine/reference/commandline/ps/#options)

---

Show stoped containers:

`docker ps -a -f "status=exited"`

[Detail](https://docs.docker.com/engine/reference/commandline/ps/#options)

---

## Changes

Show changes in container **`container_name`**:

`docker diff <comtainer_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/diff/)

---

Show log information of the container **`container_name`**:

`$ docker logs <container_name>`

[Detail](https://docs.docker.com/engine/reference/commandline/logs/)