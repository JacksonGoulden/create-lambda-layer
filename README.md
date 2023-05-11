# create-lambda-layer
Automates the creation of a lambda layer

The purpose of this CloudFormation template is to create a lambda layer.

It is

aws cloudformation create-stack --stack-name aws-create-lambda-layer --template-body file://custom_lambda_layer.yaml --capabilities CAPABILITY_NAMED_IAM