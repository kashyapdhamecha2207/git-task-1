## **Task List: Focused on Repository Management,commits,Branching, and Merging**

## **Part 1: Creating and Cloning Repositories**
### **Task 1: Create a local Git Repository**
1. Create a new project folder:
    ```bash
    mkdir MyProject
    cd MyProject
    ```
2. Initialize it as a Git repository:
    ```bash
    git init
    ```

    - **Explanation**: This command downloads the repository to your local system. 

3. Verify the repository status:
    ```bash
    git status
    ```
    - **Example Output**:
    ```bash
    On branch main
    No commits yet
    nothing to commit (create/copy files and use "git add" to track)
    ```

### **Task 2: Clone a Remote Repository**
1. Clone a GitHub repository:
    ```bash
    git clone https://github.com/username/repo.git
    ```
    - **Explanation**: This command downloads the repository to your local system.

2. Verify the cloned repository structure:
    ```bash
    cd repo
    ls -a
    ```
    - **Output**: The `.git` folder should be present.

---

## **Part 2: Understanding Commits and Commit Messages**

### **Task 3: Commit Changes Locally**
1. Create a new file and add content:
    ```bash
    echo "Welcome to Git" > README.md
    ```

2. Stage the file:
    ```bash
    git add README.md
    ```

    - **Explanation**: `git add` moves changes to the staging area.

3. Commit the staged file:
    ```bash
    git commit -m "Initial commit: Added README.md"
    ```

## **Task 4: Write Effective Commit Messages**
1. Create a detailed commit message:
    ```bash
    git commit -m "Added Iitial version of README.md with project overview"
    ```
    - **Explanation**: Commit messages should follow conventions such as starting with a capital letter, being concise, and using imperative mood.

2. Commit multiple files with one message:
    ```bash
    toutch file1.txt file2.txt
    git add .
    git commit -m "Added two new files for feature setup"
    ```

---


## **Part 3: Viewing  Commit Histoy with `git log`**
### **Task 5: View Detailed Commit History**
1. View full commit logs:
    ```bash
    git log
    ```
    - **Explanation**: Shows a detailed list of commits with hash,author,time,date,and message.

2. View commit history in a compact format:
    ```bash
    git log --oneline 
    ```
    -**Eample Output**:
    ```bash
    e23d8a7 Added initial version of README.md
    f7b3c62 Initial commit: Added README.md
    ```

### **Task 6: Customize logs with a graphical representation:**

1. View logs with a graphical representation:
    ```bash
    git log --oneline --graph --decorate
    ```

2. Filter logs for a specific file:
    ```bash
    git log README.md 
    ```

---

## **Part 4: Understanding Branching and Merging**
### **Task 7: Understanding Branching**

1. List all branches:
    ```bash
    git branch
    ```
    - **Explanation**: Displays the current branch and all other branches.

2. Create a new branch:
    ```bash
    git branch feature-branch
    ```
    - **Explanation**:Creates a new branch without switching to it .

3. Switch to the new branch:
    ```bash
    git chekout feature-branch  
    ```
    - **Alternative Command**:
        ```bash
        git checkout -b feature-branch
        ```
        -**Explanations**: Create and Switches to the branch in one command.

--- 

## **Part 5: Creating and working with branches**
### **Task 8: Make Changes in a Branch**
1. Add content to a file in the new branch:
    ```bach
    echo "Feature in progress" > feature.txt
    git add feature.txt
    git commit -m "Added feature.txt in feature-branch"
    ```

### **Task 9: Merging Branches**
1. Switch back to the `main` branch :
    ```bash
    git merge feature-branch
    ```
    - **Explanation**: Combines the changes from feature-branch into main.

---

## **Part 6: Resolving Merge Conflicts**
### **Task 10: Simulate a Merge Conflict**

1. Modify the same line in a file on two branches:
    ```bash
    echo "Main branch content" > conflict.txt
    git add conflict.txt
    git commit -m "Added conflict.txt in main branch"
    ```

2. Switch to the other branch and make conflicting changes:

    ```bash
    git checkout feature-branch
    echo "Feature branch content" > conflict.txt
    git add conflict.txt
    git command -m  "Modified conflict.txt in feature-branch"
    ```

3. Merge `feature-branch` into `main` :
    ```bash
    git chekout main
    git merge feature-branch

4. Resolve the conflict by editing the file and choosing the correct version:
    - Open `conflict.txt` and decide which changes to keep.
    - Stage the resolved file:
    ```bash
    git add conflict.txt
    ```
    - Commit the merge:
    ```bash
    git commit -m "Resolved conflict in conflict.txt"
    ```
---

## **Part 7: Deleting amd Renaming Branches**
### **Task 11: Delete a branch**
1. Delete a local branch: 
    ```bash
    git branch -d feature-branch
    ```
    - **Explanation**: This deletes the branch only if it has been fully merged.

2. Force-delete a branch:
    ```bash
    git branch -d feature-branch
    ```
    - **Explanation**: Deletes the branch if it hasn't been merged.

---
## **Consolidated Flow Summary**
1. Start by creating and cloning repositories.
2. Learn to commit changes effectively with clear messages.
3. Explore commit history using various git log commands.
4. Understand branching and practice creating, switching, and merging branches.
5. Dive into resolving merge conflicts.
6. End by managing branches through deletion and renaming.









