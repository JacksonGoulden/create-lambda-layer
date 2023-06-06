# create-lambda-layer
Automates the creation of a lambda layer using pip3 through a cloudformation template.

The purpose of this CloudFormation template is to create a lambda layer.

# Usage

There are 2 parameters to set when deploying the template. These do not need to be changed in the template itself, but are to be changed when deploying the stack. The parameters are:
- PythonPackage: The name of the pip3 python package to be included in the lambda layer. This must be changed, as by default it will install the openai package.
- InstanceName: The name of the EC2 instance to create. This can be left as the default value.


## Deploying the stack

### To deploy this stack through the AWS Console

1. Log into the AWS Console
2. Navigate to CloudFormation
3. Click on Create Stack
4. Select Upload a template file
5. Click on Choose file and select the custom_lambda_layer.yaml file
6. Click on Next
7. Enter a stack name
8. Enter the PythonPackage parameter
9. (Optional) Enter a name for the EC2 instance
10. Click on Next
11. Click on Next
12. Click on Create stack

### To deploy this stack through the AWS CLI
```
aws cloudformation create-stack --stack-name aws-create-lambda-layer --template-body file://custom_lambda_layer.yaml --capabilities CAPABILITY_NAMED_IAM
```