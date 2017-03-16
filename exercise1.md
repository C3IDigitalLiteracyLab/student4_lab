#Cloud Compass Computing, Inc.<br>Digital Literacy Course<br><br>DevOps for Product Owners - Lab 1

##Introduction

It's the morning after a release. All went well until the DM called to say the Minister had an idea to make the site AWESOME. As the message passed down the line, the urgency went through the roof. Fix it NOW! you are told.

Fortunately, the team had worked together to put a good deployment pipeline in place.  You can do this!

There's no release guide - all you have to as the developer is:

* make the code changes necessary
* commit it in a version control repo (github)

From there, the automation will build the software and deploy it to the site, where you can see the changes you make.

This exercise makes use of a basic "ToDo List" web application.

In the course of this exercise, you will experience:
 
* how to access and navigate in Github - a version control system used for most Open Source solutions
* how code is stored and organized on GitHub in repositories - "repos"
* how edits to source code can trigger builds and deployments in a DevOps environment such as OpenShift.
* see in OpenShift how an app is setup and monitored by the DevOps team, and some of the controls available.

Each student will have the use of their own repository for this exercise, but please ensure that you access your *assigned repo only* to avoid causing confusion for another student.

Login details that you'll need are in the steps below.

##Access your deployed ToDo List web application
 
The starting point of the exercise is that a version of the ToDo application has been deployed for each student. Your student number for the exercises is on the cover of your workbook.

To view your version of the ToDo application:

* Ctrl-Click your link (with your student number) from the list below to open the link in a new tab.
  * Student 1 - http://lab-student1-lab.apps.cloudcompass.ca
  * Student 2 - http://lab-student2-lab.apps.cloudcompass.ca
  * Student 3 - http://lab-student3-lab.apps.cloudcompass.ca
  * Student 4 - http://lab-student4-lab.apps.cloudcompass.ca
  * Student 5 - http://lab-student5-lab.apps.cloudcompass.ca
  * Student 6 - http://lab-student6-lab.apps.cloudcompass.ca
  * Student 7 - http://lab-student7-lab.apps.cloudcompass.ca
  * Student 8 - http://lab-student8-lab.apps.cloudcompass.ca
  * Student 9 - http://lab-student9-lab.apps.cloudcompass.ca
  * Student 10 - http://lab-student10-lab.apps.cloudcompass.ca
  * Student 11 - http://lab-student11-lab.apps.cloudcompass.ca
  * Student 12 - http://lab-student12-lab.apps.cloudcompass.ca
  * Student 13 - http://lab-student13-lab.apps.cloudcompass.ca
  * Student 14 - http://lab-student14-lab.apps.cloudcompass.ca
  * Student 15 - http://lab-student15-lab.apps.cloudcompass.ca
  * Student 16 - http://lab-student16-lab.apps.cloudcompass.ca
  * Student 17 - http://lab-student17-lab.apps.cloudcompass.ca
  * Student 18 - http://lab-student18-lab.apps.cloudcompass.ca
  * Student 19 - http://lab-student19-lab.apps.cloudcompass.ca
  * Student 20 - http://lab-student20-lab.apps.cloudcompass.ca
* Enter some items in the ToDo list.
* Congratulations, your life is now 17% more organized!

##Access your repository on GitHub

Time to add the awesome.

You will be provided a GitHub username+password and in that account will be your code repo - the one with your student number. There's one for everyone.

The steps to find your way to your assigned GitHub repository are as follows:

* Ctrl-Click (to open a new tab) the link below corresponding to your student number:
  * Student 1 - https://github.com/C3IDigitalLiteracyLab/student1_lab
  * Student 2 - https://github.com/C3IDigitalLiteracyLab/student2_lab
  * Student 3 - https://github.com/C3IDigitalLiteracyLab/student3_lab
  * Student 4 - https://github.com/C3IDigitalLiteracyLab/student4_lab
  * Student 5 - https://github.com/C3IDigitalLiteracyLab/student5_lab
  * Student 6 - https://github.com/C3IDigitalLiteracyLab/student6_lab
  * Student 7 - https://github.com/C3IDigitalLiteracyLab/student7_lab
  * Student 8 - https://github.com/C3IDigitalLiteracyLab/student8_lab
  * Student 9 - https://github.com/C3IDigitalLiteracyLab/student9_lab
  * Student 10 - https://github.com/C3IDigitalLiteracyLab/student10_lab
  * Student 11 - https://github.com/C3IDigitalLiteracyLab/student11_lab
  * Student 12 - https://github.com/C3IDigitalLiteracyLab/student12_lab
  * Student 13 - https://github.com/C3IDigitalLiteracyLab/student13_lab
  * Student 14 - https://github.com/C3IDigitalLiteracyLab/student14_lab
  * Student 15 - https://github.com/C3IDigitalLiteracyLab/student15_lab
  * Student 16 - https://github.com/C3IDigitalLiteracyLab/student16_lab
  * Student 17 - https://github.com/C3IDigitalLiteracyLab/student17_lab
  * Student 18 - https://github.com/C3IDigitalLiteracyLab/student18_lab
  * Student 19 - https://github.com/C3IDigitalLiteracyLab/student19_lab
  * Student 20 - https://github.com/C3IDigitalLiteracyLab/student20_lab

  *NOTE:* If you're a keener and have already logged into GitHub with your own personal account, log out prior to doing the next step

* Click the "Sign In" button in the top left and enter the github user ID on the front screen.
* You should be back to the screen you were on, but now logged into github.
* You should see a list of files. These are the contents of the repository.
* Congratulations! You have now completed GitHub Competency Level 1! 

##Edit a source code file

Each of the files listed in the repository you navigate to above are a part of the ToDo application, or some form of supporting material.  You will be making a change to the contents of one of these files, and then watching how it propagates through the build and deployment tooling.
 
To perform your edits:

* Locate the file "index.html" in the repository's file list and click it. The screen will update and display the contents (code) of the file.
* Switch to to the tab showing your ToDo app. Notice the title of the app is "todos" and the prompt is "What needs to be done?". So sad.  We want to change these to something awesome.
* Switch back to your GitHub tab.
* Find the Edit (pencil) button at the top-right of the area showing the source code and click it. You're now in Edit mode.
* Go to line 16 in the source code and change the text `<h1>todos</h1>` to `<h1>awesome list</h1>`
* Go to line 18 in the srouce code and change the text `placeholder="What needs to be done?"` to `placeholder="How to be awesome..."`
* Scroll to the very bottom of the page and in the "Update" field of the Commit changes" section, type something like "make app more awesome" and then click the green "Commit changes" button underneath.
* Congratulations, you're now a junior front-end dev!
  
##Follow build and deploy process

The GitHub repository containing the file you edited above is connected to an OpenShift build and will build and deploy a new version of your ToDo app for every change you make to your GitHub repository.

In this exercise, we're going to explore OpenShift a little bit to see some of the pieces that work together to build and run your app. This is where your DevOps team monitors the running system.

* Ctrl-Click https://master.labs.cloudcompass.ca:8443 to open OpenShift in a new tab
* Log in to OpenShift with a student number username (e.g. "student1", "student2", etc.)
* Use the password on the label provided to you.
  * Passwords may have the number "1", but don't have the letters "l" or "I"
* You should see and Click on a project named "studentXX - Digital Literacy Course Lab"
* You'll see an overview of the components that make up your project's home in OpenShift.

Depending on how quickly your code edits from the prior part exercise took to process, you may see a build happening (progress indicator near the top of the page), or a brand-new deployment (text like "Deployment Config lab - a few seconds ago"), meaning the build has already completed.

If the new deployment is complete, switch to your ToDo app browser tab and refresh the page.  Your (awesome) edits should appear. If the build is still running, wait for it to complete, and watch the blue glowing ring (ooh! glowing things!) as it deploys afterwards, then check for your changes in your ToDo app browser tab.

Congratulations you're now a DevOps Apprentice Level 1!

Feel free to look around a bit in OpenShift.  Want to add capacity to your app? Bump up the number of CPUs to 2. Compare that with the iStore process.