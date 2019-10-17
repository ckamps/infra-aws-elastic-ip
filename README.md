# Provision Elastic IP Address

This CloudFormation template can be used in those cases where an Elastic IP address must be provisioned before external dependencies are provisioned. 

The template exports the IP address and allocation ID so that other dependent CloudFormation templates can import it.

```
${AWS::StackName}::address
${AWS::StackName}::allocation-id 
```

For example, when setting up a site-to-site VPN connection between a VPN gateway platform and an AWS Customer Gateway, the external IP address of the local VPN gateway is needed before the AWS Customer Gateway resource can be configured.  Additionally, the local VPN gateway can't be configured until the AWS Customer Gateway is configured.