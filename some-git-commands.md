# Git Branches!

## Links

Read this tutorial first:
https://guides.github.com/activities/hello-world/

This is how you set Sublime Text as your default text editor for Git
http://stackoverflow.com/questions/8951275/how-can-i-make-sublime-text-the-default-editor-for-git


## Part 1: Branches
- Create a GitHub repo
- Clone the repo locally
- Create file, put some content in it
- Create new branch
  `git branch new-1`

- Switch to new branch
  `git checkout new-1`

- Open existing file, change it
- Add and commit changes (you can't switch branches without doing a commit first)
- Switch back to master, see how file changed
- Switch back to new-1
- Now we're going to create a copy of this branch up in GitHub
  `git push -u origin new-1`

- Look at new branch in GitHub

## Part 2: Creating a repo, invite others (do this with a partner)
- Inviting others to collaborate:
  - Under setttings > Collaborators add collaborator (using their email or GitHub user name)
- Have your partner create their own branch on their computer, then push it up to GH
  `git push -u origin [branch-name]`

- Now get your partner's branch locally:
  Viewing the branch (you can't save changes):
  `git checkout origin/[new-branch-name]`

  duplicating it locally (so you can save changes):
  `git checkout -b [local-new-branch-name] origin/[new-branch]`

  merging into master:
  `git checkout master`
  `git merge [local-new-branch]`

- Have your partner make another change to their branch, create a pull request
- Get the pull request (you'll get an email notification), accept and merge changes

## Part 3: Collaborating on another's repo
- Have your partner create a repo and invite you (following the steps above)
- Accept the invitation
- Clone the repo locally, create new branch, push
- Make a pull request

## Part 4: Merge conflicts
- Edit file in GH
- Edit same file locally, add, commit
- Do a git pull
- *** MERGE CONFLICT!!! ***
- Open the file and see what it looks like
- Make the file look like you want it to look, then add and commit again
