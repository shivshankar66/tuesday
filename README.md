# Static Web App Deployment using Docker, Jenkins & Kubernetes

This project demonstrates deployment of a **static web application**
using **Docker**, **Jenkins CI/CD**, and **Kubernetes**.

---

## Project Overview

- Static frontend application
- Docker image built and pushed using Jenkins
- Application deployed on Kubernetes
- Service exposed using LoadBalancer

---

## Tools Used

- Docker
- Jenkins
- Kubernetes
- HTML / JavaScript
- Docker Hub

---

## CI/CD Pipeline

1. Code pushed to GitHub  
2. Jenkins builds Docker image  
3. Jenkins pushes image to Docker Hub  
4. Kubernetes pulls latest image  
5. Application runs as Kubernetes Deployment  

---

## Kubernetes Setup

- Deployment name: `prodeploy`
- Replicas: `2`
- Container port: `80`
- Service type: `LoadBalancer`

---

## Access Application

Access the application using the **external LoadBalancer IP** on port **80**.

---

## Purpose

This project is created to demonstrate **end‑to‑end DevOps deployment**
using Jenkins, Docker, and Kubernetes.

---

## Author

Shiv Shankar Bhakuni  
DevOps Engineer
``
