# GIT
**Basic Git Commands**

**commands to get help :**
git help ,
git help config

**Command Reference**
**List:**

ls <-
Lists files and folders in current directory. Without parameters, will list non-hidden folders and files.

**Git Status:**

git status <-
Shows which files have been modified in the working directory vs Git's staging area.

**Git Add:**

git add file-name  <-
Adds the new or newly modified file-name to Git's staging area (index).

**Git Commit:**

git commit -m "A really good commit message"   <-
Commits all files currently in Git's staging area. The -m parameter allows for a commit message directly from the command line.

Clear!

**clear:**
Clears all previous commands from the terminal screen -- just a bit of clean up.

**Text Mate:**

mate file-name  <-
All command line demos are preformed on the MacOS. Creating and editing files is done with TextMate 2 (free) using the mate command from Terminal. Passing a file-name to the mate command will create or open that file. Windows users can use the notepad file-name command instead.

**Command Reference**
**Express Commit for Tracked files**

git commit -am "Awesome commit message"  <-
Use the -a parameter with the git commit command to directly commit newly modified tracked files. Warning: Only do this for small changes. Tracked files are files that have been previously added to Git (committed or staged).

**Adding All Changed Files**

git add .  <-
The period parameter for the git add command will recursively add all new and newly modified files.

**Unstage File**

git reset HEAD file-name  <-
Following the above command will "unstage" the specified file from Git's staging area (aka index).

**Backout Working Directory Changes**

git checkout -- file-name  <-
Following the above command will back out any changes made to the specified file and replace it with the version last committed in Git

# Command Reference

Seeing Repository History

**git log**
git log --oneline --graph --decorate --color

Git's **log** command displays the repository's history in reverse chronological order. The no-params version displays the standard view.

Git log options from above: --oneline Compacts log data on to one line, abbreviating the SHA1 hash --graph Adds asterisk marks and pipes next to each commit to show the branching graph lines --decorate Adds the markers for branch names and tags next to corresponding commits --color Adds some color to the output -- nice to have, depending on the operating system

**Removing a file using Git**

git rm file-name

**Removing a file using Terminal**

rm file-name

This removes the file outside Git's knowledge

Updating Git's Index (staging area)

git add -u

The *u* parameter will recursively update Git's staging area regarding deleted/moved files outside of Git.

Making a directory (folder)

mkdir folder-name

The **mkdir** command is a nearly universal command for creating a directory/folder.

Making a directory (folder)

git mv source destination

The **git mv** command will move the *source* (file or folder) to the *destination* with Git.

# Command Reference for SSH Authentication

Generating an SSH Key

ssh-keygen -t rsa -C "your.name@your-company.com"

Use your actual email address in the example above.

Verify SSH authentication

ssh -T git@github.com

Above command uses **ssh** to connect to GitHub over the SSH protocol.

# Command Reference for Git Remote

Creating a remote repository reference

git remote add remote-name remote-repository-location

Using **git remote add** command allows us to associate a remote repository. Normally, you want to paste in the full URL for the remote repository given to you by your Git host (GitHub). By convention, the first or primary remote repository is named *origin*.

List Git's Remotes

git remote -v

The **git remote** command lists the names of all the remote repositories and the -v parameter (verbose) will display the full URL of the remote repository for each remote name listed

Send Changes to Remote

git push -u remote-name branch-name
git push remote-name branch-name

The **git push** sends all your local changes (commits) on branch *branch-name* to the remote named *remote-name*. The **u** parameter is needed the first time you push a branch to the remote.

Receive Changes from Remote

git pull remote-name branch-name

The **git pull** receives all your remote changes (commits) from the remote named *remote-name* and on branch *branch-name*.
