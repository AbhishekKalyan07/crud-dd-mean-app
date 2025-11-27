MEAN Stack Cloud Deployment - DevOps Assessment

📌 Project Overview

This project demonstrates the containerization and cloud deployment of a full-stack MEAN (MongoDB, Express, Angular, Node.js) application. The application allows users to create, read, update, and delete (CRUD) tutorial entries.

Key Technologies:

Frontend: Angular 15

Backend: Node.js & Express

Database: MongoDB

DevOps: Docker, Nginx, AWS, GitHub Actions

🚀 Infrastructure Architecture

The application is fully containerized and deployed on an AWS EC2 instance.

Cloud Provider: AWS EC2 (Ubuntu 22.04 LTS)

Container Orchestration: Docker Compose

Reverse Proxy: Nginx (Routes traffic on Port 80 to Frontend/Backend)

CI/CD Pipeline: GitHub Actions (Automated Build & Deploy)

Container Registry: Docker Hub

🛠️ Prerequisites

To run this project, you only need Docker installed. No local Node.js or MongoDB setup is required.

Docker Desktop

⚙️ How to Run Locally (Using Docker)

Follow these steps to spin up the entire stack with one command:

Clone the Repository

git clone [https://github.com/AbhishekKalyan07/crud-dd-mean-app.git](https://github.com/AbhishekKalyan07/crud-dd-mean-app.git)
cd crud-dd-mean-app


Start the Application

docker-compose up --build -d


Access the App

Frontend: http://localhost

Backend: http://localhost/api

Stop the App

docker-compose down


🔄 CI/CD Pipeline

This repository uses GitHub Actions for automation.

Push to Main: Code changes trigger the pipeline.

Build: Docker images for Frontend and Backend are built.

Push: Images are pushed to Docker Hub.

Deploy: The pipeline SSHs into the AWS EC2 server, pulls the new images, and restarts the containers automatically.

📸 Deployment Evidence

1. Application UI (Live on AWS)

(Please refer to the attached screenshots showing the app running on the AWS Public IP).

2. Infrastructure Status

(Please refer to the attached screenshot of docker ps showing active containers).

3. CI/CD Pipeline Success

(Please refer to the attached screenshot of the GitHub Actions execution).

📂 Project Structure

backend/: Node.js API & Dockerfile.

frontend/: Angular App & Multi-stage Dockerfile.

docker-compose.yml: Defines the services (Mongo, Backend, Frontend, Nginx).

nginx.conf: Configuration for the Reverse Proxy.