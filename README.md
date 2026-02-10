# 🚀 Kubernetes CI/CD Project using Docker & GitHub Actions

This project demonstrates an **end-to-end CI/CD pipeline** for a containerized application using **Docker, GitHub Actions, and Kubernetes (Minikube)**. The goal is to automate the build and delivery process and deploy the application on a Kubernetes cluster.

---

## 📌 Project Overview

* Build a Docker image for a sample web application
* Automatically push the image to DockerHub using GitHub Actions
* Deploy the application to Kubernetes using Deployment & Service manifests
* Expose the application using Minikube

---

## 🛠️ Tech Stack

* **Docker** – Containerization
* **GitHub Actions** – CI/CD automation
* **Kubernetes** – Container orchestration
* **Minikube** – Local Kubernetes cluster
* **HTML** – Sample application

---

## 📂 Project Structure

```
k8s-cicd-project/
│
├── app/                  # Application source code
├── k8s/                  # Kubernetes manifests
│   ├── deployment.yaml
│   └── service.yaml
├── .github/workflows/    # GitHub Actions workflow
│   └── cicd.yaml
├── Dockerfile            # Docker image instructions
└── README.md
```

---

## ⚙️ CI/CD Pipeline Workflow

The pipeline is triggered **automatically on every push to the `main` branch**.

### CI Steps (GitHub Actions):

1. Checkout source code
2. Login to DockerHub using GitHub Secrets
3. Build Docker image
4. Push Docker image to DockerHub

---

## 🔐 GitHub Secrets Required

Add the following secrets in your GitHub repository:

* `DOCKER_USERNAME` → DockerHub username
* `DOCKER_PASSWORD` → DockerHub password or access token

Path:

```
GitHub Repo → Settings → Secrets and variables → Actions
```

---

## 🚢 Kubernetes Deployment

### Apply Kubernetes manifests:

```bash
kubectl apply -f k8s/
```

### Verify pods and services:

```bash
kubectl get pods
kubectl get svc
```

### Access application using Minikube:

```bash
minikube service cicd-service
```

---

## ✅ Expected Output

* Docker image available on DockerHub
* Pods running successfully in Kubernetes
* Application accessible via Minikube service URL

---

## 🎯 Learning Outcomes

* Practical understanding of CI/CD pipelines
* Hands-on experience with Docker & Kubernetes
* Automating image build and delivery using GitHub Actions
* Deploying containerized apps on Kubernetes

---

## 👤 Author

**Aaftab Pathan**
Aspiring DevOps / Cloud Engineer

---

⭐ If you like this project, feel free to star the repository!
