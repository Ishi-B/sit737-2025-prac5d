# Cloud Native Application Development - Practical 5.2D

**SIT737 - Deakin University**  

**5.2D: Dockerization- Publishing the microservice into the cloud**   


## Overview
This repository contains a cloud-native microservice Dockerized and published to Google Container Registry (GCR) as part of Deakin's Cloud Native Application Development unit.

## 🚀 Features
- Node.js microservice containerized with Docker
- Kubernetes deployment manifests
- Automated build process
- Published to Google Container Registry

## Repository Structure
sit737-2025-prac5d/
├── src/ # Source code directory
│ └── app.js # Microservice implementation
├── Dockerfile # Docker configuration
├── deployment.yaml # Kubernetes deployment
├── service.yaml # Kubernetes service
├── package.json # Node.js dependencies
└── .gitignore # Git ignore rules


## 🛠️ Prerequisites
- Node.js 16+
- Docker
- Google Cloud SDK
- kubectl

## 🔧 Installation
1. Clone the repository:
   git clone https://github.com/Ishi-B/sit737-2025-prac5d.git
   cd sit737-2025-prac5d
Install dependencies:

bash
npm install
🐳 Docker Commands
Build the image:

bash
docker build -t gcr.io/[PROJECT-ID]/my-microservice:1.0.0 .
Push to GCR:

bash
docker push gcr.io/[PROJECT-ID]/my-microservice:1.0.0
Run locally:

bash
docker run -p 3000:3000 gcr.io/[PROJECT-ID]/my-microservice:1.0.0
☸️ Kubernetes Deployment
bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
