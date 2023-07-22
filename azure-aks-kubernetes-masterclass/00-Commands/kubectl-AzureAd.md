# Relogin with different account => override current login by get credential again with same cluster
```t
az aks get-credentials --resource-group aks-rg3 --name aksdemo3 --overwrite-existing
kubectl config view
```
# Override azure AD with kubectl admin
```t
az aks get-credentials --resource-group myResourceGroup --name myManagedCluster --admin
```