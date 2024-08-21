# Redis Kubernetes Deployment

## Steps to Create and Expose Redis

1. **Create a New GitHub Repository**:
   - Created a repository and added a `pod.yml` file for Redis pod definition.

2. **Deploy the Redis Pod**:
   - Cloned the repository.
   - Applied the `pod.yml` configuration to deploy the Redis pod.
   - Verified the pod is running using `kubectl get pods`.

3. **Create a Service to Expose Redis**:
   - Exposed the Redis pod using `kubectl expose` command with NodePort type.
   - Verified the service creation using `kubectl get services` and `kubectl describe service redis-svc`.

4. **Access the Redis Server**:
   - Retrieved the Node IP and NodePort.
   - Connected to Redis using `redis-cli`.

## Commands Used

- Deploy Redis Pod: `kubectl apply -f pod.yml`
- Expose Redis Pod: `kubectl expose pod redis-pod --type=NodePort --name=redis-svc --port=6379 --target-port=6379`
- Verify Services: `kubectl get services`
- Get Service Details: `kubectl describe service redis-svc`
- Access Redis: `redis-cli -h <NodeIP> -p <NodePort>`

## Issues Encountered

- Describe any issues and resolutions encountered during the process.

