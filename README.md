**Git is a distributed version control system that tracks versions of files.** 
**It is often used to control source code by programmers collaboratively developing software.**

**Github on the other hand is a developer platform that allows developers to create, store, manage and share their code. It uses Git software, providing the distributed version control of Git plus access control, bug tracking, software feature requests, task management, continuous integration, and wikis for every project.**

**This is a well documented cheat sheet that covers all you need to know about git and github.**

**To get started, I would recommend the installation of git through this link: https://git-scm.com and launch git bash.**

**The basic syntax that I used to prepare this cheat sheet goes like this:**


**TASK TO COMPLETE:**
**command goes here**

**May we begin? of course we can! :smile:**


# GIT CHEAT SHEET

### TO CHECK GIT VERSION:
**git --version**

### GLOBAL CONFIGURATION FOR USER:
**git config --global user.name "your username"**


**git config --global user.email "your email"**
>[!NOTE]
> Use global to set the username and e-mail for every repository on your computer.
> If you want to set the username/e-mail for just the current repository, you can remove 'global'.

### TO CREATE A NEW FOLDER FOR YOUR PROJECT:
**mkdir projectname -> makes a new directory**


**cd projectname -> changes the current working directory**
>[!TIP]
>If you already have a folder/directory you would like to use for git; navigate to it in the command line, or open it in your file explorer, right-click and select 'Git Bash here'.

### INITIALIZE GIT:
**git init**

### TO LIST THE FILES IN CURRENT WORKING DIRECTORY:
**ls**

### TO SEE IF A FILE IS PART OF YOUR REPOSITORY:
**git status**

### TO ADD A FILE TO STAGING ENVIRONMENT (Make sure to input the filename or use 'git add .' to add a recently created file):
**git add filename**

### TO ADD ALL FILES IN CURRENT DIRECTORY TO STAGING ENVIRONMENT:
**git add --all**
>[!NOTE]
> The shorthand command for git add --all is git add -A

### TO COMMIT STAGING ENVIRONMENT TO YOUR REPOSITORY WITH A MESSAGE:
**git commit -m "message written here"**

### TO SEE FILE CHANGES IN A MORE COMPACT WAY:
**git status --short**
>[!IMPORTANT]
> Short status flags are:
> ?? - Untracked files
> A - Files added to stage
> M - Modified files
> D - Deleted files

### TO MAKE A COMMIT WITHOUT STAGING:
**git commit -a -m "message about the updated file"**
>[!TIP]
> The -a option will automatically stage every changed, already tracked file.

>[!WARNING]
> Skipping the Staging Environment is not generally recommended. Skipping the stage step can sometimes make you include unwanted changes.

### TO VIEW HISTORY OF COMMITS FOR A REPOSITORY, USE THE LOG COMMAND:
**git log**
>[!TIP]
> Using git reflog gives you a history of local commits.

### TO AVOID THE VERY LONG LOG LIST, AND GET JUST ONE LINE PER COMMIT:
**git log --oneline**

### HAVING A HARD TIME REMEBERING COMMANDS? USE GIT HELP:
**git commandname -help  (gives you all available options for a specific command. Note to replace 'commandname' with the specific command name) - For Example; git commit -help**
>[!TIP]
> You can also use --help instead of -help to open the relevant git manual page.

> Use git help --all to see all possible commands
> [!WARNING]
> This will display a very long list of commands

>[!TIP]
> If you find yourself stuck in the list view, use SHIFT + G to jump to the end of the list, then q to exit the view.

### TO CREATE A NEW BRANCH:
**git branch branchname**
**(replace branchname with the specific name of the branch you wish to create. E.g; git branch dev - with dev being the branch name.)**

### TO CONFIRM NEW BRANCH CREATED:
**git branch**

### TO MOVE CURRENT WORKSPACE FROM MASTER BRANCH TO A NEW BRANCH:
**git switch branchname**
**(You can also use checkout, but I prefer switch)**
>[!NOTE]
> Using the -b option (e.g; git switch -b branchname) will create a new branch, and move to it if it does not exist.
> 'git branch -c branchname' will create a new branch but not switch to it.

>[!TIP]
> You can also use 'git switch -c branchname' to create and immediately switch to a new branch.
> Remove the -c option if the branch already exists.

### TO SWITCH BACK TO THE MASTER BRANCH:
**git switch master**

### TO CREATE A NEW BRANCH TO DEAL WITH EMERGENCIES:
**git checkout -b emergency-fix (it will switch to a new branch called emergency fix, you can give it any name you want)**

### TO MERGE TWO BRANCHES, FIRST SWICTH TO THE MASTER BRANCH AND THEN USE:
**git merge newbranch (replace 'newbranch' with the name of the branch you want to merge)**

### TO DELETE A BRANCH:
**git branch -d branchname**



## USING GIT & GITHUB
**Okay, create a repository on github before you continue**

### TO ADD A REMOTE REPOSITORY WITH THE SPECIFIED URL:
**git remote add origin URL (The 'URL' will have a .git extension which you can get from your already created repository)**

### TO PUSH MASTER BRANCH TO THE ORIGIN URL(GITHUB) AND SET IT AS DEFAULT:
**git push --set-upstream origin master**
>[!NOTE]
> If you use github instead of origin, it will still work.

### TO GET ALL THE CHANGE HISTORY OF A TRACKED BRANCH/REPO:
**git fetch origin**

### TO COMBINE A CURRENT BRANCH (MASTER) WITH A SPECIFIED BRANCH (ORIGIN/MASTER):
**git merge origin/master**

### TO PULL ALL CHANGES FROM A REMOTE REPOSITORY INTO THE BRANCH YOU CURRENTLY WORKING ON (This is more like a combination of fetch and merge):
**git pull origin**
[!NOTE]
> This will also update local git.
> While working on a new branch, you can use 'git pull' to pull from your local repository so that your code is updated.

### MAKE CHANGES TO LOCAL GIT AND PUSH THEM TO REMOTE ORIGIN ON GITHUB:
**git push origin**

### CREATE A NEW BRANCH ON GITHUB:
**On github, access your repository and click the "master" branch button. Then you can create a new branch. Type in a descriptive name, and click 'Create Branch'**

### TO LIST ALL LOCAL AND REMOTE BRANCHES OF THE CURRENT GIT:
**git branch -a**
>[!NOTE]
> branch -r is for remote branches only.

### TO PUSH A NEW BRANCH FROM LOCAL REPOSITORY TO GITHUB:
**git push origin branchname**




# GIT CONTRIBUTE
**An aspect of git that allows for collaboration.**

## FORK A REPOSITORY:
**A fork is a copy of a repository. This is useful when you want to contribute to someone else's project or start your own project based on theirs.**
**Fork is not a command in Git, but something offered in GitHub and other repository hosts.**
**You can see it on the top right side of a repo**

### CLONE A FORK FROM GITHUB:
**A clone is a full copy of a repo, including all logging and versions of files.**

**How to clone:**
1. Move back to the original repository, and click the green "Code" button to get the URL to clone.

2. Open your git bash and clone the repository using; git clone URL (remember to enter the correct URL of the repo)
>[!TIP]
> To specify a specific directory to clone to, add the name of the directory after the repository URL, like this:
> git clone URL directoryname

3. Make changes and push the changes to your Github fork.



# GIT IGNORE
**Git can specify which files or parts of your project should be ignored by Git using a .gitignore file.**
**Git will not track files and folders specified in .gitignore. However, the .gitignore file itself is tracked by Git.**

## CREATE .gitignore
**To create a .gitignore file, go to the root of your local Git, and create it by using the command:**
**touch .gitignore**
>[!NOTE]
> If the touch command is not installed in your cli, you can also create the .gitignore file locally in your text editor

### STEP BY STEP PROCESS USING A BASIC EXAMPLE
>[!NOTE]
>This is just an example to give you an idea of how to use gitignore

**Open your .gitignore file using your text editor**

**We are just going to add two simple rules:**
1. Ignore any files with the .log extension
2. Ignore everything in any directory named temp

**Example:**
**# ignore ALL .log files**
***.log**

**# ignore ALL files in ANY directory named temp**
**temp/**
**Now all .log files and anything in temp folders will be ignored by Git. You can also add whatever files you want ignored there**

>[!NOTE]
> In this case, we use a single .gitignore which applies to the entire repository.
> It is also possible to have additional .gitignore files in subdirectories. These only apply to files or folders within that directory.




# GIT UNDO: An aspect of git that allows you to reset, revert and ammend commits in a repository. 

## GIT RESET
**Reset is the command we use when we want to move the repository back to previous commit, discarding any changes made after that commit.**
**To reset our repository back to the specific commit, use:**
**git reset commithash (please check next line to understand this syntax well)**
>[!IMPORTANT]
>The commithash is the first 7 characters of the commit hash found in the log

>[!WARNING]
>Messing with the commit history of a repository can be dangerous, it's more advisable to make those changes to your local repository and avoid making changes that rewrite history to remote repositories, especially if others are working with them.

### GIT UNDO RESET
**Even though the commits are no longer showing up in the log, it's not removed from Git.**
**If you know the commit hash, you can reset to it using the same command:git reset commithash**
**And then check the log again to see those changes**


## GIT REVERT
**Revert is the command we use when we want to take a previous commit and add it as a new commit, keeping the log intact.**
**We revert the latest commit using git revert HEAD (revert the latest change, and then commit), adding the option --no-edit to skip the commit message editor (getting the default revert message)**
**This is the syntax:**
**git revert HEAD --no-edit**
>[!NOTE]
>To revert to earlier commits, use git revert HEAD-x
>(x being a number. 1 means going back one more, 2 means going back two more, etc)


## GIT AMMEND
**commit --amend is used to modify the most recent commit.**
**It combines changes in the staging environment with the latest commit, and creates a new commit. This new commit replaces the latest commit entirely.**

**To use git amend, make a commit, check the log and then run this command:**
**git commit --amend -m "new message"**

>[!WARNING]
>Messing with the commit history of a repository can be dangerous, it's more advisable to make those changes to your local repository and avoid making changes that rewrite history to remote repositories, especially if others are working with them.

### GIT AMEND FILES
**Adding files with --amend works the same way as above. Just add them to the staging environment before committing.**




**I hope this repository has helped you in your next journey into version control as a developer. I would love and appreicate feedbacks.**

**I would also appreciate stars and follows on this repo and my profile (github.com/XBanTs) and also feel free to share.**
**I'm avaialable on social platforms like X(Twitter) through the user: @XBanTs_**
**Let's connect and innovate, cheers!** 
**By Ayo "XBanTs" Oyewo.**
