# serverless-crud-http-api
This CRUD HTTP API is built using Terraform, DynamoDB, Lambda, and Python on AWS. It enables users to create, read, update, and delete items stored in a DynamoDB table through HTTP requests. Terraform is used to provision infrastructure resources, such as the API Gateway, DynamoDB table, and Lambda functions.

<div id="image" align="center">
    <img src="./architecture/serverless-crud-http-api.png" width="600px"/>
</div>

# Requirements

* [Terraform CLI](https://developer.hashicorp.com/terraform/downloads)
* [AWS CLI v2](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) with AWS Account Configured
* [Python 3.10](https://www.python.org/downloads/)

# Scripts

* ### create.sh

`chmod +x ./create.sh`

### Usage:

`./create.sh create read update delete`

This script automates the process of creating a CRUD serverless API on AWS using Lambda functions, Terraform and Python. To use the script, follow the steps below:

    - Ensure that you have the necessary dependencies installed including Terraform and AWS CLI.

    - Clone the repository and navigate to the root directory.

    - Execute the script with the following arguments: create, read, update and delete.

    - When prompted, enter the region you want to deploy the infrastructure in.

    - Wait for the script to complete the following actions:
        Compress the Lambda functions
        Create an S3 bucket
        Copy the compressed functions to the S3 bucket
        Create the infrastructure using Terraform.

The serverless API is now up and running, and can be tested using the endpoints generated by the script.
    
* ### crud-tests.sh

`chmod +x ./crud-tests.sh`

### Usage:

`./create.sh arg1 arg2`

This script is used to interact with a CRUD HTTP API built with DynamoDB and Lambda on AWS.

    - Clone the repository to your local machine.
    
    - Navigate to the root directory
    
    - Set the correct file permissions for the Bash script (e.g., chmod +x crud-script.sh).
    
    - Run the script with the following command: ./crud-script.sh [ARG1] [ARG2]
        ARG1 can be one of the following CRUD operations: create, read, readone, update, or delete.
        ARG2 should be the API endpoint you want to connect to.
        
    - Follow the prompts for each operation.
    
* ### delete.sh

`chmod +x ./delete.sh`

### Usage:

`./delete.sh`

This Bash script is designed to delete an AWS S3 bucket and its associated infrastructure using the AWS CLI and Terraform.
