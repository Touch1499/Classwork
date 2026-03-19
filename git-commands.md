# Git Commands Cheat Sheet

## Pull / Update

```bash
# Pull latest changes from remote
git pull

# Pull from specific branch
git pull origin main
```

## Create Branch

```bash
# Create a new branch
git branch branch-name

# Create and switch to new branch (shortcut)
git checkout -b branch-name

# Modern way (Git 2.23+)
git switch -c branch-name
```

## Switch Branch

```bash
# Switch to existing branch
git checkout branch-name

# Modern way (Git 2.23+)
git switch branch-name

# Switch back to previous branch
git checkout -
```

## Pull Request (via GitHub CLI)

```bash
# Create a pull request
gh pr create --title "Your PR title" --body "Description"

# Create PR with base branch specified
gh pr create --base main --head feature-branch --title "Title"

# View open PRs
gh pr list

# Checkout a PR locally
gh pr checkout <pr-number>
```

## Common Workflow

```bash
# 1. Pull latest main
git checkout main
git pull origin main

# 2. Create & switch to new feature branch
git checkout -b feature/my-feature

# 3. Make changes, then commit
git add .
git commit -m "Add my feature"

# 4. Push branch to remote
git push origin feature/my-feature

# 5. Create Pull Request
gh pr create --base main --title "Add my feature"
```

## Quick Reference

| Task | Command |
|---|---|
| Pull updates | `git pull` |
| Create branch | `git branch name` |
| Create + switch | `git checkout -b name` |
| Switch branch | `git checkout name` |
| List branches | `git branch -a` |
| Delete branch | `git branch -d name` |


git push -u origin main