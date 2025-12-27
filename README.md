# Wordpress-using-CloudFormation
CloudFormation script to launch highly-available and scalable WordPress deployment. It demonstrates using the AWS CloudFormation bootstrap scripts to deploy WordPress. This template creates an Amazon EC2 instance, an Application Load Balancer and a Multi-AZ Amazon RDS database instance.

WordPress_Multi_AZ_AL2.template was created to work with older Amazon Linux 2 (AL2) AMI. But it does not work as AL2 comes with old PHP 5 and its difficult to replace with PHP 8 using CFT template.

WordPress_Multi_AZ_AL2023.template is a working template which can be used to deploy WordPress on Amazon Linux 2023 AMI. This installs latest PHP 8 and Apache 2.4.

Following these simple steps to deploy WordPress site using WordPress_Multi_AZ_AL2023.template.

1) Login to your AWS account, go to CloudFormation and create a new stack by uploading WordPress_Multi_AZ_AL2023.template.
   
2) Select the options for your stack.
<img width="1920" height="1983" alt="CFT-Stack" src="https://github.com/user-attachments/assets/46015049-aa16-4251-b530-ea8763235f08" />

3) Wait for the stack to be created. You will find load balancer URL in the Outputs tab. Open that URL to start WordPress installation.
   <img width="912" height="832" alt="WP-Setup" src="https://github.com/user-attachments/assets/19e15d25-8265-41ef-9c70-a97a2cb635de" />

4) Once the WordPress is installed, you can login to WordPress admin panel.
   <img width="1906" height="870" alt="WP-Admin" src="https://github.com/user-attachments/assets/e700566d-c872-4d23-ad49-c8f399eef8f9" />

5) You can verify the Apache and PHP versions by logging into server using SSH.
   <img width="1121" height="478" alt="Terminal-with-versions" src="https://github.com/user-attachments/assets/35b450fc-4ae4-48ad-b395-9ddb44e6cd98" />

If you are interested in details of making of this CloudFormation template, please read my <a href="https://medium.com/@mihirkagrana/hosting-wordpress-on-aws-using-cloudformation-template-2572eadd268b" target="_blank">blog</a>.
