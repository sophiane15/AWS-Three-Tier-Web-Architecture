# AWS-Three-Tier-Web-Architecture

### Project Introduction:
In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.


<img width="1017" alt="Screenshot 2024-01-26 at 14 52 47" src="https://github.com/sophiane15/AWS-Three-Tier-Web-Architecture/assets/153296722/d3ecd5d3-4bf1-488a-b962-23b35e8e10be">


### Project Overview:

## 1-  Setup: 
For this workshop, we will be downloading the code from Github and upload it to S3 so our instances can access it. We will also create an AWS Identity and Access Management EC2 role so we can use AWS Systems Manager Session Manager to connect to our instances securely and without needing to create SSH key pairs.
      Learning Objectives:
                              -	S3 Bucket Creation
                              -	IAM EC2 Instance Role Creation
	                            - Download Code from Github Repository

## 2- Networking and Security: 
In this section we will be building out the VPC networking components as well as security groups that will add a layer of protection around our EC2 instances, Aurora databases, and Elastic Load Balancers.
      Learning Objectives: Create an isolated network with the following components:
                              -	VPC
                              -	Subnets
                              -	Route Tables
                              -	Internet Gateway
                              -	NAT gateway
                              - Security Groups


## 3- Database Deployment: 
This section of the workshop will walk you through deploying the database layer of the three tier architecture.
      Learning Objectives:
	                            - Deploy Database Layer 
		                          - Subnet Groups
                              - Multi-AZ Database
                              
## 4- App Tier Instance Deployment: 
In this section of our workshop we will create an EC2 instance for our app layer and make all necessary software configurations so that the app can run. The app layer consists of a Node.js application that will run on port 4000. We will also configure our database with some data and tables.
       Learning Objectives:
	                            - Create App Tier Instance
                              -	Configure Software Stack
                              -	Configure Database Schema
                              -	Test DB connectivity

## 5- Internal Load Balancing and Auto Scaling: 
In this section of the workshop we will create an Amazon Machine Image (AMI) of the app tier instance we just created, and use that to set up autoscaling with a load balancer in order to make this tier highly available.
       Learning Objectives:
                              -	Create an AMI of our App Tier
                              -	Create a Launch Template
                              -	Configure Autoscaling
                              -	Deploy Internal Load Balancer


## 6- Web Tier Instance Deployment: 
In this section we will deploy an EC2 instance for the web tier and make all necessary software configurations for the NGINX web server and React.js website.
        Learning Objectives:
                              - Update NGINX Configuration Files
                              - Create Web Tier Instance
                              - Configure Software Stack









 
