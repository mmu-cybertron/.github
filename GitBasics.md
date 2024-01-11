# Git Basics

Use GitHub Desktop (<https://desktop.github.com/>) if you don't want to use command line

## 0.0 Clone a new repo/ existing repo (first time setup will ask to sign in)

``git clone https://github.com/mmu-cybertron/<repo name>.git`` (clone upstream repo to local)

## 1.0 Move into that directory

``cd <repo name>``

``git pull`` (update local repo with upstream)

## 2.0 Make your changes/ new files inside that directory

## 3.0 Committing

### 3.1 Staging

``git status`` (check changes to be committed [always check status to reconfirm])

``git restore <file>`` (restore changes to original state/before changes being made)

``git add <file> / git add --all`` (add all changes to be staged for commit)

``git restore --staged <file>`` (unstage changes)

### 3.2 Check commit and push

``git commit -am "<your message/ note>"`` (commit choosen changes)

``git log`` (lists commits)

``git push`` (push to upstream)

## 4.0 Temporary edits/ testing

### 4.1 Branching

``git branch -l`` (lists branches)

``git branch <branch name>`` (create a branch)

``git branch -d <branch name>`` (deletes a branch locally)

``git checkout <branch name> / git switch <branch name>`` (switch to a branch, do this before making changes)

``git checkout -b <branch name> / git switch -c <branch name>`` (create and switch to that branch)

(repeat step 2, 3)

``git push --set-upstream origin <branch name>`` (push a branch to upstream repo)

``git checkout main / git switch main`` (switch back to main)

### 4.2 Merging

``git checkout main`` (switch to main after done editing a branch)

``git merge <branch name>`` (merge a branch to main)

``git merge --abort`` (abort if can't fix conflict in changes)

(repeat step 3)

## 5.0 Undoing

### 5.1 Pushed commits

``git log --oneline`` (list commit log with a hash for that commit)

``git revert <commit hash> --no-edit`` (revert that commit)

### 5.2 Unpushed commits

``git reset <commit hash>`` (revert commit and changes will appear as uncommitted)

## 6.0 Workflow

### 6.1 Pull request

a. note that main is primary branch

b. other people that want to contribute or any temporary edits/ hotfix, create a branch and commit any changes you want while in that branch

c. push to upstream repo

d. open github page for that repo and switch/click that branch (if you want to merge it with main), create pull request, merge pull request

e. delete that branch if not using anymore (locally and/or remotely, `https://github.com/mmu-cybertron/<repo name>/branches`)

### 6.2 Direct commit

directly commit changes to main, its fine for small amount of team on a smaller scale project