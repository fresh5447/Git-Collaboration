# Git Collaboration
__Working with teams in GIT__

## ✌️ when it works

## 🔥 when it doesn't

----

#### Inviting Team Members

After you create a new project in github and sync it with your local code base, you will need to add your teammates as collaborators.


settings -> collaborators -> add collaborator ( each team member 🤓 );

Now have each of your team mates clone the project so they have their own local copy.

---

#### Rules Of Collaboration
Yes there are only 3. Miss one and you will find yourself in a dark situation. 💩

* Do __not__ work in the master branch
* __Never__ work on the same files as your teammates (communication is key)
*  __Always__ pull before your push.

----

#### Avoiding Conflicts

If you code in the `master` branch, or work on the same files as your team mates, you will run into a merge conflict. GIT becomes confused and is not sure which code is the correct code to use.

It will ask you to fix the merge conflict, basically which code should we use for master.

These aren't bad if it is a couple lines of code in a file. But these can be nightmarish if you cluelessly code away and disregard consequences. 💀


----

#### GIT Pull

So far you have been the only one pushing code up to your remote repository. When others push code up to the remote repository, your local code base becomes out of sync. This is what pull is used for.

`git pull origin master` will pull any code from the remote branch that you don't have locally. It's basically the opposite of push.

When team mates add code to the repo, you need to git it into your local code base. Always pull before you push to help avoid conflicts.

__local__ is your code  that you have on your machine.

__remote__ is the code that lives up at Github.com

---

#### Implementation Example

I am in master branch, I have been tasked to implement a Navbar. Here is my workflow.


_( on master branch )_

`git status  // -> nothing to update`

`git pull origin master // -> ensure you are in sync with remote`

`git checkout -b navbar // make navbar branch and switch to it`

_(Do your work and create some code)_
```
👾 🤖 👾 🤖 👾 🤖
code code code
code code
code code code
code
👾 🤖 👾 🤖 👾 🤖
```

`git add -A // add your code to staging`

`git commit -m 'nav bar implemented'`

`git push origin navbar //SUPER important you push to the navbar branch, not master`

`git checkout master // back to master branch`

`git pull origin master // always pull from remote, in case new code has been added`

`git merge navbar //bring your navbar code into master`

`git add -A`

`git commit -m 'msg'`

`git push origin master`
