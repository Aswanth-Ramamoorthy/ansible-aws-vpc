#Ansible role: AWS VPC Subnets.

This role handles the creation of VPC subnets and Bastion host in AWS.
* [About AWS VPC](#about aws vpc)
* [Requirements](#requirements)
* [Role Variables](#role variables)
* [License](#license)
* [Author Information](#author)

# About AWS VPC
Amazon Virtual Private Cloud (Amazon VPC) is a service that lets you launch AWS resources in a logically isolated virtual network that you define. You have complete control over your virtual networking environment, including selection of your own IP address range, creation of subnets, and configuration of route tables and network gateways. You can use both IPv4 and IPv6 for most resources in your virtual private cloud, helping to ensure secure and easy access to resources and applications.

#Requirements
* Ansible 2.5
* botocore
* boto3

#Role variables 

* region: The region which the resources will be created https://docs.aws.amazon.com/general/latest/gr/rande.html#vpc_region
* vpcCidr: CIDR Block of VPC
* subnet_cidr: CIDR Block of Subnet
* ash_IGW: IGW Name
* ash-PubRT: Public subnet Route Table
* ash-PrivRT: Private subnet Route Table
* ash_NGW: NAT Gateway name
* ash-pubsub1: Public subnet in Zone 1
* ash-pubsub2: Public subnet in Zone 2
* ash-pubsub3: Public subnet in Zone 3
* ash-privsub1: Private subnet in Zone 1
* ash-privsub2: Private subnet in Zone 2
* ash-privsub3: Private subnet in Zone 3
* Bastion-host-sg: Security group for Bastion host that allows port 22 from everywhere 

#License
* MIT License


#Author Information
- Aswanth Ramamoorthy - aswanthramamoorthy@gmail.com
