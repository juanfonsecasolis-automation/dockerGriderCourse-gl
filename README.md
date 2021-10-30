# dockerGriderCourse-gl
Juan M. Fonseca-Solis. Notes of the course https://gorillalogic.udemy.com/course/docker-and-kubernetes-the-complete-guide

## 1 Pre-requisites
* See https://docs.docker.com/install/linux/docker-ce/ubuntu/

## 2 Project set-up
TDB...

## 3 Run
TBD...

### 3.1 Docker client commands
* `docker --version`
* `docker run hello-world` (`docker build` and `docker start` on the same line)
* `docker ps --all`: list all running containers
* `docker system prune`: To delete all stoped containers (you'll have to download the containers again) 

## 4 Theory
TBD...

### 4.1 Motivation
Docker makes it easy to install and run software without worrying about setup or dependencies.

### 4.2 Docker ecosystem
* **Docker client:** interfaces for the docker server, executes CLI commands.
* **Docker server:** software that creates images and containers (docker daemon).
* **Docker Hub:** website were you can get docker images.
* **Docker Compose:** (as in the course of Kidman with selenium that uses a docker-compose.yaml)
* **Docker images:** TBD...
* **Docker machine:** TBD...

### 4.3 Terminology
* **Image:** single file with all the configurations needed to run a program. In other words, a File System snapshot with a start-up command.
* **Container:** instance of an image, or a space with isolated resources (e.g. memory).
* **Image cache:** a service that is called before downloading an image from the docker hub

### 4.4 Operative system architecture
* Programs consume resources (CPU, memory, harddisk) through the Kernel via system call.
* Different programs require different library versions, when multiple version of the same library can't co-exist a possible solution is to assign different parts of the HD to each program.
* But to assign different parts of the HD, the Kernel needs to know what program is calling what part of the HD, that's possible using namespacing, so namespacing, is a way of isolating resources per process.
* "Control groups", instead, is a way to limit the amount of resources used per process.
* A container is the combination of namespace, control groups, and resources. The kernel is the same through containers.
* In practice, there is a single Linux kernel (on a virtual machine) for all containers that is communicating with your operative system kernel. 

## 5 References
1. Stephen Grider. Build, test, and deploy Docker applications with Kubernetes while learning production-style development workflows. URL: https://gorillalogic.udemy.com/course/docker-and-kubernetes-the-complete-guide.

