# Microflix Clone: End-to-End DevOps Pipeline

This repository contains the application code and deployment pipeline for a React-based streaming application. The project demonstrates a complete, automated CI/CD lifecycle using industry-standard tools. 

## 🏗️ Architecture & Tools Used
* **Frontend:** React.js
* **Containerization:** Docker (Multi-stage build)
* **Continuous Integration:** Jenkins (Pipeline as Code)
* **Container Orchestration:** Kubernetes
* **Infrastructure Provisioning (Separate Repo):** Terraform, Ansible, AWS EC2

## ⚙️ The CI/CD Workflow
1. **Source Control:** Developers push React code to the `main` branch of this repository.
2. **Webhook Trigger:** GitHub sends an automated payload to the AWS-hosted Jenkins server.
3. **Automated Build:** Jenkins executes the Declarative Pipeline (`Jenkinsfile`), checking out the code and building a highly optimized Docker image using Node.js and Nginx.
4. **Local Orchestration:** The containerized application is deployed locally via Kubernetes manifests (`k8s/deployment.yaml` and `k8s/service.yaml`) using a `NodePort` service.

## 🚀 Future Roadmap
* Integrate Docker Hub for remote image registry.
* Add Trivy/SonarQube stages to the Jenkinsfile for automated DevSecOps scanning.
* Migrate Kubernetes deployment from local Minikube to AWS EKS.
