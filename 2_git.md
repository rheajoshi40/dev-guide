# Git & GitHub Learning Guide

## 📌 WHAT IS GIT & GITHUB?

**Git**: A version control system that tracks changes in your code

**GitHub**: A platform where you upload Git projects and collaborate online

**Why we use it**: Track history, collaborate with others, avoid losing code, manage different versions

---
## 🔰 BEGINNER LEVEL

### Essential Commands with Parameters

> use -h when in doubt like git init -h if u need to know what all things u can do with git init


#### 1. `git init` - Create a new repository
```
git init                          # Creates .git folder in current directory
git init <folder-name>            # Creates folder and initializes repo
```
**When to use**: Starting a brand new project locally

---

#### 2. `git clone` - Download a project from GitHub
```
git clone <URL>                   # Clone entire repo (all branches & history)
git clone <URL> <folder-name>     # Clone into specific folder name
git clone -b <branch-name> <URL>  # Clone specific branch only
```
**When to use**: Getting an existing project to work on locally

---

#### 3. `git add` - Stage files (prepare for saving)
```
git add <filename>                # Stage specific file
git add .                         # Stage all changed files
git add *.html                    # Stage all HTML files
git add -A                        # Stage everything (new, modified, deleted)
git add -p                        # Interactive mode - stage parts of files
```
**When to use**: Before committing, to tell Git which files to save

---

#### 4. `git commit` - Save changes with a message
```
git commit -m "message"           # Commit with short message
git commit -m "title" -m "description"  # Commit with title and description
git commit --amend                # Modify last commit (add files or fix message)
git commit --amend --no-edit      # Amend without changing message
git commit -h                     # View all options
```
**When to use**: After staging files, to create a snapshot of your code

> **Pro tip**: Write clear messages like "Add login feature" not "fixed stuff"

---

#### 5. `git push` - Upload commits to GitHub
```
git push                          # Push current branch to remote
git push origin <branch-name>     # Push specific branch to GitHub
git push -u origin <branch-name>  # Push and set upstream (first time)
git push origin --all             # Push all branches
git push origin --delete <branch> # Delete branch on GitHub
```
**When to use**: After committing locally, to save changes to GitHub

---

#### 6. `git pull` - Download latest changes from GitHub
```
git pull                          # Pull from current branch
git pull origin <branch-name>     # Pull specific branch from GitHub
git pull --no-commit              # Fetch without merging automatically
```
**When to use**: Before pushing, to sync latest changes from teammates

---

#### 7. `git status` - Check what files changed
```
git status                        # Shows modified, staged, untracked files
git status -s                     # Short format (simpler view)
```
**When to use**: Anytime to see the state of your working directory
**Output guide**:
- Red = modified but not staged
- Green = staged and ready to commit
- Untracked = new files Git doesn't know about

---

#### 8. `git branch` - Create and manage branches
```
git branch                        # List all local branches
git branch -a                     # List all branches (local + remote)
git branch <branch-name>          # Create new branch (stays on current)
git branch -d <branch-name>       # Delete branch (safe - prevents data loss)
git branch -D <branch-name>       # Force delete branch
git branch -m <new-name>          # Rename current branch
git branch -h                     # View all options
```
**When to use**: Creating separate work areas for features or fixes

---

#### 9. `git checkout` - Switch between branches
```
git checkout <branch-name>        # Switch to existing branch
git checkout -b <branch-name>     # Create AND switch to new branch
git checkout <filename>           # Discard changes in file (revert to last commit)
git checkout HEAD~1               # Go back to previous commit (detached)
git checkout -h                   # View all options
```
**When to use**: Switching between different features you're working on

---

#### 10. `git merge` - Combine branches together
```
git merge <branch-name>           # Merge branch into current branch
git merge --no-ff <branch-name>   # Merge with commit (keeps branch history)
git merge --squash <branch-name>  # Combine all commits into one
git merge --abort                 # Cancel merge if conflicts appear
git merge -h                      # View all options
```
**When to use**: After finishing feature, merge back to main
**Important**: Always pull latest before merging to avoid conflicts

---

#### 11. `git diff` - See what changed
```
git diff                          # Show unstaged changes
git diff --staged                 # Show staged changes
git diff <branch1> <branch2>      # Compare two branches
git diff <commit1> <commit2>      # Compare two commits
git diff HEAD~1                   # Compare with previous commit
git diff -h                       # View all options
```
**When to use**: Before committing, to review exactly what changed


### Understanding Merge Conflicts

> **What is a conflict?** When you and someone else edit the same line and Git doesn't know which version to keep.

**How to resolve:**
```
git merge <branch-name>           # Git will warn about conflicts
# Edit the conflicted files - Git marks them like:
# <<<<<<< HEAD  <-------------------- (conflict markers)
# your changes
# ======= (conflict markers)
# their changes
# >>>>>>> branch-name (conflict markers)

git add <resolved-file>           # Stage the fixed file
git commit -m "Resolve merge conflict"  # Complete the merge
```

**Tips to avoid conflicts:**
- Pull before pushing
- Work on different files when possible
- Communicate with teammates about what you're changing
> Learn more about merge conflicts: https://www.youtube.com/watch?v=DloR0BOGNU0

---

### GitHub Basics Checklist

- [ ] Create a GitHub account
- [ ] Create your first repository on GitHub
- [ ] Know what .gitignore is (files to ignore/not track)
- [ ] Learn how to fork a repository (copy someone else's project)
- [ ] Understand public vs private repositories

---

### First Project Setup

- [ ] Initialize a local Git repository
- [ ] Make your first commit
- [ ] Connect local repo to GitHub
- [ ] Push your first commit to GitHub
- [ ] Verify changes appear on GitHub

---

## 💡 QUICK REFERENCE: Common Workflows

### Starting a New Project
```
git init
git add .
git commit -m "Initial commit"
git remote add origin <GitHub-URL>
git push -u origin main
```

### Updating Your Local Copy
```
git pull origin main
```

### Fixing Last Commit
```
git commit --amend
```

---

## ✅ LEARNING TIPS

- Practice one concept at a time
- Create dummy repositories to experiment
- Use Git GUI tools first (GitHub Desktop, GitKraken) if commands seem scary
- Read commit messages in popular projects to learn style
- Don't memorize commands—use them repeatedly

> **When in doubt, use `-h` flag** to see help for any command!

---

### Resource 
https://www.youtube.com/watch?v=Ala6PHlYjmw