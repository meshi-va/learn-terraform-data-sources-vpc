# Learn Terraform data sources | VPC repository

I forked this repo in order to complete [this tutorial](https://learn.hashicorp.com/tutorials/terraform/data-sources?in=terraform/certification-associate-tutorials) which is part of the [Terraform Associate Tutorial List](https://learn.hashicorp.com/collections/terraform/certification-associate-tutorials).

---

## Objectives

1. In this tutorial, you will use Terraform to deploy a workspace containing a VPC and security groups on AWS in the `us-east-1` region. 
2. Next, you will use the `aws_availability_zones` data source to configure your VPC's Availability Zones (AZs), allowing you to deploy this configuration in any AWS region.
3. Then, you will use the `terraform_remote_state` data source to deploy another workspace containing your application infrastructure to your VPC. 
4. Finally, you will use the `aws_ami` data source to configure the correct AMI for the current region.



## Resource overview

This repo will configure the following resources that will affect the APP repo:

- 2 private subnets



## Completed tasks

- Forked two repos, one for the VPC configuration, and one for the [APP](https://github.com/meshi-va/learn-terraform-data-sources-app).
- Updated the VPC region using the ` aws_availability_zones` data source
- Changed the `azs` value accordingly
- Added a data source for `aws_region` and added an output block so that my second workspace can reference it
- Applied my configuration with `terraform apply -var aws_region=us-west-1`

---

The rest of the tasks were done on the [APP](https://github.com/meshi-va/learn-terraform-data-sources-app) repo, so feel free to head over and check it out.
