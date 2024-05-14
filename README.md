# Kubernetes Demo Project: MongoDB and Mongo Express Deployment

Welcome to the Kubernetes Demo Project! 

## Overview

This project showcases the deployment of MongoDB and Mongo Express within a Kubernetes environment. The setup includes configurations for pods, secrets, internal and external services, and a config map.

## Project Files

In this repository, you will find the following Kubernetes configuration files:

- `mongo.yaml` - Defines the deployment for the MongoDB database pod.
- `mongo-secret.yaml` - Manages sensitive data like MongoDB user credentials.
- `mongo-configmap.yaml` - Stores configuration data in a way that can be consumed by pods.
- `mongo-express.yaml` - Deploys Mongo Express, which acts as a web-based MongoDB client.
- `nginx-service.yaml` - Although named as an nginx service, this file is configured to expose the Mongo Express to external traffic (please check for misnaming).
- `ingress.yaml` - Sets up ingress resources for accessing the services from outside the Kubernetes cluster.
- `Slides/` - Contains presentation slides for educational purposes.
- `k8s-commands.md` - A markdown file that lists useful Kubernetes commands.
- `troubleshooting.md` - Offers solutions to common problems you might encounter.

## Getting Started

To deploy this demo on your Kubernetes cluster, follow the steps below:

1. **Apply the Secrets and Config Map:**
   ```bash
   kubectl apply -f mongo-secret.yaml
   kubectl apply -f mongo-configmap.yaml
   
## Deploy the MongoDB and Mongo Express

Execute the following commands in your terminal to deploy the MongoDB database and Mongo Express, which is a web-based MongoDB client.

```bash
kubectl apply -f mongo.yaml
kubectl apply -f mongo-express.yaml
