### **Part 1: Git Basics**

#### **Task 1: Install and Configure Git**
1. Install Git from [git-scm.com](https://git-scm.com/).
2. Configure your global Git settings.
    ```bash
    git config --global user.name "Your Name"
    git config --global user.email "Your email@example.com"
    ```
3. Verify the configuration
    ```bash
    git config --list
    ```

#### **Task 2: Initialize a Repository**

1. Create a directory and initialize it as Git repository:
    ```bash
    mkdir MyProject 
    cd MyProject
    git init
    ```

    -**Purpose** :  Initializes a `.git` folder to track changes.


---


### **Part 2: Basic workflow**

#### **Task 3: Creating and Commiting Files**

1. Create a file:
    ```bash
    echo "Hello Git" > file1.txt
    ```

2. Stage and commit the file:
    ```bash
    git add file1.txt
    git commit -m "Initial commit: Added file1.txt"
    ```

#### **Task 4: Viewing Changes**

1. Modify the file:
    ```bash
    echo "Git is awesome!" > file1.txt
    ```
2. Check file status and differences:
    ```bash
    git status
    git diff
    ```
#### **Task 5: Undoing changes**
1. Unstage a staged file:
    ```bash
    git reset file1.txt
    ```

2. Discard uncommitted changes:
    ```bash
    git checkout -- file1.txt
    ```


---


### **Part 6: Branch Management**
1. Create a branch and switch to it:

    ```bash
    git chekout -b feature-branch 

2. List branches:

    ```bash
    git branch
    ```
3. Rename a branch:

    ```bash
    git branch -m feature-branch feature-enhanced
    ```

### **Task 7: Merging Branches**

1. Merge feature-enhanced into main:

    ```bash
    git checkout main
    git merge feature-enhanced
    ```

### **Task 8: Handling Merge Conflicts**

1. Create two conflicting branches and resolve a conflict manually:

    ```bash
    git merge <branch-name>
    ```

2. Use:

    ```bash
    git add <resolved-file>
    git commit 
    ```


---


## **Part 4: Remote Repositories**
### **Task 9: Remote Setup**
1. Add a remote repository:
    ```bash
    git remote add origin https://github.com/your-username/repo.git
    ```

2. Verify the remote:
    ```bash
    git remote -v
    ```

### **Task 10: Push and Pull**
1. Push changes to the remote repository:
    ```bash
    git push -u origin main
    ```

2. Pull changes from the remote:
    ```bash
    git pull origin main
    ```

### **Task 11: Cloning a Repository**
1. Clone a remote repository:
    ```bash
    git clone https://github.com/your-username/repo.git
    ```

---


## **Part 5: Advanced Git**
### **Task 12: Stashing Changes**
1. Save uncommitted changes:
    ```bash
    git stash
    ```
2. Apply stashed changes:
    ```bash
    git stash apply
    ```
3. Drop the stash:
    ```bash
    git stash drop
    ```

### **Task 13: Tagging commits**
1. Create and annotate a tag:
    ```bash
    git tag -a v1.0 -m "Version 1.0 release"
    ```

2. Push the tag to the remote:
    ```bash
    git push origin v1.0
    ```

### **Task 14: Rewriting commit History**

1. Use interactive rebase to modify commit messages:
     ```bash
    git rebase -i HEAD~3
    ```

    - Replace `pick` with `edit` or `squash` as needed.


### **Task 15: Cherry-Picking Commits**
1. Apply a specific commit to another branch:
    ```bash
     git cherry-pick <commit-hash>
    ```

---


## **Part 6: Collaboration**
### **Task 16: Forking and Pull Request**
1. Fork a repository and clone it locally:
    ```bash
    git clone https://github.com/your-username/forked-repo.git
    ```

2. Make changes and push them:
    ```bash
    git checkout -b fix-typo
    echo "Typo fixed" >> README.md
    git commit -m "Fixed a typo"
    git push origin fix-typo
    ```
3. Open a pull request on Github.
    ```bash

### **Task 17: Simulating Team Collaboration**

1. Simulate a conflict by having two users modify the same file.
2. Practice resolving the conflict as a team.

---

## **Part 7: Ignoring Files**
### **Task 18: Using.gitgnore**

1. Create a `.gitgnore` file:
    ```bash
    echo "node_modules/' > .gitgnore"
    git add .gitgnore
    git commit -m "Added .gitgnore"
    ```

2. Verify that ignored files are not staged:
    ```bash
    git status
    ```
---
## **Part 8: Automation and Cleanup**
### **Task 19: Cleaning the repository**
1. Remove untracked files:

    ```bash
    git clean -f
    ```

### **Task 20: Aliases and Shortcuts**
1. Create an alias for frequently used commands:
    ```bash
    git config --global alias.st status
    git config --global alias.cm commit
    ```
2. Use the alias:
    ```bash
    git st
    git cm -m "Message"
    ```

