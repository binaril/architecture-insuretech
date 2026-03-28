Не удалось с помощью этого сценария достичь лимита 30Мб упирается в процессор. Для тестирования изменено на 6Мб

run

```bash
minikube start --driver=docker --driver=docker --addons=metrics-server
minikube addons enable metrics-server
minikube dashboard 

kubectl apply -f deployment.yaml 
kubectl apply -f service.yaml
kubectl apply -f scaletestapp-hpa.yaml
```

