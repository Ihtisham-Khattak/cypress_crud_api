API Testing Framework using `Cypress` with `GitHub Actions` workflow for generating and publishing test report

## 🚀 Description:

Automated CRUD (i.e., `POST`, `GET`, `PUT`, `DELETE`) operations using `Cypress`

## 🚀 Prerequisites:

- [nodejs](https://nodejs.org/en/)
- [npm](https://docs.npmjs.com/about-npm)
- [Cypress](https://www.cypress.io/)
- [Go Rest APIs](https://gorest.co.in)

## 🚀 Installation Steps:

- [Fork](https://github.com/ashikkumar23/api-testing-cypress/fork) and Clone the repository `api-testing-cypress`
- Move to the `api-testing-cypress` directory:

```commandline
cd api-testing-cypress
```

- Set up a new npm package:

```commandline
npm init
```

- Install cypress:

```commandline
npm install cypress
```

- Add the following lines to the `package.json` file, `"scripts"` section:

```json
  "scripts": {
    "cypress:open": "./node_modules/.bin/cypress open",
    "cypress:run": "./node_modules/.bin/cypress run --spec **/*.cy.js"
  }
```

## 🚀 Test Execution:

- To run the tests on your terminal:

```commandline
npm run cypress:run
```

- To run the tests against the [Cypress Test Runner](https://docs.cypress.io/guides/core-concepts/cypress-app#The-Test-Runner):

```commandline
npm run cypress:open
```

- On [Cypress Test Runner](https://docs.cypress.io/guides/core-concepts/cypress-app#The-Launchpad):
  - Select `E2E Testing`
  - Choose a browser: `Chrome` or `Electron`
  - Click on `Start E2E Testing in {browser}`
  - Once the test runner has loaded, click on the spec file i.e., `test_crud.cy.js` to run the test

## 🚀 Reporting:

  - Mochawesome is a custom reporter for use with the Javascript testing framework, mocha. 
    It runs on Node.js (>=10) and works in conjunction with mochawesome-report-generator to 
    generate a standalone HTML/CSS report to help visualize your test runs.

- Install [mochawesome](https://www.npmjs.com/package/mochawesome) dependencies:

```commandline
npm install --save-dev mocha cypress-multi-reporters mochawesome
```

```commandline
npm install --save-dev mochawesome-merge
```

```commandline
npm install --save-dev mochawesome-report-generator
```

- Add the following lines to the `package.json` file, `"scripts"` section:

```json
  "scripts": {
    "report:merge": "mochawesome-merge cypress/reports/json/*.json > index.json",
    "report:generate": "marge index.json --reportDir public --assetsDir public/assets --reportPageTitle index.html"
  }
```
