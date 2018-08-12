# Git

Git is a very powerful tool, but it can also be very confusing at first.
Below are some commands that are very useful:

```
git status
```

This command is your friend. Type it out whenever you get stuck and try to go through the
messages git provides. If something doesn't make sense, copy that line and
google it. The chances are someone else probably was confused by that same line before
and there is some sort of explanation of what it means and what to do next.

```
git --no-pager diff
```

It is useful to run this command before you add the changes. It'll show you all of your updates
and you can double check that everything looks good before you commit it.

Once you're done making the updates, add and commit the changes. This is an
important step, if you don't commit your changes, you'll lose all of your newly written
code.

**the code below assumes you're working on master branch and committing to master branch directly**

```
git add .
git commit -m "message describing your work"
```

To get the latest updates from the github from the master branch do:

```
git pull origin master
```

If you have any conflicts:
  - open the files that have problems in them and go through the code
  - by the time you're done with resolving the conflicts, you should not have the `<<<<<< HEAD ... >>>>>>> branch-a` lines
  in any of the files
  - then add the updates that you've made and commit the changes
  ```
  git add .
  git commit -m "resolve merge conflicts"
  ```

Now you're done with pulling the updates from github and you have all of the
updates from master as well as your newly written code locally.

Next step would be to push the updates back to github, so other team members can see the new changes.

```
git push origin head
```

Another great command which allows you to see the history of commits:

```
git log
```
