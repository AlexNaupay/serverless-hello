### New project
```bash
# Create one with 
serverless
# or  
serverless create --path hola-mundo --template-url https://github.com/platzi/serverless-framework/tree/main/hola-mundo

sls deploy
sls deploy function -f <FUNCTION_NAME>
sls invoke -f <FUNCTION_NAME>

# Remove
sls remove
```

### Local Deploy
```bash
npm install serverless-offline --save-dev
# or 
serverless plugin install -n serverless-offline
sls offline start 
sls invoke local -f <FUNCTION_NAME>
```

### Dynamodb local
```bash
https://www.npmjs.com/package/serverless-dynamodb
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.DownloadingAndRunning.html

npm install serverless-dynamodb
serverless dynamodb install  # download dynamodb-local aws

serverless offline start  # autostart
serverless dynamodb start  # only dynamo
aws dynamodb list-tables --endpoint-url http://localhost:8000
```

### Install AWS-Cli before
```bash
aws configure
```

#### Permissions for user in AWS
- https://gist.github.com/ServerlessBot/7618156b8671840a539f405dea2704c8
- AmazonAPIGatewayAdministrator
- AmazonS3FullAccess
- AWSCloudFormationFullAccess
- AWSLambda_FullAccess
- CloudWatchLogsFullAccess
- IAMFullAccess

## Resources
https://www.serverless.com/framework/docs/providers/aws/guide/intro
https://github.com/serverless/tutorial/tree/main/getting-started
https://github.com/dherault/serverless-offline
