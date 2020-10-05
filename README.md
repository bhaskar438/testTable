# Test Plan



**Author**: \<6300Fall20Team050\>

## 1 Testing Strategy

### 1.1 Overall strategy

#####
Back end developers will be responsible for unit tests for every non-trivial method of a class/module.  
The integration tests will also be done by developers.  Developers' Unit tests and Integration tests should be non-UI black box testing. UI testings will be done by the QA tester as described below.

#####
The QA tester will be responsible for system and regression testing; since this is a simple Android application, most likely system and regression testing would be done at the same time.  These tests will be automated UI tests; it will be done from the perspective of an End User.  Here the tester will take the most important use cases and automate user interactions in the UI.

#####
Finally, there will be some performance testing done by the developers and testers.  Developers should do both black box and white box performance testing.  For example: for the white box performance testing, developers should optimize their code such as avoiding N+1 queries and for black box performance testing, developers should check to see if the system can handle heavy use. As heavy use is very subjective, there will be some arbitrary benchmarks.  For example, adding 1000 jobs offers and then ranking them by score should be commpleted no more than a minute.  

#####
The QA tester will do performance testing through the UI.  For example, the QA tester can write a script that adds 100 jobs through the UI and see if the
system can handle ranking of job offers by score.

#####
In the absense of a client, user acceptance testing must be done by each member of our team.  Here we will assert whether we satisfy the use cases
outlined in our Use Case Model template.

### 1.2 Test Selection

#####
Test cases for black-box testing will be determined by Category Partition method.
Test cases for white-box testing will be determined by ...

### 1.3 Adequacy Criterion

TBD

### 1.4 Bug Tracking

To determine whether something is a bug, the bug must be reproducible; the developer or QA tester must repeatedly be able to reproduce the bug. 

If a developer finds a bug, then that developer must address it by modifying code and unit/integration tests.

If a QA tester finds bugs, the QA tester must report it to a developer; bugs will then be handled by a front end developer or back end developer
depending on the nature of the bug.  After the developer pushes changes for the bug fix, the QA tester must ensure the bug is no longer present.


### 1.5 Technology

Developers will use JUnit testing framework.
QA testers can use either Selendroid or Appium.

## 2 Test Cases

| Test Case Number | purpose                                                        | steps                                          | expected                  | actual | pass/fail |
|------------------|----------------------------------------------------------------|------------------------------------------------|---------------------------|--------|-----------|
|                1 | ComparisonWeights constructor should only allow integer inputs | invoke: new ComparisonWeights(1,1,1,1,"hello") | IllegalArgumentsException |        |           |
|                2 | compareJobDetails method should take two JobDetails objects    | invoke: compareJobDetails(null, null)          | IllegalArgumentsException |        |           |
|                3 | saveAllJobDetails method should take list argument             | invoke: saveAllJobDetails("hello")             | IllegalArgumentsException |        |           |
