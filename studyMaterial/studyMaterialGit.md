# Study Materials

## Table of contents
-Versions control system
-What is Git?
-Git Commands
-Rebase and Squash
-Git Rebase VS Git Merge
-Git branching strategies and flows
-Bibliography

## Content

### Versions control system:
Version control system keeps track of all code modifications in a special type of database. If a mistake is made, developers can go back in time and compare previous versions of code to help resolve the mistake, while minimizing disruption to all team members, in addition, the development efficiency is greatly increased.

### What is Git?
It is the most widely used modern version control system in the world. Git is a mature and actively maintained open source project originally developed by Linus Torvalds. 
With it we can maintain a complete version history, it has a working system with branches capable of adding, removing or returning to the content of the branches.


### Git Commands
git clone <https://name-of-the-repository-link>

Download existing source code from a remote repository

git branch <branch-name>

Create a branch locally

git push -u <remote> <branch-name>

To push the new branch into the remote repository
git branch or git branch --list

Viewing branches
git checkout <name-of-your-branch>

Switch from one branch to another
git status

Gives us all the necessary information about the current branch.
git add <file>

To add a single file
git add -A

To add all the files.
git commit -m "commit message"

setting a checkpoint in the development process which you can go back to later if needed. We also need to write a short message to explain what we have developed or changed in the source code.
git push <remote> <branch-name>

After committing your changes, the next thing you want to do is send your changes to the remote server. Git push uploads your commits to the remote repository.
git pull <remote>

The git pull command is used to get updates from the remote repository.
git merge <branch-name>

Git merge basically integrates your feature branch with all of its commits back to the dev (or master) branch.


### Rebase and Squash 
It is a way to join all the commits into one and then rebase to join them to the main branch, in this way there is a more organized branch to look at the commits later.

To combine multiple commits, we need to know either the number of commits we want to combine or the hash.
shell-
git rebase -i [your hash] or git rebase -i HEAD~(number of commits to see)
-shell
Once the command is executed, a text editor opens, where we will have the commits first, in order of time as they were created, that is, the oldest at the beginning.
   You can see pick (p) which means that this commit will remain in the history or add squash(s) which means that this commit will be merged with the previous one.
Once we close the text editor, the changes will take place and we can git push.

### Git Rebase VS  Git Merge

The biggest advantage of rebasing is that it can be used to achieve nicer, linear sequence of commits. The repository's commit history / log will be much clearer if you just use rebase.

Merge                                                                                             
-Git merge is a command that allows you to merge branches from Git
-In Git Merge logs will be showing the complete history of the merging of commits.
-All the commits on the feature branch will be combined as a single commit in the master branch.
-Git Merge is used when the target branch is shared branch.

Rebase
-Git rebase is a command that allows developers to integrate changes from one branch to another.
-Logs are linear in Git rebase as the commits are rebased.
-All the commits will be rebased and the same number of commits will be added to the master branch.
-Git Rebase should be used when the target branch is private branch.

### Git branching strategies and flows

In the Git flow workflow, there are five different branch types:
Main
The purpose of the main branch in the Git flow workflow is to contain production-ready code that can be released.

Develop
The develop branch is created at the start of a project and is maintained throughout the development process, and contains pre-production code with newly developed features that are in the process of being tested.

Feature
The feature branch is the most common.It is used when adding new features to your code. When working on a new feature, you will start a feature branch off the develop branch, and then merge your changes back into the develop branch when the feature is completed and properly reviewed.

Release
The release branch should be used when preparing new production releases. Typically, the work being performed on release branches concerns finishing touches and minor bugs specific to releasing new code, with code that should be addressed separately from the main develop branch.

Hotfix
The hotfix branch is used to quickly address necessary changes in your main branch.
The base of the hotfix branch should be your main branch and should be merged back into both the main and develop branches. Merging the changes from your hotfix branch back into the develop branch is critical to ensure the fix persists the next time the main branch is released.


## Bibliography

https://www.atlassian.com/es/git/tutorials/what-is-version-control

https://www.freecodecamp.org/news/10-important-git-commands-that-every-developer-should-know/

https://www.atlassian.com/es/git/tutorials/what-is-version-control

https://www.freecodecamp.org/news/10-important-git-commands-that-every-developer-should-know/

https://medium.com/@slamflipstrom/a-beginners-guide-to-squashing-commits-with-git-rebase-8185cf6e62ec

https://www.gitkraken.com/learn/git/git-flow
