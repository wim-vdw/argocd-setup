# Argo CD installation and configuration

## Usage

Apply the production overlay:

```bash
kubectl apply -k argocd-setup/overlays/prod
```

This setup ensures that Argo CD is installed and configured to manage its own resources within the cluster.