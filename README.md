# Terraform S3 Bucket

The Terraform S3 Bucket project facilitates the creation and management of Amazon Simple Storage Service (S3) buckets using Terraform. This project simplifies the process of provisioning S3 buckets with customizable configurations, allowing users to leverage Terraform's infrastructure as code approach for managing their cloud storage resources.

## Prerequisites

Before using this project, ensure you have Terraform installed on your system. You can download Terraform from [here](https://www.terraform.io/downloads.html) and follow the installation instructions.

## Usage

Follow these steps to execute the Terraform configuration for creating an S3 bucket:

1. **Clone the Repository**: Clone this repository to your local machine.

2. **Initialize Terraform, Plan, and Apply**: Navigate to the cloned repository directory and execute the following commands:

   ```bash
   terraform init
   terraform plan
   terraform apply

![image](https://github.com/RSauravR/Terraform-S3-Bucket/assets/121216190/837fd9d4-08ec-43a3-b237-bb5a9b1c620a)
![image](https://github.com/RSauravR/Terraform-S3-Bucket/assets/121216190/853b6406-0304-451d-915e-aba7eef50d17)
![image](https://github.com/RSauravR/Terraform-S3-Bucket/assets/121216190/9caa5b84-0e25-492c-ae96-c124ae729e0b)
![image](https://github.com/RSauravR/Terraform-S3-Bucket/assets/121216190/fd2f5c10-d8a4-4e8a-9788-615f9dcc3161)

# Adding User Token for IAM User Access

To grant Terraform access to an IAM user, you can follow these steps to generate and configure an access key and secret key:

1. **Create IAM User**: If you haven't already, create an IAM user in your AWS account through the AWS Management Console.

2. **Generate Access Key**: Once the IAM user is created, navigate to the user's details page and select "Security credentials." Under "Access keys," click "Create access key" to generate a new access key and secret key pair.

3. **Configure AWS Credentials**: After generating the access key and secret key, configure them in your Terraform environment by either:

   - **Setting environment variables**:
     ```bash
     export AWS_ACCESS_KEY_ID="your_access_key"
     export AWS_SECRET_ACCESS_KEY="your_secret_key"
     ```
   
   - **Using AWS CLI**:
     ```bash
     aws configure
     ```
   
   - **Adding credentials directly in your Terraform configuration file** (`~/.aws/credentials`):
     ```plaintext
     [default]
     aws_access_key_id = your_access_key
     aws_secret_access_key = your_secret_key
     ```

   Ensure that the IAM user associated with the access key has the necessary permissions to manage S3 buckets, either by attaching a suitable IAM policy or using IAM roles.
