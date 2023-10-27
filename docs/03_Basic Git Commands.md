# **3. Basic Git Commands**

### **`git add`**

The **`git add`** command is used to stage changes for commit. In other words, it tells Git that you want to include updates from certain files in the next commit.

Usage:

```bash
bashCopy code
git add [file/directory]

```

Examples:

- To add a single file:
    
    ```bash
    bashCopy code
    git add filename.txt
    
    ```
    
- To add all files in the current directory (and subdirectories):
    
    ```bash
    bashCopy code
    git add .
    
    ```
    
- To add all files with a certain extension (e.g., all **`.txt`** files):
    
    ```bash
    bashCopy code
    git add *.txt
    
    ```
    

### **`git commit`**

Once you've staged your changes with **`git add`**, you use **`git commit`** to capture your changes in a snapshot, which can be thought of as a "save point" in your project's history.

Usage:

```bash
bashCopy code
git commit -m "Your commit message here"

```

The **`-m`** flag allows you to add a short message describing the commit. It's essential to write clear and descriptive commit messages to understand the project's history later.

Example:

```bash
bashCopy code
git commit -m "Add initial version of the README file"

```

### **`git status`**

The **`git status`** command shows the status of changes in the working directory and staging area. It'll tell you which changes have been staged, which haven't, and which files aren't being tracked by Git.

Usage:

```bash
bashCopy code
git status

```

### **`git log`**

The **`git log`** command displays the commit history, showing details about each commit, including the author, date, and commit message.

Usage:

```bash
bashCopy code
git log

```

For a more concise view with one line per commit, you can use:

```bash
bashCopy code
git log --oneline

```

### **`git diff`**

The **`git diff`** command shows the differences between your working directory and the last commit. It's useful to see what changes you've made before staging them.

Usage:

- To see differences in the working directory not yet staged:
    
    ```bash
    bashCopy code
    git diff
    
    ```
    
- To see differences in the staged changes compared to the last commit:
    
    ```bash
    bashCopy code
    git diff --staged
    
    ```
    

### **`git revert`**

- **Purpose:** Used to reverse the changes made by a specific commit by creating a new commit. This ensures that the commit history remains intact.
- **Usage:**
    
    ```bash
    bashCopy code
    git revert [commit-hash]
    
    ```
    
- **Example Scenario:** If you've introduced a change that, in hindsight, isn't needed or is problematic, but you want to keep a record of all actions (including the mistake and its correction), you'd use **`git revert`**.

### **`.gitignore`**

**`.gitignore`** isn't a command, but a special file that you place in the root of your repository. It tells Git which files or directories to ignore and not track. This is useful for excluding files that you don't want in your repo, like temporary files, logs, or files containing sensitive information.

Example **`.gitignore`** content:

```bash
bashCopy code
# Ignore all .log files
*.log

# Ignore the build directory
/build/

# Ignore the secret configuration
secret-config.json

```

To make Git ignore the files/directories listed in **`.gitignore`**, simply create or edit the **`.gitignore`** file in your repository's root directory and list the patterns for files or directories you want to exclude.