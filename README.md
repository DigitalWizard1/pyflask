# Python Flask Demo
## Info
This was written following the tutorial at https://www.section.io/engineering-education/deploy-docker-container-to-kubernetes-cluster/

## Run Steps
```
minikube start --ports 127.0.0.1:30100:30100 --ports 127.0.0.1:30400:30400 --ports 127.0.0.1:30833:30833
eval $(minikube docker-env)
docker build --tag flask-test-app:latest .
kubectl apply -f deployment.yaml
kubectl get services
kubectl get deployments
minikube start service: flask-test-service
minikube dashboard &
google-chrome 127.0.0.1:30833 &

```