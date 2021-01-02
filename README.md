# Helm chart for deploying Syncthing to K8s

Bare bones helm chart for deploying [Syncthing](https://syncthing.net/) to k8s.

Syncthing uses UDP for discovery and k8s services don't support it so NodePort must be used for the `backend` service (unless you figure something out).

see [values.yaml](syncthing/values.yaml) for configurations.

Install using Helm v3:

```
helm repo add flipenergy https://flipenergy.github.io/k8s-homelab/
helm install my-release flipenergy/syncthing
```
