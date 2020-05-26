# **Practice Kubernetes**

## **Launch single node kubernetes cluster**

### Step 1
1. Install `minikube` local
```
minikube version
```
2. Start cluster
```
minikube start --wait=false
```


### Create namespaces  (testing)
kubectl apply -f ./namespace/namespace.yml
kubectl get namespace

### Create services (NodePort,ClusterIP, LoadBalancer)
kubectl -n testing get svc
kubectl -n testing apply -f ./service/01-service-NodePort.yml

kubectl -n testing apply -f ./service/02-service-ClusterIP.yml
kubectl -n testing apply -f ./service/03-service-LoadBalancer.yml


## Create replication-controller
kubectl -n testing get pods
kubectl -n testing appliy -f ./replication-controller/01-rc-wordpress.yml
