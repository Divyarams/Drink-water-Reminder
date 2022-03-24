# Drink-water-Reminder
An automated reminder service without server provisioning.

# Overview
Refer Architecture

Stage 1: Static website hosting in S3 bucket. The user is prompted to enter the Reminder message, Email and phone.
Stage 2: The request is passed to API GW which integrates with Lambda function. Use Lambda Proxy integration and Enable CORS.
Stage 3: Lambda function with required permissions to recieve the event, checks for preferences and starts a state machine.
Lambda returns response code and response headers for proxy integrations.
Stage 4: State Machine Execution starts and based on preference, the reciever gets an email of SMS.

# Review
Add additional functionality by including Wait time with Choice state.

