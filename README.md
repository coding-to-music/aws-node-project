<!--
title: 'AWS NodeJS Example'
description: 'This template demonstrates how to deploy a NodeJS function running on AWS Lambda using the traditional Serverless Framework.'
layout: Doc
framework: v3
platform: AWS
language: nodeJS
priority: 1
authorLink: 'https://github.com/serverless'
authorName: 'Serverless, inc.'
authorAvatar: 'https://avatars1.githubusercontent.com/u/13742415?s=200&v=4'
-->

https://www.serverless.com/framework/docs/getting-started

Install the serverless CLI via NPM:

```java
npm install -g serverless
```

# Serverless Framework AWS NodeJS Example

This project was created by the command 'serverless create --template aws-nodejs'.

or simply 'serverless' and follow the prompts.

```
serverless

Creating a new serverless project

? What do you want to make? AWS - Node.js - Starter
? What do you want to call this project? aws-node-project

✔ Project successfully created in aws-node-project folder

? Do you want to login/register to Serverless Dashboard? Yes
Logging in the Serverless Dashboard via the browser
If your browser does not open automatically, please open this URL:
https://app.serverless.com?client=cli&transactionId=Fmt7gngolypKdYRQfNs6l

✔ You are now logged in the Serverless Dashboard

? What application do you want to add this to? [create a new app]
? What do you want to name this application? my-new-app

✔ Your project is ready to be deployed to Serverless Dashboard (org: "codingtomusic", app: "my-new-app")

? Do you want to deploy now? Yes

Deploying aws-node-project to stage dev (us-east-1)

✔ Service deployed to stack aws-node-project-dev (107s)

dashboard: https://app.serverless.com/codingtomusic/apps/my-new-app/aws-node-project/dev/us-east-1
functions:
  hello: aws-node-project-dev-hello (225 kB)

What next?
Run these commands in the project directory:

serverless deploy    Deploy changes
serverless info      View deployed endpoints and resources
serverless invoke    Invoke deployed functions
serverless --help    Discover more commands
```

This template demonstrates how to deploy a NodeJS function running on AWS Lambda using the traditional Serverless Framework. The deployed function does not include any event definitions as well as any kind of persistence (database). For more advanced configurations check out the [examples repo](https://github.com/serverless/examples/) which includes integrations with SQS, DynamoDB or examples of functions that are triggered in `cron`-like manner. For details about configuration of specific `events`, please refer to our [documentation](https://www.serverless.com/framework/docs/providers/aws/events/).

## Usage

### Deployment

In order to deploy the example, you need to run the following command:

```
$ serverless deploy
```

After running deploy, you should see output similar to:

```bash
Deploying aws-node-project to stage dev (us-east-1)

✔ Service deployed to stack aws-node-project-dev (112s)

functions:
  hello: aws-node-project-dev-hello (1.5 kB)
```

### Invocation

After successful deployment, you can invoke the deployed function by using the following command:

```bash
serverless invoke --function hello
```

Which should result in response similar to the following:

```json
{
  "statusCode": 200,
  "body": "{\n  \"message\": \"Go Serverless v3.0! Your function executed successfully!\",\n  \"input\": {}\n}"
}
```

### Local development

You can invoke your function locally by using the following command:

```bash
serverless invoke local --function hello
```

Which should result in response similar to the following:

```
{
    "statusCode": 200,
    "body": "{\n  \"message\": \"Go Serverless v3.0! Your function executed successfully!\",\n  \"input\": \"\"\n}"
}
```
