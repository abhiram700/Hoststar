# 🎬 Jenkins CI/CD Pipeline for Hotstar Deployment

This repository demonstrates a fully automated **CI/CD pipeline using Jenkins** to deploy a video streaming application inspired by **Hotstar**. The setup leverages **Docker**, **AWS EC2**, **GitHub**, and optional **Nginx reverse proxy** to mimic real-world DevOps workflows.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Architecture Diagram](#architecture-diagram)
- [Prerequisites](#prerequisites)
- [Jenkins Pipeline Setup](#jenkins-pipeline-setup)
- [Deployment Steps](#deployment-steps)
- [Demo](#demo)
- [License](#license)

---

## 📖 Project Overview

This project automates the deployment of a lightweight Hotstar-like video streaming application. It uses a **Jenkins pipeline** to:

- Detect changes in the GitHub repository
- Build and push a Docker image
- SSH into an EC2 instance
- Deploy the application using Docker
- Make the app accessible via a domain or IP

---

## 🚀 Tech Stack

| Tool        | Purpose                               |
|-------------|----------------------------------------|
| Jenkins     | Continuous Integration & Deployment    |
| Docker      | Containerization                       |
| GitHub      | Source Code & Webhooks                 |
| AWS EC2     | Cloud Hosting for deployment           |
| Nginx       | Reverse proxy (optional)               |
| Web App     | Hotstar-inspired streaming frontend    |

---

## 🧭 Architecture Diagram

```mermaid
graph LR
A[GitHub Push] --> B[Jenkins Webhook]
B --> C[Build Docker Image]
C --> D[Push to DockerHub]
D --> E[SSH to EC2]
E --> F[Pull Docker Image & Deploy]
F --> G[User Access via Browser]
