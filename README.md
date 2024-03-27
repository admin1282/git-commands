#!/bin/bash

# Git Configuration and Basic Commands

# Global Configuration (set global)
git config --global user.name "username"
git config --global user.email "email"

# List all configurations
git config --list

# Clone Repository
git clone repo # Clone a repository(project)

# Check Changes
git status 
# **Changes not staged for commit** indicates modified files.
# **Untracked files** indicates newly added files.

# Explanation of status:
# Untracked: new files
# Modified: existing file changed
# Staged: after "git add .", file ready to commit
# Not Staged: not committed but files are added
# Unmodified: after commit files, unchanged

# Managing Repository Without Pulling
# Initialize a new repo
git init
git remote add origin <link git repo>
git remote -v # Verify remote
git branch # Check branch
git branch -M main # Rename branch
git push origin main 
git push -u origin branch 
# -u means set upstream, useful for long-term work in the same project

# Branch Commands
git branch # Check branch
git branch -M <branch_name> # Rename branch
git checkout <branch_name>  # Navigate
git checkout -b <branch_name>  # Create new branch
git branch -d <branch_name>  # Delete branch

# Merging Code
git diff <branch_name>  # Compare branches
git merge <branch_name> # Merge two branches

# Undoing Changes
# Case 1: Staged changes (changes added but not committed)
git reset <file_name>
git reset --hard <file_name>
git reset -- for all

# Case 2: Committed changes (for one commit)
git reset HEAD~1

# Case 3: Committed changes (for many commits)
git reset <commit-hash>
git reset --hard <commit-hash> # Remove code changes

# Note: Use these commands carefully for effective management of Git repositories.
