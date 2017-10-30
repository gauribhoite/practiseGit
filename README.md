This is to practice git commands.

Added README and then pushed it to remote master branch.
Checked out a new branch and then edited README again and pushed it to remote newly created branch
If you want to push local branch to a new remote branch you can do git push origin local-name:remote-name
If you want to squash commits into one then can do git rebase -i <remote_branch_that_you_want_to_rebase_against_with> eg: git rebase -i dev
While squashing/rebasing the commits if you have any merge conflicts then never do git rebase --skip as that might completely loose your commit, instead always resolve conflicts and commit it and then do git rebase--continue.
After rebasing when you try to git push then git will complain as the remote branch still has old commits but after rebasing you localbranch has replayed your branch on top 
f the branch you're rebasing against and newer commits, which remote branch has no idea of. so you can do git push --force-with-lease=<ref(remote branch name)> eg: git push --force-with-lease=rebase-br