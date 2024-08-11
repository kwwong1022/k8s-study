# K8s Web App + MongoDB Setup

## Prerequisite

- Docker driver installed
- Minikube installed

## Setup
1. Apply manages applications through files defining K8s resources
   ```
   # kubectl apply -f <file-name.yaml>
   # mongo-config.yaml
   $ kubectl apply -f mongo-config.yaml
   > configmap/mongo-config created  # returned message

   # mongo-secret.yaml
   $ kubectl apply -f mongo-secret.yaml
   > secret/mongo-secret created  # returned message

   # mongo.yaml
   $ kubectl apply -f mongo.yaml
   ```

2. Check if the resources have been created
   ```
   $ kubectl get all

   # list resources by type
   $ kubectl get pod | configmap | secret | ...
   ```
