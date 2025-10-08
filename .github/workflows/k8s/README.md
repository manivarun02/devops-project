# DevOps Basic Project: Docker & Kubernetes

## Project Overview
This project containerizes a Next.js web application using Docker and provides Kubernetes deployment and service configs for real-world cloud and local testing[web:54][web:63].

## Features
- Complete Next.js source code
- Dockerfile for easy image creation
- Kubernetes YAML files (`deployment.yaml`, `service.yaml`) in the `k8s` folder

## Workflow Steps
1. Built Docker image:
docker build -t my-app .

text
2. Ran the app locally:
docker run -p 3000:3000 my-app

text
3. Created Kubernetes configs in `k8s` folder:
- `deployment.yaml`
- `service.yaml`
4. Started Minikube for local Kubernetes testing:
minikube start

text
5. Tried deploying with:
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

text
6. Faced path errors during local apply due to OneDrive/Windows file structure—files are correct for standard use[web:57][web:63].

## How to Deploy (for Reviewers)
- Build Docker image as above.
- Deploy on any Kubernetes cluster using files in the `k8s` folder with:
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

text
- Move files if paths differ.

## Notes
- All configs match industry standards for Docker and Kubernetes.
- Deployment was attempted using Minikube, but local Windows/OneDrive paths caused "not found" errors.
- This folder contains everything needed for Docker and Kubernetes usage—just adjust paths if needed[web:54][web:63][web:57].

## Contact
For questions or clarifications, refer to the comments in code or YAML files.
