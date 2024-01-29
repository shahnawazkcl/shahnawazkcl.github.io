---
layout: post
title: Git and GitHub Notes
description: Notes on git and GitHub.
date: 2022-07-12
tags: Git, GitHub
---

# Notes on Git/GitHub

Before going into the details of this you are here for a disclaimer:

> Disclaimer: If you are an expert in any of the concepts, steps or terms discussed here, then please do comment or correct me. Although here my only goal is to make and keep it __simple__.  

So, the first questions is 
> **What is Git !:** It's free an Open Source version control system. That manges and stores any changes made to the document/code through its developments.  
> **Git** is the tool and **GitHub** is a website where you host all of your repositories (in short _repo_. aka Project folders).  

<center><h2>Phew....! </h2></center>

Now some **Git commands** that one uses to interact all the time, can be typed into your terminal or git bash.
* **clone**: Brings a _repos_ that is hosted on Github for instance on to yoor local machine.
* **add**: Track ur files and changes in Git.
* **commit**: Save all your changes/files in git.
* **push**: it uploads git commit from local to a remote repo, i.e. GitHub.
* **pull**: downloads all the changes made in remote repo before you push your changes.

> Note task: if you don't have GitHub account [Sign up](https://github.com/) for it. and Create your first repo. Add readme file to describe the project.  

## Some installations:
Before going forward lets do some setups:
* install git [read this article how to](https://www.atlassian.com/git/tutorials/install-git).
* Install any code editor: it could be visual studio code (vscode) or Pycharm or as simple as Notepad++. My recommendation is to get [vscode](https://code.visualstudio.com/).

## Inside vscode: 
Simple tasks to get you started with some basic Git commands.
### Starting with GitHub
* **task `clone`:** go to the explorer open an empty folder and then go to view &rarr; terminal. now pulldown the repo created on GitHub. using the command `git clone git@github.com:username/demo_1.git.git`.
* **task:** Now open the readme file you created and make some changes that is to say write your guts out since this is a markdown file consider it as simple text editor.
* **task `status`:** once made changes to any file and before saving in git (i.e. commit) we use `git status` command to see what files have been modified.
* **task `add`:** lets say you added one file _hello.py_ to the local repo then again type `git status` it will show one modified file and one untracked file because the file we created git doesn't know about that so before committing our changes we add this file to git tracking by typing `git add .`.
* **task `commit`:** Once sure to commit the changes type `git commit -m 'some msg to the commit -m "some description"`.
* **Task `push`:** once done with modification and commits just make it **public** on GitHub using `git push origin master`.

<center><h2>Take a Break...</h2></center>

### Starting with a local folder/directory
* **Task:** create a folder named '_demo_2_' and add `readme.md` file again write the gut.
* **Info:** Since this folder is not a GitHub repo we will make it one using `git init` command, **init** means initialization.
* **task `init`:** so type `git init` inside the terminal hit enter. there you go you initialized or made a normal folder into git repo.
* **task:** track all the files in the folder and commit the changes use `add` and `commit` as above. 
* **Info:** Finally. we want to push this repo live on GitHub As we have created this repo locally we first need a repo with same name on GitHub you guessed it write _not straight forward_.
* Easy way `remote`: create a repo *demo_2* on GitHub and type in terminal `git remote add origin git@github.com:username/demo_2.git`, this command creates a connection between remote and local repo.
* Now simply say `git push -u origin master` **-u** set upstream option.

## Git branching
Commands we will be using are `merge`, `checkout`, `branch`, `diff`.  
Types of Branches
* **master/main branch**:
* **feature branch**:
* **Hot fix branch (for bug fixes)**:
* **Task `branch and checkout` **: create a branch and switch between them.
> `git branch`: to see how many branches we have.  
> `git checkout -b namebranch`: create new branch (with -b) or switch branch (without -b option).  

What is **Staging**: it simply means to add the modified file or changes using `git add filename or .`. meaning _staging_ the changes made in another branch before merging.  

* **Task `diff`:** To see the changes between branches first switch to the master then type `git diff namebranch`. 
* **Task `merge`:** type `git merge namebranch`. to merge all the changes in the `namebranch` to `master`.  

> __Pull Request__ (aka PR): it's a request to be made for approval to the owner of the repo that merges the changes made by anyone working on the same project. after which the feature or hotfix branch is deleted. This process is repeated for more changes.

* **Task `PR`:** after creating and merging PR online on GitHub in terminal type `git pull`. to pull all the changes in the `master` branch locally.
* **Task `delete (-d)`:** after pulling all the changes in the `master` branch type `git branch -d namebranch` to delete that feature branch we don't need anymore.  

<center><h2>that was intense __Take a Break__. </h2></center>


### What are merge conflicts and how to deal with them.
Merge conflicts can arrive when you want to push changes into the master or any branch on which someone else has already committed that means u don't have the current version of master branch. There are many ways fix that based on the case/situation you are in more on that in **my next post**.  

>**Stash changes:** Save ur changes to a temporary holding place. 

### Undoing changes in Git.
* undo changes in file: `git reset namefile`
* undo last commit unstage: `git reset HEAD~1` the number is how many steps back or use hash `git reset hash`.
* To remove all the commits no unstaging: `git reset --hard`. with or without hash.
* To see the log of all commits: `git log`.

### Forking:
Making a copy of the repo to your personal account of any other repo on GitHub. Thus, you have complete control over this repo and can commit changes in this repo.

Next _Post_ will in more detail about the following:
* merge conflicts
* resetting or undoing changes in git.
* Forking.

<center><h1>Happy Git-ing</h1></center>
