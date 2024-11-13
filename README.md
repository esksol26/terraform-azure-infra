# terraform-azure-infra

# Network Module

This module sets up a virtual network in Azure, including subnets and network security groups.

## Variables
- `resource_group_name` (string): Name of the resource group where the network will be created.
- `vnet_name` (string): Name of the virtual network.
- `address_space` (list of strings): The address range for the virtual network.
- `subnet_name` (string): Name of the subnet to create in the virtual network.
- `subnet_address_prefix` (string): Address prefix for the subnet.

## Outputs
- `vnet_id` (string): The ID of the created virtual network.
- `subnet_id` (string): The ID of the created subnet.

## Usage
To use this module in your Terraform configuration, you can add the following code:

```hcl
module "network" {
  source = "./modules/network"  # Path to the network module folder
  resource_group_name = var.resource_group_name
  vnet_name           = var.vnet_name
  address_space       = ["10.0.0.0/16"]
  subnet_name         = "default-subnet"
  subnet_address_prefix = "10.0.1.0/24"
}
