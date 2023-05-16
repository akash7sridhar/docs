# Run Digger on GitLab Pipelines

### How to configure Digger to run on GitLab Pipelines

Lambda function needs to be configured first

### Configuring and Deploying Lambda: Step-by-Step Guide

1. Fork and clone the repository related to the Lambda function.
2. If necessary, update the `serverless.yml` file in the cloned repository. This file contains configuration settings for the Lambda function and can be customized to suit your requirements.
3. Save the `GITHUB_TOKEN` to the SSM (Systems Manager) parameter store. You can choose any path for storing the token, but ensure that the `serverless.yml` file is updated accordingly if you deviate from the default path. For example, save the `GITHUB_TOKEN` to `ssm:/gitlab-dev-webhook-handler/dev/GITLAB_TOKEN`.
4. Make sure that your AWS credentials are properly configured in the command-line interface (CLI). This ensures that you have the necessary permissions to deploy the Lambda function.
5. Run the command `npm run build` in the root directory of the cloned repository. This command will build the necessary artifacts for the Lambda function.
6. Finally, run the command `npm run deploy` in the same root directory. This will initiate the deployment process for the Lambda function using the configuration specified in the `serverless.yml` file.