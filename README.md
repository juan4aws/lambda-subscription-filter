# About

Using cloudformation/sam to configure cloudwatch logs subscription filter to lambda function.


# cfn/sam

https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-subscriptionfilter.html

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-permission.html

### cloudformation package and deploy

https://docs.aws.amazon.com/cli/latest/reference/cloudformation/package.html

aws cloudformation package \
--region us-east-1 \
--template-file splunk.yaml \
--output-template-file splunk-output.yaml \
--s3-bucket [your-bucket]


aws cloudformation deploy \
--region us-east-1 \
--template-file splunk-output.yaml \
--stack-name splunk-integration \
--capabilities CAPABILITY_IAM

# via cli

https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/SubscriptionFilters.html#LambdaFunctionExample


# misc
https://docs.aws.amazon.com/cli/latest/reference/logs/describe-log-groups.html