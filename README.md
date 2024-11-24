# AWS_Playbook
AWS Cloud Ops Playbook
# Introduction

The **AWS Cloud Operations Playbook** is a step-by-step guide aimed at helping professionals effectively manage AWS cloud resources. Whether you're deploying new instances, configuring networks, or setting up monitoring solutions, this playbook provides detailed instructions to perform a wide array of tasks essential for cloud operations.

# Connecting to EC2 Instances

## How to Connect to the Mom & Pop Cafe Test EC2 Instance

Learn how to establish a secure connection to a test EC2 instance representing a typical small business setup. This section covers:

- Retrieving the instance's public DNS and key pair.
- Using SSH to connect securely.
- Verifying the connection and instance status.

## Using the AWS CLI to Describe Instances

Utilize the AWS CLI to list and describe your EC2 instances. Topics include:

- Setting up AWS CLI credentials.
- Running `aws ec2 describe-instances`.
- Filtering results to find specific instances.

## Launching an EC2 Instance with Amazon Linux 2, t1.micro

Step-by-step guide to launching a basic EC2 instance suitable for testing and development:

- Selecting the Amazon Linux 2 AMI.
- Choosing the `t1.micro` instance type.
- Configuring security groups and key pairs.

# AWS CLI Operations

## Connecting to Your AWS Account via AWS CLI

Set up and configure the AWS CLI to interact with your AWS account:

- Installing the AWS CLI tool.
- Configuring access keys and default regions.
- Testing the setup with basic commands.

## Modifying Lab Policies Using AWS CLI

Learn how to adjust IAM policies directly from the command line:

- Listing existing policies.
- Editing policy documents.
- Applying updates to policies.

## Adding Parameters to Parameter Store

Use AWS Systems Manager Parameter Store to manage configuration data:

- Storing parameters securely.
- Accessing parameters in applications.
- Updating and versioning parameters.

# Web Server Management

## Fixing a Misconfigured Web Server

Troubleshoot and resolve common web server configuration issues:

- Identifying configuration errors.
- Adjusting server settings.
- Restarting services to apply changes.

## Changing the AMI Instance in the `create-lamp-instance.sh` Script

Modify a shell script to use a different Amazon Machine Image (AMI):

- Finding the desired AMI ID.
- Updating the script with the new AMI.
- Running the script to launch the instance.

# Scaling and Load Balancing

## Creating an Auto Scaling Group via AWS UI

Set up an Auto Scaling Group to manage EC2 instance scaling:

- Defining launch configurations.
- Setting scaling policies and thresholds.
- Monitoring group performance.

## Creating a Route 53 Health Check

Ensure your web applications are highly available:

- Configuring health checks for endpoints.
- Integrating health checks with Route 53 DNS.
- Setting up failover routing policies.

# Networking and Security

## Enabling VPC Flow Logs via CLI

Capture detailed information about the IP traffic going to and from network interfaces:

- Enabling flow logs for a VPC.
- Specifying log destination (CloudWatch or S3).
- Analyzing flow log data.

## Troubleshooting Network Connectivity on an Instance

Diagnose and fix network issues affecting your instances:

- Checking security group and NACL configurations.
- Verifying routing tables.
- Testing connectivity with `ping` and `traceroute`.

## Setting Up a VPC

Create a Virtual Private Cloud to isolate your resources:

- Defining IP address ranges.
- Creating subnets and availability zones.
- Configuring internet gateways and route tables.

## Adding a Bastion Host to a Public Subnet

Securely access instances in private subnets:

- Launching a bastion host in the public subnet.
- Configuring SSH agent forwarding.
- Establishing connections to private instances.

# Storage and Data Management

## Taking a Snapshot of an EBS Volume

Backup your Elastic Block Store volumes:

- Creating point-in-time snapshots.
- Restoring volumes from snapshots.
- Automating snapshot management.

## Synchronizing Files Using AWS CLI (`aws s3api` and `aws s3`)

Manage files between local systems and S3 buckets:

- Using `aws s3` commands for high-level operations.
- Utilizing `aws s3api` for detailed control.
- Setting up synchronization scripts.

## Creating an S3 Bucket via CLI

Set up object storage for your applications:

- Running commands to create a new bucket.
- Configuring bucket policies and permissions.
- Enabling versioning and encryption.

## Adding an Event Notification to an S3 Bucket

Trigger actions in response to bucket events:

- Defining event types (e.g., object created, deleted).
- Setting up notifications to SNS, SQS, or Lambda.
- Testing the event notifications.

# Monitoring and Logging

## Installing the CloudWatch Agent

Collect system-level metrics and logs:

- Downloading and installing the agent.
- Configuring metrics and logs to collect.
- Verifying data in the CloudWatch console.

## Creating CloudWatch Events and EventBridge Notification Rules

Automate responses to system events:

- Setting up rules to match events.
- Targeting actions like Lambda functions or SNS topics.
- Monitoring rule invocations.

## Creating a CloudWatch Alarm Using Metrics-Based Filters

Set up alarms to monitor resource utilization:

- Defining metric filters.
- Configuring alarm thresholds and notifications.
- Responding to alarm states.

## Using AWS Config to Monitor Resources

Track resource configurations and compliance:

- Enabling AWS Config service.
- Setting up rules and remediation actions.
- Viewing configuration history and compliance reports.

# Automation and Management Tools

## Using the Prebuilt Stopinator Script

Automate instance management tasks:

- Understanding the purpose of the Stopinator script.
- Executing the script to stop instances based on tags.
- Scheduling the script for regular execution.

## Detecting Drift in a CloudFormation Template

Ensure your infrastructure remains consistent:

- Running drift detection on CloudFormation stacks.
- Interpreting drift results.
- Correcting drift to match the template.

## Creating a Batch File to Update the Café Website Colors

Automate website updates:

- Writing a batch script to modify website assets.
- Executing the script to apply changes.
- Verifying updates on the live site.

# Data Analysis

## Creating an Amazon Athena Table

Query data stored in S3 using SQL:

- Setting up the data catalog.
- Defining table schema and partitions.
- Running queries and analyzing results.

## Manually Reviewing Access Logs for Anomalous User Activity

Enhance security through log analysis:

- Locating and downloading access logs.
- Identifying unusual patterns or entries.
- Taking action based on findings.

# AWS Lambda and Layers

## Creating a Lambda Layer and Adding It to a Function

Reuse code across multiple Lambda functions:

- Packaging libraries and dependencies into a layer.
- Publishing the layer to AWS Lambda.
- Associating the layer with your functions.

## Creating a Lambda Function from a Prebuilt Package

Deploy serverless applications efficiently:

- Preparing the deployment package.
- Uploading the package to Lambda.
- Configuring function settings and triggers.

# Identity and Access Management

## Setting Up IAM for Role Assumption

Manage permissions securely:

- Creating IAM roles and policies.
- Allowing users to assume roles.
- Testing role access with AWS CLI.

## Adding Inbound Rules to Security Groups and Network ACLs

Control network traffic to your resources:

- Defining rules for specific ports and protocols.
- Understanding the precedence of security groups and NACLs.
- Auditing rules for security compliance.

# Encryption and Security

## Encrypting the Root Volume of an Existing EC2 Instance

Protect data at rest:

- Creating an encrypted snapshot of the root volume.
- Launching a new instance with the encrypted volume.
- Verifying encryption status.

# Messaging and Notifications

## Creating an SNS Topic

Set up messaging for distributed systems:

- Creating a new SNS topic.
- Configuring access policies.
- Publishing messages to the topic.

## Subscribing to an SNS Topic

Receive notifications and messages:

- Adding email, SMS, or HTTP subscriptions.
- Confirming subscriptions.
- Testing message delivery.

# Conclusion

This playbook serves as a practical resource for performing a wide range of AWS operations. By following these guides, you can enhance your cloud management skills, improve system reliability, and ensure best practices are upheld across your AWS environments.

**Note**: Always ensure you have the necessary permissions and that you are operating in the correct AWS environment to prevent unintended changes or security issues.

# Author

*Your Name*

Cloud Engineer | AWS Certified Solutions Architect

[LinkedIn](#) | [GitHub](#) | [Portfolio](#)
