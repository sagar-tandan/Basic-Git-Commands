# 🚀 Beginner Git Commands - All-in-one Guide

This markdown file is your complete beginner guide to using **Git**, the most popular version control system. Learn step-by-step with clear explanations, visualizations, and command examples.

---

## What is Git?

Git is a version control system that tracks changes in your code. It helps with:

- Saving your work in snapshots (commits)
- Collaborating with others without conflict
- Going back in time if something breaks

---

## 1. Git Configuration

Set your identity before committing:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

This ensures all your commits are labeled with your name and email.

---

## 2. Create a Repository

### a. Initialize a Repository

```bash
git init
```

Creates a hidden `.git/` folder to start tracking your project.

```
project/
├── index.html
└── .git/         ← Git starts tracking
```

### b. Clone a Repository

```bash
git clone <repository-url>
```

Copies a remote GitHub repository to your local machine.

---

## 3. Daily Git Workflow

### a. Check Status

```bash
git status
```

See which files are:

- Modified
- Untracked
- Staged

---

### b. Stage Files

```bash
git add <file>
git add .     # Adds everything
```

Moves changes to the **staging area**.

---

### c. Commit Changes

```bash
git commit -m "Add feature or fix bug"
```

Saves a snapshot of staged changes.

```
[ Staging Area ] ── git commit ──▶ [ Local Repository ]
```

---

## 4. Work with Remote Repositories

### a. Push Changes

```bash
git push -u origin main
```

Sends your local commits to the remote GitHub repo.

```
[ Local Repo ] ── git push ──▶ [ GitHub ]
```

---

### b. Pull Changes

```bash
git pull origin main
```

Fetches and merges remote updates to your local branch.

```
[ GitHub ] ── git pull ──▶ [ Local Repo ]
```

---

## 5. Branching and Merging

### a. Create a Branch

```bash
git branch feature-xyz
```

Makes a new branch from the current HEAD.

### b. Switch to a Branch

```bash
git checkout feature-xyz
```

Switches to the branch you just created.


### c. Create and switch to new branch in single command
```bash
git checkout -b <Branch_Name>
```

Creates new branch and switch to it automatically.

---

### c. Merge a Branch

```bash
git checkout main
git merge feature-xyz
```

Combines changes from the feature branch into `main`.

```
main ──A──B──C
             \
feature-xyz   D──E
               \
                └──▶ merged into main
```

---

### d. Delete a Branch

```bash
git branch -D feature-xyz
```

Removes a branch after merge.

---

## 6. View History and Changes

### a. View Commit History

```bash
git log
```

Shows all commits, messages, authors, and dates.

### b. View Differences

```bash
git diff
```

Shows file changes (unstaged vs staged).

---

## 7. Undo and Reset

### a. Unstage a File

```bash
git reset <file>
```

Removes file from staging area (keeps changes in working directory).

---

## 8. Ignore Files

Create a `.gitignore` file:

```
node_modules/
.env
dist/
```

Prevents Git from tracking specified files/folders.

---

## Final Tips

- Always `pull` before you `push` to avoid conflicts.
- Use branches for features and bug fixes.
- Never commit sensitive files — use `.gitignore`.
- Practice Git daily — it's the brain of every project.

Happy Coding! 🎉  
_You now know the essential Git commands to version and manage your code like a pro!_
