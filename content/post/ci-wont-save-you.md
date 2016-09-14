+++
date = "2016-09-14T12:28:08+01:00"
draft = false
title = "Sunday sermon #2 - help your project, use CI!"
categories = ["sermon", "sunday", "ci", "automation", "quality", "continuous integration"]
+++

### 1. What's CI
CI stand for continous integration. The simplest way I could explain what it really is is with an example.

Say, you remember when you started your first coding related job, or maybe the second. Hopefully the company/environment provided you with opportunity to review code throughout the team. If so you may have noticed that often it is not the solution itself that takes the most time but the actual codereviews, discussions and merging that is the problem.
 
Now the idea of CI is that those submitted changes once reviewed/documented/whatever is in the process get merged and integrated into the code base.

### 2. Benefits of CI
Now you may have been unlucky and had the unpleasant opportunity of deployments straight to staging/production in versioning approach [simply deploying with version only].
 
 That often means that your code gets merged and integrated not after it was reviewed BUT during the deployment process. A few days taken out of the team life just to fix broken tests, conflicts, bad merges and other hidden problems. Not to mention that the actual deployment usually takes a lot of time as well: executing migrations, updating codebase, regenerating caches/static content.

In comes CI with it's integral part - automation. Although the CI itself does not mean automation, once you start implementing CI to your project the automation part comes as a natural step.

##### 2.1 Deployment/build automation
Assuming that you guys still deploy manually you sure know how long it takes. Starting from executing migrations on the DB, updating indexes, the codebase itself, regenerating caches/static content. All of those take a lot of time, yet they don't have to.

All of those steps are simple enough to automate them. Since if any of the step fails you usually rollback anyway - so should the automated part. Follow steps, prepare environment, deploy. If any steps fail - do not dpeloy. 

Protip: Those automation steps should be external to your CI solution, eg. CI shouldn't contain the scripts themselves but only execute them.

##### 2.2 Test execution automation
If you are no writing any tests - change either your work quality or the work itself. Benefits are outrageous, but even if you do write them test execution is problematic. From the integration point of view  - tests tell you how well your changes integrated into the existing code. 

This makes them valuable to execute on each codebase change made. Without any automation it is quite problematic since tests are ran on your own project and your project have it's own dependencies. But this is why we automated the environment setup in 2.1. If you have it automated - the tests execution is childplay. 

Build the environment, deploy, execute tests and provide testsuite results to interested parties (eg. code reviewers).

##### 2.3 Deployment methodology change
You have just read about quality assurance through test writing and execution per submitted change. At the beginning of this short post you have also read about deployment methodologies. There are many, I have mentioned versioning deployments.

Well, since you have went a long way from having to do everything yourself, perhaps enhancing your code quality through tests, integrating the automation in your software development process. At this point you may notice that: if change is tested, does not bring any integration issues and has been reviewed by the team - why wait with the merging?

Aand you have just created a great environment to use the CI with : )