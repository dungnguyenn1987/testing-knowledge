# FPT INTERVIEW
#### 1. What does tester do in development phase?
<details>

- Test planning consists of defining the test objectives and then selecting an approach that best achieves the objectives within the constraints imposed by the overall context. 
- Test monitoring and test control. Test monitoring involves the ongoing checking of all test activities and the comparison of actual progress against the plan. Test control involves taking the actions necessary to meet the test objectives.
- Test analysis includes analyzing the test basis to identify testable features. Associated test conditions are defined and prioritized, taking the related risks and risk levels into account. The test basis and the test object are also evaluated to identify defects they may contain and to assess their testability. Test analysis is often supported by the use of test techniques. Test analysis answers the question “what to test?” in terms of measurable coverage criteria. 
- Test design includes elaborating the test conditions into test cases and other testware (e.g., test charters). This activity often involves the identification of coverage items, which serve as a guide to specify test case inputs. Test techniques can be used to support this activity. Test design also includes defining the test data requirements, designing the test environment and identifying the necessary infrastructure and tools. Test design answers the question “how to test?”.
- Test implementation includes creating or acquiring the testware necessary for test execution (e.g., test data). Test cases can be organized into test procedures, which are often assembled into test suites. Manual and automated test scripts are created. Test procedures are prioritized and arranged within a test execution schedule for efficient test execution. The test environment is built and verified to be set up correctly.

</details>

#### 2. Can tester start testing when funcitonality under development does not complete yet? can tester replace the other testing activity?
<details>
  
Principle of early testing is sometimes referred to as shift left because it is an approach where testing is performed earlier in the SDLC. Shift left basically suggests that testing should be done earlier (e.g., not waiting for code to be implemented or for components to be integrated), but it does not mean that testing later in the SDLC should be neglected.

  There are some good practices that illustrate how to achieve a “shift left” in testing, which include:
  
  - Reviewing the specification from the perspective of testers. These review activities on 
specifications often find potential defects, such as ambiguities, incompleteness, and 
inconsistencies
  - Writing test cases before the code is written and have the code run in a test harness during code 
implementation
  - Using CI and even better CD as it comes with fast feedback and automated component tests to 
accompany source code when it is submitted to the code repository
  - Completing static analysis of source code prior to dynamic testing, or as part of an automated 
process
  - Performing non-functional testing starting at the component test level, where possible. This is a 
form of shift left as these non-functional test types tend to be performed later in the SDLC when a 
complete system and a representative test environment are available

Shift left might result in extra training, effort and/or costs earlier in the process but is expected to save 
efforts and/or costs later in the process.

For shift left it is important that stakeholders are convinced and bought into this concept.

</details>

#### 3. How we test locally?
<details>
  
</details>

#### 4. API schema
<details>

An API schema defines the structure of the data exchanged between a client and an API. It acts as a blueprint or contract that outlines how the data is formatted, what fields are expected, and the relationships between different data entities.

There are several ways to define API schemas depending on the type of API, such as REST, GraphQL, or others. Below are a few common ways to describe an API schema:

- OpenAPI Specification (formerly Swagger)
  - The OpenAPI Specification (OAS) is a widely used standard for describing RESTful APIs. It provides a comprehensive way to document API endpoints, request/response formats, authentication methods, and more.
- GraphQL Schema
  - For GraphQL APIs, the schema defines types, queries, mutations, and subscriptions that the API supports. It allows clients to request only the data they need, in contrast to REST APIs.
- JSON Schema
  - A JSON schema defines the structure of JSON data, typically used to validate and document data formats for API requests and responses.

</details>

#### 5. when it's wrong when API return 200?
<details>
  
</details>

#### 6. PO/stackholders request to add more feature in the middle of sprint, what should you do?
<details>

Here’s a step-by-step guide on what you should do when this happens:

1. Assess the Request
  - Clarify the request: Ensure you understand the specifics of the new feature request. Is it a new priority feature, a change in scope, or a quick fix? Ask questions to get clarity.
  - Impact on current work: Evaluate how adding the new feature will affect the ongoing sprint. Does it conflict with existing priorities? Will it require significant resources or time?
  - Urgency: Determine the urgency of the new feature. Is it a critical feature for the sprint or is it something that can wait until the next sprint?
2. Check Sprint Capacity and Priorities
  - Review the sprint backlog: Look at the work your team has already committed to in the current sprint. Is the new request realistic to include without overloading the team?
  - Check team capacity: Evaluate if the team has enough capacity to handle the new request while still completing the planned work. Adding work mid-sprint may result in delays or quality issues if the team is stretched too thin.
  - Reprioritize if necessary: If the new feature is crucial, you may need to revisit the priorities. 
3. Communicate with the Product Owner
Transparent conversation: Have an open discussion with the PO or stakeholders about the impact of adding new work to the sprint. Explain the trade-offs and the consequences of changing the scope.
If the request is important but can’t be completed in the current sprint, suggest moving it to the next sprint or creating a backlog item for future work.

4. Determine the Best Course of Action
Depending on the context of the request and the impact, you have a few options to proceed:

  - Defer the request: If the new feature is not urgent and doesn’t align with the sprint goal, recommend deferring it to the next sprint. This keeps the current sprint stable and avoids overloading the team.
  - Re-prioritize the backlog: If the feature is urgent and critical, work with the PO to re-prioritize the backlog. You may need to remove lower-priority work to make room for the new feature.
  - Re-scope the sprint: If the team has the capacity and the new feature aligns with the sprint goal, you can adjust the scope by removing or deferring lower-priority items and adding the new feature.

</details>

#### 7. How setup the full process of CI/CD
<details>

Setting up Continuous Integration (CI) / Continuous Delivery (CD) for automation test scripts involves configuring a system that will automatically build, test, and deploy your code whenever changes are pushed to your version control system (e.g., Git). The goal is to integrate automation testing into the CI/CD pipeline to ensure that new code changes do not break existing functionality.

Steps to Set Up CI/CD for Automation Test Scripts
1. Ensure that your project is stored in a Git repository (e.g., GitHub, GitLab, Bitbucket).
Your test scripts should be in the repository so that the CI/CD pipeline can access and run them. Some of the most commonly used ones are:

  - Jenkins
  - GitHub Actions
  - GitLab CI
  - CircleCI
  - Travis CI
  - Azure DevOps

2. Write and Organize Automation Test Scripts

Ensure that your tests are automated, idempotent (can be rerun without changing the result), and independent (tests don't depend on one another).

4. Set Up the CI/CD Pipeline
You'll need to configure the pipeline (create pipeline file) to perform the following tasks:

  - Clone the Repository: The CI tool needs to pull the latest version of the code from your repository.
  - Install Dependencies: Ensure that any dependencies (e.g., npm packages, Python packages) are installed before the tests are executed.
  - Run the Automated Tests: using command line by your test runner
  - Generate Test Reports:Most CI tools can generate test reports in various formats (e.g., JUnit XML, HTML). This helps in viewing the results and analyzing failures.
  - Set Up Notifications via emails or any channels

Example: .github/workflows/test.yml
```
name: Run Automated Tests

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test

      - name: Upload test results
        uses: actions/upload-artifact@v2
        with:
          name: test-results
          path: ./test-reports
```

</details>

#### 8. Describe your current automation framework, could it cover both UI and API
<details>

A typical Selenium framework architecture looks like this:

- Test Scripts: The scripts that define the test steps using Selenium WebDriver.
- Page Object Classes: Contains UI elements and methods that represent the web pages.
- Utils: Helper classes for managing things like reading data files, taking screenshots, handling wait times, etc.
- Test Data: The data required for running the tests, stored in files or databases.
- Reports: A reporting module that generates test execution reports.
  
</details>

#### 9. Challenges/Difficult you faced in automation testing
<details>
  
</details>

#### 10. What is other pattens that applied in automation framework besides of POM?
<details>

Applying OOP principles in Page Object Model (POM) results in a modular, scalable, and maintainable automation framework. 

- **Encapsulate**  is achieved by hiding the details of the web elements and providing only the necessary methods to interact with them.
  - Private Web Elements: Web elements are made private so that they are not accessible from outside the Page Object class.
  - Public Methods: Methods are provided to interact with these private elements. These methods are exposed to the test scripts, which can invoke them to interact with the web page.
- **Abstract** away the complexity of page interactions from the test scripts by creating high-level methods (e.g., login, logout).
- **Inheritance** is useful when there are common actions or utilities that can be shared between different page objects.
  - BasePage Class: A BasePage class can be created to contain common functionality such as navigating to different pages, waiting for elements, or performing common actions (e.g., clicking buttons, checking alerts).
  - The Page Object classes can then inherit from the BasePage class to reuse common methods.
- **Polymorphism** allows different page objects or actions to be handled using the same interface. This can be useful when you want to extend functionality or handle different page interactions in a unified way. Method overriding:
  - Redefine methods in the subclass
  - Define other methods with the same name, but different parameters
  
</details>

#### 11. Explain DI Container
<details>
  
</details>

#### 12. Strategy to manage the large number of test cases, for business or test results
<details>
  
</details>

#### 13. How to solve the large number of failed tests
<details>
  
</details>

#### 14. Different btw BDD and TDD, and when to apply
<details>
  
- Test-Driven Development (TDD):
  - Directs the coding through test cases (instead of extensive software design) 
  - Tests are written first, then the code is written to satisfy the tests, and then the tests and code are 
refactored
- Acceptance Test-Driven Development (ATDD):
  - Derives tests from acceptance criteria as part of the system design process
  - Tests are written before the part of the application is developed to satisfy the tests 
- Behavior-Driven Development (BDD):
  - Expresses the desired behavior of an application with test cases written in a simple form of 
natural language, which is easy to understand by stakeholders – usually using the 
Given/When/Then format
  - Test cases should then automatically be translated into executable tests

</details>

#### 15. when execute performance test, how to determine the system throughput
<details>

To determine system throughput during a performance test, follow these steps:

- Define the appropriate throughput metric (RPS, TPS, etc.).
- Run the load test, simulating real-world traffic.
- Calculate throughput using the formula (Total Requests / Test Duration).
- Monitor system resources (CPU, memory, network) to identify potential bottlenecks.
- Assess throughput vs. latency to find the optimal balance. As the system handles more requests (higher throughput), the response time (latency) may increase, especially if the system approaches its capacity limits. Ideally, throughput should be high while maintaining acceptable latency levels.
- Adjust the test parameters and rerun the tests as needed.
- Analyze and report the results, identifying areas for improvement.
  
</details>

#### 16. PO/stackholders have an urgent milestone, they need the quick response about the quality of some features that can be deployed or not. We have UI, some API and datastorage. which testing you prefer?
<details>

Perform the one of Testing types with the opening Devtools to make sure application function to be smooth without any network or console errors:
- Smoke Testing: Perform high-level tests to ensure the most critical features are functioning correctly.
- Sanity Testing: After bug fixes or new feature development, run sanity checks to confirm that the issue has been resolved and the changes haven’t broken other parts of the application.
- Exploratory Testing: Allocate time for exploratory testing, where testers use their knowledge and creativity to identify high-impact issues, especially in areas that may not be fully automated.
- Boundary Value Testing: Focus on testing the boundaries (limits) of inputs, especially where validation is involved, as this is where many bugs often occur.
  
</details>

#### 17. How long to adapt the new programming language?
<details>
  
</details>

# Others
#### 1. Cases cannot be done by automation
<details>

- Unstable features
- One time test cases
- Adhoc cases
- Exploratory testing
- UI/GUI
- Technical challenges (Capcha, ActiveMQ, Azure storage..)
  
</details>

#### 2. How to test without document
<details>

- Apply exploratory testing to understand the existing product
- Discuss to PO/Seniors to get business knowledge
- Go through production bugs to identify the edge cases
  
</details>

#### 3. How to make sure enough test cases
<details>

- Understand and analyze requirement carefully to list out test scenarios
- Apply test types/ techniques to identify positive/negative test cases in each scenario/functionality
- For complex flows, using traceability matrix to cover all business rules and requirement specifications
  
</details>

#### 4. How to select the right automation tool/framework
<details>

- Verify the complexity of project requirements
- Define the scope of automation
  - Implement automation scripts (simple or complex)
  - Reporting
  - Integration to CI/CD
  
</details>
