# 🐳 Davine Internship — Week 4 Docker Project

<div align="center">

### 🚀 Docker & Docker Compose Practical Project

A hands-on DevOps project demonstrating Docker fundamentals, containerization,
Dockerfile, volumes, networks, Docker Compose, Docker Hub, and GitHub.

</div>

---

## 📌 Project Overview

This project was developed as part of the **Davine Technologies DevOps Internship — Week 4**.

The objective of this project is to understand the fundamentals of Docker and
apply them by containerizing a simple web application using **Nginx**.

The project covers the complete basic Docker workflow:

```text
Application
    ↓
Dockerfile
    ↓
Docker Image
    ↓
Docker Container
    ↓
Docker Network + Volume
    ↓
Docker Compose
    ↓
Docker Hub
    ↓
GitHub
🎯 Objectives

The main objectives of this project are:

Understand Docker and containerization
Learn the difference between Docker images and containers
Create and use a Dockerfile
Build a custom Docker image
Run and manage Docker containers
Create and use Docker volumes
Create and use custom Docker networks
Use Docker Compose to manage an application
Push a Docker image to Docker Hub
Maintain the project using Git and GitHub
🛠️ Technologies & Tools
Technology	Purpose
🐳 Docker	Containerization
⚙️ Docker Compose	Container orchestration
🌐 Nginx	Web server
📄 HTML	Web application
💾 Docker Volumes	Persistent storage
🌐 Docker Networks	Container communication
☁️ Docker Hub	Image registry
🔧 Git	Version control
🐙 GitHub	Source code management
💻 Git Bash	Command-line environment
📂 Project Structure
week-4-docker/
│
├── 📄 Dockerfile
├── 📄 docker-compose.yml
├── 📄 README.md
├── 📄 .gitignore
│
└── 📁 app/
    └── 📄 index.html
🐳 Docker Implementation
1. Docker Installation & Verification

Docker Desktop was installed and configured with the Linux container
environment.

Docker installation was verified using:

docker version

The Docker Engine was also tested using:

docker run hello-world

A successful Hello from Docker! message confirmed that the Docker
client could communicate with the Docker daemon.

2. Docker Image

Docker images provide the template used to create containers.

The project uses the official Nginx image as the base image.

The custom application image was built using:

docker build -t week4-docker-app .

The resulting image was:

week4-docker-app:latest

3. Dockerfile

The project uses the following Dockerfile:

FROM nginx:latest

COPY app/index.html /usr/share/nginx/html/index.html
Dockerfile Explanation
FROM
FROM nginx:latest

Uses the official Nginx image as the base image.

COPY
COPY app/index.html /usr/share/nginx/html/index.html

Copies the application's HTML file into the default Nginx web directory.

This allows Nginx to serve the custom webpage.

🚀 Docker Container

A Docker container is a running instance of a Docker image.

The custom application was tested inside a Docker container.

Example:

docker run -d --name week4-app -p 8080:80 week4-docker-app

The application was then accessed through the browser.

Note: Port 8080 was already in use during testing, so the Compose
deployment uses port 8082.

💾 Docker Volume

A Docker volume was created for persistent storage:

docker volume create week4-volume

The volume can be inspected using:

docker volume inspect week4-volume
Why use a volume?

Docker volumes allow data to exist independently of a container's lifecycle.

The project uses:

week4-volume

for persistent Docker storage.

🌐 Docker Network

A custom Docker bridge network was created:

docker network create week4-network

The network can be inspected using:

docker network inspect week4-network
Why use a custom network?

A custom Docker network allows containers to communicate with each other
using Docker's internal networking.

Project network:

week4-network

Network driver:

bridge
⚙️ Docker Compose

Docker Compose is used to define and run the application using a YAML
configuration file.

The project uses:

docker-compose.yml

The application can be started with:

docker compose up -d

Check the running Compose services:

docker compose ps

Stop the application:

docker compose down
🧩 Compose Architecture

The current Compose application consists of an Nginx web container:

              🌐 Browser
                   │
                   │ HTTP :8082
                   ▼
        ┌────────────────────┐
        │  week4-compose-app │
        │       Nginx         │
        └──────────┬─────────┘
                   │
          week4-network
                   │
                   ▼
             💾 week4-volume
🌐 Accessing the Application

After starting Docker Compose:

docker compose up -d

The application is available at:

http://localhost:8082

The Compose port mapping is:

8082 → 80

where:

8082 = host port
80 = Nginx container port
☁️ Docker Hub

The custom Docker image was pushed to Docker Hub.

Docker Hub Repository
nidhi8901/week4-docker-app
Image Tag
latest

The image can be pulled using:

docker pull nidhi8901/week4-docker-app:latest
🐙 GitHub Repository

This project is maintained using Git and GitHub.

Repository
https://github.com/Nidhi8901/Davine-internship-docker

Git was used for:

Repository initialization
Tracking project files
Creating commits
Connecting the local repository to GitHub
Pushing the project to GitHub
🔍 Useful Docker Commands
Check Docker version
docker version
Check Docker information
docker info
List images
docker images
List running containers
docker ps
List all containers
docker ps -a
Stop a container
docker stop <container-name>
Start a container
docker start <container-name>
View container logs
docker logs <container-name>
List volumes
docker volume ls
List networks
docker network ls
List Compose services
docker compose ps
🧠 Key Concepts Learned

Through this project, the following Docker concepts were practiced:

🐳 Docker

Docker provides a platform for packaging applications and their dependencies
into portable containers.

📦 Image

An image is a read-only template used to create containers.

🚀 Container

A container is a running instance of an image.

📝 Dockerfile

A Dockerfile contains instructions used to build a custom Docker image.

💾 Volume

A volume provides persistent storage that exists independently of a
container.

🌐 Network

A Docker network allows containers to communicate with each other.

⚙️ Docker Compose

Docker Compose allows application services and their configuration to be
defined in a YAML file and managed together.

☁️ Docker Hub

Docker Hub is used as a registry for storing and sharing Docker images.

📸 Project Evidence

The project includes practical evidence for:

Docker installation and verification
Docker containers
Docker images
Docker volume
Docker network
Docker Compose
Running web application
Docker Hub image
GitHub repository
👨‍💻 Author

Nidhi kumari

DevOps Intern
Davine Technologies

GitHub
https://github.com/Nidhi8901
Docker Hub
https://hub.docker.com/u/nidhi8901




