# AWS Serverless and Event-Driven Architecture

## 1. Architecture Overview

This architecture demonstrates an AWS-based serverless and event-driven application integrating storage, compute, database, messaging, API management, automation, monitoring, and security services.

The application is divided into independent workflows to make each component easier to understand, operate, and maintain.

## 2. Architecture Diagram

The complete architecture diagram is maintained in the Mermaid source below.

## 3. Main Components

| Component | AWS Service | Responsibility |
|---|---|---|
| File Storage | Amazon S3 | Stores uploaded files |
| Event Trigger | S3 Event Notification | Starts processing when a file is uploaded |
| File Processing | AWS Lambda | Reads and processes uploaded files |
| Database | Amazon DynamoDB | Stores processing records |
| Notifications | Amazon SNS | Publishes processing notifications |
| Message Queue | Amazon SQS | Holds asynchronous messages |
| Queue Processor | AWS Lambda | Processes SQS messages |
| REST API | Amazon API Gateway | Exposes GET and POST endpoints |
| API Handler | AWS Lambda | Handles API requests |
| Automation | EventBridge Scheduler | Starts and stops EC2 instances |
| Compute | Amazon EC2 | Provides the instance used for automation exercises |
| Maintenance | AWS Systems Manager | Runs maintenance commands |
| Monitoring | Amazon CloudWatch | Monitors metrics and triggers alarms |
| Secret Storage | AWS Secrets Manager | Stores application secrets |
| Permissions | AWS IAM | Controls access to AWS resources |

## 4. Architecture Design

The application uses separate Lambda functions for S3 file processing, SQS message processing, and REST API handling.

This separation provides clear responsibilities and makes the workflows easier to maintain.

## 5. AWS Region

Asia Pacific (Osaka) — `ap-northeast-3`

## 6. Security Considerations

- Use IAM roles instead of hardcoded AWS credentials.
- Apply least-privilege permissions.
- Keep secrets out of source code.
- Restrict access to AWS resources.
- Review CloudWatch logs and alarms regularly.
