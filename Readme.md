# Git Lab


### Ex1

- .git is the brain of the repo. it stores everything. no .git, no repo
- in staging area ("Changes to be committed"). goes from untracked to staged
- bcz git diff by default shows the unstaged changes. when staging, to see changes, one should use git diff --staged
- usually it's 7, but i got away with 3 (might not work if there are more commits, cz there might be collisions with other commits, the smaller the ID gets.


### Ex1 - stretch

- Status looks like one file was deleted and waiting to be staged, and a new one was created as untracked file. So i can't commit now. If we want git to understand that this was a rename we have to use "git add -A" using content similarity.
- --stat shows change stats per file in log, show and diff

### Ex 2

### Ex2 - stretch

- I see file marked as unmerged
- git commit immediately after saving the file does not work.
- one should add the file to tell git that the conflict has been resolved (mark resolution)

### Ex 3

- Changes are gone from step 5
- could've used git restore file3.py
- revert creates a new commit to undo what was done, therefore preserving history whereas checkout just discards the uncommited changes
- Move HEAD to the parent of the current commit and changes are now staged, and the commit disappears
- backup current commit with new branch
- Changes of the current commit are now unstaged, when before they were staged.
- HEAD is used so that we don't we remove any commit, just un-stage commits.
- To reset the latest commit
- the default (or scope) of git reset is --mixed.
- everything in working directory and commit history is wiped
- Git uses HEAD as default
- After the commit --hard would have wiped the working changes to match the target

### Ex 3 - stretch

- git checkout -- file --> discards working tree edits and HEAD pointer still at the same place
- git revert HEAD~2..HEAD --> will do 2 revert commits , so one for file4 and one for file 5
- the files have their old content backup
### Ex 4

- yes using git checkout -b ...
- rebase master: replays the commits on top of master, so base becomes master, meaning the feature branch is rewritten to be after master
- Graph becomes linear on the feature branch, because rebase rewrites history while merge preserves histories of boths branchs and adds a merge commits
- if git --abort: repo returns to state from before the rebase, and yes i can rerun the rebase and finish properly
- the commit graph is linear
- master commits come first, the feature commits on top
- merge = non-linear graph (DAG) / rebase = linear line (history rewritten)
- squash = combine commits (fewer but bigger commits, considered as cleaner history)
- modify during interactive rebase and mark it as edit, then amend (git commit --amend)
