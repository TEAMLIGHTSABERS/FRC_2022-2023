# LIGHTSABERS Getting Started with FRC Robot Code

[![Gradle](https://github.com/wpilibsuite/allwpilib/actions/workflows/gradle.yml/badge.svg?branch=main)](https://github.com/wpilibsuite/allwpilib/actions/workflows/gradle.yml)
[![Java Documentation](https://img.shields.io/badge/documentation-java-orange)](https://github.wpilib.org/allwpilib/docs/development/java/)

Welcome to the LIGHTSABERS Robot Code Repository for the FRC 2022-2023 Season. This Repository Contains the steps for installing the Coding Environment and loading in last year's FRC Robot Code.

- [Preliminaries with Git](#preliminaries-with-git)
- [Robot Home](#robot-home)
- [Zero to Robot](#zero-to-robot)
- [GitHub Revisited](#GitHub-Revisited)
- [Programming Basics](#programming-basics)
- [Creating a New Robot Project](#creating-a-new-robot-project)
- [3rd Party Libraries](#3rd-party-libraries)
- [Copy Last Years Robot Code](#copy-last-years-robot-code)
- [Git Update](#git-update)
- [Next?](#next)


# Preliminaries with Git

First of all, I'm assuming that you are reading this README.md file from the "main" branch on the LIGHTSABERS Web-based GetHub site (i.e. the remote Github repository).  This repository should not be cloned from the "main" branch.  The first thing to do is to create a new branch by clicking on the "branch" icon at the top of this repository.
![image](https://user-images.githubusercontent.com/54441806/205994006-44c873f8-bac8-4605-8b4d-bd86b5a21ced.png)
This will bring up a "branch" page, and on the right side of this page is a green button called "New Branch".  Click on the "New Branch" button, type "{yourname}Dev" in the Branch Name, make sure that the source is set to the "main" branch, and then click "Create Branch".  
![image](https://user-images.githubusercontent.com/54441806/205996651-fa7224c6-71c3-4abe-b60e-2d3e37ea0f4c.png)
The resulting "Overview" page will then show that there is an Active branch called "{yourname}Dev".  You can click on the "{yourname}Dev" branch and you will see that it has the same files as were in the "main" branch.
![image](https://user-images.githubusercontent.com/54441806/205998157-9fa5980c-fed6-4cf2-befc-6f007a0b72eb.png)
  
At this point, I will assume that you are reading this README.md file from the "{yourname}Dev" branch.  You are now ready to setup your computer to receive your local repository of the FRC_2022-2023 Code.  To avoid having this repository proliferate on your computer, it will be stored in the Public User's workspace.  Create a new storage folder on your Windows computer to act as your local Git repository for the FRC 2022-2023 Code:
  
"{Drive_Letter}:\Users\Public\GitHub\FRC_2022-2023"

Note: if this location already exists you must cleanup the computer.  If this is the case, follow the instructions at [Zero to Robot: Uninstalling](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/wpilib-setup.html#uninstalling).

# Robot Home

In this repository is a folder called "Robot_Code".  All Robot code projects for the 2022-2023 year will be created in this folder.  Each will have it's own folder, which will be named in a manner that provides a basic idea of what the code does.

Last year's robot code will be in the folder "Robot_Code/Last_Year.

# Zero to Robot

Starting with Step 2 of the Zero to Robot instructions (https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/wpilib-setup.html) install the WPILib libraries. *Since we are programming in Java and we are not building the WPILib libraries, it is not necessary to perform the steps for the "Additional C++ Installation for Simulation".*  When the instructions on this web page have been completed, the following will be installed on your computer:
  
Visual Studio Code - The supported IDE for 2019 and later robot code development. The offline installer sets up a separate copy of VS Code for WPILib development, even if you already have VS Code on your machine. This is done because some of the settings that make the WPILib setup work may break existing workflows if you use VS Code for other projects.

C++ Compiler - The toolchains for building C++ code for the roboRIO

Gradle - The specific version of Gradle used for building/deploying C++ or Java robot code

Java JDK/JRE - A specific version of the Java JDK/JRE that is used to build Java robot code and to run any of the Java based Tools (Dashboards, etc.). This exists side by side with any existing JDK installs and does not overwrite the JAVA_HOME variable

WPILib Tools - SmartDashboard, Shuffleboard, RobotBuilder, Outline Viewer, Pathweaver, Glass, SysID

WPILib Dependencies - OpenCV, etc.

VS Code Extensions - WPILib extensions for robot code development in VS Code

Continue to the next page in the instructions and select the "Visual Studio Code Basics" hyperlink.

# GitHub Revisited

Assuming that you have returned to this README.md file on the Web-based GitHub (remote repository), near the top of this repository is a green button called "Code" next to the word "About".  Left click on the "Code" button and select the "Open with GitHub Desktop" option.  If the GitHub Desktop Application doesn't exist on your computer, GitHub will download it and ask you to log-in.  If you don't have an account, create one for free and repeat the process of left clicking on "Code" and logging-in to the GitHub Desktop.

![image](https://user-images.githubusercontent.com/54441806/206072601-60adb60e-19bf-4245-85d4-27e3497e33dd.png)
---------------------------------------------------------------------------------------------------------------
When GitHub Desktop opens, then it will default to looking at the "main" branch.  Switch it to the "{yourname}Dev" branch.

![image](https://user-images.githubusercontent.com/54441806/206074279-9abeab05-935d-456a-8e2c-fa2f417320b7.png)

This repository now exists locally on your computer at:

"{Drive_Letter}:\Users\Public\GitHub\FRC_2022-2023"

Any files that you add, modify, or delete in this directory are compared by GitHub Desktop to what it considers to be the official version of that file.  If there is a difference, GitHub Desktop displays that difference in its window.  For example: In the directory above -- if you were to open the README.md file in a text editor (ex. wordpad), change the spelling of a word, and then save the file in the repository, the GitHub Desktop will change to look like this:

![image](https://user-images.githubusercontent.com/54441806/206082745-758bfe6e-c9ea-4745-9dae-d1e5575a19e8.png)

Any change shown GetHub Desktop window is not considered to be "official" until you commit the change to GitHub.  To commit the change, add a short summary of the change in the summary box above the blue "Commit to {yourname}Dev" button, then click the button.  The change will disappear from the GitHub Desktop window, which means that the local GitHub repository considers the change to now be "official".  To back up the change(s) of your local repository to the Remote Repository on the Web, click on the "Push origin" button at the top of the GitHub Window (make sure that the branch selection shows "{yourname}Dev" before taking this action).

![image](https://user-images.githubusercontent.com/54441806/206085043-25b620a6-297c-477d-adf6-412e7a08d93c.png)

That's it.  Now you can create or open Robot project files in the local repository using the Visual Studio Code editor and after you save them, you can commit them to local Git storage and back them up to the Git remote storage on the Web. 

# Programming Basics

The "Visual Studio Code Basics" hyperlink redirects to a webpage called "Visual Studio Code Basics and WPILib Extension" (https://docs.wpilib.org/en/stable/docs/software/vscode-overview/vscode-basics.html#visual-studio-code-basics-and-the-wpilib-extension), which is part of the "Programming Basics" Tutorial.

Read this page to get familiar with how to call the WPILib command from the command set list.  Click the "Next" button a the bottom of the page to go to next page where a description of each of the WPILib commands is found.  Click the "Next" button to go to the next page, which starts with a discussion on Robot Program and how a Robot Base Class is selected.  Pay particular attention to the "Timed Robot Template". 


# Creating a New Robot Project
  
Eventually, a section called "Creating a New WPILib Project" is found toward the middle of the Robot Program Page (https://docs.wpilib.org/en/stable/docs/software/vscode-overview/creating-robot-program.html).  Perform the tasks stated in your Visual Studio Code application. 

While doing these tasks, a "New Project Creator Window" will pop up.  Select the following on the first row:

Project Type:  Template
Language:      java,
Base:          Timed Robot

Other item on the creator page are filled in as:
Base Folder:  {Drive Letter}:/Users/Public/GitHub/FRC_2022-2023/Robot_Code 
Use the "Select a new project folder" button to graphically select the Base Folder

Project Name: Last_Year,
Team Number:  3660.

Then click on the "Generate Project" button.

Visual Studio will now have a project created in the FRC_2022-2023 Folder called "Last_Year".

After creating the project in Visual Studio Code, continue reading the webpage instructions to end of the page and click the "Next" button to continue to "libraries".

# 3rd Party Libraries

At this point in the process, you should be on the 3rd Party Libraries Page of the Web instructions(https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html). Read down to "Managing VS Code Libraries".  In VS Code, use the "Manage Vendor Libraries > Manage Current Libraries" to show you that the:

WPILib-New-Commands

library is already part of your project.  Note: If your managed libraries are project specific.  If you closed the project, then it must be reopened to show the libraries currently in use.

Pay attention to the "command line" option for installing vendor libraries.  Three-quarters of the way down this page is a list of common vendors and their web pages.

Add the Rev library and the Phoenix Library to your project by:

1. Open a terminal in VS Code from the "View > Terminal" tab.

2. Navigate the directory "<Drive Letter>:\Users\Public\Documents\GitHub\FRC_2022-2023\Robot_Code\Last_Year"

3. Give the following commands at the terminal command prompt:

> ./gradlew vendordep --url=https://software-metadata.revrobotics.com/REVLib.json

>./gradlew vendordep --url=https://maven.ctr-electronics.com/release/com/ctre/phoenix/Phoenix-frc2022-latest.json

Note: these website addresses were valid for the 2022 season.

In VS Code, use the "Manage Vendor Libraries > Manage Current Libraries" to show you 3 libraries are part of the project:

CTRE-Phoenix
RevLib
WPILib-New-Commands

# Copy Last Years Robot Code

Last year's robot code is in the Robot_Code directory.  Go to that directory on your computer, copy the file called "Robot.java", and navigate to your project's "robot" directory:
  
  {Drive_Letter}\Users\Public\GitHub\FRC_2022-2023\Robot_Code\Last_Year\src\main\java\frc\robot

This directory will have the following files it it:

Main.java
Robot.java

If you want to see the differences between the default code for a "Timed Robot" and Last Year's code.  Save the Robot.java file to another name before taking the next step.

Now, paste the file that you copied from the "Robot_Code" directory into the project's robot directory.  This will overwrite the "Robot.java" file in that directory with a new one that contains Last Year's code.

If you copied the default "Timed Robot" code, then delete the file when you are done looking at it. 

# Git Update

Save any open files in the project.  In the GitHub Desktop, commit the changes by typing "Created Project for Last Year's Robot" in the commit summary box and clicking on the "Commit to {yourname}Dev" button. Backup the change to the remote repository by clicking on the "Push Origin" button on the top of the GitHub Desktop window.  You're done.

# Next?

It is now time to build your own Robot Code.  So, go create a new project to do something else.  What might you do?  Check out the examples in:

C:\Users\Public\Documents\GitHub\LS\FRC_2022-2023\allwpilib-main\allwpilib-main\wpilibjExamples\src\main\java\edu\wpi\first\wpilibj\examples 
