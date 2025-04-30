 Deploy a 3-Tier App on Amazon EKS
================================================================

In this project, I deployed a full-stack microservices application to a production-like **Amazon EKS (Kubernetes)** cluster. The app comprises multiple components:

*   🐍 Python-based **vote** service
*   🟩 Node.js **result** service
*   🟪 .NET **worker** service
*   🟥 **Redis** queue
*   🟦 **PostgreSQL** database

The application code used in the **vote**, **result**, and **worker** services is sourced from: [https://github.com/Pokfinner/ironhack-project-1/](https://github.com/Pokfinner/ironhack-project-1/)

🎯 Project Goals
----------------

1.  **Provision an EKS Cluster:** Used `eksctl` to provision a secure and scalable Amazon EKS cluster.
2.  **Containerize & Deploy:** Dockerized all services and deployed them using Kubernetes manifests.
3.  **Ingress Setup:** Used **NGINX Ingress Controller** (via Helm) to route external traffic to the correct services.
4.  **CI/CD Pipeline:** Implemented GitHub Actions workflows to:
    *   Build Docker images for each microservice
    *   Push the images to Docker Hub
    *   Apply Kubernetes manifests to EKS cluster automatically

🔐 Secrets Management
---------------------

All sensitive data (e.g., Docker credentials, AWS cluster config, and environment variables) are securely stored in **GitHub Secrets** and accessed by GitHub Actions workflows at runtime.

✅ Outcome
---------

The final architecture is a fully containerized, Kubernetes-based microservices app deployed on AWS EKS with a working GitHub Actions CI/CD pipeline for continuous deployment.

📂 Technologies Used
--------------------

*   Amazon EKS
*   Docker & Docker Hub
*   Kubernetes (kubectl, manifests)
*   Helm (for NGINX Ingress)
*   GitHub Actions
*   Python, Node.js, .NET Core
*   Redis, PostgreSQL

