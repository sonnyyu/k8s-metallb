# k8s-metallb
Get Install Software
```sh
git clone https://github.com/sonnyyu/k8s-metallb
cd k8s-metallb
```
Setup Metallb
```sh
kubectl get nodes
kubectl get deployments --all-namespaces
kubectl get service -o wide --all-namespaces
kubectl get pods --all-namespaces
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.12.1/manifests/namespace.yaml
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.12.1/manifests/metallb.yaml
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
Remove Metallb
```sh
kubectl get service -o wide --all-namespaces
kubectl delete svc <service_name>
kubectl get deployments --all-namespaces
kubectl delete deployment <deployment_name>
kubectl delete -f config.yaml
kubectl delete -f https://raw.githubusercontent.com/metallb/metallb/v0.12.1/manifests/namespace.yaml
kubectl delete -f https://raw.githubusercontent.com/metallb/metallb/v0.12.1/manifests/metallb.yaml
```
