# AWS-Cloudformation-Scripts

This repository contains a collection of AWS CloudFormation templates for automating the deployment and configuration of AWS infrastructure. The templates cover EC2, VPC, AWS Backup, CloudWatch, SNS, and RDS services, providing a comprehensive approach to managing AWS resources using Infrastructure as Code (IaC).

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [CloudFormation Templates](#cloudformation-templates)
  - [EC2](#ec2)
  - [VPC](#vpc)
  - [AWS Backup](#aws-backup)
  - [CloudWatch](#cloudwatch)
  - [SNS](#sns)
  - [RDS](#rds)
- [Requirements](#requirements)
- [Setup and Usage](#setup-and-usage)
- [Best Practices](#best-practices)

## Overview

AWS-Cloudformation-Scripts is designed to simplify the setup and management of AWS services through reusable CloudFormation templates. By leveraging these scripts, you can quickly provision resources, ensure consistency, and automate repetitive tasks, enhancing both productivity and security in AWS environments.

## Features

- **Automated Provisioning**: Easily deploy AWS resources using CloudFormation templates.
- **Scalable**: Templates are designed to be scalable and customizable for various environments.
- **Secure Configurations**: Implements best practices for security, including encryption, IAM roles, and least-privilege access.
- **Cost Optimization**: Efficiently manages resources to help minimize costs.
- **Integrated Monitoring and Alerts**: Includes CloudWatch configurations for monitoring and notifications.

## CloudFormation Templates

### EC2
- **Description**: Deploy EC2 instances with customizable settings.
- **Key Features**:
  - Define instance types, AMIs, and security groups.
  - Configure IAM roles for EC2.
  - User data scripts for initial configuration.
  - Elastic IP and Auto Scaling options.

### VPC
- **Description**: Create a Virtual Private Cloud for secure networking.
- **Key Features**:
  - Configurable subnets (public, private) and route tables.
  - Internet Gateway, NAT Gateway, and VPN connections.
  - Security Groups and Network ACLs for traffic control.
  - VPC Peering and endpoints configuration.

### AWS Backup
- **Description**: Automate backup processes for critical resources.
- **Key Features**:
  - Create backup vaults and plans with retention settings.
  - Resource assignments for EC2, RDS, and EFS.
  - Scheduled backups with automated lifecycle management.

### CloudWatch
- **Description**: Monitor AWS resources and set up alarms.
- **Key Features**:
  - Configure dashboards, metrics, and alarms.
  - Log Groups and retention policies.
  - Automated actions based on alarm states.
  - Integration with SNS for notifications.

### SNS
- **Description**: Manage notifications and messaging for your infrastructure.
- **Key Features**:
  - Create topics and manage subscriptions.
  - Integrate with CloudWatch for alarm notifications.
  - Supports email, SMS, and Lambda triggers.

### RDS
- **Description**: Provision and manage Relational Database Services.
- **Key Features**:
  - Set up DB instances with security and performance settings.
  - Multi-AZ deployments for high availability.
  - Automated backups and snapshots.
  - Read replicas for load balancing and performance.

## Requirements

- AWS Account with proper permissions.
- AWS CLI configured with access credentials.
- Basic understanding of YAML/JSON and CloudFormation.

## Setup and Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/anilsolanki2645/AWS-Cloudformation.git
   cd AWS-Cloudformation

2. **Review Templates**:

- Navigate to the /templates directory.
- Customize template parameters as per your requirements.

3. **Deploy a Template**:

- Use the AWS CLI to deploy the stack.
- Example command:
  ```bash
  aws cloudformation deploy --template-file templates/ec2.yaml --stack-name my-ec2-stack

4. **Updating a Stack**:

- Modify the template and use the following command
  ```bash
  aws cloudformation update-stack --stack-name my-ec2-stack --template-body file://templates/ec2.yaml

5. **Deleting a Stack**:
   
- Use the AWS CLI or Management Console to delete the stack when no longer needed.
  ```bash
  aws cloudformation delete-stack --stack-name my-ec2-stack

## Best Practices

- **Version Control**: Keep track of changes in templates using Git.
- **Parameters and Mappings**: Use parameters to make templates reusable.
- **Stack Policies**: Protect critical resources from unintended updates.
- **Resource Tags**: Use tags for cost allocation, security, and resource management.
- **Validation**: Use `cfn-lint` or AWS CloudFormation Designer to validate templates before deployment.

