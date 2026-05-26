# Assessment Submission - Task 1 & Task 2

## Overview

This repository contains solutions for:

-   Task 1 - Manual QA Testing and Bug Reporting
-   Task 2 - n8n Workflow Automation

------------------------------------------------------------------------

# Task 1 - QA Testing

## Application Tested

SauceDemo testing website was used for exploratory manual testing.

Testing included:

-   Login functionality
-   Validation testing
-   Checkout flow
-   Cart behavior
-   Sidebar navigation
-   UI and UX observations

------------------------------------------------------------------------

## Bugs Identified

### 1. Password visibility toggle missing

Observation:

Password input field does not provide show/hide password functionality.

Impact:

Lower usability and user convenience.

Severity:

Low

------------------------------------------------------------------------

### 2. Login error message clipping issue

Observation:

When invalid credentials are entered, login error text overlaps and
becomes partially unreadable.

Impact:

Poor user experience and readability.

Severity:

Medium

------------------------------------------------------------------------

### 3. "All Items" navigation gives no visible feedback

Observation:

When user clicks "All Items" from sidebar while already on product page,
there is no visible feedback.

Impact:

Can create impression that click action failed.

Severity:

Low

------------------------------------------------------------------------

### 4. Checkout possible with empty cart

Observation:

System allows proceeding toward checkout without products.

Impact:

Business validation issue.

Severity:

Medium

------------------------------------------------------------------------

### 5. Zip code validation issue

Observation:

Checkout accepts invalid zip code values such as alphabet input.

Example:

"a"

Impact:

Invalid checkout information accepted.

Severity:

Medium

------------------------------------------------------------------------

## QA Deliverables

Files included:

-   Excel bug report
-   Word QA report
-   Root cause analysis

------------------------------------------------------------------------

# Task 2 - n8n Workflow Automation

## Objective

Build workflow automation using public APIs, transformation, conditional
routing, output integration and error handling.

------------------------------------------------------------------------

## Workflow Design

Schedule Trigger

↓

HTTP Request 1

↓

Code Node

↓

HTTP Request 2

↓

IF Node

↓

Edit Fields

↓

Google Sheets

------------------------------------------------------------------------

## APIs Used

### API 1

JSONPlaceholder Posts API

Purpose:

Fetch public post information.

API:

https://jsonplaceholder.typicode.com/posts

------------------------------------------------------------------------

### API 2

JSONPlaceholder Users API

Purpose:

Enrich original records using user information.

API:

https://jsonplaceholder.typicode.com/users/{userId}

------------------------------------------------------------------------

## Data Transformation

Code node performed:

-   Filter top 5 records
-   Keep only required fields
-   Reduce unnecessary payload

Selected fields:

-   id
-   title
-   userId

------------------------------------------------------------------------

## Data Enrichment

Second API request fetched:

-   User name
-   Email
-   Company
-   City

Additional information enriched original records.

------------------------------------------------------------------------

## Conditional Branch

IF node condition:

id \> 3

Behavior:

TRUE:

Records processed further.

FALSE:

Records separated through alternate branch.

------------------------------------------------------------------------

## Output Integration

Final processed output stored inside:

Google Sheets

Credential storage handled using n8n credential system.

No secrets hardcoded.

------------------------------------------------------------------------

## Error Handling

HTTP nodes configured using:

Continue On Fail

Behavior:

Workflow continues execution safely even if API request fails.

Silent workflow failures avoided.

------------------------------------------------------------------------

## Files Included

Task 1:

-   QA Excel report
-   QA Word report

Task 2:

-   workflow.json
-   workflow screenshot
-   README

------------------------------------------------------------------------

## Technologies Used

Task 1:

-   Manual QA Testing

Task 2:

-   n8n
-   HTTP APIs
-   JSONPlaceholder
-   Google Sheets

------------------------------------------------------------------------

Assessment completed successfully.
