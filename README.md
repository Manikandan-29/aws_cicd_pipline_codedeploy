# Auto Deploy Static App using AWS CICD Pipeline Code Deployment to AWS EC2 Instance


<b>User Data for Dependencies installations for AMAZON Linux 2:-</b>

#!/bin/bash<br />
sudo yum -y update<br />
sudo yum -y install ruby<br />
sudo yum -y install wget<br />
cd /home/ec2-user<br />
wget https://aws-codedeploy-ap-south-1.s3.ap-south-1.amazonaws.com/latest/install<br />
sudo chmod +x ./install<br />
sudo ./install auto<br />
sudo yum install -y python-pip<br />
sudo pip install awscli<br />
sudo systemctl restart codedeploy-agent






# you can create 2 roles for this project 
1. AWScodedeployrole.  ( this is for code-deploy)
2. AmazonEC2RoleforAWSCodeDeploy && AmazonEC2RoleforAWSCodeDeployLimited ( this 2 roles for auto-deploy your application to your server )

   ![4 drawio](https://github.com/Manikandan-29/aws_cicd_pipline_codedeploy/assets/114275756/187cbfa6-d4b6-4854-b931-5c18e049d140)

