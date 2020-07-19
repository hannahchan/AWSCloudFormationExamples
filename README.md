# AWS CloudFormation Examples #

AWS CloudFormation is an *Infrastructure-as-Code* solution to model and provision AWS resources in a predictable and repeatable way. This repository contains examples of AWS CloudFormation templates intended to be used for learning purposes.

## Creating CloudFormation Stacks ##

You can create CloudFormation stacks from the example templates either via the [CloudFormation Console](https://console.aws.amazon.com/cloudformation/) or via the [AWS Command Line Interface (CLI)](https://aws.amazon.com/cli/). If using the AWS CLI, you can use the following example command to help you get started.

```
aws cloudformation create-stack --stack-name <stack-name> --template-body file://<path-to-template>/<template>.json
```

## More Information ##

To learn more about AWS CloudFormation, head over to their product page at;

- https://aws.amazon.com/cloudformation

For detailed information about how to use AWS CloudFormation, check out their documentation at;

- https://docs.aws.amazon.com/cloudformation
