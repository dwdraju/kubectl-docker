# Docker for executing kubectl - Built for CI/CD

### Usage

##### Local
```
docker run --rm -v ~/.kube/config:/root/.kube/config dwdraju/kubectl-docker kubectl cluster-info
```

##### Gitlab CI/CD
```
echo $KUBE_CONFIG | base64 -d > ${HOME}/.kube/config
kubectl get pods
```