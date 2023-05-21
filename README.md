# Git commands

### General

Create repository:

	git init

Add file:

	git add <file>

Remove file:

	git rm <file>

Commit changes:

	git commit -m "message"

Show changes:

	git status

Show log:

	git log

Show log with tags:

	git log --decorate

Search thru commit messages:

	git log --grep="<search>"

Add remote repository:

	git remote add origin <url>

### Branches

Show branches:

	git branch

Create branch:

	git branch <branch>

Create and checkout branch:

	git checkout -b <branch>

Checkout branch:

	git checkout <branch>

Rename branch:

	git branch -m <from> <to>

Delete branch:

	git branch -d <branch>

Review differences:

	git diff <commit1> <commit2>

Merge branch into current:

	git merge <branch>

Resolve merge conflicts:

	mate <file>
	git add <file>
	git commit

### Tags

Show tags:

	git tag

Create tag:

	git tag -a <tag>

Create tag for specific commit:

	git tag -a <tag> <commit>

Show tag data:

	git show <tag>

Delete tag:

	git tag -d <tag>

### Push

Push to master:

	git push origin master

Push with tags:

	git push origin master --tags

### Pull

Fetch from remote repository:

	git fetch origin

Merge remote branch into current:

	git merge origin/master

Fetch and merge into current branch:

	git pull

### Clone

Clone repository:

	git clone <url>

### Stash

Stash changes:

	git stash

Show stashes:

	git stash list

Restore stash:

	git stash apply

Restore specific stash:

	git stash apply <stash>

Remove stash:

	git stash drop <stash>

Restore and remove stash:

	git stash pop

## Special

Remove last commit (not pushed):

	git reset --hard HEAD~1

## Misc

Get the number of commits in the current branch:

	git log --pretty=oneline | wc -l

## Configuration

Set name:

	git config --global user.name "<name>"

Set email:

	git config --global user.email "<email>"
