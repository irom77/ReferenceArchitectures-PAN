# ReferenceArchitectures-PAN

### Deployemnt

rg="panlab-ref"
dn="panlab-ref-deployment"
file="main.json"
parm="parm"

az group create --name $rg  --location "East US"
az group deployment create \
  --name $dn \
  --resource-group $rg \
  --template-file $file \
  --parameters "$parm"
az group delete -n $rg  