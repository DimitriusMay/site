# Kubernetes pet project

# [Video Instruction here](https://youtu.be/kWIZ_bYZXY4)
A 4-minute video shows the steps of working with local Kubernetes

- project goal: to demonstrate the launch of containerized web-applications managed by Kubernetes.

A standard github nginx image, and a custom image, uploaded to hub.docker.com/repository/docker/dmay17/k8s-web-to-nginx-ru - are used.

The project consists of containerized applications, presenting:
No. 1 - produces a response from one of the pods with a caption and pod identifier
No. 2 - produces the standard nginx response "Welcome to nginx!"
No. 3 - produces a response from a request to a third-party site jsonplaceholder.typicode.com/todos



--------------------------------------------------------------------------------------------------------

# Docker Compose pet web-application

- purpose: to demonstrate the launch of a containerized web-application, that displays an on-screen clock and the function of saving timestamps.

The application consists of 4 Docker images:
- of which there are two custom images (frontend and backend(api)) from my custom repository on DockerHub:
1. https://hub.docker.com/repository/docker/dmay17/time-app-api-dev
2. https://hub.docker.com/repository/docker/dmay17/time-app-frontend-dev
- and two official images (database and database interface) from DockerHub:
3. MySQL
4. Adminer

Installation instructions:
- after installing Docker Desktop for Windows or Docker Engine for Linux, and Docker compose on the computer:
1) downloading the docker-compose.pub.yml file to a local folder
2) by going to the terminal (cd <path>) to this folder and entering the command in the terminal:
docker-compose -f docker-compose.pub.yml up -d

After the installation process is automatically completed, the application is available in a web browser at:
http://localhost:3000/
After closing the web application, its containers can be deleted with the command in the terminal:
docker-compose -f docker-compose.pub.yml down


* According to B. Stashchuk’s training courses on Kubernetes, Docker and Docker Compose