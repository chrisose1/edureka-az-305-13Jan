# initial setup
 - Create Free Tier account of Azure - https://azure.microsoft.com/en-us/
 - installation - link (https://code.visualstudio.com/download)
 - Install VS Code extension - azure resource manager tools extension (https://marketplace.visualstudio.com/items?itemName=msazurermtools.azurerm-vscode-tools)
 - install git bash on your system(windows) : https://git-scm.com/download/win
 - Install CLI on the local PC:
https://learn.microsoft.com/en-us/cli/azure/

- verify the installation (git bash (windows) /terminal  (mac)):
`az --version`

# Azure basics

- https://portal.azure.com - azure portal


```
az account set --subscription "subscription_name"

```

# Getting Started with Azure Resource Manager
```
az login
az group create --name arm-vscode --location eastus

az deployment group create --resource-group arm-vscode --template-file demo.json 
```


# Demo 2
```
az login
az group create --name arm-vscode --location eastus

az deployment group create --resource-group arm-vscode --template-file demo.json --parameters dev.parameters.json

az deployment group create --resource-group arm-vscode --template-file demo.json --parameters prod.parameters.json
```

# Demo 3
```
az group create --name arm-vscode --location eastus

az deployment group create --resource-group arm-vscode --template-file variables.json --parameters variables.parameters.json
```


# Demo 4
```
az group create --name arm-vscode --location eastus

az deployment group create --resource-group arm-vscode --template-file outputs.json --parameters outputs.parameters.json
```