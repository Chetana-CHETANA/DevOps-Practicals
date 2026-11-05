# Practical 02: Fetching and Synchronizing a Git Repository

## 1. Aim
To clone a GitHub repository, fetch remote changes, and synchronize the local repository.

## 2. Requirements
- Git
- GitHub
- VS Code
- Internet Connection

## 3. Theory
Fetching downloads information about changes from a remote repository, whereas pulling downloads and integrates the latest changes into the local repository.

## 4. Procedure
Step 1: Open GitHub and copy the repository URL.

Step 2: Clone the remote repository.

Step 3: Make changes in the remote repository on GitHub.

Step 4: Fetch the remote changes.

Step 5: Pull the latest changes into the local repository.

Step 6: Verify synchronization.

## 5. Commands
```bash
git clone https://github.com/USERNAME/DevOps-Practicals.git

cd DevOps-Practicals

git status

git fetch origin

git branch -a

git pull origin main

git log --oneline

git status
```

## 6. Result
The remote GitHub repository was successfully fetched and synchronized with the local repository.
