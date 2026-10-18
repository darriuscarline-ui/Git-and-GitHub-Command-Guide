
# Branching and Pull Requests in Git

## Introduction
Branches allow developers to work on new features without
changing the main version of a project. Pull requests
provide a way to review and merge changes into the main
branch.

## Creating a Branch
Use the following command to create and switch to a
new branch:

```bash
git switch -c feature/new-feature
```

## Switching Between Branches
To switch to an existing branch:

```bash
git switch main
```

## Viewing Branches
To see all local branches:

```bash
git branch
```

## Pushing a Feature Branch
After committing your changes, push the feature branch
to GitHub:

```bash
git push -u origin feature/new-feature
```

## Creating a Pull Request
1. Open your repository on GitHub.
2. Select the Pull Requests tab.
3. Click New pull request.
4. Select main as the base branch and your feature
   branch as the compare branch.
5. Enter a descriptive title and summary.
6. Click Create pull request.

## Conclusion
Branches and pull requests help developers organize
changes, review work, and maintain a stable main branch.
  
## Merging and Deleting Branches

After a pull request has been reviewed, the changes
can be merged into the main branch on GitHub.

To update the local main branch:

```bash
git switch main
git pull origin main
```

To delete a completed local feature branch:

```bash
git branch -d feature/new-feature
```

Deleting completed branches helps keep a repository
organized and easier to maintain.
