# Git & Github tutorial 
here's a simple, yet useful tutorial of git & github to get started with

## What is Git & GitHub?

- **Git**: A software used for version control. It helps you save changes to your code and revert to previous versions when needed. Think of it as a notebook for tracking code changes.

- **GitHub**: A website that allows you to store code managed with Git online and share it with others. It’s like a social network for developers, where they can collaborate on projects.

## Table of Contents

- [0. Key Takeaways](#key-takeaways)
- [1. Installing Git on Windows](#installing-git-on-windows)
- [2. Basic Git Concepts](#basic-git-concepts)
- [3. Creating, Editing, and Cloning a Repository](#creating-editing-and-cloning-a-repository)
- [4. Project Organization with Branches](#project-organization-with-branches)
- [5. Installing and Running Git on Linux Terminal](#installing-and-running-git-on-linux-terminal)
- [6. Creating a PAT for Your Account](#creating-a-pat-for-your-account)
- [7. Adding a Repository to Your System Using Clone](#adding-a-repository-to-your-system-using-clone)
- [8. List of Essential Git Commands](#list-of-essential-git-commands)
- [9. Editing the README](#editing-the-readme)
- [10. GitHub Project Options](#github-project-options)
- [11. Using Git in VSCode](#using-git-in-vscode)

![logo](images/github-color.svg)

## Key Takeaways

Here are the key steps summarized. If you encounter any issues, refer to the corresponding section for detailed explanations:

1. Install Git and GitHub Desktop (If using Linux, refer to sections 5, 6, 7, and 8).
2. Clone the project repository to a designated folder in GitHub Desktop.
3. Switch to the relevant branch in GitHub Desktop (top of the screen).
4. Upload or edit your files in the cloned folder. Ensure that GitHub Desktop recognizes the changes.
5. When committing and pushing changes, include appropriate descriptions in the commit message.
6. Before starting work, always use the **Fetch Origin** option in GitHub Desktop to ensure your branch is up to date.
7. Maintain organized branches for easier analysis and collaboration.
8. If required by the project manager, update the `README.md` file alongside your code and files, as documentation is essential for the project's continuity (refer to section 9 for README editing instructions).

## Installing Git on Windows

Follow these steps to install Git on Windows:

1. Search for "Git" in your browser and download the Windows version from Git's official website.
2. Run the downloaded installer, accept the default settings (they can be modified later if needed), and complete the installation.
3. Search for "GitHub Desktop" in your browser, download it from GitHub’s official site, and install it.
4. Open the Command Prompt (CMD) and type `git`. If you see details about the Git command, it means Git has been installed successfully.

> **Note:** Git has several essential commands for project control. However, on Windows, you can use GitHub Desktop's graphical interface instead of the command line. Regardless, understanding Git commands is important, as covered in the Linux section below.

## Basic Git Concepts

- **Repository (Repo):** A folder that stores all code and change history, similar to an archive that keeps all files and previous versions. Repositories are usually created on GitHub and changes are stored online.
- **Clone:** A command to copy a repository from GitHub to your local system. The copied folder remains linked to GitHub, allowing updates and modifications.
- **Commit:** Saves changes in the repository. Each commit is like a snapshot of the files at a specific moment, enabling you to revert to that point later.
- **Push:** Uploads committed changes from your computer to GitHub for sharing.
- **Pull:** Downloads the latest changes from an online repository to your computer to stay in sync.
- **Branch:** An independent path for making changes without affecting the main code. You can experiment with changes in a branch before merging them with the main branch.

> **Tip:** The difference between `commit` and `push` is that `commit` only saves changes locally, whereas `push` shares them on GitHub. Similarly, `fetch` retrieves updates from GitHub without modifying local files, while `pull` updates the local files as well.

## Creating, Editing, and Cloning a Repository

1. Create a GitHub account and log in.
2. On the homepage, view the list of repositories on the left. Click **New** to create a new repository.
3. Choose a repository name, set it as **public** or **private**, check **Add a README.md**, and create the repository.
4. You can also join repositories created by others and collaborate on projects.
5. Open GitHub Desktop, log in, and link your GitHub account.
6. Select a repository and **clone** it to a specific location on your computer.
7. Now, you have the project repository on your local system and can manage changes through GitHub Desktop.

![desktop](images/1.png)

## Project Organization with Branches

Repositories in GitHub have a default **main** branch. Additional branches can be created for better organization. The purpose of multiple branches is to test and apply changes in a separate environment without directly modifying the main files.

For example, if a developer is working on `control.cpp`, they can create a **test** branch, apply changes, and test them separately. Once satisfied, they can merge the changes into the **main** branch.

Keeping branches well-organized ensures better collaboration and readability.

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

## Adding a Repository to Your System Using Clone

1. On GitHub, open the repository and copy its URL (format: `https://github.com/user/repository`).
2. Open your Linux terminal and navigate to your desired directory using `cd`.
3. Use the following command, replacing `<username>` with your GitHub username and `<PAT>` with your token:

```sh
git clone https://<username>:<PAT>@github.com/user/repository
```

This clones the repository to your system, allowing you to pull, commit, and push changes.

---
This guide provides a complete introduction to Git and GitHub. Refer to each section for detailed explanations of installation, repository management, and working with branches.

