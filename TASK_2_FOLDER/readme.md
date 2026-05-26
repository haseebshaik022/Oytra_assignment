# Task 2 - Workflow Automation

## APIs Used

### API 1
JSONPlaceholder Posts API

https://jsonplaceholder.typicode.com/posts

Reason:
Used as a free public API to fetch sample post data for processing.

### API 2
JSONPlaceholder Users API

https://jsonplaceholder.typicode.com/users/{userId}

Reason:
Used to enrich the original data by fetching additional user information such as name, email, company, and city.

---

## Transformation Logic

A Code node was used to:

- Keep only the top 5 records
- Extract required fields:
  - id
  - title
  - userId

An IF node was used for conditional routing:

Condition:

id > 3

True branch processed matching records further.

An Edit Fields node cleaned the final output before sending data to Google Sheets.

---

## Output

Final processed records are appended to Google Sheets.

Google Sheets credentials were stored using n8n Credentials Store.

---

## Error Handling

Continue On Fail was enabled in HTTP Request nodes.

If an API call fails, the workflow does not stop silently and continues execution safely.
