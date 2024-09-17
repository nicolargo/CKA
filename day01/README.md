Date: 17/09/2024

# Difference between VM and Container

VM:        (INFRA | OS | HYPERVISOR)       | (VM | GUEST OS | LIB | APP)
CONTAINER: (INFRA | OS | CONTAINER ENGINE) | (LIB | APP) 

# Build a container

Dockerfile == Build ==> Docker Image == Push ==> Registry

Registry for Docker registry: Docker hub, Artifactory, ...

# Deploy a container

Registry == Pull ==> Dev|Test|Prod environment

The "docker run" from your target environment.

# Docker architecture

Docker client    ==
                     build ==> Docker daemon ==> Local image
Dockerfile (Git) ==
The Docker image will be hosted and can be run on the host where
the client has been ran (dev for example).


Docker client == push ==> Docker daemon ==> Docker registry
The Docker image will be pushed to the factory.


Docker client == pull ==> Docker daemon ==> Docker registry
The Docker image will be pull from the factory to the host where
the client has been ran (prod for example).

