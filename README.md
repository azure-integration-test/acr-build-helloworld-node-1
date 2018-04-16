# ACR Build Hello World

This Node.js application is for use in demonstrating Azure Container Registry Build (ACR Build), a suite of features within Azure Container Registry for performing Docker container builds in the cloud.

## Features

This project includes three Dockerfiles:

* Dockerfile - Non-parameterized Dockerfile for building the application. References a base image in Docker Hub.
* appDockerfile - Parameterized, accepts the `REGISTRY_NAME` argument to specify the FQDN of the container registry from which the base image is pulled.
* baseDockerfile - Defines the base image for the application defined in *appDockerfile*.

## Getting Started

### Prerequisites

This project is for use with the following Azure Container Registry articles:

* [Build container images in the cloud with Azure Container Registry Build](https://docs.microsoft.com/azure/container-registry/container-registry-tutorial-quick-build)
* [Automate container image builds with Azure Container Registry Build](https://docs.microsoft.com/azure/container-registry/container-registry-tutorial-build-task)
* [Automate image builds on base image update with Azure Container Registry Build](https://docs.microsoft.com/azure/container-registry/container-registry-tutorial-base-image-update)

### Quickstart

1. `git clone https://github.com/Azure-Samples/acr-build-helloworld-node`
1. `cd acr-build-helloworld-node`
1. `docker build -t helloacrbuild:v1 .`
1. `docker run -d -p 5000:5000 helloacrbuild:v1`
1. Navigate to http://localhost:5000 to view the running application

## Resources

[Azure Container Registry](https://azure.microsoft.com/services/container-registry/)

[Azure Container Registry documentation](https://docs.microsoft.com/azure/container-registry/)
