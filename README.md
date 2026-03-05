# learn-k8s

```sh
minikube start --extra-config="apiserver.cors-allowed-origins=['http://boot.dev']"

# create deployment
kubectl create deployment synergychat-web --image=docker.io/bootdotdev/synergychat-web:latest
kubectl get pods
# replace PODNAME
kubectl port-forward PODNAME 8080:8080
kubectl logs PODNAME
kubectl delete pod PODNAME
# 'wide' output (IP, NODE, ...)
kubectl get pods -o wide
kubectl proxy

kubectl get deployment synergychat-web -o yaml
kubectl edit deployment synergychat-web

kubectl get deployment synergychat-web -o yaml > web-deployment.yaml

kubectl apply -f web-deployment.yaml
```
