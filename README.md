# Terraform Lambda Deployment Project

## 🚀 Project Overview

This project demonstrates **Infrastructure as Code (IaC)** using Terraform to provision:
- An AWS **Lambda function**
- An **API Gateway** to access the Lambda
- An **S3 bucket** for storage
- **IAM roles and policies** to manage secure permissions

Everything is deployed in **AWS** using Terraform.

---

## 🎯 Objectives

- Understand key components of **cloud computing**
- Create and manage AWS Lambda functions using Terraform
- Connect Lambda with API Gateway to handle HTTP requests
- Configure an S3 bucket and IAM roles for storage and access control
- Manage resource dependencies in Terraform

---

## 📦 Project Structure

### 📝 Task 1: Create AWS Lambda Function with Terraform
- Define `aws_lambda_function` resource.
- Set up basic IAM roles and permissions using:
  - `aws_iam_role`
  - `aws_iam_policy_attachment`

**Hands-on Activity:**  
Create a Lambda using Terraform.

---

### 🌐 Task 2: Create API Gateway for Lambda
- Define resources:
  - `aws_api_gateway_rest_api`
  - `aws_api_gateway_resource`
  - `aws_api_gateway_method`
- Connect GET/POST methods to Lambda using `aws_api_gateway_integration`.

**Hands-on Activity:**  
Configure API Gateway endpoints to trigger Lambda functions.

---

### ☁️ Task 3: Create S3 Backend and IAM Roles
- Define the S3 bucket using `aws_s3_bucket`.
- Use IAM resources:
  - `aws_iam_policy`
  - `aws_iam_role_policy_attachment`

**Hands-on Activity:**  
- Set S3 bucket as a backend for Lambda.
- Grant Lambda permissions to read/write from S3.

---

### 🔗 Task 4: Manage Dependencies with Terraform
- Use `depends_on` to explicitly define the creation order of resources.

---

## ⚙️ Provider Setup

```hcl
provider "aws" {
  region = "us-east-1"
}
