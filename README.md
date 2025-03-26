sls deploy --stage dev --region us-east-1
sls remove

Chaos Testing of Lambda Using AWS FIS
=====================================
AWS offers the Fault Injection Service (AWS FIS) to execute chaos testing across various AWS services including 
EC2 and ECS. Recently, AWS has extended FIS support to its first serverless service, Lambda. The FIS experiments 
allow you to improve the performance of your application by creating disruptive events. This project is an example 
on how to enable FIS in a lambda application.

## Sample Application
This sample application features an [Amazon API Gateway](https://aws.amazon.com/api-gateway/) as the entry point to 
a REST API. The REST API includes a `/hello` endpoint integrated with an [AWS Lambda](https://aws.amazon.com/lambda/). 
The application is managed by the [Serverless framework]((https://www.serverless.com/).

## Prerequisites
Before exploring the sample applications, please make sure your computer is properly set up with the required tools.

- Node.js and NPM
- yarn
- Serverless

## Deploy Sample Application

### Build Application
After retrieving the sample application from the GitHub repository, ensure its successful build by executing the 
following command:

```
yarn install
```

### Deploy Application
Execute the following command to deploy the sample application:

```
sls deploy --stage dev --region us-east-1
```