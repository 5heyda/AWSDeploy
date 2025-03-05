# AWSDeploy 🚀

This is a simple Terraform project to deploy a single EC2 instance in AWS ☁️

## Prerequisites 📋

- Terraform installed (brew install terraform) 🛠️
- AWS CLI installed [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) 🔧
- SSH key pair created in AWS (aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem) 🔑

## How to deploy 🏗️

```bash
terraform init
terraform plan -out=tfplan.json
terraform apply tfplan.json --auto-approve
```

Go on AWS console and check the EC2 instance. 🖥️
An instance with the name AWSDeploy-ec2-only should be running :white_check_mark:

## How to destroy 💣

```bash
terraform destroy
```