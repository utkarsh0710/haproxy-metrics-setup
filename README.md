# HAProxy and Metrics Deployment

This project automates the deployment of:
1. HAProxy Container: A fixed HAProxy image load-balancing three NGINX processes.
2. Metrics Container: A Python-based Flask application exposing system metrics at /metrics

## Steps to Complete the Tasks

### Task 1: Fix HAProxy Container
1. Pulled the original image from Docker Hub: mkassaian/docker-challenge
2. Fixed missing NGINX configuration and updated HAProxy to be accessible via localhost.
3. Modified the HTTP response to include "it works!".
4. Created a new Docker image and pushed it to Docker Hub: (https://hub.docker.com/r/utkarsh0710/haproxy-fixed).

### Task 2: Deploy Metrics Container
1. Created a Python Flask application to expose system metrics using psutil
2. Added a Dockerfile to package the application.
3. Built the image and pushed it to Docker Hub: (https://hub.docker.com/r/utkarsh0710/metrics-image).
4. Used Ansible to automate:
   - Rendering the Dockerfile.
   - Building the image.
   - Deploying the container on `localhost:5000`.
