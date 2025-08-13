# GitHub Repository Usage Tutorial 
RE||ƎЯ, 2025/8/13

## Table of Contents
  - [Introduction](#introduction)
  - [Cloning](#cloning)
  - [Branching](#branching)
  - [Commiting](#commiting)
  - [Pushing](#pushing)
  - [Pulling](#pulling)
  - [Issues](#issues)
  - [Collaboration](#collaboration)
  - [Maintenance](#maintenance)
  - [Conclusion](#conclusion)

---

## Introduction

- This tutorial will walk you through the steps of using a GitHub repository. 
- Whether you're contributing to a project, managing a repository, or collaborating with teammates, these guidelines will help you navigate and utilize GitHub repositories effectively.

---

## Cloning

Cloning a repository means creating a copy of it on your local machine so you can make changes and interact with it.

### Steps to Clone a Repository:
1. **Go to the Repository**:
   Navigate to the GitHub repository page you want to clone (e.g., `https://github.com/username/repository`).
   
2. **Copy the Clone URL**:
   - On the repository page, click the green "Code" button.
   - Copy the URL from the dropdown menu (e.g., `https://github.com/username/repository.git`).

3. **Clone Using Git**:
   Open your terminal (or Git Bash) and run the following command:
   
   ```bash
   git clone https://github.com/username/repository.git
   ```

4. **Navigate to the Repository Folder**:
   Once cloned, navigate to the repository directory:

   ```bash
   cd repository
   ```

---

## Branching

Branching allows you to work on different features or bug fixes in isolation without affecting the main codebase.

### Common Git Branching Workflow:
1. **Main Branch**:
   The main branch contains the stable production-ready code.

2. **Develop Branch**: 
   The develop branch is where features and fixes are integrated before being merged into main.

3. **Feature Branches**: 
   When working on a new feature or bug fix, create a new branch from develop (or main).

### Create a New Branch:
   - To create a new branch, run the following command:
   ```bash
   git checkout -b feature/my-new-feature
   ```
   - Replace feature/my-new-feature with a descriptive branch name related to the task you're working on.

---

## Changing

After you've created a branch, make the necessary changes to the files in the repository.

1. Open files in your preferred code editor (e.g., VSCode, Sublime Text).

2. Modify, add, or delete code as required.

---

## Commiting

Once you've made changes to files, it's important to commit them with clear, descriptive messages.

### Steps to Commit Changes:

1. **Check the Status**:
   To see which files have been changed, use:
   ```bash
   git status
   ```
   
2. **Stage Changes**:
   To stage your changes for commit, run:
   ```bash
   git add <file-name>
   ```
   To add all modified files:
   ```bash
   git add .
   ```
   
3. **Commit the Changes**:
   Once your changes are staged, commit them with a meaningful message:
   ```bash
   git commit -m "Add new feature: user authentication"
   ```
   - Use a present-tense, concise message that describes the change (e.g., `Fix bug in login functionality`).
   
---

## Pushing

After committing your changes, you need to push them to the remote repository on GitHub.

### Push the Changes to GitHub:

```bash
git push origin feature/my-new-feature
```
This will push your local branch to GitHub.

---

## Pulling

A Pull Request (PR) is used to propose changes from your branch to another branch (usually `develop` or `main`).

### Steps to Create a Pull Request:

1. **Go to the Repository on GitHub.**
   - Navigate to the repository page where you pushed your branch.

2. **Create a Pull Request**:
   - GitHub will automatically prompt you to create a pull request for any branch you've pushed.
   - Click the "Compare & pull request" button.

3. **Fill out the PR Form**:
   - Provide a descriptive title and a summary of the changes you’ve made.
   - Select the base branch (usually `develop` or `main`) and compare it to your branch.

4. Request Reviewers:
   - You can assign reviewers to look over your code and approve the changes.

5. Submit the Pull Request:
   - Once you're ready, click the "Create pull request" button.
   
---

## Issues

GitHub Issues allow you to track bugs, feature requests, and other tasks.

### Steps to Work with Issues:

1. **View Issues**:
   - Navigate to the repository's "Issues" tab to see existing issues.

2. **Create a New Issue**:
   - Click "New Issue" and fill out the title and description.
   - You can assign labels (e.g., `bug`, `enhancement`), assign the issue to someone, and set a milestone.

3. **Comment and Update Issues**:
   - Leave comments on issues to ask questions or provide updates.
   - If you resolve an issue, you can close it by clicking "Close Issue" on the issue page or referencing it in your commit message (e.g., `Fixes #123`).

4. **Link Issues to Pull Requests**:
   - In your PR description, you can mention issues by including `Fixes #issue_number` to automatically close an issue when the PR is merged.
   
---

## Collaboration

1. **Keep Pull Requests Small**: 
   Keep your PRs focused and small. This makes it easier for reviewers to provide feedback and approve changes.

2. **Write Clear Commit Messages**: 
   Each commit should represent a single logical change. Write concise, meaningful commit messages.

3. **Test Locally**: 
   Before pushing changes or submitting a PR, test your changes locally to ensure they work as expected.

4. **Use GitHub Actions for CI/CD**: 
   Set up automated workflows to run tests, linters, and deploy your code when changes are pushed.

---

## Maintenance

1. **Update Dependencies Regularly**:
   - Regularly run `npm update` (or equivalent commands for other package managers) to keep dependencies up to date.
   - Use **Dependabot** to automate dependency updates.

2. **Tag Releases**:
   - Use tags to mark stable versions of your code with a version number (e.g., `v1.0.0`).

3. **Clean Up Stale Branches**:
   - After merging a PR, delete the feature branch both locally and on GitHub to keep the repository clean.
   - **Delete a local branch**:
   ```bash
   git branch -d feature/my-new-feature
   ```
   - **Delete a remote branch**:
   ```bash
   git push origin --delete feature/my-new-feature
   ```
   
---

## Conclusion

- Now that you know how to use a GitHub repository, you're ready to collaborate, contribute, and manage your code effectively. 
- Remember, communication and clear documentation are key to maintaining an efficient and smooth workflow. Happy coding!