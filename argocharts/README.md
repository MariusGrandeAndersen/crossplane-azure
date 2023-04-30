from this folder on local kind cluster with argocd and crossplane installed and being connected to azure subscription:
helm install argocharts .
k port-forward svc/argo-cd-argocd-server 8080:80
kubectl -n default get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d