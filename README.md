## **Functional Testing of GitHub API Tests**

The scope of functional testing will cover the following GitHub API functionalities:
- CRUD Operations: Repositories in GitHub.
- Authentication: Token-based authentication.
- Error Handling: Proper handling of error responses for invalid inputs and requests.
- Positive and Negative Test Cases: Validation for successful operations and failure scenarios

**Design Pattern**
- REST API design patterns is selected. It has resources as collections, and the HTTP methods used are GET, POST, PUT, and DELETE.

**SET UP**

Required tools: Postman, npm and newman
- Clone the project from https://github.com/gkb67/Github-API-Tests/
Install the dependencies:
- npm install
- npm install -g newman
- npm install -g newman-reporter-html\

**Test Cases**

**Authentication Handling**
- Scenario 1 – Verify Valid Authentication
- Scenario 2 - Verify Invalid Authentication

**Repository Management**
- **Positive tests**
  - Scenario 1 – Verify that website is opened succussfully
  - Scenario 1 – Verify that user can create Repository with valid name and description
  - Scenario 2 – Verify that user can update repository details
  - Scenario 3 - Verify that user can delete an existing repository.
  - Scenario 4 - Verify that user can retrieve all available repositories
  - Scenario 5 - Verify that user can retrieve details of an existing repository.
 
- **Negative tests**
  - Scenario 1 - Verify that user cannot create a repository with an invalid data.
  - Scenario 2 - Verify that user cannot update a non-existent repository.

**How to Run Tests**

Test run results with Newman
1.	Export the collection and environment from https://www.postman.com/gzd8/workspace/github-api-testing
2.	newman run yourCollectionFile.json -e yourEnvironmentFile.json --reporters='cli,htmlextra'
3.	See the results in Newman folder in your selected path

Test run results in git actions
1. Open https://github.com/gkb67/Github-API-Tests/actions/ and see the test results
2. Tests are automatically run every day
