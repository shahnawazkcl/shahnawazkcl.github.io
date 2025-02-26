---
layout: post
title: Git and GitHub Notes
description: Notes on git and GitHub revised.
date: 2025-02-26
tags: Git, GitHub

---

# Notes on Git/GitHub Revised P1
## **Git Mastery: From Beginner to Intermediate**  
### **Section 1: Introduction to Git & Version Control**  

#### **What is Git?**  
Git is a **distributed version control system** that allows multiple people to collaborate on code, track changes, and revert to previous versions if necessary.  

#### **Why Use Git?**  
Imagine you are writing a book. Without version control, you might:  
- Save multiple copies like `book_v1.docx`, `book_v2_final.docx`, `book_v3_really_final.docx`.  
- Lose track of what changes were made and when.  
- Have trouble collaborating with co-authors.  

With Git, you:  
✅ Track all changes automatically.  
✅ Roll back to previous versions easily.  
✅ Work with multiple people on the same files.  

#### **Key Concepts**  
| Concept  | Explanation  |
|-----------|-------------|
| **Repository (Repo)** | A Git project, like a folder containing all files and their history. |
| **Commit** | A saved change, like a checkpoint in your project. |
| **Branch** | A separate version of the project that allows independent work without affecting the main version. |
| **Merge** | Combining branches back together. |
| **Remote** | A version of your repository stored online (like GitHub, GitLab, or Bitbucket). |

#### **Installing Git**  
To check if Git is installed, run:  
```sh
git --version
```
If not installed, download it from [git-scm.com](https://git-scm.com/) and follow the installation steps.

#### **Setting Up Git (First Time Only)**  
After installing Git, configure your identity:  
```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
To verify:  
```sh
git config --list
```
---

## **Section 2: Initializing and Managing a Git Repository**  

### **Creating a New Git Repository**  
1️⃣ **Initialize a repository:**  
```sh
git init
```
This creates a hidden `.git` folder, where Git stores all version history.

2️⃣ **Check the status of your repository:**  
```sh
git status
```
This tells you whether files are tracked, untracked, or staged.

3️⃣ **Adding files to tracking:**  
```sh
git add filename.txt
```
or add all files:  
```sh
git add .
```

4️⃣ **Committing changes:**  
```sh
git commit -m "Initial commit"
```
A commit is like a **checkpoint** in your project.

---

### **Real-Life Scenario**  
Imagine you're writing an essay.  
- You **draft** the first version (adding files to Git).  
- You **save a checkpoint** before making big changes (commit).  
- You can **go back** if you make a mistake (Git lets you revert to previous commits).

---
