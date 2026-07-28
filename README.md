# module-ixnetwork-web-app/azurerm

## Description
Terraform module for IxNetwork Web application deployment on Microsoft Azure

## Deployment
This module creates a single instance having a single network interface.

## Usage
```tf
module "App" {
	source = "git::https://github.com/Keysight/terraform-azurerm-module-ixnetwork-web-app.git"
	Eth0SubnetId = module.Vnet.PublicSubnet.id
	ResourceGroupName = azurerm_resource_group.ResourceGroup.name
	SshKeyName = azurerm_ssh_public_key.SshKey.name
}
```
