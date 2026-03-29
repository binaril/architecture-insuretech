run

```bash
minikube start --driver=docker --addons=metrics-server --cpus=8 --memory=12g

minikube addons enable metrics-server
minikube dashboard 

kubectl apply -f deployment.yaml 
kubectl apply -f service.yaml
kubectl apply -f scaletestapp-hpa.yaml

minikube service scaletestapp-service --url



kubectl apply -f locust-test.yaml
kubectl logs -f job/locust-test
```

