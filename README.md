# Repository1
Description: Learning to use git ang github
=================================================================
Git Hub
========
agenda
-------
version control(why)
different tools
github and git
case study
git features
git operation and commands

version control: creates snapshot every time we make changes
version control is the management of changes(modifying or adding) to documents, computer programs, large websites and other collection of information.These changes are usually termed as versions.
whole purpose is to go back the previous version, when we need

WHY
---
collaboration(combined contribution): collboration b/n all developer, to remove conflict real time
version control vs saving all data: cant get the diff b/n versions, saves lots of space 
Backup: always can get back to the files, takes the data from central copy in case of data loss
Analyse: can get steps of evolution of project with time line and with developername also


central version controlling vs distributed version controlling

Git: Distributed version control tool that support distributed non linear workflows by providing data assurance for developing quality software. Allows local repository that can interact with central repository.

git features
Distributed : allows local repo, every developer has a local copy of entire development history and changes are copied from one repository to another

Compatible: git is compatible with svn, svn and svk repo can be directly accessed by using svn git

Non-linear: supports non-linear development of software, includes various techniques to navigate and visualize non linear development history. It facilitates non-linear by using non-linear.

Branching: Takes only few seconds to create and merge branches, allows completely independent branches, master branch always contain production quality code

light weight: Use lossless compression technique to compress data on the client side(compress data when we commit to local repo and uncompress the data when we fetch the data from local repo to our workspace)

Speed: No need to fetch data from remote repo so fast as we are fetching data from local repo(no network I/O), git is written in c, ie is very close to machine language, so very less overhead at runtime. so very fast.

Open Source: can modify source code according to our need

Reliable: can fetch from local repo, can fetch from central repo, can ask other developer to commit their local repo and get the data from central repo

Secure: u cant deny after commit

Economic: free VC, saves money for saving the data, as we dont need the high end server and disk to store our data


Repository: A directory or storage space where your projects can live. It can be local to a folder on your computer, or it can be storage space on git hub or another online host. You can keep code files, text files, image files, you name it, inside a repository

Two types of repositories
Central repository
Local repository

Git operations and commands:

Create github repo
Install git at local machine(git for windows by using a blog)
create a directory, go inside and right click and click on (get bash here)
git bash emulator
git init (will initialise empty repository)
link local and remote repo
git remote add origin <link>
git pull origin master
git push

git status: tells you whci files are added to indes and are ready to commit

git add: lets you add files to your index

git commit: It refers to recording snapshots of the repository at a given time. Committed snapshots will never change unless done explicitly

git commit -m "message for commit" (to commit in local repo)

git add -A (to add all files in index)

git commit -a -m "committing all files in local repo"

git log

PARALLEL DEVELOPMENT

parallel development/ branching
Branches are pointers to a specific commit
Branches are of two types
Local branches
Remote tracking branches
git branch {branchName} to create a branch, contains all the files from master branch
git checkout branchName: to switch to branchName
git merge branchName (you should be in master branch, as branch is going to merge in master)
git pull= git fetch+ git merge
Rebasing
---------
git rebase master
git rebase branchName

git push to commit your work on master repository
must have some security, so that everyone cant commit their code
so for pushing the changes we need to connect with ssh
connect to ssh
ssh-keygen on your git bash
go to setting>SSH and GPG key
copy the key and create a new ssh key
ssh -T git@github.com : for newly created key authentication
git push origin branchName: to commit whole branch to central repository
git push origin master
to revert back
git checkout <firstEightDigitFromLogHash> fileName
