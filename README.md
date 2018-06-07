# cloud-render-prepare-ARM
# Prepre Cloud-based Render Environment on Azure using ARM Template

This template prepares the environment for a basic cloud-based rendering solution on Azure. 
![cloud-render-arm](https://user-images.githubusercontent.com/15788466/41114802-554fbc60-6a3a-11e8-9008-c9ae5ab618a5.jpg)

The ARM automation scripts creates:
1.	An Azure virtual network (VNet) with following subnets
    - Render Subnet (for render clients)
    - FastCache Subnet (for Avere vFXTs)
    - Management Subnet (for jump hosts)
    -	Gateway Subnet (for VPN/ExpressRoute connectivity)
    - Shared Storage Subnet (for intermediary job data storage)
3.	Network Security Groups with basic rules
4.	A jump host for management / administration / Fast Cache build using the a Ubuntu based custom managed image

Pre-requisites:
- This template assumes a Azure managed custom image is available within the subscription and in the location requested.

Note: This template does not create render clients.
