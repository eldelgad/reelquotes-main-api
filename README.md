# ReelQuotes Main API

This directory contains the source code for the ReelQuotes Main Backend API, built with [NestJS](https://nestjs.com/) and deployed to AWS ECS Fargate via a CI/CD pipeline.

## Description
The Main API provides core backend functionality for the ReelQuotes platform. It is written in TypeScript using the NestJS framework and is designed for scalable, production-grade deployments.

## Project Setup
```bash
npm install
```

## Build and Run
```bash
# Development
npm run start

# Watch mode
npm run start:dev

# Production build
npm run build
npm run start:prod
```

## Testing
```bash
# Unit tests
npm run test

# End-to-end tests
npm run test:e2e

# Test coverage
npm run test:cov
```

## Deployment
This service is deployed to AWS ECS Fargate using a multi-stage Dockerfile and a GitHub Actions workflow. On every push to the `develop` branch, the CI/CD pipeline:
- Builds and tags a Docker image
- Pushes the image to Amazon ECR
- Updates the ECS service to use the new image
- Verifies the service is healthy via the Application Load Balancer

## Health Check
The API exposes a `/health` endpoint for load balancer health checks.

## License
This project is licensed for use by the ReelQuotes team.
# Trigger workflow reload
