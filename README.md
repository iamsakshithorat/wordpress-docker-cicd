# WordPress Deployment Automation using Jenkins & Docker

## Project Overview

This project demonstrates a production-style CI/CD pipeline for deploying a WordPress application using Jenkins and Docker on AWS EC2.

The architecture consists of two EC2 instances:

- Jenkins Server (Ubuntu)
- Docker Server (Amazon Linux)

Whenever code is pushed to GitHub, Jenkins automatically triggers the pipeline, connects to the Docker server through SSH, and deploys WordPress with a MySQL database using Docker containers.

---

## Architecture

              GitHub Repository
                     │
                     │ Push
                     ▼
             GitHub Webhook
                     │
                     ▼
        Jenkins Server (Ubuntu EC2)
                     │
              Execute Pipeline
                     │
                 SSH Connection
                     │
                     ▼
      Docker Server (Amazon Linux EC2)
             │                   │
             ▼                   ▼
      MySQL Container      WordPress Container
                     │
                     ▼
                  Browser


## Technologies Used

- AWS EC2
- Jenkins
- Docker
- WordPress
- MySQL
- GitHub
- GitHub Webhooks
- SSH
- Linux

---

## Features

- Automated CI/CD Pipeline
- Automatic deployment after every GitHub push
- Secure SSH deployment
- Docker-based application deployment
- WordPress + MySQL containerized setup
- Production-style two-server architecture

---

## Pipeline Workflow

1. Developer pushes code to GitHub
2. GitHub Webhook triggers Jenkins
3. Jenkins reads Jenkinsfile
4. Jenkins connects to Docker Server via SSH
5. Existing containers are removed
6. Latest Docker images are pulled
7. MySQL container starts
8. WordPress container starts
9. Application becomes available in the browser

---

## Project Structure

.
├── Jenkinsfile
├── README.md

---

## Future Improvements

- Docker Compose
- Terraform Infrastructure
- Nginx Reverse Proxy
- SSL using Let's Encrypt
- Kubernetes Deployment

---

## Author

Sakshi Thorat
