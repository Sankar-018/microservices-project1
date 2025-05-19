# 🛒 Cloud-Native E-Commerce Microservices Project

## 📌 Overview

This project is a cloud-native e-commerce application built using 11 microservices. Each microservice is maintained in a separate Git branch and integrated with Jenkins multibranch pipelines. The application is deployed on Amazon EKS, with Docker images pushed to Docker Hub and secure deployments managed using Kubernetes service accounts and IAM roles.

---

## ⚙️ Tech Stack

- **Microservices:** 11 services (auth, user, product, order, etc.)
- **CI/CD:** Jenkins Multibranch Pipeline + GitHub Webhooks
- **Containerization:** Docker
- **Orchestration:** Kubernetes (Amazon EKS)
- **Cloud Services:** AWS EC2, IAM, EKS
- **Registry:** Docker Hub

---

## 🚀 CI/CD Workflow

- Code is pushed to a specific microservice Git branch
- GitHub webhook triggers the Jenkins multibranch pipeline
- Jenkins builds the Docker image using a branch-specific `Jenkinsfile`
- Docker image is pushed to Docker Hub
- Kubernetes manifests are applied to deploy/update services on EKS

---

## 🔐 AWS & Kubernetes Configuration

- EC2 instance configured as Jenkins host with Docker, `awscli`, `kubectl`, and `eksctl`
- IAM user with required policies created for AWS resource access
- EKS cluster created using `eksctl` and configured with `kubectl`
- Jenkins integrated with Docker, GitHub credentials, and service account tokens for Kubernetes
- Kubernetes Role and Service Account created and bound for secure deployments

---

## 🏗️ Microservice Deployment

Each microservice:
- Lives in its own Git branch
- Has a dedicated `Jenkinsfile`
- Gets built, containerized, and pushed to Docker Hub
- Is deployed to the EKS cluster with Kubernetes manifests

---




