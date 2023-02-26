# remote-package-install-script
Hosting collection of Bash and Powershell scripts to install packages various automation tools in Linux and Windows Environment 


For Linux Host on Azure 
```bash
az vm extension set \
  --resource-group <your rg> \
  --vm-name <your vm> \
  --name customScript \
  --publisher Microsoft.Azure.Extensions \
  --version 2.1 \
  --settings '{"fileUris":["<raw github url>"]}' \
  --protected-settings '{"commandToExecute": "./<script-to-run>.sh"}'
```

Basic az commands to get your rg and vm
```bash
# List all RGs located <region>
 az group list --query "[?location=='<region>']" -o table


# List all VM in RG
 az vm list --resource-group  <RG> -o table
 
 ```bash
