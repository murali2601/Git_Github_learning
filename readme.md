# Git Commands Cheat Sheet

A quick reference guide to commonly used Git commands with explanations, use cases, and examples.

---

## 1. **git stash**

### **Purpose**:
Temporarily save your changes without committing them.

### **Use Case**:
When you want to switch branches or fix a bug without losing your current work.

### **Commands**:

- **Save changes to stash**:
  ```bash
  git stash
  ```
  Saves your uncommitted changes.

- **Save untracked files to stash**:
  ```bash
  git stash -u
  ```
  Includes untracked files in the stash.

- **List stashed changes**:
  ```bash
  git stash list
  ```
  Shows a list of saved stashes, e.g., `stash@{0}`.

- **Apply the latest stash**:
  ```bash
  git stash apply
  ```
  Re-applies the latest stashed changes.

- **Apply a specific stash**:
  ```bash
  git stash apply stash@{0}
  ```
  Applies the specific stash.

- **Drop a stash**:
  ```bash
  git stash drop stash@{0}
  ```
  Deletes the specified stash.

---

## 2. **git commit**

### **Purpose**:
Save changes to the repository.

### **Use Case**:
When you want to save your progress or completed work.

### **Commands**:

- **Commit with a message**:
  ```bash
  git commit -m "Fixed bug and updated feature"
  ```

- **Amend the last commit**:
  ```bash
  git commit --amend
  ```
  Updates the last commit (useful for fixing commit messages).

---

## 3. **git revert**

### **Purpose**:
Undo changes from a specific commit by creating a new commit.

### **Use Case**:
When you want to safely undo a commit in a shared branch.

### **Commands**:

- **Revert a specific commit**:
  ```bash
  git revert <commit-hash>
  ```
  Creates a new commit that undoes the changes introduced by `<commit-hash>`.

- **Revert multiple commits**:
  ```bash
  git revert abc123 def456
  ```
  Reverts the specified commits individually.

- **Revert a range of commits**:
  ```bash
  git revert HEAD~3..HEAD
  ```
  Reverts the last 3 commits (from `HEAD~3` to `HEAD`).

---

## 4. **git push**

### **Purpose**:
Send local commits to a remote repository.

### **Use Case**:
When you want to share your changes with others.

### **Commands**:

- **Push changes to a remote branch**:
  ```bash
  git push origin <branch-name>
  ```

- **Force push (use with caution)**:
  ```bash
  git push --force
  ```
  Overwrites the remote branch with your local changes.

---

## 5. **git log**

### **Purpose**:
View commit history.

### **Use Case**:
When you want to see past commits and their details.

### **Commands**:

- **View commit history**:
  ```bash
  git log
  ```

- **View a brief history**:
  ```bash
  git log --oneline
  ```
  Shows a condensed view of commits.

---

## 6. **git reset**

### **Purpose**:
Undo changes by moving the branch pointer to a previous commit.

### **Use Case**:
When you want to clean up commits in your private branch.

### **Commands**:

- **Reset to a specific commit** (keep changes unstaged):
  ```bash
  git reset <commit-hash>
  ```

- **Hard reset (discards all changes)**:
  ```bash
  git reset --hard <commit-hash>
  ```
  **Caution**: This deletes uncommitted changes.

---

## 7. **git add**

### **Purpose**:
Stage changes for a commit.

### **Use Case**:
When you want to include specific changes in your next commit.

### **Commands**:

- **Stage specific files**:
  ```bash
  git add <file-name>
  ```

- **Stage all changes**:
  ```bash
  git add .
  ```

---

## 8. **git status**

### **Purpose**:
Check the current state of your repository.

### **Use Case**:
To see which files are staged, modified, or untracked.

### **Command**:

```bash
git status
```

---

## 9. **git stash vs git revert vs git reset**

### **Comparison Table**:
| **Command**    | **What it does**                         | **Use Case**                                |
|----------------|------------------------------------------|---------------------------------------------|
| `git stash`    | Temporarily saves uncommitted changes    | Switch tasks without losing progress        |
| `git revert`   | Creates a new commit to undo a change    | Undo specific commits in a shared branch    |
| `git reset`    | Moves branch pointer to a specific commit| Clean up commits in your local branch       |

---

