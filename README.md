# webapps
This project implemented to touch and feel 3-tier webapp communication flow 

Phase 0: lauch ec2 instance "Sandbox"

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


Phase 1: Packer






Phase 2: Terraform





Phase 3: Ansible
