# ProTasker Analytics Service

## Overview

The ProTasker Analytics Service is a serverless backend microservice responsible for generating project-level insights and task performance metrics.

It aggregates task and project data to provide user-specific analytics, secured using Amazon Cognito JWT authorization.

This service is designed to operate fully serverless within the AWS Always Free Tier.

---

## Architecture

- AWS Lambda (Analytics processing logic)
- Amazon API Gateway (REST endpoints)
- Amazon DynamoDB (Project and task data queries)
- Amazon Cognito (Authentication and JWT validation)
- IAM roles with least privilege access

---

## Responsibilities

- Generate project performance metrics
- Provide task completion statistics
- Aggregate user-specific insights
- Support dashboard analytics retrieval
- Enforce user-scoped access control

---

## Security

- Cognito User Pool integration
- JWT authorization via API Gateway
- User identity extraction from token claims
- IAM-based least privilege permissions

---

## Deployment Model

This microservice is deployed independently and communicates via secured API Gateway endpoints.

All requests must include a valid Cognito access token in the Authorization header.

---

## Tech Stack

- Node.js
- AWS Lambda
- DynamoDB
- API Gateway
- Amazon Cognito

---

## Status

Initial analytics service architecture and scaffolding phase.
