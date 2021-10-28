# DataCenter Enviroment 2C

Source Code for this Module (https://github.com/WEEMR/terraform-aws-DataCenter_Enviroment_2C)

Terraform Registery         (https://registry.terraform.io/modules/WEEMR/DataCenter_Enviroment_2C/aws/latest)

The module will create the below resources:


- 2 x VPCs, one of Hub and one for Spoke
- Networking Stack (VPC, Subnets, Route Tables, Security Groups and Internet Gateway) - Please refer to the diagram below. 
- 2 x FortiGate with 3 interfaces (Two Interfaces in two different Public Subnets and one in the Private subnets)
- Windows Server 2019 Behind the FGT Port 3 [LAN]
- Ubunutu Server with Apache installed, iperf, fzf, pydf, firefox, lynx and elinks installed on it behind the FGT port 3 [LAN]
- Route53 DNS Public Hosted Zones

- FortiManager and FortiAnalyzer will be deployed as well behind the Hub FGT on Port 3 [LAN]


![image](https://user-images.githubusercontent.com/83562796/135917134-e282029b-3fdb-434a-a411-e4f1dfdd9a44.png)


// The DNS Hosted Zones must be sub-zones for a domain that is registered or managed by AWS Route53 //

// i.e xyz.com is the domain name and the script will create the subzone Lab1.xyz.com // 


![image](https://user-images.githubusercontent.com/83562796/135913871-7e4c667a-1271-4492-90ed-17c38b47d64b.png)
