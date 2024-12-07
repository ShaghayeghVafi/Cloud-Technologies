
# Docker Containerization for Application Deployment
## Overview
This project focuses on using Docker to containerize and deploy an application efficiently. By utilizing Docker and Docker Compose, we created a multi-container setup to connect Joomla! and MySQL, ensuring portability, consistency, and ease of deployment across various platforms.

## Key Features
Containerization: Docker provides isolated environments that are lightweight and faster than traditional VMs.
Multi-Container Setup: Docker Compose simplifies the configuration and management of multiple containers, including handling dependencies.
Platform Independence: The application can run on any system with Docker installed, avoiding vendor lock-in.
## Deployment Steps
Install Docker Engine on an Ubuntu virtual machine.
Use official Joomla! and MySQL images from DockerHub.
Define the configuration in the compose.yaml file, including ports, environment variables, and dependencies:
yaml
## Copy code
depends_on:
  - joomladb
ports:
  - 8080:80
environment:
  JOOMLA_DB_HOST: joomladb:3306
platform: linux/x86_64
#### Test the application using a command-line browser (lynx) or through SSH port forwarding.
## Challenges and Solutions
Database Connectivity: Resolved port configuration issues by specifying port 3306 in the compose.yaml file.
Apple Silicon Compatibility: Fixed issues by adding explicit platform specifications (linux/x86_64) for the MySQL container.
## Benefits
Using Docker containerization, we achieved:

Portability across hosting environments.
Simplified development and deployment workflows.
Freedom to choose cost-effective hosting options without being tied to a specific vendor.
### Project report can be viewed at [Overleaf](https://www.overleaf.com/read/dzykcyxnhkpc).
