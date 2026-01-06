# Git Workflow Guide

## Setup (One-time)

### Point your repo to your fork
```bash
git remote set-url origin https://github.com/YOUR_USERNAME/Module-0.git
```

### Add upstream (original repo) for syncing
```bash
git remote add upstream https://github.com/minitorch/Module-0.git
```

### Verify remotes
```bash
git remote -v
```

---

## Syncing with Upstream

### Fetch and merge upstream changes
```bash
git fetch upstream
git merge upstream/master
```

### Or as a shortcut
```bash
git pull upstream master
```

### Push synced changes to your fork
```bash
git push origin master
```

---

## Creating a Pull Request

### 1. Create a new branch for your feature
```bash
git checkout -b your-feature-branch
```

### 2. Make your changes and stage them
```bash
git add .
# Or add specific files:
git add file1.py file2.py
```

### 3. Commit your changes
```bash
git commit -m "Descriptive message about your changes"
```

### 4. Push to your fork
```bash
git push origin your-feature-branch
```

### 5. Create the Pull Request on GitHub
1. Go to https://github.com/minitorch/Module-0
2. Click **Pull requests** → **New pull request**
3. Click **compare across forks**
4. Select your fork and branch
5. Fill in the title and description
6. Click **Create pull request**

---

## Common Git Commands

### Check status
```bash
git status
```

### View commit history
```bash
git log --oneline
```

### Switch branches
```bash
git checkout branch-name
```

### Discard changes to a file
```bash
git restore filename
```

### Stash changes temporarily
```bash
git stash
git stash pop  # restore stashed changes
```

---

## Troubleshooting

### Undo last commit (keep changes)
```bash
git reset --soft HEAD~1
```

### Undo last commit (discard changes)
```bash
git reset --hard HEAD~1
```

### Fix merge conflicts
1. Open conflicted files and resolve conflicts
2. Stage resolved files: `git add filename`
3. Complete the merge: `git commit`
