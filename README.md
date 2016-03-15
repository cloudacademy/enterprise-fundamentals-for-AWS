#Enterprise Fundamentals for AWS

#####This repository is part of the [Enterprise Fundamentals for AWS](https://cloudacademy.com/amazon-web-services/enterprise-fundamentals-for-aws-course/) course at [CloudAcademy.com](http://cloudacademy.com).

-----------


###Integrating with on-premises:

Use this quick guide to follow the examples.

#####Creating resources with CloudFormation

Use [this](https://aws.amazon.com/quickstart/quick-launch/activedirectory-architecture/) quick start reference to create the AD infrastructure that will simulate out on-premises network. You can also download the template in [here](https://s3.amazonaws.com/quickstart-reference/microsoft/activedirectory/latest/templates/QuickTemplate_1_AD_2012.template) and launch it directly from the CloudFormation console.

Use [this](/https://raw.githubusercontent.com/cloudacademy/enterprise-fundamentals-for-AWS/master/Public-Private-VPC.template) CloudFormation template to create the Cloud VPC

#####Connecting to the Active Directory Domain

	To connect to the DC instances via the Remote Desktops gateway you need to add an inbound rule in the RDGWSecurityGroup allowing connections on the HTTPS port (443). You can also simply use the Gateways as Bastion hosts and open an RDP connection direct to them, in this case you don't have to change anything on the Security Groups.

Take the Elastic IP from the outputs of the CloudFormation stack and use it to connect to the machines. These are the credentials for the built in Domain Admin account:

```
Username: StackAdmin
Password: Password123
```



