# AMEX

Personal Banking Service

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What do you need to install to make local setup to work and how to install it.
Examples:

```Git
To run this service you need to install

-VS Code 1.44* (download section: https://code.visualstudio.com/download)
-NodeJS  14.14.22* (download section: https://nodejs.org/en/download/)
-WebdriverIO - use this "$ npm i --save-dev @wdio/cli"
-npm install (install the dependencies in the local node_modules folder)
-mocha - npm install --global mocha (to install mocha)
-npm install chai (chai assertion library)
-Git (downlaod section: https://git-scm.com/downloads)
```

After installing successfully, make the changes below to take the latest pull from master.

```Git
  git pull origin master (to dowaload the latest code)
```

### Project Creation and Framework

- After installing successfully now it is time to create your test file. You are going to store all of your test files in your project folder and make js file according to your story. e.g basic.js and start writing your script. In this you can use **mocha** framework and **page object pattern**.

- The **page object pattern** : The goal of using page objects is to abstract any page information away from the actual tests. Ideally, you should store all selectors or specific instructions that are unique for a certain page in a page object, so that you still can run your test after you have completely redesigned your page.
- Making A Page Object First off, we need a main page object that we call Page. It will contain general selectors or methods which all page objects will inherit from. We will always export an instance of a page object, and never create that instance in the test.

- The **Mocha** framework consists of some describe block and it block as you can see in below example, in describe block you can add the description of your script and in IT block you can add the particular steps

### Running locally

All private project should be installed in the VS CODE
Add the steps on how to start your project using the **wdio.conf.js**

- Create a new js file
- add your script
- run using `npm test`

**suites.config.js** :

- In this file you can add your suites.
  e.g- Registration: ['./amex/test/specs/foldername/testcasename.js'],

**package.json** :

- Package.json is shared file for both mobile and website project. Add this line in your package.json file
  "e2e:mobile:foldername": "node_modules/.bin/wdio wdio.browserstack.conf.js --suite foldername", this is used to run test browserstack.

After adding your file in suites.config and package.json , it will displayed your NPM SCRIPT and to run this just click on that.

What is **wdio.conf.js** file ?

- This file contains specs path , browsers , baseURL , framework,timeouts,hooks, etc . all the necessary and config file are present in wdio.conf.js file. So when we run the script then it will find all the details from this file and will execute accordingly.

Example:

```javascript
describe('description of your test script', () => {
  it('should do some steps', () => {
    //-------------------------
  });
});

## Running the tests

Define commands to run the different tests that can be run
• Unit test
• Functional test
• Bdd test
• Etc

```npm
* Examples :
Execute this command to run all the tests
  -npm run test
To run only functioncal test
  -npm run test:functional
```
