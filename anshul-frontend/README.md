# Git Beginner Guide

This guide explains the basic steps to work with Git in a simple way. It covers cloning a project, working on branches, saving your work, and keeping your fork updated.

---

## What is Git?

Git is a tool that helps you track changes in your code and work with others without overwriting each other's work.

---

## Basic Setup (one-time)

Tell Git who you are:

```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## Clone a Repository

Cloning means copying a project from the internet to your computer.

```
git clone <repository-url>
cd <repository-folder>
```

---

## Working with Branches

A branch is like a separate workspace. You should never work directly on the main branch.

### Create a New Branch

```
git branch my-branch
```

### Switch to a Branch

```
git switch my-branch
```

Or create and switch in one step:

```
git switch -c my-branch
```

### See All Branches

```
git branch
```

### Delete a Branch

```
git branch -d my-branch
```

---

## Make Changes and Save Them

### Check What Changed

```
git status
```

### Add Changes

```
git add .
```

### Save Changes (Commit)

```
git commit -m "Write a short message about your changes"
```

---

## Push Changes to Your Branch

Always push to your own branch, not main.

```
git push origin my-branch
```

---

## Pull Latest Changes

Get updates from the remote project:

```
git pull origin main
```

---

## Sync Your Fork

If you forked a project, you need to keep it updated.

### Add Original Project (only once)

```
git remote add upstream <original-repo-url>
```

### Get Latest Changes

```
git fetch upstream
```

### Update Your Main Branch

```
git checkout main
git merge upstream/main
```

### Push Updated Main to Your Fork

```
git push origin main
```

---

## Switch Between Branches

```
git checkout branch-name
```

---

## Stashing (Save Work Temporarily)

If you want to switch branches but are not ready to commit:

### Save Your Work

```
git stash
```

### See Saved Work

```
git stash list
```

### Apply Saved Work

```
git stash apply stash@{n}
```

### Remove Saved Work

```
git stash drop stash@{n}
```

---

## Simple Daily Workflow

1. Clone the project
2. Create a new branch
3. Make changes
4. Add and commit
5. Push to your branch
6. Create a pull request (on the website)

---

## Important Rules

* Never push directly to main
* Always create a new branch for your work
* Write clear commit messages
* Pull latest changes before starting work

