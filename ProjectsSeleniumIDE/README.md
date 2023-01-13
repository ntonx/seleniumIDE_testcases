# Selenium-side-runner

This is a Selenium funcionality that helps to perform a test without using IDE, get some metrics and use different browsers in test cases; but we need install some requirements

---
## Install nodejs in your system and execute the next commands:

```yaml
$ node --version
$ npm install selenium-side-runner
$ selenium-side-runner --version
```

Install the libraries to connect Browsers with selenium

```yaml
$ npm install -g geckodriver
$ npm install -g edgedriver
$ npm install -g chromedriver
```

---
Execute the command:

```
$ selenium-side-runner <ProjectName.side>
$ selenium-side-runner -c "browserName=firefox" <ProjectName>
$ selenium-side-runner -c "browserName=firefox" FlowControls.side
```

a)  The first command executes in all browsers configured in selenium-side-runner
b)  To set a browser in which executes the test, use -c flag
c)  You have to download the binary file (.exe) of browser dependency and save on the test directory

In this case the project must to be save as Project Suite in SeleniumIDE:
1. In SeleniumIDE (left side) > TestSuite > Rename DefaultSuite > Click on 3 dots > Click on Add test > select test > Save Project 

The result of selenium-side-runner command must be something like:

```
 PASS  C:/Users/anico/AppData/Roaming/npm/node_modules/selenium-side-runner/dist/main.test.js (21.142 s)
  Running project FlowControls
    Running suite FlowControlSuiteTest
      √ Running test DoLoopTest (5356 ms)
      √ Running test WhileTest (5259 ms)
      √ Running test caloriesIFelse (9448 ms)

Test Suites: 1 passed, 1 total
Tests:       3 passed, 3 total
Snapshots:   0 total
Time:        21.271 s, estimated 27 s
Ran all test suites within paths "
```

This helps us to define a set of test in different browsers (if we save selenium-side-runner commands in a bash) and get execution time results
