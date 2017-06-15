Git Collaboration

After you create a new project in github and sync it with your local code base, you will need to add your teammates as collaborators.


settings -> collaborators -> add collaborator (each team member);

Now have each of your team mates clone the project so they have their own local copy.

Rules Of Collaboration

* Do __not__ work in the master branch
* __Never__ work on the same files as your teammates (communication is key)
*  __Always__ pull before your push.

I am in master branch, I have been tasked to implement a Navbar. Here is my workflow.


( on master branch )
`git status  // nothing to update`
`git pull origin master // ensure you are in sync with remote`
`git checkout -b navbar // make navbar branch and switch to it`
Do your work and create some code
`git add -A // add your code to staging`
`git commit -m 'nav bar implemented'`
`git push origin navbar //SUPER important you push to the branch, not master`
`git checkout master // back to master branch`
`git pull origin master // always pull from remote, in case new code has been added`
`git merge navbar //bring your navbar code into master`
`git add -A`
`git commit -m 'msg'`
`git push origin master`
