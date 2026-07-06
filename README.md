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

<img width="1918" height="912" alt="Image" src="https://github.com/user-attachments/assets/dcc74606-715f-4d9d-a52a-f56716b70e7f" />

<img width="1918" height="917" alt="Image" src="https://github.com/user-attachments/assets/348a89d2-ec7f-4f57-b21c-08e484d58ada" />

<img width="1915" height="901" alt="Image" src="https://github.com/user-attachments/assets/f5e0f8af-380b-4226-85d2-44e06de78d32" />

<img width="1911" height="803" alt="Image" src="https://github.com/user-attachments/assets/8aa5f056-fb28-4282-8893-295c327189b4" />

<img width="1907" height="970" alt="Image" src="https://github.com/user-attachments/assets/b4be07dc-f222-4c43-aaa8-24584d87c832" />

<img width="1901" height="976" alt="Image" src="https://github.com/user-attachments/assets/0336f2af-2e20-4bc9-87fd-ea42a369664e" />

<img width="1907" height="532" alt="Image" src="https://github.com/user-attachments/assets/f30c75d1-9f3b-434f-a311-46244a6afdaf" />

<img width="1913" height="1006" alt="Image" src="https://github.com/user-attachments/assets/88730348-3b1f-46f1-8f49-649be177a51b" />
