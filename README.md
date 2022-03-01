# k8s-metallb
```sh
kubectl get nodes
kubectl get pods --all-namespaces
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.11.0/manifests/namespace.yaml
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.11.0/manifests/metallb.yaml
kubectl get pods --all-namespaces
kubectl apply -f config.yaml
kubectl -n metallb-system get configmaps
kubectl -n metallb-system get all
kubectl create deployment nginx --image=nginx
kubectl expose deployment nginx --type=LoadBalancer --port=80
kubectl -n metallb-system get configmaps
kubectl get deployments.apps
kubectl get service -o wide
curl http://192.168.1.3
```
