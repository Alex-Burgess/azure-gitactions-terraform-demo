# Azure GitHub Actions Demo
Demonstrates how to create Azure resources using Terraform with a CI/CD pipeline.

## Terraform Setup

1. Create resource group:
```
az group create --name tfstate --location uksouth
```
1. Create storage account
```
az storage account create --resource-group tfstate --name tfstate24288 --sku Standard_LRS --encryption-services blob
```
1. Create blob container
```
az storage container create --name $CONTAINER_NAME --account-name $STORAGE_ACCOUNT_NAME
```
1. Update details in `backend.tf`
1. Test Locally
```
terraform init
terraform apply
```

## Terraform Git Actions setup


## References
- https://learn.microsoft.com/en-us/azure/developer/terraform/store-state-in-azure-storage?tabs=azure-cli
