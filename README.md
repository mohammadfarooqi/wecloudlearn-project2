# Infrastructure Provisioning Automation - Terraform and Ansible

This project demonstrates how to provision AWS cloud infrastructure using Terraform and Ansible. The infrastructure includes a VPC, internet gateway, public subnet, private subnet, Internet Gateway, NAT Gateway, public route table, and EC2 instances (DB and API Server).

## Prerequisites

Before running the scripts, ensure you have the following prerequisites in place:

- **AWS Account**: You need an AWS account with appropriate permissions to create VPC resources and EC2 instances.

- **Terraform**: Make sure you have Terraform installed on your local machine.

- **Ansible**: Install the Ansible on API Server.

## Project Structure

The project consists of the following folders:

- **`ansible`**: Ansible code to configure DB Server and API Server.

- **`terraform`**: Terraform code to provision infrastructure.

- **`README.md`**: This documentation file.
