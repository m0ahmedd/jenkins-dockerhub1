# Jenkins Declarative Pipeline to Build and Push Docker Image to Docker Hub

This project demonstrates how to create a Jenkins declarative pipeline that automates the process of building a Docker image from a Dockerfile, running the image, and pushing it to Docker Hub.

## Prerequisites

Before you start, make sure you have the following:

1. **Jenkins** setup and running. You can install it from [here](https://www.jenkins.io/download/).
2. **Docker** installed on the machine running Jenkins. You can install it from [here](https://www.docker.com/get-started).
3. A **Docker Hub account** for pushing the Docker images. You can create one from [Docker Hub](https://hub.docker.com/).
4. A **Jenkins Docker plugin** installed, which provides Docker integration in Jenkins. You can install it from the Jenkins plugin manager.

## Project Overview

This Jenkins pipeline will:

- **Build** a Docker image using the `Dockerfile` located in the repository.
- **Run** the built Docker image in a container for testing.
- **Push** the image to Docker Hub.

The pipeline is written in **Jenkins Declarative Pipeline Syntax** and uses **Docker** as the tool for building and running containers.
