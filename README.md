# Infrastructure Provisioning Automation - Terraform and Ansible

This project demonstrates how to provision AWS cloud infrastructure using Terraform and Ansible. The infrastructure includes a VPC, internet gateway, public subnet, private subnet, Internet Gateway, NAT Gateway, public route table, and EC2 instances (DB and API Server).

## Prerequisites

Before running the scripts, ensure you have the following prerequisites in place:

- **AWS Account**: You need an AWS account with appropriate permissions to create VPC resources and EC2 instances.

- **Terraform**: Make sure you have Terraform installed on your local machine.

- **Ansible**: Install Ansible on the API Server.

## Project Structure

The project consists of the following folders:

- **`ansible`**: Ansible code to configure the DB Server and API Server.

- **`terraform`**: Terraform code to provision infrastructure.

- **`README.md`**: This documentation file.

## Usage Instructions

### Provisioning Infrastructure

To provision the infrastructure using Terraform and configure it with Ansible, follow these steps:

1. Navigate to the `terraform` directory.

2. Run the following Terraform commands to create the infrastructure:

   ```bash
   terraform init
   terraform plan
   terraform apply
   ```

   Terraform will prompt you to confirm the resource creation. Type `yes` to proceed.

3. Once Terraform has created the infrastructure, navigate to the `ansible` directory.

4. Use Ansible to configure the DB Server and API Server. You may need to update the Ansible inventory file with the appropriate IP addresses of the instances and update the variables under `group_vars/all`.

   ```bash
   ansible-playbook -i inventory.ini db_server.yml
   ansible-playbook -i inventory.ini api_server.yml
   ```

### Shutting Down and Cleaning Up

To shut down and clean up the infrastructure:

1. Navigate to the `terraform` directory.

2. Run the following Terraform command to destroy the resources:

   ```bash
   terraform destroy
   ```

   Terraform will prompt you to confirm the resource deletion. Type `yes` to proceed.

3. This will remove all the created resources, including the VPC, EC2 instances, and associated components.

4. Ensure that you have properly terminated and cleaned up any other resources that were not managed by Terraform or Ansible.

By following these instructions, you can easily provision and configure the infrastructure using Terraform and Ansible, as well as shut down and clean up the resources when they are no longer needed.
