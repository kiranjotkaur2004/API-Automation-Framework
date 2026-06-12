# Postman API Automation Testing Framework

### Project Overview
This project is a **REST API Automation Testing Framework** developed using Postman to validate backend APIs. It covers end-to-end testing of CRUD operations and demonstrates real-world QA automation practices used in software testing environments.

### Objective
To automate REST API testing and ensure:
- API functionality validation (CRUD operations)
- Accurate response status codes
- Data integrity in responses
- Data-driven test execution using external datasets

### Tools & Technologies
- Postman
- REST API (JSONPlaceholder / Local Backend)
- JavaScript (Postman Test Scripts)
- CSV (Data-driven Testing)
- Postman Collection Runner

### API Used
Public API:
https://jsonplaceholder.typicode.com

### Features Implemented <br>
#### CRUD Operations Testing
- Create User (POST)
- Get Users (GET)
- Get User by ID (GET)
- Update User (PUT)
- Delete User (DELETE)
####  Automated API Validation
- Status code verification
- Response body validation
- Response time checks
- Basic JSON structure validation
####  Data-Driven Testing (DDT)
- External CSV file used for multiple test cases
- Same API executed with different datasets automatically
####  Environment Management
- Base URL stored in environment variables
- Easy switching between dev and test environments
#### Sample Test Script
```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

### Test Cases

### Create User (POST /users)
- Verify status code is 201  
- Verify response contains name  
- Verify response contains email  
- Verify response time is within limit  

### Get All Users (GET /users)
- Verify status code is 200  
- Verify response is in JSON format  
- Verify response is not empty  
- Verify list contains multiple users  

### Get User by ID (GET /users/1)
- Verify status code is 200  
- Verify user ID is correct  
- Verify response contains user details (name, email)  

### Update User (PUT /users/1)
- Verify status code is 200  
- Verify updated data is reflected in response  
- Verify correct name and email update

### Delete User (DELETE /users/1)
- Verify status code is 200 or 204  
- Verify successful deletion response  
