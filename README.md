Kinga Kurowska

Assignment 5 - 08.04.2025

# Git - summary

## Setting up git

### Configure git

```
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
git config --list
```
--------------------
### SSH Key

```
 ls -al ~/.ssh
 ssh-keygen -t name -C "your-email@example.com"
 cat ~/.ssh/id_name.pub OR: pbcopy < ~/.ssh/id_name.pub
 ssh -T git@github.com
```
* Go to your GitHub website > settings
* Paste your SSH key to SSH and GPG keys
-------------------
### Clone git repository
```
git clone link
```

## Using git

### Adding and committing files


```
git add file.py
git commit -m "my first commit"
git push origin main
```
tracking all files in the directory at once:
```
git add .
```
If you accidentally mistype a commit message, you can change it using the ```--amend``` flag

-----------------------------

### Branching and merging

Branches allows to develop features, fix bugs, or safely experiment with new ideas in a contained area of repository.

Createing new branch:

```
git branch new_branch
```

Changing working branch to the "new_branch":

```
git checkout new_branch
```

Comparing the 2 branches:

```
git diff main..new_branch
```

Merging the branch to main:

```
git merge new_branch
git push
```

show the commit history for the currently active branch:
```
git log
```

**In case of merging conflict:**

Edit the file deleting unwanted lines and commit

----------------

### Pulling changes

* ```git pull```: Downloads from remote and merges with local
* ```git fetch```: Downloads info from remote, but does not merge with local.

More details in the Git commands [CheatSheet](https://education.github.com/git-cheat-sheet-education.pdf).
