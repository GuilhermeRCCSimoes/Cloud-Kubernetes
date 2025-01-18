# Kubernetes Application Deployment Exercise
## Overview
This exercise demonstrates how to deploy an Odoo application (see what this is [here](https://odoo.com)) in a Minikube cluster using Kubernetes objects. The repository contains an Odoo application project, and your task is to implement the necessary Kubernetes resources to run this application in a local Minikube environment.
### Prerequisites

- Minikube installed and running
- kubectl configured to work with Minikube
- Basic understanding of Kubernetes concepts
- Docker installed (for building custom images if needed)

## Exercise Steps

- Clone the repository containing the Odoo application project.
- Create the following Kubernetes objects: a. Deployment for Odoo
    - Service to expose Odoo
    - ConfigMap for PostgreSQL configuration
    - Deployment for PostgreSQL
    - Ingress configured to make application able to be connected via HTTPS (Certificates are also needed here)
      - You will need to adapt `/etc/hosts` for the domain of your choice
    - Ensure your Kubernetes objects adhere to the following requirements:
      - Use the official Odoo image
      - Configure environment variables for database connection
      - Expose the Odoo service on a ClusterIP
      - Use a persistent volume for PostgreSQL data storage
    - Apply the Kubernetes objects to your Minikube cluster using kubectl apply -f <filename>.yaml.
    - Verify the deployment by accessing the Odoo application through the domain name

## Submission
- [ ] Create a fork of this repository so I can take a look later on. 
- [ ] create `kubernetes` directory in the project repository and place all your Kubernetes YAML files there. Include a brief explanation of each resource in comments within the YAML files.

> [!IMPORTANT]
> Create also a text file in Drive 


Good luck

________________________________________________________________________________________________________________________________

# Odoo Kubernetes Deployment

This project deploys Odoo and PostgreSQL on a Kubernetes cluster using Minikube.

## Prerequisites
1. Install Minikube and kubectl.
2. Install Cert-Manager for TLS certificates.

## Steps to Run
1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd odoo-kubernetes

### **How to Use**
1. Clone or create the folder structure as shown.
2. Save the provided YAML and script files into the appropriate folders.
3. Run the `apply-all.sh` script to deploy everything at once.