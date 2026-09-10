# Event Management API Automation

Overview

This project is a Postman API automation framework created to automate and validate REST APIs for an Event Management application.

The framework covers positive and negative API scenarios, reusable assertions, environment-based configuration, dynamic test data, authentication, and response validation.

## Tools & Technologies

* Postman
* JavaScript
* Postman CLI
* Git
* GitHub
* REST APIs
* JSON Schema Validation

## Project Structure

Postman-API-Automation/
│
├── collections/
│   └── Event Management API Automation.postman_collection.json
│
├── environments/
│   ├── Event Management - QA.postman_environment.json
│   ├── Event Management - Dev.postman_environment.json
│   └── Event Management - Stage.postman_environment.json
│
└── README.md


## Authentication

The collection covers authentication APIs including:

* User Registration
* User Login
* Get Authenticated User
* Invalid Login
* Invalid Registration Data
* Missing Authentication Token
* Invalid/Expired Token

The authentication token generated during login is stored as a collection variable and reused by subsequent authenticated requests.

## API Coverage

### Authentication

* Register User
* Login User
* Get Authenticated User

### Events

* Create Event
* Get All Events
* Get Event
* Update Event
* Delete Event
* Verify Deleted Event

### Bookings

* Create/Book Event
* Get All Bookings
* Get Booking by ID
* Get Booking by Reference code
* Cancel booking
* Verify Booking Cancellation

### Negative Testing

some of the Negative scenarios are:

* Invalid login credentials
* Invalid email
* Invalid password
* Register Invalid email
* Register missing email
* Register empty email
* Register missing password
* Missing required fields
* Empty required fields
* Invalid authentication token
* Missing authentication token

## Validations

The framework includes validations for:

* HTTP status codes
* Response time
* Response headers
* Response body
* Data types
* Required fields
* Array validation
* Field values
* Authentication tokens
* Business rules
* JSON schema validation

## Dynamic Test Data

Dynamic values are generated using Postman JavaScript scripts to avoid hardcoding test data.

Example:
* Invalid test data

Variables are passed between requests to support end-to-end API workflows.

## Environments

The collection supports multiple environments:

* QA
* Dev
* Stage

Environment variables such as `base_url` are used to avoid hardcoding API URLs.

## API Workflow

The collection supports an end-to-end workflow such as:


Register
   ↓
Login
   ↓
Get Authenticated User
   ↓
Create Event
   ↓
Get Event
   ↓
Update Event
   ↓
Get Event
   ↓
Delete Event
   ↓
Book Event
   ↓
Get Bookings
   ↓
Delete Event


Variables generated from one request are reused by subsequent requests where required.

## Running the Collection

### Run using Postman

Select the desired environment and run the collection using the Postman Collection Runner.

### Run using Postman CLI

command:

postman collection run "<collection-id>" 
-e "<environment-id>" 
--env-var "base_url=https://api.eventhub.rahulshettyacademy.com/api"

Replace the collection and environment IDs with the appropriate values.

## Reporting

The collection can be executed using Postman CLI and test results can be generated for automation runs.

HTML reporting can also be generated for test execution results.
To run the collection and get the report:
postman collection run "<collection-id>" 
-e "<environment-id>" 
--env-var "base_url=https://api.eventhub.rahulshettyacademy.com/api" -r html --reporter-html-export reports\postman-report.html

## Future Enhancements

Planned improvements include:

* Jenkins CI/CD integration
* Additional negative scenarios
* Expanded schema validations
* Data-driven testing

## Author

**Archana Prasannan**

QA Automation Engineer | API & UI Test Automation

### Skills demonstrated

Postman • JavaScript • REST API Testing • API Automation • JSON Schema • Git • GitHub