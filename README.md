# DevOps Capstone Project: QR Code Generator

## Overview
The QR Code Generator is available at [rishabkumar7/devops-qr-code](https://github.com/rishabkumar7/devops-qr-code) web application that converts a URL into a QR Code. This project consists of three main components: a Front-end, an API, and a Storage solution. All components are containerized and hosted using a cloud provider of your choice. The goal of this project is to apply DevOps practices such as containerization, CI/CD, observability, and monitoring.

## Project Components

### 1. Application Components
- **Front-End**: A web application where users can submit URLs.
- **API**: An API that receives URLs and generates QR codes. The API can store the generated QR codes in cloud storage (e.g., AWS S3, Azure Blob Storage, GCP Cloud Buckets).
- **Storage**: A storage solution to hold the generated QR codes, ensuring security and accessibility for the stored data.

### 2. Programming
The sample application code is available at [rishabkumar7/devops-qr-code](https://github.com/rishabkumar7/devops-qr-code). The application is built using:
- **Front-End**: Next.js
- **API**: FastAPI (Python framework)
- **Storage**: AWS S3

## Requirements

### 1. Containerization
- Create Dockerfiles to containerize both the front-end and API components.

### 2. CI/CD
- Write a CI/CD pipeline to automate the deployment of the containers whenever there is a change in the source code or Dockerfile.

### 3. Infrastructure as Code (IaC)
- Use Terraform to define and deploy the cloud infrastructure, specifically a Kubernetes cluster.

### 4. Kubernetes YAML Files
- Create deployment and service YAML files for both the Next.js front-end and the FastAPI backend.

### Optional Enhancements
- Customize the provided application. The sample app uses AWS S3, but you can utilize cloud SDKs/modules (e.g., `boto3` for AWS, `google-cloud` for GCP, `azure` for Azure) to interact with the respective cloud storage services.

## Deployment Steps

1. **Containerization**: 
   - Containerize the front-end and API using Docker.

2. **Setup CI/CD**: 
   - Push the containers to a container registry (e.g., Azure Container Registry, Amazon ECR, Google Container Registry, or Docker Hub).

3. **Kubernetes Setup**: 
   - Set up a Kubernetes service within your cloud provider (e.g., Azure AKS, Amazon EKS, or GCP GKE).
   - Use IaC tools like Terraform to define and deploy the Kubernetes cluster.

4. **Deploy Containers**: 
   - Deploy the front-end and API containers to the Kubernetes cluster.
   - Ensure that the containers are interconnected for seamless data flow.

5. **CI/CD Pipeline**: 
   - Set up a CI/CD pipeline to deploy the Kubernetes manifests to the cluster after any source code changes.

## Implementation

### Web Application
- Users can access the front-end, which is publicly accessible via a URL and includes an input field for entering URLs.

### API Interaction
- Once a URL is entered by a user, the web application makes a request to the API container to convert the URL into a QR Code.

### Storage
- The generated QR Code is stored and displayed on the web application for the user.

### CI/CD Pipeline
- Set up a CI/CD pipeline to deploy the containers and application after any source code changes. You can utilize tools like GitHub Actions or Azure DevOps.

### Monitoring
- Set up monitoring for the containers to track key metrics and gain insights. Options include Azure Monitor for AKS, Amazon CloudWatch Container Insights for EKS, or setting up Grafana for more advanced monitoring.

## Conclusion
This project aims to demonstrate the application of DevOps practices in a real-world scenario by containerizing a QR Code generator application and automating its deployment using CI/CD pipelines. The project also emphasizes the importance of observability and monitoring in maintaining a robust application.
