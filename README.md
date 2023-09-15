
# GIT and Version Control

**GIT** is a tool that helps you keep track of changes in your files and work on them with others, making it easier to manage your projects.

### Setting up GIT

- Install GIT and open GIT Bash
- Configure the user details using commands below

```
$ git config --global user.name "Amandeep"
$ git config --global user.email "amanmewar1718@gmail.com"
```

<img src="https://i.imgur.com/1zAiSqJ.png" alt="Alt Text" width="700" height="500">

* The **git init** command is used to initialize a new Git repository in a directory while the **git status** command is used to check the current status of your Git repository.

    ```
    $ git init

    $ git status
    ```
    
<img src="https://i.imgur.com/GMjzhsf.png" alt="Alt Text" width="500" height="300">


  ```
  $ git add --a

  $ git commit -m "Initial Commit"

  $ git log
  ```

<img src="https://i.imgur.com/Xz2ecLA.png" alt="Alt Text" width="500" height="500">


* **git add --a** command is used to stage all changes in your working directory for the next commit.

* **git commit -m** command is used to save the changes in your repository as a new commit with a meaningful commit message.

* **git log** command is used to view the history of commits in your Git repository.

### Clone a Repository

**Clone** refers to the process of creating a copy of a remote Git repository on your local computer.

When you clone a Git repository, you essentially make an identical copy of all the files, commit history, and branches from the remote repository on your own machine.

```
$ git clone <repository_url>

```

<img src="https://i.imgur.com/jlsbHIs.png" alt="Alt Text" width="500" height="400">


### GIT Ignore

**gitignore** refers to a mechanism for specifying files and directories that should be ignored by Git. This means that Git will not track changes to these files, and they won't be included in commits.

1. Create a .gitignore file

2.  Add the files or directories you want git to ignore.
* To ignore a specific file:
    ```
    filename.txt
    ```

* To ignore all files with a specific extension (e.g., .log files):

    ```
    *.log
    ```
*   To ignore all files in a specific directory:
    ```
    directoryname/
    ```
* To ignore all files in a specific directory with a specific extension:
    ```
    directoryname/*.txt
    ```



### Diffence Between Commits, Staging Area & Working directory

* Compares the Working directory with staging area:
    ```
    $ git diff
    ```

    ```
    $ git diff --staged
    ```

### Unstaging & Unmodifying

* Unstage the file from staged area:

    ```
    $ git restore --staged filename.txt

    ```
    
<img src="https://i.imgur.com/Vc7RSCh.png" alt="Alt Text" width="600" height="500">

* revert changes to the last committed version:

    ```
    $ git restore filename.txt
    ```
    
<img src="https://i.imgur.com/bZy2bJT.png" alt="Alt Text" width="600" height="400">

### Rename & Deleting files

* Rename file from filename1.txt to NewName.txt:
    ```
    $ git mv filename1.txt NewName.txt
    ```
<img src="https://i.imgur.com/FMI5rQP.png" alt="Alt Text" width="600" height="500">

* Delete file :
    ```
    $ git rm filename.txt
    ```
    
<img src="https://i.imgur.com/Z5YtDVB.png" alt="Alt Text" width="400" height="600">

* Removes the files from git tracking:
    ```
    $ git rm --cached filename.txt
    ```
    
<img src="https://i.imgur.com/DGt8YaL.png" alt="Alt Text" width="500" height="600">

### Working on Remote Repository

* List of remote repositories that are associated with local Git repository:

    ```
    $ git remote -v
    ```
    
<img src="https://i.imgur.com/pJpwBiy.png" alt="Alt Text" width="700" height="300">

* Adding remote repository:
    ```
    $ git remote add origin <repository_url>
    ```

### GIT Push to remote repository

* Push changes to the remote repository named "origin."

    ```
    $ git push origin <branch_name>
    
    
<img src="https://i.imgur.com/zQ9Y3AI.png" alt="Alt Text" width="700" height="800">

* In case of unrelated commit'd branches:

    ```
    $ git push origin master --allow-unrelated-histories
    ```
* Update local repository with remote repository:

    ```
    $ git pull origin master
    ```
### Branches in GIT

* Create a new branch:

    ```
    $ git checkout -b <new_branch_name>
    ```
    
<img src="https://i.imgur.com/oWTezlv.png" alt="Alt Text" width="600" height="800">

* Switch to another branch:
    
    ```
    $ git checkout <branch_name>
    ```

* List of branch names:

    ```
    $ git branch
    ```

### Merging branches

***Note: Merge is always done with master branch.***

* Merging master and <branch_name>:

    ``` 
    $ git merge <branch_name>
    ```
    
<img src="https://i.imgur.com/ZSxSNLl.png" alt="Alt Text" width="500" height="400">


### Alias Setting

* In case you are looking for a pseudo name or some shorthand for a command:

    ```
    $ git config --global alias.cm "commit -m"
    ```

    ```
    $ git sc "Files added"
    ```
