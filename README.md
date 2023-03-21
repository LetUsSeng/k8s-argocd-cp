# k8s-argocd-cp

## Prerequisite

### Environment Setup

For this local POC, use the below in order to provision a local Kubernetes cluster.

- [docker desktop](https://docs.docker.com/desktop/)
- [rancher](https://rancherdesktop.io/)
- [k3s](https://k3s.io/)
- [microk8s](https://microk8s.io/)

### AWS Setup
For this POC, we are going  to create a bucket that is managed by a combination of ArgoCD and Controlplane.

### ArgoCd Setup

I setup ArgoCD via kustomize and ArgoCD's [declarative approach](https://argo-cd.readthedocs.io/en/release-1.8/operator-manual/declarative-setup/#manage-argo-cd-using-argo-cd)

```bash
kubectl create ns argocd
kubectl apply -k argocd/overlays/production -n argocd
```

### Crossplane