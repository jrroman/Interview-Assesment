# DevOps Assessment

## Summary

This assessment will gauge the candidates technical aptitude for DevOps and basic programming and scripting related tasks.

In this assessment we will be interacting with log data from AWS load balancer logs their format and documentation for these logs can be found here:
[AWS Access Logs](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-access-logs.html)

We will also be using Terraform to provision some infrastructure within AWS. The associated documentation can be found here:
[Terraform AWS Docs](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)

### Assessment Requirements

In this assessment we will be using Terraform to create a new AWS Elastic Container Registry repository to store a docker image, a VPC with public and private subnets. Within the public subnets there should be an AWS Application Load Balancer, within the private subnets should be an AWS Elastic Container Service task running the docker image that we have stored in the newly created AWS ECR repo. Once this infrastructure is created we should be able to see "Status Ok" when making a request to the load balancer endpoint URL.

1. Write a Terraform script to provision a private ECR repository to store our docker image

2. Write a bash script which will build and push the docker image to the newly created ECR repository

1. Write a Terraform script to provision the following AWS services:
    - VPC with two public and two private subnets
    - AWS Application Load Balancer which lives only in the public subnets. Please enable load balancer logging
    - AWS Elastic Container Service based on our ECR docker image that lives only in the private subnets
    - This Terraform script should output the VPC id, all four subnet ids, and the load balancer URL

### Bonus Points
- Write a python script which queries the AWS API and gets load balancer logs
    - These logs should be parsed for status codes and the script should return a dictionary of all the status codes found and how many times they were seen
