# DevOps-Project-deployment-of-webapp-
 NOTE:- "Must read in order to understand the sequeence of project"

It is a full fledge project of DevOps that deploy a sample webApp on the TOMCAT server and  illustrate the knlowledege of tools like :- 
*Git & Github
*Ant
*Jenkins
*J-unit
*Server used :- TOMCAT 

In this Project a simple webapp will be deployed using a CI/CD pipeline(jenkins) on the TomCat server that inculde different jobs in jenkins that are mentioned below including it's plugin used as well 

*JOB 1 :- GitHubPull
plugin used -github plugin

 DESCRIPTION :- This Jenkins Job will pull the code from github repository and make it available automatically for next jenkins job to perfrom operation on it.
 
 *JOB 2 (CONTINUOUS BUILDING) :- BUild & Code Review
 plugin used for build - ANT plugin
 plugin used for Code review :- Warning next generation plugin
 
 DESCRIPTION :- After the first job is done with it's task by pulling the source code from github then the functionality of this job gonna start ,after getting the code it will build the code using "ANT" plugin and review the code using "Warning next generation " and if this job get executed successfully then it will automatically invoke the 3rd Jenkin job to get started

*JOB 3 (CONTINUOUS TESTING) :- Unit test
plugin used :- JUnit realtime test report plugin

DESCRIPTION :- the main aim of this jenkins job it to "Run test and Publish JUnit test Reports" it means if after the code is build and reviewed successfully the it need to be tested , if the code gets tested successfully then it will invoke to the last jenkins job to start but if not then the JUnit will create a realtime error report for the developer to rectify the error.


*JOB 4 (CONTINUOUS DEPLOYMENT) :- Deploy code to production 
plugin used :- Deploy to container
plugin used to created pipeline:- Build pipeline

DESCRIPTION :-after the successfull execution of the previous jobs of jenkins the last stage is to depoly it .
Note :- if every job get's done without any error then deployment will be done automatically and you will be able to see the pipeline of your deployed sample web app without any error in green color(it menas deployed the webapp successfully).
