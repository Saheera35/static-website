# static-website
AWS DevOps project for automating the deployment of a static website

This project demonstrates how to automate the deployment of a static website using AWS DevOps tools.

## Project Overview

The project uses AWS CodePipeline for orchestrating the CI/CD pipeline, AWS CodeBuild for building the static website artifacts, and Amazon S3 for hosting the deployed website.

### Prerequisites

Before you begin, ensure you have:

- An AWS account with appropriate permissions to create CodePipeline, CodeBuild, S3 buckets, and IAM roles.
- AWS CLI installed and configured on your local machine.
- A GitHub repository containing your static website content.

### Setup Instructions

1. **Deploy the CloudFormation Stack:**
   - Upload `template.yml` to AWS CloudFormation.
   - Fill in GitHub repository details in the CloudFormation parameters.

2. **Configure AWS CodePipeline:**
   - Navigate to AWS CodePipeline console.
   - Connect to your GitHub repository and select the appropriate branch.
   - Configure CodeBuild as the build provider.

3. **Access Your Deployed Website:**
   - Once the pipeline is set up and runs successfully, your static website will be deployed to the specified S3 bucket.
   - Access your website using the S3 bucket URL.

### Additional Notes

- Customize `buildspec.yml` for specific build requirements (e.g., npm packages, build commands).
- Monitor pipeline executions and troubleshoot any issues in AWS CodePipeline console.
