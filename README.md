# gitall
git init
git config --global user.name "sivachanikyamiriyala"
git config --global user.email sivachanikyamiriyala@gmail.com
git config --global --list
git remote add origin https://github.com/sivachanikyamiriyala/gitall.git
git push -u origin master(To push only master branch)
git push origin --all(to push all the branches)
1.Branching:This is the feature of git where developers can create separate functionalities on different branches and later merge th              em with the master branch this helps in creating the code in unclustered and organised way
 a)To see the list of all local branches
   git branch 
 b)To see the list of all local and remote branches
   git branch -a
 c)To see the list of all remote branches  
   git branch -r
 d)To create a branh
   git branch branchname
 e)To create a branch and automatically move into that branch
    git checkout -b brahcname
 f)To delete a branhc
   git branch -d branchname
 g)To delete a remote branch in github
   git push origin -d branchname
 h)Ti delete a remote branh in local repo
   git branch -rd origin/branchname
 i)soft and hard delete
   git branch -d branchname(after merging deleting)
   git branch -D branchname(the branch is deleted before merging)

2.Merging:The commits taht are present on the branch are moved into the master branch as per the time stamp of the commits made
             
3.Rebasing:
4.CHECKIN  
  a)git push:
5.CHECKOUT OUT
  a)git clone:This will download the entire github repo irrespective of whether that code already present on out local machine or not

  b)git fetch:This will work when there are some differnes betweeen the code present in your local repo and remote repo git fetch will              download the modified files and save them on a remote branch.we can checkout to that remote branch and the modifications              are acceptable then we can merge that remote branch with master branch

  c)git pull:This will also work only when there are changes b/w remote github and local repo.It will download only the modified files             and merge them with the master branch  
               (fetch+merge=pull)


6.Rebasing:
  a)Thsi is used for fast forward merge This helps in scenarios when ever a new feature is developed on the branch if you want to incl    ude that new feature on the top of the commit history of the master branch
  b)We can change the  commit history
    git rebase -i HEAD~4
7.Cherry-picking:In both merge and rebase all the comits are moved into master branch but in cherry-pick we are seleteing a particular
                 commitId       (git cherry-pick commitid)
8.Git stash: The files that are present in stagging area ,untracked sectiona and .gitiginore can be left over and we can start the new  functionality 
  The advantage is unfinished functionality can be left over and we can start the new functionality
  git stash  ----->The files present in staggig area can be hidden
  git stash -u ---->the files presetn in untracked and stagging area can be hidden
  git stash -a  ---->The files present in untracked ,stagging,.gitignore can be left over
  git stash pop --->To bring the latest stash to be popped out
  git stash list  -->To list all the stashes
9.git squash:Multiple commits can be made as one single commit using git rebase command
10.Tagging:Tagging is generally used for placing bookmarks on the comits .These are generally given for important commits and relea               se of the software
  git tag tagname        ---------------------------->light weight tag
  git tag   ----------------------------------------->to list the tags
  git tag -a tagnaem -m "message" comitid         --->Anoted tag name
  git push --tags        ------->To push all the tags
  git tag -d tagname   --------->to delete a tag in locla repo
  git push origin :tagname  --->to delte a tag im github
