This command is used to change the default branch name
"git config --global init.defaultbranch <name>"

This command is used to check whether the folder you are present is a git repository or not. It also shows which files in your repository are untracked.
When changes to the files has been made and this command is used again.It tells the user which files have been modified and have not yet been committed 
"git status"

This command is used to initialize the repository you are present in as a git repository i.e. git will keep track of this repository. Also this command creates a folder .git which is usually hidden from the user 
"git init"

The following command is used to display or show the .git folder 
"ls -la"

This command is used to change the name of a branch
"git branch -m <name>"

The following command is used to distinguishh between a folder and a file. 
"ls -l"

The workflow of commit is as follows:
write - add - commit 
Description: 
"git init"
Made the directory as a git repository. 
Added the .git to the repository for tracking 
"git add"
This command is used to add the files/folder in a staging area. 
Staging area means the repositories are ready to be tracked but not yet tracked. It's like people are standing on the stage to perform but not performing yet. It is the place where the files are kept before commiting.
The followning are the ways to use the git add command:
git add <filename> - used when you need to add only specific files
git add . - used to add all files.

Just likw we use the "git add" command to move the files to the stating area. The "git rm --cached <filename>" command is used to unstage files/folders.

After adding the files to the staging area the following command is used to commit the changes.
"git commit -m (commit message)"
The -m is like a flag i.e. it marks as the command is commit and not any other command

Note: Remember that when using the git add command always provide the file extensions of the file you are going to add. For example: git add one.txt

To see all the commits made the following command is used
"git log" 
To see the log details in a single line the flag "oneline" is used:
"git log --oneline"

Note: Flags are like additional features or attributes of a git command which are used to use the command in multiple ways.

To chaneg the code editor in yout system to vscode. The following command is used 
git config --global core.editor "code --wait"

While commiting if you forget to add the -m flaf git opens an editor file where you can add the commit message. The type of file being opened can depend on the code editor. After adding the commit message you need to save the file and close the file. By doing this the commit message has been added and the commit command has been executed.

The .gitignore folder is an in-built folder which is used to include the files whicn you as a user need to ignore. Suppose when working with thousand of files there will be some files where minute chnages will occur which will result in git to trigger. To avoid this from happening the .gitignore folder is used which includes all the files/folder you need to ignore. However changes made to the .gtignore file will be needed to commit.

For future purposes when empty folders are created the .gitkeep file is created to avoid empty folder from tracking. It prevents git from tracking empty folder. For example A folder named images is created in that folder .gitkeep file is created. Now what this will do is whenever an empty folder is created git will not be triggered instead it will only track the images folder and never an empty folder.

A branch is like a seperate copy of your project's timeline where you can work on changes without affecting the main version of the project.
Its like a writer has published his book but when need to add another chapter or to correct some mistakes he/she does not work on the published version but on a copy of the published version.

The command "git branch" tells you on whicb branch you are present currently. It also lists down all the branches just like git log 
To create a new branch the command "git branch <branch_name>" is used.

After you have created a new branch the command git switchh <branch_name> is used to switch to the newly created branch.

Note: Files/folders created in the alternate branch are only present in the alternate branch. After switching to the main branch all files created will disappear.

The following command is used to do both tasks i.e. branch creation and branch switching at the same time.
"git switch -c (branch_name)"

The following commad checks whether the branch exists or not. If exists switches to it if not returns an error.
"git checkout (branch_name)"

When you need to work with files from another branch or need files/folders from aother branch the follwing command is used.
git merge (branch_name from where you need to get the files/folders)

When merge conflicts occur the to abort the merge the follwoing command is used:
git merge --abort 

To remane a branch the following command is used
git branch -m <old-branc name> <new-branch name>

In order to delete a branch the following command is used
git branch -d <branch-name>

"git diff" is an informative command used to compare between two files in staging area or branches or commits.
It has certain flags which are used for comparison.
For example: "git diff --staged" is used to compare a file that is in the staging area from x point to y point
"git diff (branch_one name) (branch_two name)" this command is used to compare two branches 
Another syntax for this is "git diff (branch_one name)..(branch_two name)"
"git diff <commit-id-1> <commit-id-2>" is usedto compare specific commits as per the provided hash code 
Another way to do this is "git diff <commit-id-1>..<commit-id-2>"

A stash is a temporary storage area where Git saves your uncommitted changes so that your working directory becomes clean again.
Think of it as putting your unfinished work into a locker.
"git stash"

You can also add a message to your stash by using the following command
"git stash save "your_message"

To list all your stash you can use the following command:
"git stash list"

To apply specific stash you can use the following command:
"git stash apply stash@{number}"

To restore and stashed work and to remove the stash from the stash list use the following command:
"git stash pop"

To drop a specific stash i.e. to remove a specific stash the following command is used:
"git stash drop stash@{number}"

You can apply stash to a particular branch by using the following command:
"git stash apply stash@{number} <branch_name>"

To clear or remove all stashes at once use the command:
"git stash clear"

A tag is like a bookmark. No matter what happens a tag remains where it has been placed.
It can be used to add extra information to it
"git tag <tag-name>"

To add an additional message along with tag the following command is used:
"git tag -a <tag-name> -m <your-message>"

To list all tags the following command is used:
"git tag"

Note: when a tag has been placed to a specific commit you can view it using the git log --oneline command as it shows the tag along with the commit message

To delete a tag you can use te following command:
git tag -d <tag-name>

Note: They are mainly used when an important versions of a software or application or anything are released

Git rebase is a command that takes your branch's commits, creates new copies of them, and places them on top of another branch to create a clean, linear commit history.
Rebase moves your work to the latest version of another branch by replaying your commits as new commits.
"git rebase <branch-name>"

For precise log history the following command is used it is similary to git log but more precise.
"git reflog"

To get precise details of a specific commit the same command is used along wiht the commit ID or hash code
git reflog <commit-ID>
