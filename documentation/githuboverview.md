# Git and GitHub Overview

## Prerequisites

Prior to using GitHub in this repository, you will need to:

- **GitHub account** - [Register Here](https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)
- **Git Client** - Install a git client such as [GitHub Desktop](https://desktop.github.com/) or [Visual Studio Code](https://code.visualstudio.com/) with [necessary extensions](https://code.visualstudio.com/docs/sourcecontrol/github)

## Objectives

- [Introduction](#introduction)
- [Git and GitHub](#git-and-github)
- [GitHub Workflow](#github-workflow)
- [GitHub Issues](#issues)
- [GitHub Pull Requests](#pr)

- [Ontology Development Workflows](#workflow)


- [Open Source Etiquette](#etiquette)
- [Further Resources](#resource)


<a name="introduction"></a>

## Introduction

The content of this file is adapted from the Github Classroom starter assignment, which is designed to give you a brief introduction to Git and GitHub. 

<a name="git-and-github"></a>

## Git and GitHub

**Git** is a system for tracking changes to your code, collaborating, and sharing. With Git you can track the changes you make to your project so you always have a record of what you’ve worked on and can easily revert back to an older version if need be. 

**GitHub** is a web-based platform that builds on Git, by adding an intuitive interface, automating workflow actions, and allowing for transparent communication around projects. 

<a name="github-workflow"></a>

## GitHub Workflow 

The **GitHub Flow** is a workflow that allows you to experiment and collaborate on your projects easily, without the risk of losing your previous work. 

A **repository** is where your project work happens--think of it as your project folder. It contains all of your project’s files and revision history.  You can work within a repository alone or invite others to collaborate with you on those files. Repositories also contain **README**s, which are used to explain to other people why your project is useful, what they can do with your project, and how they can use it. 


A README is a text file that introduces and explains a project. It is intended for _everyone_, not just the software or ontology developers. Ideally, the README file will include detailed information about the ontology, how to get started with using any of the files, license information and other details. The README is usually on the front page of the GitHub repository.


Git repositories typically have a main branch that is not directly edited. Changes are made by creating a **branch** from main, which is essentially a complete copy of the main branch along with its entire history of updates.




You can copy (fork) any GitHub repo to some other location on GitHub without having to ask permission from the owners.  If you modify some files in that repo, e.g. to fix a bug in some code, or a typo in a document, you can then suggest to the owners (via a Pull Request) that they adopt (merge) you your changes back into their repo.

If you have permission from the owners, you can instead make a new branch. For this training, we gave you access to the repository. See the [Appendix](../howto/github-create-fork.md) for instructions on how to make a fork.




When a repository is created with GitHub, it’s stored remotely in the cloud. You can **clone** a repository to create a local copy on your computer and then use Git to sync the two. This makes it easier to fix issues, add or remove files, and push larger commits. Cloning a repository pulls down all the repository data that GitHub has at that point in time, including all versions of every file and folder for the project. This can be helpful if you experiment with your project and then realize you liked a previous version more. 

A **fork** is another way to copy a repository, but is usually used when you want to contribute to someone else’s project. Forking a repository allows you to freely experiment with changes without affecting the original project and is very popular when contributing to open source software projects.

**Committing** and **pushing** are how you can add the changes you made on your local machine to the main course repository so that your instructor can see your latest work. You should add a helpful **commit message** to remind yourself or your teammates what work you did. Once you have a commit or multiple commits that you’re ready to add to your repository, you can use the push command to add those changes to your remote repository. 

When working with branches, you can use a **pull request** to tell others about the changes you want to make and ask for their feedback. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add more changes if need be. You can add specific people as reviewers of your pull request which shows you want their feedback on your changes! Once a pull request is ready-to-go, it can be merged into your main branch.

**Issues** are a way to track enhancements, tasks, or bugs for your work on GitHub. Issues are a great way to keep track of all the tasks you want to work on for your project and let others know what you plan to work on. 

## Github Workflow 

To illustrate, suppose you want to edit a file from the Common Core Ontologies GitHUb. You should then 'fork' the develop branch of the CCO repository on your personal Github account, so that you can make whatever changes you like.  

When you make changes to your personal Github CCO repository then go to save them in GitHub, you will be prompted to either "commit to the main branch' or "create a new branch for this request and start a pull request". You should almost always open a 'pull request'. By opening a pull request, you open the door for your peers to help you refine the submission. That in mind, when you open a pull request, it is good practice to tag others and request they review your work. Once your reviewers have 'approved' your work, you will then 'merge' your work to your personal repository. 

Once you have merged your work there, you will open another pull request - this time tagging one of the lead CCO developers - so they can review your work before merging it to the develop branch of CCO. Over time, when sufficient updates have been made to CCO, the develop branch will be merged into the main branch, triggering a new release of CCO. 

You can visualize the process as something like:  

```mermaid
    gitGraph
       commit id: "1"
       commit id: "2"
       branch Your_Work
       checkout Your_Work
       commit id: "3"
       checkout main
       commit id: "4"
       checkout Your_Work
       branch Your_Work_in_PR
       commit id: "5"
       checkout Your_Work
       merge Your_Work_in_PR id: "Reviewed!"
       checkout main
       merge Your_Work id: "Submit Work"
       commit id: "6"
       checkout main
       commit id: "7"
  ```
Where the numbers instances where changes have been made to a repository. The top grey line represents the main course repository. At change - or 'commit' - 2, you create a copy of the repository and begin working. You periodically check to make sure that your copy is up to date with the main branch, and this is reflected in your making commit 3 then making commit 5. This is because commit 4 occurred on the main branch, but you - good student that you are - updated your personal repository to keep up with the main course repository. Eventually, you submit your work to the main branch and it is 'merged'. Afterwards, you'll be able to see your work on the main course repository. 



<a name="workflow"></a>

### CCO Development Workflow

The steps below describe how to make changes to Common Core Ontologies content.

1. Clone the CCO GitHub repository. The example below describes how to clone the Mondo Disease Ontology repo, but this can be applied to any ontology that is stored in GitHub.

#### Clone the CCO Repository

1.  Navigate to the [Common Core Ontologies repository](https://github.com/CommonCoreOntology/CommonCoreOntologies)
2.  Click Code

![image](https://user-images.githubusercontent.com/6722114/116610830-801b0480-a8ea-11eb-8567-9da0c1159954.png)

3. Click 'Open with GitHub Desktop'

![image]()

4. You will be given an option as to where to save the repository. Consider creating a folder on your local device named "Git" or "Repos", which will be the home for any repositories you save locally.
5. This will open GitHub Desktop and the repo should start downloading. This could take some time depending on how big the file is and how much memory your computer has.

#### Create a branch using GitHub Desktop

6. Click the little arrow in Current Branch
7. Click New Branch
8. Give your branch a name: 

![image]()



## GitHub Pull Requests (adapted from OBOOK)

### Committing, Pushing and Making Pull Requests

1.  Changes made to the ontology can be viewed in GitHub Desktop.

2.  Before committing, check the diff. Examples of a diff are pasted below. Large diffs are a sign that something went wrong. In this case, do not commit the changes and ask the ontology editors for help instead.

Example 1:

![]()

1.  Commit: Add a meaningful message in the Commit field in the lower left, for example

NOTE: You can use the word 'fixes' or 'closes' in the description of the commit message, followed by the corresponding ticket number (in the format #1234) - these are magic words in GitHub; when used in combination with the ticket number, it will automatically close the ticket. Learn more on this GitHub Help Documentation page about [Closing issues via commit messages](https://help.github.com/en/articles/closing-issues-using-keywords).

1.  Note: 'Fixes' and "Closes' are case-insensitive.

2.  If you don't want to close the ticket, just refer to the ticket # without the word 'Fixes' or use 'Adresses'. The commit will be associated with the correct ticket but the ticket will remain open. NOTE: It is also possible to type a longer message than allowed when using the '-m' argument; to do this, skip the -m, and a vi window (on mac) will open in which an unlimited description may be typed.

3.  Click Commit to [branch]. This will save the changes to the cl-edit.owl file.

4.  Push: To incorporate the changes into the remote repository, click Publish branch.




<a name="etiquette"></a>

## Open Source Etiquette

- Be respectful in your requests and comments.
- Do not include any private information.
- GitHub sends notifications to your email, and you can respond via your email client. However, responses are posted publicly. Be sure to delete your email signature if it includes personal information, such as your phone number.
- Many ontologies have limited resources and personnel for development and maintenance. Please be patient with your requests.
- If your ticket/request has been unanswered for a long period of time, you may check in by commenting on the ticket.

<a name="resources"></a>

##  Resources 
* [A short video explaining what GitHub is](https://www.youtube.com/watch?v=w3jLJU7DT5E&feature=youtu.be) 
* [Git and GitHub learning resources](https://docs.github.com/en/github/getting-started-with-github/git-and-github-learning-resources) 
* [Understanding the GitHub flow](https://guides.github.com/introduction/flow/)
* [How to use GitHub branches](https://www.youtube.com/watch?v=H5GJfcp3p4Q&feature=youtu.be)
* [Interactive Git training materials](https://githubtraining.github.io/training-manual/#/01_getting_ready_for_class)
* [GitHub's Learning Lab](https://lab.github.com/)
* [Education community forum](https://education.github.community/)
* [GitHub community forum](https://github.community/)







# Merging Branches

## Merging Branches in VS Code Using the Command Palette

1. **Open VS Code**: Launch Visual Studio Code.

2. **Open the Command Palette**:
   - Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac) to open the Command Palette.

3. **Switch to the `master` (or `main`) Branch**:
   - Type `Git: Checkout to...` and select it from the dropdown.
   - Choose `master` or `main` from the list of branches.

4. **Pull the Latest Changes (Optional but Recommended)**:
   - Open the Command Palette again.
   - Type `Git: Pull` and select it from the dropdown.
   - Choose the remote branch you want to pull changes from, typically `origin/master` or `origin/main`.

5. **Merge the `dev` Branch into `master` (or `main`)**:
   - Open the Command Palette.
   - Type `Git: Merge Branch...` and select it.
   - Choose `dev` from the list of branches to merge into the currently checked-out branch (`master` or `main`).

6. **Resolve Any Merge Conflicts**:
   - If there are conflicts, VS Code will show them in the editor. Open the conflicted files.
   - Use the inline merge conflict resolution tools provided by VS Code to resolve the conflicts.

7. **Commit the Merge**:
   - If conflicts were resolved, go to the Source Control view to commit the merge.

8. **Push the Changes**:
   - Open the Command Palette.
   - Type `Git: Push` and select it to push the changes to the remote repository.


## Merging Branches in VS Code Using Source Control View

1. **Open VS Code**: Launch Visual Studio Code.

2. **Open the Source Control View**:
   - Click on the Source Control icon in the [Activity Bar](https://code.visualstudio.com/docs/getstarted/userinterface) on the side of the window, or press `Ctrl+Shift+G` (Windows/Linux) or `Cmd+Shift+G` (Mac).

3. **Switch to the `master` (or `main`) Branch**:
   - Click on the branch name in the bottom-left corner of the Status Bar.
   - Select `master` or `main` from the list of branches to switch to it.

4. **Pull the Latest Changes (Optional but Recommended)**:
   - Click on the ellipsis (`...`) in the Source Control view.
   - Select `Pull` from the dropdown to fetch the latest changes from the remote repository.

5. **Merge the `dev` Branch into `master` (or `main`)**:
   - Click on the ellipsis (`...`) in the Source Control view.
   - Select `Merge Branch...`.
   - Choose `dev` from the list of branches to merge into the currently checked-out branch (`master` or `main`).

6. **Resolve Any Merge Conflicts**:
   - If there are conflicts, VS Code will highlight them in the editor. Open the conflicted files and use the inline tools to resolve them.

7. **Commit the Merge**:
   - If conflicts were resolved, you will see the merge changes in the Source Control view. Enter a commit message and commit the merge.

8. **Push the Changes**:
   - Click on the ellipsis (`...`) in the Source Control view.
   - Select `Push` to push the merged changes to the remote repository.


## Merging Branches Using Git in the Command Line

1. **Open Terminal and Navigate to Your Repository**:
   - cd /path/to/your/repo

2. **Fetch the Latest Changes from Remote (Optional but Recommended)**:
   - git fetch origin

3. **Switch to the Master (or Main) Branch**:
   - git checkout master (or git checkout main)

4. **Pull the Latest Changes to Master (or Main)**:
   - git pull origin master (git pull origin main)

5. **Merge the Dev Branch into Master (or Main)**:
   - git merge dev

6. **Resolve Any Merge Conflicts (If They Arise)**:
   - Open conflicted files in a text editor and resolve conflicts.
   - After resolving conflicts, add the resolved files:
   - git add <file>

7. **Complete the Merge if There Were Conflicts**:
   - git commit

8. **Push the Changes to the Remote Repository**:
   - git push origin master (git push origin main)