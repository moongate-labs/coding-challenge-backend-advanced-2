# Overview

You're working on an NFT ticketing platform built with Node.js microservices and MongoDB. After a user purchases a ticket, an NFT is minted and airdropped to their wallet. However, the airdrop process is prone to failures due to various blockchain-related issues. Your task is to implement a queue-based job processor system that handles retries for failed airdrops.

## Assumptions

An external scheduler will ping the `/jobs/airdrop/retry` endpoint every minute.

## Objectives

1. API Endpoint:

   - Implement a POST endpoint `/jobs/airdrop/retry` that triggers the retry process.
   - The endpoint should process up to 20 failed airdrops per invocation.

2. Data Schema Design:

   - Design and implement a MongoDB schema for storing airdrop information.

3. Retry Logic:

   - Implement a retry mechanism.
   - Define the maximum number of retry attempts before marking an airdrop as permanently failed.

4. Mock Airdrop Function:

   - Create a mock function that simulates the airdrop process with the following characteristics:
     - 80% success rate
     - Random completion time between 1-70 seconds
     - Throws an error if execution time exceeds 60 seconds

5. Error Handling:

   - Develop comprehensive error handling and logging throughout the application.

6. Testing:
   - Write unit tests using Jest for core components of your system.
   - Include a test case to handle unexpected duplicate triggers of the retry process.

## Requirements

1. Use Node.js (latest LTS version) and Express.js for the API.
2. Use TypeScript (latest stable version) with ES6 features.
3. Use mongodb-memory-server for in-memory MongoDB data storage.
4. Implement proper concurrency control to handle multiple simultaneous requests.
5. Include appropriate error handling and logging.
6. Write unit tests using Jest.
7. Include inline documentation to explain complex logic, key design decisions, and algorithmic approaches, where appropriate.

## Evaluation Criteria

- **Functionality**: The application should meet all outlined objectives.
- **System Design**: Practicality and simplicity in the overall system architecture, with particular attention to code modularization for different components.
- **Code Quality**: Cleanliness, readability, and inline documentation.
- **Modularity and Scalability**: Effective use of modular design patterns to enhance code scalability and maintainability.
- **Testing**: Comprehensive coverage and quality of unit tests.
- **Error Handling**: Robustness in handling various error scenarios.
- **Concurrency Control**: Effectiveness in managing multiple simultaneous requests.

## Submission Guide

Please submit your solution using one of the following methods:

1. CodeSandbox.io (Recommended):

   - Fork the provided repository in CodeSandbox.
   - Complete your implementation in the CodeSandbox environment.
   - Provide the link to your CodeSandbox project.

2. GitHub:

   - Fork the provided repository on GitHub.
   - Complete your implementation and push your changes to your forked repository.
   - Provide the link to your GitHub repository.
