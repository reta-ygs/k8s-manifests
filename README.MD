# Setup
## Doppler CLI
```shell
doppler login
doppler setup
```
## Doppler Token Secret
```shell
kubectl create namespace doppler-operator-system 
kubectl create secret generic doppler-token-secret \
  --namespace doppler-operator-system \
  --from-literal=serviceToken=$(doppler configs tokens create doppler-kubernetes-operator --plain)
```

## Kustomize
```shell
kubectl apply -k .
```