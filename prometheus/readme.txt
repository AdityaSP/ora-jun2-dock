kubectl create namespace monitoring
kubectl create -f cluster-role.yml
kubectl create -f config-map.yml -n monitoring
kubectl create  -f prometheus-deployment.yml --namespace=monitoring
kubectl get deployments --namespace=monitoring
kubectl create -f prometheus-service.yml--namespace=monitoring
