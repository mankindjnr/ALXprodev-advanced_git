# Git-Flows

## Setting up gitflow
```bash
# install git-flow
apt install git-flow

# create an empty repo and clone it locally
# initialize git flow within the repository with default settings
git flow init -d

# create README.md file

# to push changes - add -commit
git add .
git commit -m "describe your changes"
```

#### push the changes
`confirm which branch you are in`
- whichever has * is the active branch (*develop)
```bash
git branch
```

`to push to develop branch`
```bash
git push origin develop
```

`to push the master branch instead - switch to it first`
```bash
git checkout master
git push origin master
```
`to explicitly push to a branch`
```bash
git push --set-upstream origin develop
```
this will link the local `develop` branch with the remote `develop` branch. Afterward, you can just use `git push`

### Push all branches
To push both `master` and `develop` branches at the same time:
```bash
git push all
```
This will synchronize all branches with their respective remote branches.

## SUMMARY
For most workflows in a Git Flow setup:
- Push changes from `develop` to the remote `develop` branch during active deevlopment.
- Merge or finish a feature/release branch, then psh to `develop` or `main` as necessary.