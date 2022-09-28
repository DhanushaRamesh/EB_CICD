## Create a CICD Pipeline to  update the web application in Elastic Beanstalk :-

We will explore how to build a CICD pipeline and update the background colour and text of an elastic beanstalk-running web application.

## CODE COMMIT :-
  1. Navigate to AWS Console and open AWS Code Commit
  2. Create a new repository and upload the files provided in nodejs folder in this repository.
  <img width="900" alt="image" src="https://user-images.githubusercontent.com/48701982/192682441-56cf02db-2287-43e1-8065-967f7a37b9c8.png">
  3. Establish a notifcation rule to receive notifications of updates done to the Code Commit repository.

## CODE BUILD :-
  1. Create a new build project on Code Build.
  2. Choose Code Commit from the source tab, then choose the nodejs repository.
  <img width="557" alt="image" src="https://user-images.githubusercontent.com/48701982/192682997-d8aa86a3-585f-4e75-9991-ef1220b941d7.png">
  3. Select Managed image and Ubuntu as the operating system in the Environment tab.
  <img width="401" alt="image" src="https://user-images.githubusercontent.com/48701982/192685771-5b446b65-22df-44f5-b746-3b75608911d2.png">
  4. Insert the build commands listed below in the Buildspec tab.
  <img width="587" alt="image" src="https://user-images.githubusercontent.com/48701982/192683512-f8546933-f06b-418a-a9eb-9e647c7a4b30.png">
  <img width="388" alt="image" src="https://user-images.githubusercontent.com/48701982/192683705-e9555366-14e7-40de-a03c-991c0927ef64.png">
  5. Launch the build project while leaving the rest at its default settings.

## CODE Pipeline :- 
  1. Create a new pipeline application.
  2. Choose the Code Commit NodeJS repository created for the source tab.
  <img width="681" alt="image" src="https://user-images.githubusercontent.com/48701982/192684491-b7d5ab52-38b9-4df7-836d-c0b772833fb1.png">
  3. Select the already created Code Build project name and leave the rest at its default settings.
  <img width="774" alt="image" src="https://user-images.githubusercontent.com/48701982/192684632-349bca95-3472-4eb6-9adc-4f210376d341.png">
  4. Choose the already createde Elastic beanstalk environment for Code deploy.
  <img width="787" alt="image" src="https://user-images.githubusercontent.com/48701982/192684885-fd7f8d66-8100-41ab-ba4e-8e9d99b1c556.png">
  5. Review the pipeline and create the pipeline.
 
Note :- You can also add a manual approval before code deploy step - which should be reviewed and approved manually for the pipeline to trigger deployment.

## Deployed Application :
  1. Once the CICD pipeline succeeds, Navigate to Elastic Beanstalk console and access the same url of the created environment. Now you could see the changes done in the source code been deployed in the webpage.
  <img width="901" alt="image" src="https://user-images.githubusercontent.com/48701982/192686330-46f2b2dd-87c2-4aa0-9d88-bb27d59379a1.png">


