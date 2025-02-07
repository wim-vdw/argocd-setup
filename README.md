# Argo CD installation and configuration

This repository is used for bootstrapping Argo CD on a Kubernetes cluster.  
It also enables self-management of Argo CD using Argo CD itself.

To ensure separation of concerns three repositories are used to manage the Argo CD setup:

* Argo CD installation and
  configuration: [https://github.com/wim-vdw/argocd-setup](https://github.com/wim-vdw/argocd-setup)
* Argo CD application definitions: [https://github.com/wim-vdw/argocd-apps](https://github.com/wim-vdw/argocd-apps)
* Kubernetes manifests or Helm charts used by Argo CD
  applications: [https://github.com/wim-vdw/argocd-k8s-resources](https://github.com/wim-vdw/argocd-k8s-resources)

## Usage

Apply the production overlay (everything will be deployed in the `argocd` namespace):

```bash
kubectl apply -k argocd-setup/overlays/prod
```

This setup ensures that Argo CD is installed and configured to manage its own resources within the cluster.
