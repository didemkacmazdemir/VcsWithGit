# VcsWithGit
Git is a version-control system for tracking changes in computer files and coordinating work on those files among multiple people.
Git takes you and your friend changes are maded by independently and merges them to a single “Master” repository.
What is a Repository ?
repo is nothing but a collection of source code.

working directory - (Git Add) -> Staging Area - (Git Commit) -> Local Repo(HEAD) - (Git Push) -> Remote Repo(MASTER)

(            From local to working directory <- Git Merge                      )  ( from remote to local <- Git Fetch )
(                                             <- Git Pull <-                                                          )
1-) git add : is a command used to add a file that is in the working directory to the staging area.
2-) git commit : is a command used to add all files that are staged to the local repository.
3-) git push : is a command used to add all committed files in the local repository to the remote repository. 
So in the remote repository, all files and changes will be visible to anyone with access to the remote repository.
4-) git fetch : is a command used to get files from the remote repository to the local repository but not into the working directory.
Git gathers any commits from the target branch that do not exist in your current branch and stores them in your local repository. 
However, it does not merge them with your current branch
5-) git merge : is a command used to get the files from the local repository into the working directory.
To integrate the commits into your master branch, you use git merge.
6-) git pull : is command used to get files from the remote repository directly into the working directory. 
It is equivalent to a git fetch and a git merge .
git pull automatically merges the commits without letting you review them first.

Git Introduce yourself
git config --global user.name "YOUR_USERNAME" 
git config --global user.email "im_satoshi@musk.com"

*****From Local To Remote Repo*****
Create a folder for pulling created git repo
1-) cd Desktop/MuskCult 
2-) touch README.md    # To create a README file for the repository
3-) git init           # Initiates an empty git repository

Add files to the Staging Area for commit:
1-) cd Desktop/MuskCult 
2-) git add .  # Adds all the files in the local repository and stages them for commit **OR** git add README.md # To add a specific file

Before we commit let’s see what files are staged:
1-) cd Desktop/MuskCult 
2-) git status # Lists all new or modified files to be committed

Commit Changes you made to your Git Repo:
1-) cd Desktop/MuskCult 
2-) git commit -m "First commit"# The message in the " " is given so that the other users can read the message and see what changes you made

Uncommit Changes you just made to your Git Repo:

1-) git reset HEAD~1# Remove the most recent commit# Commit again!git reset HEAD~1# Remove the most recent commit# Commit again!


Add a remote origin and Push:
Now each time you make changes in your files and save it, it won’t be automatically updated on GitHub. 
All the changes we made in the file are updated in the local repository. Now to update the changes to the master:

1-) git remote add origin remote_repository_URL # sets the new remote
2-) git remote -v # List the remote connections you have to other repositories.
3-) git push -u origin master # pushes changes to origin Now the git push command pushes the changes in your local repository up to the remote repository you specified as the origin.

See the Changes you made to your file:
1-) git diff # To show the files changes not yet staged

Revert back to the last committed version to the Git Repo:
Now you can choose to revert back to the last committed version by entering:

1-) git checkout . **OR** git checkout -- <filename> #specific file

View Commit History:
1-)git log
**** From Remote to Local ****

Cloning a Git Repo:
1-) git clone remote_repository_URL

Each time you make some changes and push it into the master repo, your friend has to pull the changes that you pushed into the git repo
Meaning to make sure you’re working on the latest version of the git repo each time you start working, a git pull command is the way to go.
2-) git pull origin master

.gitignore tells git which files (or patterns) it should ignore. 
It's usually used to avoid committing transient files from your working directory that aren't useful to other collaborators, 
such as compilation products, temporary files IDEs create, etc.
