# Argo-cd Ezcluster plugin

## Post install

Get initial password and change it

```
argocd login argocd.ingress.ksprayX.XXX --username admin --password $(kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2)
argocd account update-password --current-password $(kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2) --new-password admin
```

## Add repo:

```
argocd repo add https://github.com/mycompany/myrepo.git --username "user@mycompany.com" --password xxxx
```



