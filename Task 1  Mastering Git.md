# Task 1 : Mastering Git

##### Question 1 : What is VCS? and why it is so important?

**VCS** stands for Version Control System. This is basically the method which tells us the changes made in the source code.  So to understand this in the simple way we see what a developer or coder does -> we create things, we save things, we edit things like adding something to it or deleting something from it and then we save them again. So basically the goal is to save it again and again and how version control helps is it provides you clarity as to when and why you did it and what changes you did. Yes, it keeps track of the changes you did to the source code.

Well with what we saw by now it's very simple and straightforward for a single person and you don't need to do anything you made the change so you know when and why you did it. But what happens if there are many people working on the same/similar or adjacent file or same/similar or adjacent source code. Then the every other time you open it you'll have no idea who changed what and when and most importantly, why they changed it. With the VCS, because it keeps tracks of changes you'll know who changed whatever they changed and why they changed it. And what it does it it unifies these back together in what is called as merge. 

so we can say like there are 2 sets, one set is a change made by me and other set is the change made by any other person. so the tool handles the changes very precisely even if they are done at the same time. and if there is a need of unification of the 2 sets like there are similar changes and they need to be unified or there is a conflict so it brings up the idea to unify and this is called as merge. 

*So, **Git** is a fast and modern impletation of Version Control*

##### Question 2 : how to clone a git repository ?

Follow these steps to clone the repository :

1. From the repository, click **+** in the global sidebar and select **clone this repository** under **get to work**.
2. copy the clone command in the https protocol, if you're using SSH protocol, ensure your public key is in BitBucket and loaded on the local system to which you are cloning.
3. from a termnal window, change to the local directory where you want to clone your repository.
4. paste the command you copied from BitBucket. For example:

cloning in https:  $ git clone https://username@bitbucket.org/teamsinspace/documentation-tests.git

cloning in SSH: $ git clone ssh://git@bitbucket.org:teamsinspace/documentation-tests.git

##### Question 3 : how to pull/push to remote repository ?

To push :

1. create a new branch : 

   git checkout -b

   feature_branch_name

2. edit, add and commit your files.

3. Push your branch to remote repository :

   git push -u origin

   feature_branch_name

To pull :

​	git pull <remote> 

and it is equivalent to :

​	git fetch

​	git merge origin/master

##### Question 4 : how to check the status of repository ?

to check the status of the repository :

​	git status

##### Question 5 : how to create and switch to a branch ?

to create a branch:

​	git checkout -b <branch name>

this is the shortcut for git branch <branch name> followed by a git checkout <branch name>

then you can later add styles.

to navigate through branches:

​	use git checkout to navigate through branches 

to go to the master branch : git checkout master

to go to the other branch: git checkout <branch name>

##### Question 6 : how to connect to a remote repository ?

use  git remote add origin <remote_repo_url>



ot if the repository is already existing in a remote machine and you do not have anything in your local repository, you can just clone it - which we learned in question 2.

##### Question 7 : how to merge two branch ?

we merge 2 distinct branches to restore changes into a single branch. 

so here let's say we have 2 branches i.e. a master branch and other branch named styles.

so if we wanna merge styles into master branch, use :

​	first go to to styles branch and then merge it.

​	git checkout styles

​	git merge master

this merges both the branches.

##### Question 8 : how to resolve merge conflicts ?

when you merge two branches, sometimes there are conflicts and then you need to resolve them manually and make changes to your file to achieve the following result.

and then make a commit of conflict resolution.   

##### Question 9 : how to commit changes ?

the commit command is used to save changes to the local repository. You need to tell git explicitly which changes you want to include in a commit  before running the "git commit" command. this means that file won't be automatically included just because it was changed. instead you need to use the "git add" command to mark the desired changes for inclusion.and also the commit is not automatically pushed to the remote server, to do that we need to use git push to send it to remote server. 

​	-m <message> : sets the commit's message. Here, make sure to provide a concise description that helps 								  your teammates.

​	-a : includes all currently changed files in this commit. Here, new files/untracked files are not included.

​	--amend : rewrites the very last commit with any currently staged changes and/or a new commit 					  message.

##### Question 10 : how to stash changes ?

stashing changes is like a clipboard for your changes. 

So, let's consider you have a couple of local modifications, now if you want to work on a different thing or some urgent bug or something. you can't commit them because they are unfinished but  this is where stash comes in. It's like all the local changes have now been saved in this clipboard and you can work on something else now.

command : git stash 

now to continue from where you left off you just need to use the command "git stash pop". the "pop" flag will reapply the last saved state and at the same time delete its representation on the stash.