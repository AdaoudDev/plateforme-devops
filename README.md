# Notes Ahmad 
- Lancer le projet avec :
```bash 
terraform init && terraform apply
```
- Commande pour obtenir le mot de passe ArgoCD : 
```bash
kubectl --context kind-plateforme -n argocd get secret argocd-initial-admin-secret -o jsonpath='{.data.password}' | base64 -d ; echo
```
- Pour lancer ArgoCD :
```bash
kubectl --context kind-plateforme -n argocd port-forward svc/argocd-server 8443:443
```

- Pour passer un apply/plan avec le fichier tfvars : 
```bash
terraform plan -var-file=plateforme.tfvars
```