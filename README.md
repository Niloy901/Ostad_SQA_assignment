# 🧪 Software Quality Assurance (SQA) Testing Portfolio

A practical Software Quality Assurance portfolio demonstrating hands-on
experience in **Manual Testing**, **API Testing**, and **Database
Testing**. This repository contains structured test plans, test cases,
exploratory testing, defect reports, REST API validation, SQL-based
database validation, integrity testing, and transaction reliability
testing.

## 📌 Project Overview

  ----------------------------------------------------------------------------------------------------------------------------
  Project           Testing Focus     Tools /           Documentation
                                      Technologies      
  ----------------- ----------------- ----------------- ----------------------------------------------------------------------
  Manual Testing    Functional,       Chrome, Brave,    [View Manual Testing Report](./Manual%20Testing%20of%20ChatGPT.docx)
                    exploratory,      Windows 11,       
                    usability,        Android 14        
                    validation,                         
                    responsive and                      
                    accessibility                       
                    checks                              

  API Testing       REST API testing  Postman, JSON,    [View API Testing
                    and AI chat API   HTTP              Report](./Api%20testing%20with%20postman%20%26%20documentation.docx)
                    test design                         

  Database Testing  Schema, CRUD,     SQL, MySQL-style  [View Database Testing Report](./Database%20Testing.docx)
                    constraints,      syntax            
                    integrity, SQL                      
                    queries and                         
                    transactions                        
  ----------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 🖥️ 1. Manual Testing of ChatGPT

**Application Under Test:** ChatGPT\
**Testing Type:** Black-box testing and end-user testing

### Scope Covered

-   Authentication testing
-   Login, logout and password-reset flows
-   Core prompt and response functionality
-   Conversation creation, rename and deletion
-   Empty and long-input validation
-   Special characters and emoji handling
-   Theme switching
-   Stop generating, regenerate, copy and feedback controls
-   Exploratory testing
-   Responsive and mobile checks
-   Basic accessibility checks
-   Cross-browser testing
-   Basic performance observation

### Test Environment

  Item         Environment
  ------------ ---------------------------------
  Desktop OS   Windows 11
  Mobile OS    Android 14
  Browsers     Google Chrome and Brave Browser
  Devices      Laptop and smartphone
  Network      Broadband Wi-Fi and mobile data

### 📊 Execution Summary

  Metric                                              Result
  --------------------- ------------------------------------
  Test cases executed                                     12
  Passed                                                  12
  Defects documented                                       4
  Major                                                    1
  Minor                                                    2
  Trivial                                                  1
  Recommendation          GO with improvement recommendation

### 🐞 Defect Summary

  -----------------------------------------------------------------------
  Bug ID            Finding           Severity          Priority
  ----------------- ----------------- ----------------- -----------------
  BUG-01            Rapid Send        Minor             Medium
                    interaction may                     
                    cause                               
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
                    rename edit may                     
                    close without                       
                    confirmation                        
                    after tapping                       
                    outside                             

  BUG-04            Stop Generating   Trivial           Low
                    control may                         
                    briefly remain                      
                    visible after                       
                    completion                          
  -----------------------------------------------------------------------

### Exploratory Testing Focus

A 60-minute exploratory testing session focused on:

-   Prompt input behavior
-   Conversation history
-   Response controls
-   Double-click behavior
-   Rapid navigation
-   Interrupted actions
-   UI state consistency

📄 **Full documentation:** [Manual Testing of
ChatGPT](./Manual%20Testing%20of%20ChatGPT.docx)

------------------------------------------------------------------------

## 🔌 2. API Testing with Postman

**Tool:** Postman\
**Target API:** JSONPlaceholder public REST API

### REST Endpoints Tested

  Method   Endpoint        Main Validation
  -------- --------------- ----------------------------------------------------
  GET      `/users`        HTTP status, JSON array and required fields
  GET      `/users/1`      Single-resource response and nested structure
  GET      `/users/9999`   Non-existent resource handling
  POST     `/posts`        Creation status, submitted fields and generated ID
  PUT      `/posts/1`      Update behavior
  DELETE   `/posts/1`      Delete behavior
  GET      `/users`        Basic response-time observation

### Validation Areas

-   HTTP status-code validation
-   JSON response validation
-   Required-field validation
-   Positive testing
-   Negative testing
-   Resource creation
-   Resource update
-   Resource deletion
-   Non-existent resource behavior
-   Basic performance observation

### 🤖 AI Chat API Test Design

The project also contains test design for an AI chat-completion API.

#### Authentication Tests

-   Missing API key
-   Malformed API key
-   Revoked API key

#### Validation and Negative Tests

-   Empty `messages` array
-   Missing `model` field
-   Invalid role value
-   Invalid `max_tokens` value

#### Response Schema Checks

Successful responses are designed to validate:

-   `id`
-   `model`
-   `choices`
-   `choices[0].message.content`
-   `usage.total_tokens`

#### Rate Limit and Security Checks

-   Quota-exhaustion behavior
-   `429 Too Many Requests`
-   API-key exposure checks
-   HTTPS enforcement
-   Sensitive error leakage
-   Stack-trace exposure
-   Internal database-error exposure

📄 **Full documentation:** [API Testing with Postman &
Documentation](./Api%20testing%20with%20postman%20%26%20documentation.docx)

------------------------------------------------------------------------

## 🗄️ 3. Database Testing

**Database Under Test:** `ai_saas_db`

The database represents an AI SaaS platform with data related to users,
subscriptions, chat sessions, messages, API keys and usage logs.

### Schema and Structural Validation

-   Table listing
-   Column inspection
-   Primary-key verification
-   Foreign-key verification
-   Unique email constraint validation
-   Restricted plan-value validation

### CRUD and Constraint Testing

-   Insert a valid user
-   Attempt duplicate email insertion
-   Attempt invalid plan insertion
-   Update a user's plan
-   Delete test data
-   Verify cascade behavior
-   Verify referential integrity

### Data Integrity and Business-Rule Queries

SQL queries cover:

-   Users without subscriptions
-   Total token usage per user
-   Total cost per user
-   Chat session with the highest message count
-   Revoked API keys with owner information
-   Orphaned message detection

### 🔄 Transaction Reliability Testing

#### COMMIT Scenario

The test verifies that a user-plan upgrade and related subscription
insertion are successfully committed as one logical operation.

#### ROLLBACK Scenario

The test performs related changes inside a transaction, rolls them back,
and verifies that the original database state remains unchanged.

#### Why Transaction Testing Matters

Subscription upgrades can require multiple related writes. Transaction
testing helps verify atomicity and prevents inconsistent states such as:

-   Enterprise plan without a matching subscription record
-   Subscription record without the matching user plan
-   Partial updates after an application or connection failure

📄 **Full documentation:** [Database Testing
Report](./Database%20Testing.docx)

------------------------------------------------------------------------

## 🎯 Skills Demonstrated

  -----------------------------------------------------------------------
  Category                            Skills
  ----------------------------------- -----------------------------------
  Test Planning                       Scope, approach, environment,
                                      risks, entry and exit criteria

  Test Design                         Scenarios, test cases, expected
                                      results, actual results and
                                      priority

  Manual QA                           Functional, negative, boundary,
                                      usability and exploratory testing

  Defect Reporting                    Reproduction steps, expected vs
                                      actual behavior, severity and
                                      priority

  API QA                              REST methods, HTTP status
                                      validation, JSON and negative
                                      testing

  API Security Awareness              Authentication, credential
                                      exposure, HTTPS and error leakage

  Database QA                         Schema, CRUD, constraints, PK/FK
                                      and referential integrity

  SQL                                 JOIN, LEFT JOIN, GROUP BY,
                                      aggregate functions, subqueries and
                                      filtering

  Reliability Testing                 COMMIT, ROLLBACK and transaction
                                      atomicity

  Cross-Platform QA                   Desktop, mobile, browser and
                                      responsive testing
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🛠️ Tools & Technologies

![Postman](https://img.shields.io/badge/Postman-API_Testing-orange?logo=postman)
![SQL](https://img.shields.io/badge/SQL-Database_Testing-blue)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue?logo=mysql)
![Chrome](https://img.shields.io/badge/Chrome-Cross_Browser_Testing-green?logo=googlechrome)
![Git](https://img.shields.io/badge/Git-Version_Control-orange?logo=git)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?logo=github)

------------------------------------------------------------------------

## 📂 Repository Structure

``` text
.
├── README.md
├── Manual Testing of ChatGPT.docx
├── Api testing with postman & documentation.docx
└── Database Testing.docx
```

The documentation links in this README match the report filenames shown
above. Keep the same filenames after uploading the files to the
repository root so the links work correctly.

------------------------------------------------------------------------

## 🚀 Portfolio Highlights

This repository demonstrates the ability to:

-   Create structured test plans and test cases
-   Execute functional and exploratory tests
-   Document reproducible defects
-   Validate REST APIs using Postman
-   Design authentication, validation, schema and security-aware API
    tests
-   Validate relational database schemas and constraints
-   Write SQL queries for integrity and business-rule verification
-   Test referential integrity and cascade behavior
-   Verify transaction reliability using COMMIT and ROLLBACK
-   Present QA work in a clear and reviewable GitHub portfolio

------------------------------------------------------------------------

## 👤 Author

### Masuduzzaman Niloy

**Software Quality Assurance (SQA) Enthusiast**

Interested in Manual Testing, API Testing, Database Testing, Test
Automation, and building reliable software through systematic quality
assurance practices.
