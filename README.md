# Terraform Learning Repository

This repository contains various Terraform code snippets and projects to help me learn and understand Terraform, a popular infrastructure as code tool. Created by (Tolu).

## Prerequisites

Before you start, make sure you have the following installed:

- [Terraform](https://www.terraform.io/downloads.html)
- [AZURE CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) (if you're using AZURE as your infrastructure provider)

## Steps

1. Clone the repository.

2. Change into the repository directory:

3. Initialize Terraform:

4. Create a Terraform plan:

5. Apply the Terraform plan:

6. Destroy Terraform-managed resources:


## Projects

1. `example-01`: A Terraform project to create a vitual network, subnet, security group and virtual machine .
2. `example-02`: A Terraform project that creates a vm and automatically install 

## Explanaition of the differnt scripts and files which i have 

- `data.tpl` -firt script which i tried using to install docker 
- `data2.pl` - the actuall script that executes and runs the docker on the vm 
- `toly.tf` - this is my docker file 



# personal notes taken 

what is terraform:
- this is a tool that is used  for automating task for the cloud  this is also called infrastructure as code (IAC)  using code to automate the use of cloud infrastructure and utilities.
- Terraform is a tool for building, changing, and versioning infrastructure safely and efficiently.

## what i have created / done on this project 
- i have created a resource group
- i have created a virtual network 
- i have created a subnet 
- i have created a security group 
- i have created a security rule 
- i also had to associate the security group to a subnet 
- create the public ip adress 
- create the nic  for my vm 
- creating a vm 
- creating a key pair for us to be able to login to the vm  to run scripts for installation 
- template file that install all the dependencies 
- using file base 64 to push my installation 
- terraform data sources 


## bash script i ised with my template file for me to be able to install docker 
```bash
#!/bin/bash 
sudo apt-get install -y \ 
    apt-transport-https \ 
    ca-certificates \ 
    curl \ 
    software-properties-common 
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - 
sudo apt-key fingerprint 0EBFCD88 
sudo add-apt-repository \ 
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \ 
   $(lsb_release -cs) \ 
   stable" 
sudo apt-get update 
sudo apt-get install -y docker-ce 
sudo docker run hello-world 
# Linux post-install 
sudo groupadd docker 
sudo usermod -aG docker $USER 
sudo systemctl enable docker

```
## Conclusion

This repository is meant to be a hands-on learning experience for Terraform. As you go through each project, try to understand what each Terraform configuration file does and why it's necessary.

