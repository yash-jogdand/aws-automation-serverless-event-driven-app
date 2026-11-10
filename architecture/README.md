# Architecture Documentation

This directory contains the architecture documentation for the AWS Automation, Serverless and Event-Driven Application.

## Main Architecture Document

**[AWS Architecture Diagram and Design](aws-architecture.md)**

The main document describes the project's AWS services, application components, data flows, event-driven workflows, automation, monitoring, and security boundaries.

## Architecture Topics

- S3-triggered file processing using Lambda, DynamoDB, and SNS
- Asynchronous message processing using SQS and Lambda
- REST API integration using API Gateway, Lambda, and DynamoDB
- Scheduled EC2 start and stop operations using EventBridge Scheduler
- EC2 management through Systems Manager
- CPU monitoring and alert integration using CloudWatch and SNS
- Secrets Manager storage, with Lambda integration documented as future work

## Region

`ap-northeast-3` — Asia Pacific (Osaka)

## Documentation Status

The architecture document describes the intended service relationships. Refer to each workflow document for its implementation and validation status.
