# 🌐 Terraform AWS S3 Static Website

This project uses **Terraform** to deploy a static website on **AWS S3**. It creates and configures an S3 bucket, uploads HTML files (`index.html` and `error.html`), and sets the bucket up for website hosting.

## 📁 Project Structure
         .
         ├── main.tf # Main infrastructure configuration
         ├── provider.tf # Provider and Terraform setup
         ├── variables.tf # Input variable definitions
         ├── furni-1.0.0/
         │ ├── index.html # Website home page
         │ └── error.html # Custom error page


## 🚀 Features

- Creates an S3 bucket with a custom name
- Enables public read access for static files
- Uploads `index.html` and `error.html` to the bucket
- Configures the bucket for static website hosting
- Sets ownership and access control policies

## 🔧 Requirements

- [Terraform](https://developer.hashicorp.com/terraform/downloads)
- AWS account
- AWS CLI configured (`aws configure`)
- Basic knowledge of Terraform and AWS

## 🛠️ Usage

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
## Initialize Terraform
      terraform init

## Preview the plan
      terraform plan

## Apply the configuration
      terraform apply

Type yes when prompted.

## Access your website
After deployment, visit the S3 website endpoint printed in the output or format it like:

    http://<your-bucket-name>.s3-website.<region>.amazonaws.com/

🧼 Clean Up
To destroy the resources created by Terraform:

      terraform destroy

📌 Notes
Make sure the HTML files are present in the furni-1.0.0/ folder.

This setup allows public-read access — do not use it for sensitive content.

Tested with Terraform 1.6.x and AWS provider 6.0.0-beta2.


