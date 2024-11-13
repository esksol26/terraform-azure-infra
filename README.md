# terraform-azure-infra

# Network Module
This module sets up a virtual network in Azure, including subnets and network security groups.

## Variables
- `resource_group_name`: Name of the resource group where the network will be created.
- `vnet_name`: Name of the virtual network.
- `address_space`: The address range for the virtual network.

## Outputs
- `vnet_id`: The ID of the created virtual network.

## Usage
