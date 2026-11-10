# AWS Automation, Serverless and Event-Driven Application

A hands-on AWS cloud project demonstrating serverless computing, event-driven architecture, automation, monitoring, and secure resource management using multiple AWS services.

## Project Overview

This project implements an event-driven application on Amazon Web Services (AWS). It uses AWS Lambda to process events, Amazon S3 to store uploaded files, DynamoDB to store processing records, and SNS/SQS to support asynchronous messaging and notifications.

It also demonstrates REST API development, scheduled EC2 automation, Systems Manager operations, CloudWatch monitoring, and Secrets Manager.

The project is designed to demonstrate practical knowledge of AWS services and how they work together in a cloud-based application.

## Architecture

The project contains the following major components:

1. **File processing workflow:** S3, S3 Event Notifications, Lambda, DynamoDB, and SNS.
2. **Asynchronous messaging workflow:** SQS and a dedicated Lambda function.
3. **REST API workflow:** API Gateway, Lambda, and DynamoDB.
4. **Infrastructure automation:** EventBridge schedules for EC2 start and stop operations.
5. **Operations and monitoring:** Systems Manager and CloudWatch.
6. **Secret management:** AWS Secrets Manager.

The architecture diagram and detailed workflow documentation will be added to this repository.

## AWS Services Used

| AWS Service | Purpose |
|---|---|
| Amazon S3 | Stores uploaded files |
| AWS Lambda | Executes serverless processing code |
| Amazon DynamoDB | Stores application and file-processing records |
| Amazon SNS | Sends processing notifications |
| Amazon SQS | Provides asynchronous message queuing |
| Amazon API Gateway | Exposes REST API endpoints |
| Amazon EventBridge Scheduler | Automates scheduled EC2 operations |
| Amazon EC2 | Provides the instance used for automation and maintenance exercises |
| AWS Systems Manager | Runs remote maintenance commands |
| Amazon CloudWatch | Monitors metrics and manages alarms |
| AWS Secrets Manager | Stores application secrets |
| AWS IAM | Manages roles and permissions |

## Main Project Workflows

### 1. S3 File Processing

- Upload a file to an Amazon S3 bucket.
- S3 Event Notification triggers the file-processing Lambda function.
- Lambda reads the uploaded file.
- Processing information is stored in DynamoDB.
- SNS publishes a notification about successful processing.

### 2. SQS Message Processing

- A message is sent to an SQS queue.
- The queue triggers a dedicated Lambda function.
- Lambda reads the message and stores its information in DynamoDB.
- The message is removed from the queue after successful processing.

### 3. REST API Integration

- API Gateway exposes GET and POST methods.
- API Gateway invokes the API Lambda function.
- POST creates a new application record in DynamoDB.
- GET retrieves records from DynamoDB.

### 4. EC2 Automation

- EventBridge Scheduler invokes EC2 start and stop operations.
- Dedicated IAM roles provide the required permissions.
- Scheduled automation reduces the need for manual instance management.

### 5. Systems Manager Maintenance

- Systems Manager manages the EC2 instance.
- Run Command executes maintenance and verification commands.
- The SSM Agent status can be checked through Systems Manager.

### 6. CloudWatch Monitoring

- CloudWatch monitors EC2 metrics.
- A CPU utilization alarm is configured.
- SNS is configured as the alarm notification destination.

### 7. Secrets Management

- AWS Secrets Manager stores application secret values.
- Secret values are managed separately from application source code.

## Technology Stack

- **Cloud Platform:** Amazon Web Services
- **Programming Language:** Python
- **Runtime:** Python 3.12
- **Architecture:** Serverless and Event-Driven
- **Database:** Amazon DynamoDB
- **Messaging:** Amazon SNS and Amazon SQS
- **API:** Amazon API Gateway
- **Automation:** Amazon EventBridge Scheduler
- **Monitoring:** Amazon CloudWatch
- **Security:** AWS IAM and AWS Secrets Manager

## AWS Region

Asia Pacific (Osaka) — `ap-northeast-3`

## Security Practices

- Separate Lambda functions are used for different processing responsibilities.
- IAM permissions are restricted to the project resources and required actions where possible.
- Dedicated IAM roles are used for scheduled EC2 operations.
- Secrets are stored in AWS Secrets Manager rather than committed to source code.
- AWS resources should be reviewed regularly to avoid unnecessary costs.

## Repository Structure

The documentation will be organized into the following sections:

- `architecture/` — Architecture diagram and design explanation.
- `workflows/` — Step-by-step explanation of project workflows.
- `screenshots/` — Evidence of AWS configuration and successful tests.
- `security/` — IAM policies and security practices.
- `deployment/` — Project setup and deployment instructions.
- `troubleshooting/` — Issues encountered and their solutions.

## Learning Outcomes

Through this project, I gained practical experience with:

- Building serverless applications using AWS Lambda.
- Configuring event-driven S3 integrations.
- Working with DynamoDB for application data storage.
- Implementing asynchronous messaging using SQS and SNS.
- Building REST APIs using API Gateway and Lambda.
- Automating EC2 operations with EventBridge Scheduler.
- Performing maintenance operations through Systems Manager.
- Monitoring AWS resources using CloudWatch.
- Managing application secrets with Secrets Manager.
- Applying IAM least-privilege principles.

## Project Status

**Implementation:** Completed  
**Documentation:** In progress

Additional architecture diagrams, configuration explanations, screenshots, and testing evidence will be added as the documentation is completed.

## Author

**Yash Satyavan Jogdand**

GitHub: [yash-jogdand](https://github.com/yash-jogdand)
