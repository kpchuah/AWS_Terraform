## Launch an AWS instance with Terraform

I used the following user data script to launch my main Linux instance, with Terraform installed.
> #! /bin/bash   
> sudo yum update -y  
> sudo yum install -y unzip  
> wget https://releases.hashicorp.com/terraform/0.12.29/terraform_0.12.29_linux_amd64.zip  
> unzip terraform_0.12.29_linux_amd64.zip  
> sudo mv terraform /usr/local/bin/  
> terraform --version  
> sudo yum install python3-pip -y
> pip3 install awscli --user
> pip3 install ansible --user
> # house all ansibe tf templates in one folder 
> mkdir deploy_iac_tf_ansible
> cd deploy_iac_tf_ansible
> wget https://raw.githubusercontent.com/linuxacademy/content-deploying-to-aws-ansible-terraform/master/aws_la_cloudplayground_version/ansible.cfg
