# Miiingle.NET - Helm Chart for the Kubernetes Cluster
The Helm Chart for All the Apps installed on the Kubernetes Cluster

## Install Helm
- download
```
https://github.com/helm/helm/releases
```
- unpack
```
tar -zxvf helm-v3.0.0-linux-amd64.tar.gz
```
- move to executable
```
sudo mv linux-amd64/helm /usr/local/bin/helm
```

## Add Tiller User
```
kubectl apply -f raw/tiller-user.yaml
```

## Install the kube-utils
```
helm install -f kube-utils/values.yaml kube-utils ./kube-utils
```

## Install the backend
```
helm install -f backend/values.yaml backend ./backend

//upgrade to new version
helm upgrade -f backend/values.yaml backend ./backend
```