# Local infrastructure

## Startup cluster
k3d cluster create --config configs/k3d-config.yaml

## Apply manifests
kubectl apply -f manifests

## Install helm charts
### MongoDB
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install mongodb --namespace mongodb --values helm-charts/mongodb/values.yaml bitnami/mongodb

## Start skaffold
skaffold dev --cache-artifacts=false