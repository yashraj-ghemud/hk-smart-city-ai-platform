# hk-smart-city-ai-platform

> Repository contains a single README describing a proposed "HK Smart City AI Platform"—a cross-sector AI system for tourism, retail, F&B, and fintech that claims deep AWS integration (Amazon Bedrock, Amazon Q Developer, Lambda, DynamoDB, S3, SageMaker, etc.). The README outlines architecture, features, deployment commands, and example file paths, but no source code or infrastructure files were provided in the supplied dossier.

## Overview

As described in README.md: provides a multi-modal AI assistant and platform for Hong Kong that aims to deliver a tourist mobile app (React Native), merchant dashboard (web), and admin console (Python/Flask). Features described include itinerary planning, dynamic pricing, inventory prediction, restaurant intelligence, payment orchestration (AlipayHK, Octopus, WeChat Pay), and cross-border transaction optimization. These are claims in the README; no implementation artifacts were supplied to verify functionality.

## Key capabilities

- Real-time itinerary planning and multi-language AI assistant (Cantonese/Mandarin/English) — README claim
- Augmented reality navigation and multi-modal input for mobile app — README claim
- Dynamic pricing analysis and inventory prediction for retail — README claim
- Real-time restaurant intelligence, dietary optimization, and delivery route optimization for F&B — README claim
- Payment orchestration and cross-border transaction optimization integrating AlipayHK, Octopus, WeChat Pay — README claim
- Admin console for system monitoring and ML model management (Python/Flask) — README claim
- Proposed use of 14 AWS services for end-to-end functionality — README claim

## Technology

- Amazon Bedrock
- Amazon Q Developer
- AWS Lambda
- Amazon DynamoDB
- Amazon S3
- Amazon SageMaker
- Amazon Comprehend
- Amazon Translate
- Amazon Kinesis
- Amazon Lex
- AWS IoT Core
- Amazon API Gateway
- Amazon CloudWatch
- AWS IAM
- React Native (mobile)
- Python / Flask (admin console)

## Repository structure

The following top-level files and directories were observed in the repository:

- `README.md`

## Getting started

The inspected repository does not expose a complete, conventional dependency manifest or reproducible startup command. Start by reviewing the top-level files and any existing project notes before extending or rebuilding the project.

## Configuration

README describes a serverless/API-driven architecture: User Interfaces (mobile/web/chatbots) → API Gateway (rate limiting/authentication) → AWS Lambda (business logic) → Amazon Bedrock (AI processing) → DynamoDB (user data) + S3 (analytics) → External integrations (IoT, payments, social). The README also references CloudFormation at infrastructure/cloudformation.yaml and Lambda code under src/backend/lambda_functions, but those files were not present in the provided dossier.

## Development and quality notes

- No dedicated test files were identified in the audited tree.
- No continuous-integration configuration was identified during the audit.

### Current improvement opportunities

- Add actual source code and infrastructure: commit infrastructure/cloudformation.yaml and at minimum a minimal Lambda handler under src/backend/lambda_functions/handler.py to make the README examples reproducible.
- Include an OpenAPI (swagger.yaml) or API spec for API Gateway endpoints to clarify contracts between UI and backend.
- Add a basic README section linking to actual directories and a CONTRIBUTING.md with setup steps for developers.
- Introduce secrets management and example IAM least-privilege policies (e.g., iam/policies/*.json or Terraform/IaC snippets) rather than placeholder ARNs.
- Create skeleton automated tests and CI: add .github/workflows/ci.yaml with lint, unit test, and build steps.

## Contributing

Before submitting changes, keep the implementation aligned with the existing project structure, add or update relevant tests where the project supports them, and describe any configuration changes in the pull request.
