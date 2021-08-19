# Local infrastructure

## Startup cluster
k3d cluster create --config configs/k3d-config.yaml

## Start skaffold
skaffold dev --cache-artifacts=false