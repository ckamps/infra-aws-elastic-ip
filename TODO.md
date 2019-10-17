* Since the AWS::EC2::EIP CloudFormation resource does not yet support assigning a "Name" tag to this resource, consider reusing one of open source examples of CloudFormation custom resources to do so.  When this is done, then our standard attributes will be applied. i.e.

```
...Name: !Sub '${pOrg}-${pSystem}-${pApp}-${pPurpose}-${pEnvPurpose}' 
```