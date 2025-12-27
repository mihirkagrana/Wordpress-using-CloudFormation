# Wordpress-using-CloudFormation
CloudFormation script to launch highly-available and scalable WordPress deployment. It demonstrates using the AWS CloudFormation bootstrap scripts to deploy WordPress. This template creates an Amazon EC2 instance, an Application Load Balancer and a Multi-AZ Amazon RDS database instance.

WordPress_Multi_AZ_AL2023.template is a working template which can be used to deploy WordPress on Amazon Linux 2023 AMI. This installs latest PHP 8 and Apache 2.4.

WordPress_Multi_AZ_AL2.template was created to work with older Amazon Linux 2 (AL2) AMI. But it does not work as AL2 comes with old PHP 5 and its difficult to replace with PHP 8 using CFT template.
