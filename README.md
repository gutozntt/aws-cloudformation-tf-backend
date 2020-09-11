# Set Up your Terraform Backend

Create a CloudFormation Stack with this template to create a DynamoDB Lock Table and a S3 Bucket to store the Terraform State files.

## After run the template

Your terraform backend will look like this:

```
terraform {
  backend "s3" {
    region         = "us-east-1" # region of the bucket
    bucket         = "your-stack-name" # state file bucket name
    key            = "terraform.tfstate" # state file key name
    dynamodb_table = "your-stack-name" # name of dynamodb lock table
  }
}
```
