# Testing Foundation

---

## Understanding the Testing Mindset

- The mindset of testing is more important then any method, tools, and frameworks
- QA teams and software development teams view applications in different ways, developers build, while QA teams break
- An easy way to start with tests are to have an end goal, and work backwards
- In Agile, test cases can be captured in user stories as accerptance criteria for the story to be done

## Identifying What to Test

- Identifying what to test is difficult, especially when the application is already in production.

### User Journeys

- To start writing tests for already existing applications, start by writing tests for most critical pieces
  - Examples
    - login/authentication
    - purchasing a product
    - processing credit card
    - sign-up forms
  - These tests should be end to end
- User journeys are the essential paths in which a user of your application takes
- This journey should be done in a single test to make sure all the pieces within the application are working correctly
- Testing user journeys also tests all the layers within the tech stack. Testing front-end, back-end, database layer, networking, and API layers
- The user journey tests the critical pieces of an application, providing confidence that the application is behaving as it should

### New Features

- To test new features starting with the end goal is the best method
  - what problem does the feature solve
  - what exactly does the feature does
- Breaking the feature down to small steps, which can be translated into tests
- With tests, you can write code necessary to ensure the tests pass
- This makes it easier to refactor code later to ensure you have not broken anything during refactoring

### Bugs

- Its good to write tests around any bugs that appear
- Writing failing tests, allows you to ensure the bug has been fixed when the test passes

## Manual vs Automated Testing

### Manual Testing

- Manual testing involves physically interacting with an application
- Manual testing is very time consuming since it requires performing the same tasks over and over
- Shipping code multiple times a day is next to impossible when only manually testing

### Automated Testing

- Shift Left, developers are becoming more involved with tests
- This means testing is becoming more part of the development cycle instead of an afterthought
- Automation is becoming the norm

## Who should be responsivle for testing?

- Testing is everyone involved in the development's job

### 1. Dedicated Development and QA teams.

- When companies have dev and QA teams, software development is for the devs, testing is for the QA teams

### 2. Designer, Developer, QA, etc.

- When teams have designers, developers, and QA, QA is typically responsible for testing

### 3. Fullstack Solo Developer

- For small teams without QA teams, developers are responsible for writing the code, and ensuring it works
- In small teams, testing is everyone's responsibility and should be thought about through the entire process

## What is the Testing Pyramid?

- The pyramid illustrates testing types and their relationships

### Unit tests

- Unit tests are at the bottom of the pyramid
- Foundation upon other tests rest
- Unit tests test single unit within function, meaning they are not dependant on other parts of the system
- Unit tests are done as "Black Box"
- Black Box tests are done with no concerne of the logic inside, only concerned about the specific output type given a specific input

### Integration tests

- Integration tests aim to ensure pieces of the applications are working together
- These tests fundemantaly dependent
- The main difference between unit and integration is integration tests are not done in isolation

### Component tests

- Component testing allows you to test component in isolation
- Allows testing of complex UI elements outside of testing the web page

### End to End tests

- Test anything that is run in the browser
- E2E tests often replace integration testing
- Test user interaction within the application
