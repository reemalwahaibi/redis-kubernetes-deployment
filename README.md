# Redis Deployment on Kubernetes

## Overview

This document provides a step-by-step guide to deploy a Redis server on Kubernetes and expose it using a NodePort service. It also includes instructions on how to access the Redis server.

## Prerequisites

- Kubernetes cluster running (local or cloud-based)
- kubectl CLI tool installed
- Docker installed (for local testing)

## Steps

### 1. Create a Pod Definition

1. **Create `pod.yml`**: Define a Redis pod using the following YAML configuration.

   ```yaml
   apiVersion: v1
   kind: Pod
   metadata:
     name: redis-pod
     labels:
       app: redis
   spec:
     containers:
     - name: redis-container
       image: redis
       ports:
       - containerPort: 6379
