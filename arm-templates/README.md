```ps1
$RESOURCE_GROUP='<Put your resource group name>'
$LOCATION='japaneast'
$PREFIX='<Put your prefix>'

az group create --name $RESOURCE_GROUP --location $LOCATION

az group deployment create `
    --resource-group $RESOURCE_GROUP `
    --handle-extended-json-format `
    --template-file ./arm-templates/resources.json `
    --parameters `
        prefix=$PREFIX
```
