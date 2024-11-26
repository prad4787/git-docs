# Git Flow and Best Practices

## 1. Branch Naming Conventions

Branch names should be descriptive, easy to understand, and follow a consistent naming convention. Here are some common branch name types:

- **`main`**: The main branch where the production-ready code is located.
- **`develop`**: Used as a base for development. All feature branches are merged here.
- **Feature branches**: For new features or improvements, use:
  - `feature/<feature-name>`
  - Example: `feature/login-functionality`
- **Bugfix branches**: For fixing bugs in `develop`, use:
  - `bugfix/<issue-or-description>`
  - Example: `bugfix/login-error`
- **Hotfix branches**: For urgent fixes in `main`, use:
  - `hotfix/<issue-or-description>`
  - Example: `hotfix/security-patch`
- **Release branches**: For final testing before going to `main`, use:
  - `release/<version>`
  - Example: `release/v1.0.0`

## 2. Git Commit Message Convention

Follow these guidelines to ensure commit messages are clear, consistent, and helpful:

- **Commit Message Format**: `<type>(<scope>): <description>`
- **Type**: The type of change. Common types:
  - `feat`: A new feature
  - `fix`: A bug fix
  - `docs`: Documentation updates
  - `style`: Code style changes (formatting, indentation)
  - `refactor`: Refactoring code without changing functionality
  - `test`: Adding or modifying tests
  - `chore`: Minor changes that do not affect the codebase directly
- **Scope**: The part of the codebase affected (optional but recommended).
- **Description**: A short summary of the change (use imperative, present tense, e.g., “add login functionality” instead of “added” or “adds”).

- **Examples**:
- `feat(login): add user authentication flow`
- `fix(profile): correct profile image loading`
- `docs(readme): update contribution guidelines`

### Commit Message Tense
- Use **imperative, present tense** (e.g., "fix", "add", "update") rather than past tense (e.g., "fixed", "added").

## 3. Common Git Commands and Usage

### **Basic Git Commands**

- **`git init`**: Initialize a new Git repository.
- *Use when*: Starting a new project that isn’t already in version control.

- **`git clone <repository-url>`**: Clone an existing repository to your local machine.
- *Use when*: You want a copy of a remote repository on your local machine.

- **`git add <file(s)>`**: Stage changes for commit.
- *Use when*: You've made changes to files and are ready to commit them.

- **`git commit -m "commit message"`**: Commit staged changes with a message.
- *Use when*: You’ve staged changes and are ready to save a snapshot of the current state.

### **Branch Management**

- **`git branch <branch-name>`**: Create a new branch.
- *Use when*: You’re starting a new feature or task and want to keep it isolated.

- **`git checkout <branch-name>`**: Switch to a different branch.
- *Use when*: You need to work on a different branch or test code on a separate branch.

- **`git merge <branch-name>`**: Merge changes from another branch into the current branch.
- *Use when*: Your feature is complete, and you’re ready to integrate it with `develop` or `main`.

- **`git rebase <branch-name>`**: Rebase the current branch on top of another branch.
- *Use when*: You want a cleaner history by replaying your commits onto the latest code of a base branch.

### **Working with Remote Repositories**

- **`git pull`**: Fetch and integrate changes from the remote repository.
- *Use when*: You need to sync your local branch with the latest remote updates.

- **`git push`**: Upload local commits to the remote repository.
- *Use when*: Your work is complete and ready for others to see.

- **`git fetch`**: Fetch updates from the remote repository without merging.
- *Use when*: You want to see changes on the remote without altering your local files.

### **Undoing Changes**

- **`git reset --soft <commit-hash>`**: Move the HEAD to a previous commit without changing the working directory.
- *Use when*: You want to keep changes staged and redo a commit.

- **`git reset --hard <commit-hash>`**: Discard all changes after a specific commit.
- *Use when*: You need to undo commits and changes permanently.

- **`git revert <commit-hash>`**: Create a new commit that undoes changes from a previous commit.
- *Use when*: You want to undo a commit but keep it in the history.

---
