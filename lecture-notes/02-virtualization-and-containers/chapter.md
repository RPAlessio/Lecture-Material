# Virtual machines and containers

In this chapter we discuss virtual machines and containers and their potential use in (simulation) software engineering. Both techniques are used for the testing

## Virtual machines vs. containers

- [Virtual Box](https://www.virtualbox.org/)
- Virtual Box (see Sec. \ref{sec:virtualmachines})
- [Vagrant](https://www.vagrantup.com/)

There have been extensive discussions[^1] on what the differences between virtual machines, containers and their related tools are and when to use what.

[^1]: An infamous discussion of the creators of vagrant and Docker about the respective tools can be found on Stackoverflow [@vagrantvsdocker]

## Virtual machines  {#sec:virtualmachines}

### Virtual Box  {#sec:virtualbox}

### Vagrant  {#sec:vagrant}

Strictly speaking Vagrand is not a virtual machine, but it is a tool to manage virtual machines.
## Containers

- podman
- [lxc/lxd](https://linuxcontainers.org/)


The container technologies discussed here are not the only ones available, but not that common in science yet. We still want to mention the availability of Podman [@podman], lxc/lxd [@lxc] and

### Docker


```Dockerfile
# Example taken from https://github.com/carlossg/docker-maven
FROM openjdk:7-jdk-alpine

RUN apk add --no-cache curl tar bash
```
#### Usage of containers

#### Build your own container

#### DockerHub

### Singularity


## Summary

In this section, we have dealt with virtual machines and containers. Both are valuable tool for software development, testing, accessibility, and preservation of software. Virtual machines are more flexible in terms of what can be run within a virtual machines, but it also is less lightweight than containers.

One risk with each of discussed tools, in the context of sustainable research, is the lifetime of software. Ideally, the software stays around for ever, but it is common that software disappears due to companies go bankrupt, the interest in a project simply dies, or another project becomes more successful. Therefore, it makes sense to keep an eye on the developments.