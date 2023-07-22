# Create aks with auto scaler
```t

# Setup env
export RESOURCE_GROUP=
export REGION=
export AKS_CLUSTER=

# Create resource group
az group create --location ${REGION} --name ${RESOURCE_GROUP}

# Create AKS cluster
az aks create --resource-group ${RESOURCE_GROUP} \
              --name ${AKS_CLUSTER} \
              --enable-managed-identity \
              --generate-ssh-keys \
              --node-count 1 \
              --enable-cluster-autoscaler \
              --min-count 1 \
              --max-count 5

# Get credential
az aks get-credentials --name ${AKS_CLUSTER} --resource-group ${RESOURCE_GROUP}              
```