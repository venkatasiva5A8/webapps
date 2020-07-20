# webapps
This project implemented to touch and feel 3-tier webapp communication flow 

# Phase 0: lauch ec2 instance "Sandbox"

$vi /etc/yum.repos.d/ansible.repo

[Ansible]

name = ansible

baseurl = https://releases.ansible.com/ansible/rpm/release/epel-7-x86_64/

enabled = 1

gpgcheck = 0

$vi setup.sh

yum update -y && yum upgrade -y

yum install git -y && yum install wget -y && yum install unzip -y && yum install curl -y && yum install epel-release

wget https://releases.hashicorp.com/packer/1.5.5/packer_1.5.5_linux_amd64.zip && unzip packer_1.5.5_linux_amd64.zip && mv packer /bin/ && rm -rf ./packer*

wget https://releases.hashicorp.com/terraform/0.12.24/terraform_0.12.24_linux_amd64.zip && unzip terraform_0.12.24_linux_amd64.zip && mv terraform /bin/ && rm -rf ./terraform* 

yum install ansible -y


# Phase 1: Packer
step 1: clone repo

$git clone https://github.com/krishnamaram2/Image_Builder.git

step 2: enter src directory

$cd Image_Builder/src

step 3: enter access key and secret key

vi variables.json

{

"aws_access_key": "",

"aws_secret_key": "",

"region": "us-east-1"

}

Step 4: validate syntax

packer validate -var-file=variables.json builders.json

Step 5: Build custome AMI

packer build -var-file=variables.json builders.json






Phase 2: Terraform





Phase 3: Ansible
