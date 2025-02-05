# Git & Github tutorial 
here's a simple, yet useful tutorial of git & github to get started with

## What is Git & GitHub?

- **Git**: A software used for version control. It helps you save changes to your code and revert to previous versions when needed. Think of it as a notebook for tracking code changes.

- **GitHub**: A website that allows you to store code managed with Git online and share it with others. It’s like a social network for developers, where they can collaborate on projects.

## Table of contents

- [1. Installing Git on Windows](#installing-git-on-windows)
- [2. Basic Git Concepts](#basic-git-concepts)
- [3. Creating, Editing, and Cloning a Repository](#creating-editing-and-cloning-a-repository)
- [4. Managing codes with github branch](#Managing-codes-with-github-branch)
- [5. Installing and Running Git on Linux Terminal](#installing-and-running-git-on-linux-terminal)
- [6. Creating a PAT for Your Account](#creating-a-pat-for-your-account)
- [7. Cloning a repository using the PAT](#Cloning-a-repository-using-the-PAT)
- [8. List of Essential Git Commands](#list-of-essential-git-commands)
- [9. Editing the README](#editing-the-readme)
- [10. Using Git in VSCode](#using-git-in-vscode)

![logo](images/github-color.svg)

## Installing Git on windows

Follow these steps to install Git on Windows:

1. Search for "Git" in your browser and download the Windows version from [Git's official website](https://git-scm.com/downloads).
2. Run the downloaded installer, accept the default settings (they can be modified later if needed), and complete the installation.
3. Search for "GitHub Desktop" in your browser, download it from [GitHub’s official site](https://desktop.github.com/download/), and install it.
4. Open the Command Prompt (CMD) and type `git`. If you see details about the Git command, it means Git has been installed successfully.

> **Note:** Git has several essential commands for project control. However, on Windows, you can use GitHub Desktop's graphical interface instead of the command line. Regardless, understanding Git commands is important, as covered in the Linux section below.

## Basic git concepts

- **Repository (Repo):** A folder that stores all code and change history, similar to an archive that keeps all files and previous versions. Repositories are usually created on GitHub and changes are stored online.
- **Clone:** A command to copy a repository from GitHub to your local system. The copied folder remains linked to GitHub, allowing updates and modifications.
- **Commit:** Saves changes in the repository. Each commit is like a snapshot of the files at a specific moment, enabling you to revert to that point later.
- **Push:** Uploads committed changes from your computer to GitHub for sharing.
- **Pull:** Downloads the latest changes from an online repository to your computer to stay in sync.
- **Branch:** An independent path for making changes without affecting the main code. You can experiment with changes in a branch before merging them with the main branch.

> **Tip:** The difference between `commit` and `push` is that `commit` only saves changes locally, whereas `push` shares them on GitHub. Similarly, `fetch` retrieves updates from GitHub without modifying local files, while `pull` updates the local files as well.

## Creating, editing, and cloning a repository

on github:
1. Create a GitHub account and log in.
2. On the homepage, view the list of repositories on the left. Click **New** to create a new repository.
3. Choose a repository name, set it as **public** or **private**, check **Add a README.md**, and create the repository.
4. You can also join repositories created by others and collaborate on projects.
5. Open GitHub Desktop, log in, and link your GitHub account.
6. Select a repository and **clone** it to a specific location on your computer.
7. Now, you have the project repository on your local system and can manage changes through GitHub Desktop.

![desktop](images/1.png)

on local machine: 
1. create a folder and open it
2. open cmd(or terminal) on that path and enter `git init`
3. add files and use `git add .` for git to recognize the files
4. commit using `commit -m "message"`
5. open github and create a github repository and copy its URL
6. add the remote repo using `git remote add origin https://github.com/your-username/repository.git`
7. push the changes using `git push -u origin main`

   




## Managing codes with Github branch

Repositories in GitHub have a default **main** branch. as you work on your code, there are many times where you need to organize your workspace into multiple seprated workspaces where you can work on diffrent aspects of the code, or when you simply want to modify the code for new features without actually changing the main code. that's when you need to create new branches and source it to an older branch so all the files from that branch is copied to the new workspace. Additional branches can be created for better organization. The purpose of multiple branches is to test and apply changes in a separate environment without directly modifying the main files.
For example, if 3 developers are working on the same program, first developer wants rewrite the code and make it cleaner, second developer wants to add and test some new features and third developer wants to write a modulated library for the program. it is not so hard to tell that these three developers can't directly modify the main program or work on the same files. so they simply create some other branches and work separately and at the end, they can merge they changes to the main program.

Keeping branches well-organized ensures better collaboration and readability.

```sh
git branch <branch name> # to create a new branch
git checkout <branch name> # to switch between branches
git checkout -b <branch name> #to create and switch to a new branch
git branch # to list all the branches
git branch -m <old branch name> <new branch name> #rename a branch
git push origin --delete <branch name> # delete a branch from remote
git push -u origin <branch name> #add a branch to remote
git merge <branch name> #merge a branch to the current branch which is usaully main or master branch
```

## Installing and Running Git on Linux Terminal

For Debian-based Linux distributions, open the terminal and install Git with:

```sh
sudo apt update
sudo apt install git
```

After installation, verify it with:

```sh
git --version
```

To configure your username and email for commits:

```sh
git config --global user.name "username"
git config --global user.email "email@example.com"
```

## Creating a PAT for Your Account

To clone a repository, your Git account must be authenticated. On Linux, authentication with a username and password is not allowed, so you need a **Personal Access Token (PAT)**.

1. Click your profile picture on GitHub, then go to **Settings**.
2. Scroll down and click **Developer Settings**.
3. Select **Personal Access Tokens > Generate New Token (Classic)**.
4. Set a token name and enable necessary permissions.
5. Generate the token and **store it securely** as it won't be shown again.

## Cloning a repository using the PAT

1. On GitHub, open the repository and copy its URL (format: `https://github.com/user/repository`).
2. Open your Linux terminal and navigate to your desired directory using `cd`.
3. Use the following command, replacing `<username>` with your GitHub username and `<PAT>` with your token:

```sh
git clone https://<username>:<PAT>@github.com/user/repository
```

This clones the repository to your system, allowing you to pull, commit, and push changes.

---
This guide provides a complete introduction to Git and GitHub. Refer to each section for detailed explanations of installation, repository management, and working with branches.

