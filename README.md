# cfn-AWS CloudFormation Templates
This repository contains various AWS CloudFormation templates that can be used to create infrastructure resources such as EC2 instances, S3 buckets, and more.

CloudFormation is an infrastructure-as-code service that allows you to define your infrastructure in code and automatically provision and manage resources in AWS.

## Getting Started

To use these templates, you will need an AWS account and an understanding of CloudFormation. You can deploy the templates using the AWS Management Console or the AWS CLI.

## DDoS Simulation Environment

### Description

This AWS CloudFormation template creates a development environment with an EC2 instance for DDoS simulation, which can be used to train a machine learning model for DDoS attack detection.

### Getting Started

To get started with this template, simply deploy it in the AWS Management Console or using the AWS CLI.

### Prerequisites

Before deploying this CloudFormation template, you should have:

- An AWS account
- A key pair for SSH access to the instances

### Deployment

You can deploy this template in the following ways:

- AWS Management Console: Simply upload the ddos-sim.yaml file in the AWS Management Console and follow the prompts to launch the stack.
- AWS CLI: Use the `aws cloudformation create-stack` command to deploy the template.

### Parameters

The template provides the following parameters that you can customize:

- AttackerInstanceType: The instance type for the DDoS attacker (default: t2.micro)
- ProtectedInstanceType: The instance type for the protected server (default: t2.micro)

### Outputs

The template provides the following outputs:

- AttackerInstanceID: The instance ID for the DDoS attacker.
- ProtectedInstanceID: The instance ID for the protected server.
- AttackerPublicIP: The public IP address of the DDoS attacker instance.
- ProtectedPublicIP: The public IP address of the protected server instance.

### Usage

Once you have deployed the template, you can use the DDoS simulation environment to train a machine learning model for DDoS attack detection. The `ddos-sim.yaml` file creates an EC2 instance for the DDoS attacker and an EC2 instance for the protected server. The DDoS attacker instance is configured to simulate a DDoS attack on the protected server using the hping3 tool.

To train your machine learning model, you can monitor the network traffic between the DDoS attacker and the protected server using a network capture tool such as Wireshark. You can then use this network capture data to train your machine learning model to detect DDoS attacks.

## Fedora EC2 Instance

### Description

This AWS CloudFormation template spins up an EC2 instance with Fedora 33 on it and installs Apache HTTP Server on the instance.

### Getting Started

To get started with this template, simply deploy it in the AWS Management Console or using the AWS CLI.

### Prerequisites

Before deploying this CloudFormation template, you should have:

- An AWS account
- A key pair for SSH access to the instance

### Deployment

You can deploy this template in the following ways:

- AWS Management Console: Simply upload the `fedora.yaml` file in the AWS Management Console and follow the prompts to launch the stack.
- AWS CLI: Use the `aws cloudformation create-stack` command to deploy the template.

### Parameters

The template provides the following parameter that you can customize:

- InstanceType: The instance type for the EC2 instance (default: t2.micro)

### Outputs

The template provides the following output:

- EC2InstanceIP: The public IP address of the EC2 instance.

### Usage
To use the Fedora EC2 instance, you can connect to it using SSH and verify that the Apache HTTP Server is running on the instance. You can then customize the instance further according to your requirements.

## Optimum Gentoo EC2 Instance

### Description
This AWS CloudFormation template spins up an EC2 instance with Gentoo Linux and installs the Optimum configuration on it.

### Getting Started
To get started with this template, simply deploy it in the AWS Management Console or using the AWS CLI.

### Prerequisites
Before deploying this CloudFormation template, you should have:

- An AWS account
- A key pair for SSH access to the instance

### Deployment
You can deploy this template in the following ways:

- AWS Management Console: Simply upload the optimum-gentoo.yaml file in the AWS Management Console and follow the prompts to launch the stack.
- AWS CLI: Use the aws cloudformation create-stack command to deploy the template.

### Parameters
The template provides the following parameter that you can customize:

- InstanceType: The instance type for the EC2 instance (default: t2.micro)

### Outputs
The template provides the following output:

- EC2InstanceIP: The public IP address of the EC2 instance.

### Usage
To use the Optimum Gentoo EC2 instance, you can connect to it using SSH and verify that the Optimum configuration is installed on the instance. You can then customize the instance further according to your requirements.
