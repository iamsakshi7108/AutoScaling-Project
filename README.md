# Application Load Balancer with Auto Scaling Group Project

##  Project Overview
This project demonstrates how to deploy a highly available and scalable web application on AWS using:
- **Application Load Balancer (ALB)** for distributing traffic.
- **Auto Scaling Group (ASG)** for automatic scaling of EC2 instances.
- **Launch Template** (or Launch Configuration) to define instance settings.
- **Target Group** to register healthy EC2 instances behind the ALB.

##  Architecture Diagram

![](./Pictures/Diagram.png)

## Steps to Deploy
### 1.Create a Launch Template:

- Choose an AMI (Amazon Linux 2 or Ubuntu).

- Select instance type (e.g., t2.micro).

- Add User Data to install web server
 
 ![](./Pictures/LT.png)

### 2.Create Target Group:

- Protocol: HTTP

- Port: 80

- Health check path: /

![](./Pictures/TG.png)

### 3.Create Auto Scaling Group:

![](./Pictures/ASG.png)


### 4.Create Application Load Balancer and add rules with particular path:

![](./Pictures/Rules.png)

### 5.Attach the Target Group:

![](./Pictures/Attach_LB_Home.png)

![](./Pictures/Attach-LB_Laptop.png)

![](./Pictures/Attach_LB_Mobile.png)


### 6.Get the ALB DNS Name:

![](./Pictures/DNS.png)


### 7.Test the Setup:


![](./Pictures/Home_Page.png)

![](./Pictures/Laptop_Page.png)

![](./Pictures/Mobile_Page.png)


## Summary

In this project, we deployed a highly available, fault-tolerant, and scalable web application using AWS services.
The Application Load Balancer evenly distributed incoming traffic, while the Auto Scaling Group ensured that the right number of EC2 instances were always running based on demand.






