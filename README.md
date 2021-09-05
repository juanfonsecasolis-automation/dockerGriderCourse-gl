# dockerGriderCourse-gl
Notes of the course https://gorillalogic.udemy.com/course/docker-and-kubernetes-the-complete-guide

## Instalation 
See https://docs.docker.com/install/linux/docker-ce/ubuntu/

## Docker ecosystem
* Docker client: interfaces for the docker server, executes commands.
* Docker server: software that creates images and containers (docker daemon).
* Docker Hub: website were you can get docker images.
* Docker Compose (as in the course of Kidman with selenium that uses a docker-compose.yaml)
* Docker images
* Docker machine

## Terminology
* Image: single file with all the configurations needed to run a program. In other words, a File System snapshot with a start-up command.
* Container: instance of an image, or a space with isolated resources (e.g. memory).
* Image cache: a service that is called before downloading an image from the docker hub

# Docker client commands
* `docker --version`
* `docker run hello-world`

# Operative system architecture
* Programs consume resources (CPU, memory, harddisk) through the Kernel via system call.
* Different programs require different library versions, when multiple version of the same library can't co-exist a possible solution is to assign different parts of the HD to each program.
* But to assign different parts of the HD, the Kernel needs to know what program is calling what part of the HD, that's possible using namespacing, so namespacing, is a way of isolating resources per process.
* "Control groups", instead, is a way to limit the amount of resources used per process.
* A container is the combination of namespace, control groups, and resources. The kernel is the same through containers.
* In practice, there is a single Linux kernel (on a virtual machine) for all containers that is communicating with your operative system kernel. 

# References
1. Stephen Grider. Build, test, and deploy Docker applications with Kubernetes while learning production-style development workflows. URL: https://gorillalogic.udemy.com/course/docker-and-kubernetes-the-complete-guide.

