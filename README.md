# Cloud Microsegmentation Demo Simulation

Welcome to the Microsegmentation Demo Simulation App! This project is designed to highlight the power of Illumio's Cloudsecure by demonstrating its ability to secure and microsegment a vulnerable application environment effectively.

## Overview

The primary goal of this project is to demonstrate how Illumio Cloudsecure can be leveraged to implement microsegmentation within a complex cloud environment.

Microsegmentation is a critical aspect of modern network security, and Illumio provides robust solutions for Microsegmentation. This demo simulation serves as a realistic, intentionally vulnerable application that users can use alongside Illumio Cloudsecure to witness firsthand how microsegmentation enhances security.

To run this CFT template - 

1. Go to Cloudformation on your AWS console. 
2. Upload the template that best fits your region
3. CFT template will usually take 5-10 mins to deploy

The AWS CloudFormation template included in this project creates various AWS resources, including:

- **Virtual Private Cloud(VPC)**
- **Subnets**
- **Internet Gateway**
- **NAT Gateway**
- **EC2 Instances**
- **RDS Instances**
- **S3 Bucket**
- **VPC peering between ACME1 and ACME2**
- **Lambda**
- **Dynamo DB**
- **API Gateways**
- **VPC Endpoint**


Additionally, it will automatically create flow logs from the VPC's to the S3 bucket. 

In our scenario, we have defined 3 subnets (prod, dev and staging) spread across 2 different VPC's. Within each subnet, we have created 3-tier applications using EC2 instances. This will be created using the provided Cloudformation template along with the flows. 

<img width="1062" alt="image" src="https://github.com/adityakrishnan142/CloudSecure-Demo-Template/assets/56053567/b14d59c7-49b9-4b4e-8a3d-f3eab6556e95">


**Note**: Please go through the demo script and video provided to you to get a detailed overview of demo'ing cloudsecure and its capabilities. 

## Cleaning Up

To tear down the demo simulation app, follow these steps:

1. Log into the AWS CloudFormation Console and find the stack you created for the demo app
2. Delete the stack
3. Delete the S3 bucket created by the cloudformation template
4. Delete the DynamoDB created by the Cloudformation template
