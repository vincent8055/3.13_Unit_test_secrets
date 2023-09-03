# 3.13_Unit_test_secrets - Assignment submission


### Instructions:

1. Create a new Node.js application using the Express framework.
2. Set up automatic testing for the application using a testing framework such as Jest or Mocha.
3. Create new branch on your existing repository.
4. Set up a CI/CD pipeline using a tool such as Github Action, Jenkins, Travis CI, or CircleCI.
5. Configure the pipeline to automatically build and test the code whenever changes are pushed to the code repository.
6. Deploy the application to a serverless platform such as AWS Lambda or Google Cloud Functions.
7. Store some information using Secret Management on AWS, then get the information as part of the pipeline.
8. Configure the pipeline to automatically deploy the code to the serverless platform whenever changes are pushed to the code repository and all tests pass.
9. Write a documentation explaining the steps you have done, including the tools and services used.

#### Deliverables:

- The Node.js application with automatic testing set up
- Code repository with the CI/CD pipeline configured
- Documentation explaining the steps taken to set up the pipeline.

## Assignment 3.11 submission

This repo runs a CI/CD pipeline in GitHub Action to deploy a Lambda function in AWS.  It also echo's out the variable stored in AWS Secrets Manager parameter store.  The output of the node.js application also contains the secret message.

#### Steps taken:
1. Create a repo and configure the AWS credentials in GitHub secrets and variables store
2. git clone the repo into local
3. create a github workflow yml file "secrets.yml" to define the workflow which includes:
- Pre-deploy - echoing a message on the automated job displaying the user 
- installing the dependencies required to perform the deployment
- perform an automated unit-testing to check for errors
- performing a vulnerability scan
- displaying the secrets from AWS Secrets Parameter Store
- deploying the Lambda function into AWS
![Screenshot 2023-09-03 at 3 35 35 PM](https://github.com/vincent8055/3.13_Unit_test_secrets/assets/127754761/f297d06e-578d-4ec3-bb06-01d7c357f8ee)
![Screenshot 2023-09-03 at 3 36 20 PM](https://github.com/vincent8055/3.13_Unit_test_secrets/assets/127754761/8c2d9852-b16d-444d-939f-ddbc27c1306c)





4. Install node dependencies such as node, serverless, serveless-offline, jest
5. Add in a index.test.js to test the application
6. Add in a function to extract the secret in AWS Secrets Manager parameter store
7. Include a function to display the secret in the Lambda function when invoked.
![Screenshot 2023-09-03 at 3 37 13 PM](https://github.com/vincent8055/3.13_Unit_test_secrets/assets/127754761/1bd2778d-3b5b-4aa4-bf8d-546f34a6abca)

![Screenshot 2023-09-03 at 3 39 50 PM](https://github.com/vincent8055/3.13_Unit_test_secrets/assets/127754761/7631d289-fdeb-4a31-8a01-5ac5652e763d)


