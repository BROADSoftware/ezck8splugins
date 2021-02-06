# Argo-cd Ezcluster plugin

## Post install

Get initial password and change it

```
kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2
argocd login argocd.shared1
argocd account update-password
```
## Add repo:

```
argocd repo add https://github.com/mycompany/myrepo.git --username "user@mycompany.com" --password xxxx
```



