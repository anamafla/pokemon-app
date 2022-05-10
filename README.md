# Pokemon-app
This repository contains the Pokemon app source code.

This project is built with Vanilla JS.

## Prerequisites
You will need the following tools installed:

1. [Git](http://git-scm.com/)

## Installation
```
git clone https://github.com/anamafla/pokemon-app.git
```

## Version control

### Branching Strategy
We use git flow as our branching strategy. This approach consists of two main branches:

**Primary Branches**
- main: The primary branch where all the production code is stored. Once the code in the "develop" branch is ready to be released, the changes are merged to the master branch and used in the deployment.

- develop: This is where all the actual development happens. All the pre-production code is stored here, and the completed code of all the supporting branches is merged directly to the develop branch.

**Support Branches**
We should always branch from **develop** and merge back again whenever a feature/bug/hotfix is complete.

- feature/* feature branches are used to develop new features.
- bugfix/* This branch is used to aggregate fixes and improvements.
- hotfix/* This is to deal with production issues where quick fixes are required.


### Creating a Pull Request (PR)
Pull Request happens in Github.


- **Commit Messages**: Please use the following format to write your commit messages.
  ```
  Task Title

  Changes:
  * Explain the changes included in this commit.
  ```

- **Generate PR**: Pull Request is created using the following commands.
  ```
  git push origin HEAD:refs/for/<DEVELOPMENT_BRANCH>

  ```

- **Rebasing and Squashing your branch**: In order to rebase and squash into a single commit with follow steps. Oftenly, PR will have be outdated from DEVELOPMENT_BRANCH and require rebase before get merged into DEVELOPMENT_BRANCH.

  ```
  # Check out and get latest <DEVELOPMENT_BRANCH>
  git checkout <DEVELOPMENT_BRANCH>
  git pull origin <DEVELOPMENT_BRANCH> --rebase

  # Check out the desire local branch
  git checkout <LOCAL_BRANCH>

  # Rebase local branch to DEVELOPMENT_BRANCH interactive
  git rebase -i <DEVELOPMENT_BRANCH>

  # If any conflict, resolve and continue rebase
  git rebase --continue

  # Squash all the commits and leave only one to push
  ```
