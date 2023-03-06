<h1> Git - Github study </h1>

<p><i>Just a summary of the most important commands and concepts of Git and Github. My development environment is Windows 11, but after installing Git Bash on a Windows computer, users have the same set of Git commands available as in Git's native environment (a Unix-style system like Linux or macOS).</i></p>

<h1> Table of Contents </h1>

-  [I. Git](#i-git)
   -  [I.1. What is Git?](#i1-what-is-git)
   -  [I.2. Git Installation and Configuration](#i2-git-installation-and-configuration)
      -  [I.2.1. Install Git](#i21-install-git)
      -  [I.2.2. Configure Git](#i22-configure-git)
   -  [I.3. Git terms](#i3-git-terms)
      -  [I.3.1. Repository](#i31-repository)
      -  [I.3.2. Working directory](#i32-working-directory)
      -  [I.3.3. Staging area](#i33-staging-area)
      -  [I.3.4. Commit](#i34-commit)
      -  [I.3.5. Branch](#i35-branch)
      -  [I.3.6. Merge](#i36-merge)
      -  [I.3.8. Fork](#i38-fork)
      -  [I.3.9. Pull request](#i39-pull-request)
      -  [I.3.10. Clone](#i310-clone)
      -  [I.3.11. Push](#i311-push)
      -  [I.3.12. Pull](#i312-pull)
      -  [I.3.13. Fetch](#i313-fetch)
      -  [I.3.14. Remote](#i314-remote)
      -  [I.3.15. Origin](#i315-origin)
      -  [I.3.16. Upstream](#i316-upstream)
      -  [I.3.17. HEAD](#i317-head)
      -  [I.3.18. Master](#i318-master)
      -  [I.3.19. Stash](#i319-stash)
      -  [I.3.20. Tag](#i320-tag)
      -  [I.3.21. Revert](#i321-revert)
      -  [I.3.22. Reset](#i322-reset)
      -  [I.3.23. Checkout](#i323-checkout)
      -  [I.3.24. Diff](#i324-diff)
      -  [I.3.25. Status](#i325-status)
      -  [I.3.26. Log](#i326-log)
   -  [I.4. Git basic command](#i4-git-basic-command)
      -  [I.4.1. git status](#i41-git-status)
      -  [I.4.2. git init](#i42-git-init)
      -  [I.4.3. git add](#i43-git-add)
      -  [I.4.4. git commit](#i44-git-commit)
      -  [I.4.5. git log](#i45-git-log)
      -  [I.4.6. git branch](#i46-git-branch)
      -  [I.4.7. git checkout](#i47-git-checkout)
      -  [I.4.8. git merge](#i48-git-merge)
      -  [I.4.9. git diff](#i49-git-diff)
      -  [I.4.10. git stash](#i410-git-stash)
      -  [I.4.11. git tag](#i411-git-tag)
      -  [I.4.12. git revert](#i412-git-revert)
      -  [I.4.13. git reset](#i413-git-reset)
      -  [I.4.14. git remote](#i414-git-remote)
      -  [I.4.15. git push](#i415-git-push)
      -  [I.4.16. git pull](#i416-git-pull)
      -  [I.4.17. git fetch](#i417-git-fetch)
      -  [I.4.18. git clone](#i418-git-clone)
      -  [I.4.19. git config](#i419-git-config)
      -  [I.4.20. git mv](#i420-git-mv)
      -  [I.4.21. git rm](#i421-git-rm)
      -  [I.4.22. git restore](#i422-git-restore)
-  [II. GitHub](#ii-github)
   -  [II.1. What's the difference between Git and GitHub?](#ii1-whats-the-difference-between-git-and-github)

### 2. [GitHub](#II-github)

---

# I. Git

## I.1. What is Git?

Simplify, Git is a tool that helps developers keep track of changes made to their code. It allows multiple people to work on the same codebase without causing conflicts. It also helps developers undo changes or experiment with new features without affecting the main codebase. Git is widely used in software development because it is flexible, fast, and reliable. There are also many tools and services available that integrate with Git, making it easy to use in various development workflows.

You can think of Git as a time machine that allows you to travel back to previous versions of your code. It also allows you to travel to different timelines, where you can create new versions of your code without affecting the main timeline. This is useful when you want to experiment with new features without affecting the main codebase.

About history of Git, you can check it by yourself [here](https://www.geeksforgeeks.org/history-of-git/).

## I.2. Git Installation and Configuration

### I.2.1. Install Git

You can download Git [here](https://git-scm.com/downloads). After downloading, you can install Git by following the instructions on the screen.

If you have installed Git successfully, you can check the version of Git by typing the following command in your terminal:

```bash
git --version
```

And update Git to the latest version by typing:

```bash
git update-git-for-windows
```

### I.2.2. Configure Git

Config Git is very important. It will help you to identify who you are when you commit changes to the repository. Just open your terminal and type:

```bash
git config --global user.name [your_username]
git config --global user.email [your_email]
```

Example:

```bash
git config --global user.name "Mr Brown"
git config --global user.email browninsuit@gmail.com
```

## I.3. Git terms

### I.3.1. Repository

A repository is a storage space where you can keep all the files related to your project, including code, documentation, and other resources. It's like a folder or directory on your computer, but with additional features that make it easy to manage changes and collaborate with others. In Git, a repository is also known as a "repo" and it tracks changes made to the files in the repository over time. Developers use repositories to manage their code and collaborate with others on the same project.

### I.3.2. Working directory

The working directory is the directory on your local computer where you have your Git repository files stored. It's the directory where you make changes to the files in your repository. When you make changes to files in the working directory, Git detects the changes and allows you to stage and commit them to the repository. In other words, the working directory is the place where you do your work and make changes to your code, while the repository is the place where Git tracks and manages those changes.

### I.3.3. Staging area

In technical terms, the staging area is the middle ground between what you have done to your files (also known as the [working directory](<(#i32-working-directory)>)) and what you had last committed (the [HEAD](#i317-head) commit). As the name implies, the staging area gives you space to prepare (stage) the changes that will be reflected on the next [commit](#i34-commit).

### I.3.4. Commit

In Git, a commit is like taking a picture of the changes you made to your code. When you make changes to your code, you can use the "git commit" command to save those changes to the Git repository. Each commit has a unique identifier that allows you to track the changes you've made over time. This is useful for collaboration, debugging, and keeping track of your project's history.

### I.3.5. Branch

In Git, a branch is a separate line of development that allows you to work on new features or make changes to your code without affecting the main codebase.

When you create a branch, you're essentially creating a copy of the current codebase. You can make changes to the files in the branch without affecting the main codebase. This allows you to experiment with new features or make changes without worrying about breaking the existing code. Once you're done making changes in the branch, you can merge the changes back into the main codebase.

Branches are important in Git because they allow developers to work on multiple features or bug fixes at the same time without interfering with each other. They also allow developers to collaborate on the same codebase without stepping on each other's toes. Overall, branches are a powerful feature in Git that allow developers to work more efficiently and safely.

### I.3.6. Merge

### I.3.8. Fork

### I.3.9. Pull request

### I.3.10. Clone

### I.3.11. Push

### I.3.12. Pull

### I.3.13. Fetch

### I.3.14. Remote

### I.3.15. Origin

### I.3.16. Upstream

### I.3.17. HEAD

### I.3.18. Master

### I.3.19. Stash

### I.3.20. Tag

### I.3.21. Revert

### I.3.22. Reset

### I.3.23. Checkout

### I.3.24. Diff

### I.3.25. Status

### I.3.26. Log

## I.4. Git basic command

### I.4.1. git status

### I.4.2. git init

### I.4.3. git add

### I.4.4. git commit

### I.4.5. git log

### I.4.6. git branch

### I.4.7. git checkout

### I.4.8. git merge

### I.4.9. git diff

### I.4.10. git stash

### I.4.11. git tag

### I.4.12. git revert

### I.4.13. git reset

### I.4.14. git remote

### I.4.15. git push

### I.4.16. git pull

### I.4.17. git fetch

### I.4.18. git clone

### I.4.19. git config

### I.4.20. git mv

### I.4.21. git rm

### I.4.22. git restore

---

# II. GitHub

## II.1. What's the difference between Git and GitHub?

Git and GitHub are related but distinct tools.

Git is a distributed version control system that allows developers to keep track of changes to their code and collaborate with others. It's a command-line tool that runs on your local computer and manages the changes to your code.

GitHub, on the other hand, is a web-based platform that provides hosting for Git repositories. It allows developers to store their Git repositories on GitHub's servers and collaborate with others on their projects. GitHub provides a user-friendly interface for managing Git repositories, as well as features like pull requests, issue tracking, and project management tools.

In summary, Git is a tool for managing code changes locally, while GitHub is a web-based platform that provides hosting for Git repositories and collaboration tools. While Git can be used independently of GitHub, GitHub relies on Git as its underlying technology.
