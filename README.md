# AWS CloudFormation Examples

AWS CloudFormation is an _Infrastructure-as-Code_ solution to model and provision AWS resources in a predictable and repeatable way. This repository contains examples of AWS CloudFormation templates intended to be used for learning purposes.

## Creating CloudFormation Stacks

You can create CloudFormation stacks from the example templates either via the [CloudFormation Console](https://console.aws.amazon.com/cloudformation/) or via the [AWS Command Line Interface (CLI)](https://aws.amazon.com/cli/). If using the AWS CLI, you can use the following example command to help you get started.

    aws cloudformation create-stack --stack-name <stack-name> --template-body file://<path-to-template>/<template>

### Creating CloudFormation Stacks with Local Artifacts

Before you can create CloudFormation stacks with templates that reference local artifacts, you will need to upload those artifacts to a S3 bucket. You can do this by using the `aws cloudformation package` command.

    aws cloudformation package --template-file <path-to-template>/<template> --s3-bucket <s3-bucket>

This command returns a copy of your template, replacing references to local artifacts with the S3 location where the command uploaded the artifacts.

Examples of artifacts that CloudFormation templates may reference include;

- Nested CloudFormation templates
- Source code for an AWS Lambda function
- OpenAPI/Swagger documents for an AWS API Gateway REST API

## Linting CloudFormation Templates

When developing CloudFormation templates in this repository, please remember to lint your templates. We use [`cfn-lint`](https://github.com/aws-cloudformation/cfn-python-lint) and [Prettier](https://prettier.io/).

## More Information

To learn more about AWS CloudFormation, head over to their product page at;

- https://aws.amazon.com/cloudformation

For detailed information about how to use AWS CloudFormation, check out their documentation at;

- https://docs.aws.amazon.com/cloudformation
