# plural sight Notes
## This is a repository dedicated to my notes from plural sight course with Aaron Stewart on git fundamentals
The course begins by explaining what Git is, Git is a version control System. In simple terms this means you can track every change you made to your file/ code. You can see who changged it, when they changed it and what was changed. Something super important to remember about Git is that it's Explicit- meaning it requires your explicit instruction and will not do anything you do not tell it to do, so if you don't tell it to track a version of a file it won't.

Therefore... DON'T FORGET TO SAVE YOUR FILES BEFORE YOU CHANGE THEM. This way you can actually see the different versions.

Some of the other benefits of GIT is that if you mess up something in your code you can go back to an earlier version of that project to fix it, this can save you alot of time. Also using Git you can easily collaborate with others without stepping on each others toes because you guys each have you own copy of the code and you can check it before merging it together.

## Branches

you can also use Branches; when you use branches you can esssentially work on features on different timelines of your project. for example say you want to test a new information gathering feature but you want to test it first. You can create a branch where you can test that without interrupting the main project or having any new updates you're already confident moving on with interrupting the feature you're testing.

git push -u origin main for example would push the updates you've made to the Main branch of your project. If you don't want to push it to the main branch but instead a different branch you would just need to change the location from 'Main' to the name of the branch yu'd like to push the update to. (given you've done all the proper steps leading up like initializing the repo, commiting the files to the staging area etc.)
(note to self: follow up on how to switch branches inside command line)

## Remote Repositories 

There is also a command called git fetch which can "fetch" or retrieve changes made in other repositories, for example if someone is working on a different branch of the project while you are also working on the project you can fetch their updates to see what their doing and ultimately decided if you want to integrate it into your repository.

Git pull- retrieves and integrates the changes from other repositories (which may cause some bugs and it will be your job to fix them)
git clone- copies an entire repository into a new .git directory

## Git Clone

git clone = making a copy of a project to work on your own version/ local network no one will see it until you push it
you can use the link you find inside github under the code section in a repositiory grab the link and use git clone followed by that link to copy the code onto your local network to work on the projec as well. If you want you can push the change back up in the form of a commit but you don't need to use -u because the repositiory is already linked when clone the network at the start

## What is git Remote

In Git, a remote is like the connection between your project and your collaboration partner's project on the internet 

 When you use git remote add, you’re saying “here’s where my friend’s project lives on the internet.” Setting up a connection so you can send and receive changes.
(git push): If you make some changes to your project and want to share them, you use git push. This sends your changes to the remote project (like mailing your updates).
Getting Changes (git pull): If your partner makes changes to the project and you want to see them, you use git pull. (like getting a letter back with your partners updates).

## Merge Conflicts

what is a merge conflict? This occurs when there are conflicting changes being introduced to the same contents in the same file. 
examples:
when more than one person changes the same line in a file and tries to merge the change to the same branch

when someone deletes contents in a file but another person edits the content thats deleted and they both try to merge to the same branch

when this occurs git doesn't know which change to follow so it sends a merge conflict notification to the second person who tries to merge and they need to give directions to which information to follow and which to ignore

## Git Reset: three options + How to undo a git reset

Git reset is like an undo button for your project, but it comes in three different strengths: soft, mixed, and hard. Each one undoes more than the last

git reset --soft
This is the gentlest reset. Use --soft when you want to uncommit your changes but still keep them ready to commit again

git reset --mixed: Undo the commit, unstaged changes stay in your files.

git reset --hard: Undo the commit and erase changes from your files.
(note to self: need a clearer understanding on the different use case between git reset (default) and soft)

Git keeps a log of everything, including things you've "undone" with a reset. use the reflog to find your lost commit. "git reflog" is the command 
(further explore git reflog because it looks like there could be additional steps)
