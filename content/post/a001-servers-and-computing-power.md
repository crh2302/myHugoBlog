+++
title = "Foundational & Compute Service"
description = "Servers and Computing Power in the Cloud with AWS"
date = 2019-01-18T12:00:00Z
author = "Cervantes Hernandez"
+++

## Introduction
I'm making this post as part of my journey in the Cloud Track of [Udacity's Bertelsmann Technology Scholarship program](https://www.udacity.com/bertelsmann-tech-scholarships). #TheBlogChallenge

I will use this opportunity to review **Lesson 13: Foundational & Compute Service**. The lesson is about the importance of cloud servers and their security, and also about some [AWS](https://aws.amazon.com) cloud services.

# Table of content
1. [The importance of servers in the cloud](#the-importance-of-servers-in-the-cloud)
2. [Elastic Cloud Compute](#elastic-cloud-compute-ec2)
3. [Elastic Cloud Block](#elastic-block-store-ebs)
4. [The importance of security in the cloud](#the-importance-of-security-in-the-cloud)
5. [Virtual Private Cloud (VPC)](#virtual-private-cloud-vpc)
6. [The importance of Compute power](#the-importance-of-compute-power)
7. [Lambda](#lambda)
8. [Elastic Beanstalk](#elastic-beanstalk)

# The importance of servers in the cloud 
There are several advantages of using servers in the cloud. 

- Not having to invest in the hardware, labor and maintenance of internal data centers can save money and time. 
- Deploying applications in the cloud eases its accessibility from and to the world.
- Solutions can be deployed in a matter of minutes. 
- Cloud services as [AWS](https://aws.amazon.com) charge for what it is used and don't have long-term contracts. 
- Cloud services allow building resilient servers with the capacity to adapt to different scenarios.

## Elastic Cloud Compute (EC2)
[Elastic Cloud Compute or EC2](https://aws.amazon.com/ec2/) is an [AWS](https://aws.amazon.com) service that provides servers for rent in the cloud. These servers are called instances. **Instances** are physical servers in an [Availability Zone (AZ)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-regions-availability-zones) or [Data Center](https://en.wikipedia.org/wiki/Data_center). The word elastic in its name means that it can grow or shrink based on rules, e.g., application load.

There are several pricing options for EC2: On-Demand, Dedicated Host, Spot, Reserved Instances. [Spot instances](https://aws.amazon.com/ec2/spot/) can save you up to 90% off the on-demand pricing. Spot Instances are cheaper because they take advantage of unused EC2 capacity in the AWS cloud.

## Elastic Block Store (EBS)
[Elastic Block Store or EBS](https://aws.amazon.com/ebs/) is an AWS storage solution for EC2 instances. An EC2 instance storage can be increased by attaching an EBS. 

EBS are physical hard drives and there are several volume types fall under the categories of [Hard Disk Drives (HDD)](https://en.wikipedia.org/wiki/Hard_disk_drive) and [Solid State Drives (SSD)](https://en.wikipedia.org/wiki/Solid-state_drive).

Unlike the instance store, the EBS data persists after the EC2 instance is terminated or shut down. Also, the Amazon EBS volume is automatically replicated within its availability zone.

# The importance of security in the cloud 
Cloud services offer security options that allow you to have complete control over your virtual networking environment.
It is possible to configure a virtual network with public or private facing subnets and launching servers in the selected network to secure access.

## Virtual Private Cloud (VPC)
[Amazon VPC](https://aws.amazon.com/vpc/) allows the provision of an isolated section of the AWS cloud where AWS resources can be launch in a configurable virtual network. A VPC spans all the Availability Zones in the region.

IP address ranges, subnets, route tables, and network gateways are configurable within a VPC virtual network environment.The default limit is 5 VPCs per Region. This limit can be increased by request. 

AWS resources are automatically provisioned in a default VPC. Creating and using a VPC, does not have additional charges. Access restriction can be configured for data stored in Amazon S3 so that it's only accessible from instances in your VPC.

# The importance of Compute power
- Serverless 
- Applications can automatically scale
- In response to events running code on demand 
- Pay only when the code runs


## Lambda
[AWS Lambda](https://aws.amazon.com/lambda/) runs code without provisioning or managing servers. You pay only for the consumed compute time. 

More information about lambdas:
- Lambdas have a 15 minutes time limit.
- "Lambda function" is the code that is run on an AWS Lambda
- Other AWS services can trigger Lambda code
- Lambda code can be written via the console.
- AWS Lambda supports Java, Go, PowerShell, Node.js, C#/.NET, Python, and Ruby. 
- There is a Runtime API that allows you to use other programming languages to author your functions.


## Elastic Beanstalk
[Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/) is an orchestration service that allows the deployment of a web application on demand. It achieves this by spinning up or provisioning the services needed to run the application. It can create EC2 instances, elastic load balancers, and setup auto-scaling, spin up databases, VPCs and security groups.

It supports Java, PHP, Python, .NET, Node.js, Ruby, Docker, Apache, HTTP, Tomcat, Engine X, and IIS.