# serverless-crud-http-api
This CRUD HTTP API is built using Terraform, DynamoDB, Lambda, and Python on AWS. It enables users to create, read, update, and delete items stored in a DynamoDB table through HTTP requests. Terraform is used to provision infrastructure resources, such as the API Gateway, DynamoDB table, and Lambda functions.

# Scripts

### create.sh

`chmod +x ./create.sh`

This script automates the process of creating a CRUD serverless API on AWS using Lambda functions, Terraform and Python. To use the script, follow the steps below:

    - Ensure that you have the necessary dependencies installed including Terraform and AWS CLI.

    - Clone the repository and navigate to the root directory.

    - Modify the BUCKETNAME variable in the script to a unique name for your S3 bucket.

    - Execute the script with the following arguments: create, read, update and delete.

    - When prompted, enter the region you want to deploy the infrastructure in.

    - Wait for the script to complete the following actions:
        Compress the Lambda functions
        Create an S3 bucket
        Copy the compressed functions to the S3 bucket
        Create the infrastructure using Terraform.

    The serverless API is now up and running, and can be tested using the endpoints generated by the script.

Note: The script assumes that you have created the Lambda functions with the appropriate naming conventions and file structure. If not, modify the script to match your file structure.
