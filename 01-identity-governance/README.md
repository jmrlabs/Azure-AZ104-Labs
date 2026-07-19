PS C:\WINDOWS\system32> AZ LOGIN
Select the account you want to log in with. For more information on login with Azure CLI, see https://go.microsoft.com/fwlink/?linkid=2271136

Retrieving tenants and subscriptions for the selection...

[Tenant and subscription selection]
No     Subscription name     Subscription ID    Tenant
[1] *  Azure subscription 1  <redacted>         Default Directory

Tenant: Default Directory
Subscription: Azure subscription 1 (<redacted>)

PS C:\WINDOWS\system32> az account show
{
  "environmentName": "AzureCloud",
  "homeTenantId": "<redacted>",
  "id": "<redacted>",
  "isDefault": true,
  "managedByTenants": [],
  "name": "Azure subscription 1",
  "state": "Enabled",
  "tenantDefaultDomain": "<redacted>",
  "tenantDisplayName": "Default Directory",
  "tenantId": "<redacted>",
  "user": {
    "name": "<redacted>",
    "type": "user"
  }
}

PS C:\WINDOWS\system32> az group create --name az104-labs-rg --location eastus
{
  "id": "/subscriptions/<redacted>/resourceGroups/az104-labs-rg",
  "location": "eastus",
  "managedBy": null,
  "name": "az104-labs-rg",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "type": "Microsoft.Resources/resourceGroups"
}
