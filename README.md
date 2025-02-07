# Argo CD installation and configuration

This repository is used for bootstrapping Argo CD on a Kubernetes cluster.  
It also enables self-management of Argo CD using Argo CD itself.

## Usage

Apply the production overlay:

```bash
kubectl apply -k argocd-setup/overlays/prod
```

This setup ensures that Argo CD is installed and configured to manage its own resources within the cluster.