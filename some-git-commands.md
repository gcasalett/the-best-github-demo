# Quick list of useful Git commands:

### General

Grab all changes and get them ready to commit (a.k.a. "staging" your changes):  
`$ git add -A`

Commit changes (save a snapshot in the history of your repo):  
`$ git commit -m "My commit message"`

Grab all the latest commits from the repo's source (in our case, GitHub) and merge them into your local branch:  
`$ git pull`

Push your latest commits to the source (note: this only pushes changes from the branch you are currently working on):   
`$ git push`

For safety's sake, if you're not on master, specify which branch you're pushing to:  
`$ git push origin [my-branch]`

### Branches

List local branches, see which one is active (checked out):  
`$ git branch`

Create a new branch:   
`$ git branch [new-branch-name]`

Delete a branch:   
`$ git branch -D [branch-to-be-deleted]`

Create a new branch and immediately switch to it:   
`$ git checkout -b [new-branch-name]`

Switch to another branch:  
`$ git checkout [brach-name]`

If you create a branch locally, copy it it GitHub:  
`$ git push -u origin [branch-name]`

If you create a branch in GitHub, create a local copy:  
`$ git fetch`  -> Updates your local list of branches that exist in GitHub  
`$ git checkout origin/[new-branch-in-github]`  -> This creates a preview of the remote branch. You can't edit this yet!  
`$ git checkout -b [new-branch-in-github] origin/[new-branch-in-github]`  -> The first [name] is what the branch will be called locally. The branch names should always match.

### Merging

Given two branches, merge the changes from branch-1 into branch-2. **Note:** This only works one way; in this case branch-2 will get the changes from branch-1, but branch-1 will remain unchanged:  
`$ git checkout branch-2`  
`$ git merge branch-1 -m "Merge comment goes here"`

## Some things to remember

1. After fixing a merge conflict, you always have to add and commit changes to finalize the pull/push/merge
2. When collaborating, always remember to do all your work on your own branch. Don't mess with master!
3. Sometimes you may end up in Vi (or Vim), which is a hellish text editor for the command line. This can happen after fixing a merge conflict, or if you forget to add a message to a commit or merge command. **to exit Vim**:
  - Press the escape (esc) key
  - Then type ":x" (without the quotes). This should appear at the bottom of the window
  - Press enter

## Links

This is how you set Sublime Text as your default text editor for Git (so you don't end up in Vim):
http://stackoverflow.com/questions/8951275/how-can-i-make-sublime-text-the-default-editor-for-git
