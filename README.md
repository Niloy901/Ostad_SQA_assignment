# 🧪 SQA Testing Portfolio

> A hands-on Software Quality Assurance portfolio demonstrating
> practical experience in **Manual Testing**, **API Testing**, and
> **Database Testing** through structured test planning, execution,
> defect reporting, validation, and reliability testing.

## 📌 Portfolio Overview

This repository contains three practical SQA testing projects designed
to demonstrate end-to-end testing skills across UI, API, and database
layers.

  -----------------------------------------------------------------------
  Project           Testing Focus     Tools /           Highlights
                                      Technology        
  ----------------- ----------------- ----------------- -----------------
  Manual Testing    Functional,       Chrome, Brave,    12 test cases
                    exploratory,      Windows 11,       executed, 4
                    usability, input  Android 14        defects
                    validation,                         documented
                    responsive and                      
                    basic                               
                    accessibility                       
                    testing                             

  API Testing       REST API          Postman, JSON,    GET, POST, PUT,
                    validation and AI HTTP              DELETE, negative,
                    chat API test                       schema, auth,
                    design                              quota and
                                                        security tests

  Database Testing  Schema,           SQL, MySQL-style  PK/FK, UNIQUE,
                    constraints,      syntax            cascade delete,
                    CRUD, integrity,                    orphan checks,
                    business queries                    COMMIT and
                    and transactions                    ROLLBACK
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 📂 Repository Structure

``` text
SQA-Testing-Portfolio/
│
├── Manual Testing of ChatGPT.docx
├── Api testing with postman & documentation.docx
├── Database Testing.docx
├── screenshots/
│   ├── manual-testing/
│   ├── api-testing/
│   └── database-testing/
└── README.md
```

> **Tip:** Add your evidence screenshots to the suggested `screenshots`
> folders and link them from the relevant sections below.

------------------------------------------------------------------------

# 🖥️ 1. Manual Testing Project

## Application Under Test

**ChatGPT Web Application**

## Testing Approach

-   Black-box testing
-   Functional testing
-   Input validation testing
-   Usability testing
-   Exploratory testing
-   Responsive testing
-   Basic accessibility checks
-   Cross-browser and cross-device testing
-   Basic performance observation

## Test Environment

  Item         Environment
  ------------ ---------------------------------
  Desktop OS   Windows 11
  Mobile OS    Android 14
  Browsers     Google Chrome, Brave Browser
  Devices      Laptop and smartphone
  Network      Broadband Wi-Fi and mobile data

## Features Tested

-   Login with valid and invalid credentials
-   Logout
-   Password reset
-   Prompt submission and response
-   Empty prompt handling
-   New conversation creation
-   Conversation rename
-   Conversation deletion
-   Special characters and emoji input
-   Long prompt handling
-   Theme switching
-   Stop response generation
-   Regenerate response
-   Copy response
-   Feedback controls
-   Mobile responsiveness
-   Keyboard navigation and focus visibility

## 📊 Manual Testing Dashboard

  Metric                                               Result
  ---------------------- ------------------------------------
  Planned test cases                                       12
  Executed test cases                                      12
  Passed test cases                                        12
  Defects documented                                        4
  Major                                                     1
  Minor                                                     2
  Trivial                                                   1
  Final recommendation     GO with improvement recommendation

## 🐞 Key Defects and Observations

  -----------------------------------------------------------------------
  Bug ID            Issue             Severity          Priority
  ----------------- ----------------- ----------------- -----------------
  BUG-01            Rapid Send        Minor             Medium
                    interaction may                     
                    produce                             
                    inconsistent                        
                    submission                          
                    behavior                            

  BUG-02            No visible        Major             High
                    warning when                        
                    approaching a                       
                    very large                          
                    prompt/input                        
                    limit                               

  BUG-03            Conversation      Minor             Low
                    rename edit can                     
                    close without                       
                    confirmation                        
                    after tapping                       
                    outside                             

  BUG-04            Stop Generating   Trivial           Low
                    control may                         
                    briefly remain                      
                    visible after                       
                    generation                          
                    completes                           
  -----------------------------------------------------------------------

## Exploratory Testing

A 60-minute exploratory testing charter focused on:

-   Prompt input behavior
-   Conversation history
-   Response controls
-   Rapid user actions
-   Double-click behavior
-   Fast navigation
-   Interrupted actions
-   UI state consistency

### Release Recommendation

**GO**, with a recommendation to improve the prompt-length feedback
experience and review the documented interaction inconsistencies.

------------------------------------------------------------------------

# 🔌 2. API Testing Project

## Tool and Target

**Tool:** Postman\
**Public Practice API:** JSONPlaceholder

## REST Operations Tested

  -----------------------------------------------------------------------
  Method                  Endpoint                Validation
  ----------------------- ----------------------- -----------------------
  GET                     `/users`                Status code, JSON
                                                  array, record count and
                                                  required fields

  GET                     `/users/1`              Single resource and
                                                  nested object structure

  GET                     `/users/9999`           Non-existent resource
                                                  handling

  POST                    `/posts`                Creation status, echoed
                                                  fields and generated ID

  PUT                     `/posts/1`              Update behavior

  DELETE                  `/posts/1`              Delete behavior

  GET                     `/users`                Basic response-time
                                                  observation
  -----------------------------------------------------------------------

## API Validation Areas

-   HTTP status codes
-   Response body structure
-   JSON data types
-   Required fields
-   Positive scenarios
-   Negative scenarios
-   Resource creation
-   Resource update
-   Resource deletion
-   Non-existent resource behavior
-   Basic response-time observation

## 🤖 AI Chat API Test Design

A separate API test design was prepared for an AI chat-completion
endpoint.

### Positive Testing

Validates that a correct authenticated request returns:

-   Successful HTTP status
-   Response ID
-   Model information
-   Non-empty choices array
-   Non-empty assistant content
-   Usage/token information

### Authentication Testing

Designed scenarios include:

-   Missing API key
-   Malformed API key
-   Revoked API key

### Validation and Negative Testing

Designed scenarios include:

-   Empty messages array
-   Missing model field
-   Invalid role value
-   Invalid token-limit value

### Schema Validation

Successful responses should validate:

-   `id`
-   `model`
-   `choices`
-   `choices[0].message.content`
-   `usage.total_tokens`

### Rate Limit and Security Awareness

The test design also covers:

-   Quota exhaustion behavior
-   `429 Too Many Requests`
-   Retry guidance where supported
-   API key exposure checks
-   HTTPS enforcement
-   Sensitive internal error leakage
-   Stack-trace and database-error exposure checks

------------------------------------------------------------------------

# 🗄️ 3. Database Testing Project

## Database Under Test

`ai_saas_db`

The database represents an AI SaaS platform containing data related to:

-   Users
-   Subscriptions
-   Chat sessions
-   Messages
-   API keys
-   Usage logs

## Database Testing Coverage

### Schema and Structural Validation

-   List database tables
-   Inspect table columns
-   Verify primary keys
-   Verify foreign keys
-   Validate unique email constraint
-   Validate restricted plan values

### CRUD and Constraint Testing

-   Insert valid user
-   Attempt duplicate email insertion
-   Attempt invalid plan insertion
-   Update user plan
-   Delete related records
-   Verify referential integrity
-   Verify cascade behavior

### Data Integrity and Business Rules

SQL queries were designed and executed to validate:

-   Users without subscriptions
-   Total tokens used per user
-   Total cost per user
-   Highest-activity chat session
-   Revoked API keys and their owners
-   Orphaned messages

## 🔄 Transaction Reliability Testing

### COMMIT Scenario

A multi-step subscription upgrade flow was tested by:

1.  Starting a transaction
2.  Updating the user's plan
3.  Creating the corresponding subscription record
4.  Committing the transaction
5.  Verifying the final state

### ROLLBACK Scenario

Rollback reliability was tested by:

1.  Recording the original state
2.  Starting a transaction
3.  Updating plan information
4.  Inserting a subscription record
5.  Rolling back the transaction
6.  Verifying that the original state remained unchanged

### Why This Matters

Subscription and billing changes often require multiple related database
writes. Transaction testing verifies **atomicity** so the system does
not leave inconsistent states such as:

-   Enterprise plan without a valid subscription record
-   Subscription billing record without the matching user plan
-   Partial updates after connection or application failure

------------------------------------------------------------------------

# 🎯 Skills Demonstrated

  -----------------------------------------------------------------------
  Category                            Skills
  ----------------------------------- -----------------------------------
  Test Design                         Test scenarios, test cases,
                                      expected vs actual results,
                                      priority

  Manual QA                           Functional, negative, boundary,
                                      usability and exploratory testing

  Defect Management                   Reproduction steps, severity,
                                      priority, justification and
                                      evidence planning

  API QA                              REST methods, HTTP status
                                      validation, JSON validation,
                                      negative testing

  API Security Awareness              Authentication, credential
                                      exposure, HTTPS and error leakage
                                      checks

  Database QA                         Schema, CRUD, constraints, PK/FK
                                      and referential integrity

  SQL                                 JOIN, LEFT JOIN, GROUP BY,
                                      aggregate functions, subqueries and
                                      filtering

  Reliability                         COMMIT, ROLLBACK and atomic
                                      transaction verification

  Cross-Platform QA                   Desktop, mobile, browser and
                                      responsive checks
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# 🛠️ Tools & Technologies

![Postman](https://img.shields.io/badge/Postman-API_Testing-orange?logo=postman)
![SQL](https://img.shields.io/badge/SQL-Database_Testing-blue)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue?logo=mysql)
![Chrome](https://img.shields.io/badge/Chrome-Cross_Browser_Testing-green?logo=googlechrome)
![Git](https://img.shields.io/badge/Git-Version_Control-orange?logo=git)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?logo=github)

------------------------------------------------------------------------

# 📸 Test Evidence

For better portfolio presentation, evidence can be organized like this:

``` text
screenshots/
├── manual-testing/
│   ├── test-case-execution/
│   └── defect-evidence/
├── api-testing/
│   ├── get-request/
│   ├── post-request/
│   ├── put-request/
│   └── delete-request/
└── database-testing/
    ├── schema-validation/
    ├── constraint-testing/
    ├── crud-testing/
    └── transaction-testing/
```

Example Markdown for adding evidence later:

``` md
![GET Users Test](screenshots/api-testing/get-request/get-users.png)
```

------------------------------------------------------------------------

# 🚀 What This Portfolio Demonstrates

This repository demonstrates the ability to:

-   Understand a product from an end-user and QA perspective
-   Prepare structured test plans and test cases
-   Execute functional and exploratory testing
-   Document reproducible defects
-   Validate REST API behavior with Postman
-   Design authentication, negative, schema and security-aware API tests
-   Validate relational database structure and constraints
-   Write SQL for integrity and business-rule verification
-   Test transaction reliability with COMMIT and ROLLBACK
-   Present QA work in a structured and reviewable format

------------------------------------------------------------------------

# 👤 Author

## Masuduzzaman Niloy

**Software Quality Assurance (SQA) Enthusiast**

Interested in Manual Testing, API Testing, Database Testing, Test
Automation, and building reliable software through systematic quality
assurance practices.

------------------------------------------------------------------------

⭐ If you find this testing portfolio useful, feel free to explore the
reports and test documentation in this repository.
