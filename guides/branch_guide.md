# Branching Etiquette
General Etiquette for Branching

## Overview
Following a standard branching guide is useful for navigating merge conflicts and avoiding stepping on each other's toes.
A few years back, I stumbled upon [this branching model](http://nvie.com/posts/a-successful-git-branching-model/) that has served as the foundation of my branching style for personal and professional projects.
Though the article goes further in depth on supporting branches than is necessary for our purposes, I think it's still important to follow the ideas surrounding the `main`, `develop`, and `feature` branches.

## The Big Three

### Main
The `main` branch should contain only production-ready code releases.
That means all bug fixes and feature development is completed and ready for use.
We should be pushing the least to this branch.

### Develop
The `develop` branch contains all in-progress code that is not yet ready to be pushed to the `master` branch.
Usually, all work is housed here until we reach a certain milestone.
Upon completion of the milestone, we would push to the `master` branch for milestone release.
Though all work should be done in this branch, it is imperative that separate feature work be done in individual `feature` branches as described below.

### Feature Branches
Feature branches are reserved for all the individual work we'll be doing, including feature development, bug fixes, and refactoring.
These branches are how we can ensure our work doesn't directly interfere with someone else's work while both being done simultaneously in the `develop` branch.
The main idea is to create a new branch off of `develop` whenever you begin working on a new feature.
On completion of that feature development, merge the feature branch back into `develop`.
In this way, we can have multiple features branching and merging back into `develop` simultaneously, thus avoiding merge conflicts that run rampant when multiple developers are working directly on `develop` at the same time.

## Naming Conventions
You only need to worry about naming feature branches, bug fixes, and refactoring branches (all of which apply to the Feature Branches section above).
Each word in a branch name should be separated with a hyphen.  
Good: `branch-name`  
Bad: `branchName`

### Feature and Refactoring Branches
In general, it's best to name feature branches according to whatever feature you are developing on.
For example, working on a login feature could be named `login`.
The same applies to refactoring branches.

### Bug fixes
For bug fixes, a general rule of thumb is to prefix the bug-fix branch name with `bug-`.
As an example, fixing a login feature to correctly hash passwords might be named: `bug-login-password-hashing`.
