# Git Lab


## Tracking Files

### What is .git?
A folder automatically created once a git repository is initialized using "git init". It's a hidden folder (starts with .) and contains all the necessary information to help git do its job (track changes, manage history, etc.).

### What is the status of an added file?
The file is now ready to be commited, therefore it's marked as modified by git and is now in the staging area.

### Why does diff show nothing after staging changes? what to do to see the diff result?
Becuase the default for the git diff command is showing the unstaged changes. When staging, to see changes, one should use git diff --staged


### How many characters of the commit identifier can you get away with typing at a minimum?
Usually it's 7, but i got away with 4 (that might not work if there are more commits, because there might be collisions with other commits the smaller the ID gets)

### Difference between git rm and rm:
git rm not only deleted but also added the changes to the staging aread.
Whereas rm just deletes the file, and the change is not staged. You'd have to do that manually.


### Difference between git mv and mv
Status looks like one file was deleted and waiting to be staged, and a new one was created as untracked file.
So i can't commit now.
If we want git to understand that this was a rename we have to use "git add -A" using content similarity.

### --stat
shows change stats per file in log, show and diff

## Git Branches

