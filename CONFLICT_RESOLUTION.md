
# Merge Conflict Resolution

## Overview

This document explains how I created and resolved
a merge conflict while working with Git branches.

## Creating the Conflict

I created two separate feature branches:

- feature/readme-update-a
- feature/readme-update-b

On the first branch, I changed the README.md title
to "A Beginner's Guide to Git Commands and Version
Control."

On the second branch, I changed the same title to
"A Practical Guide to Git and GitHub for Beginners."

Both changes were committed separately.

## Encountering the Conflict

While working on feature/readme-update-b, I ran:

```bash
git merge feature/readme-update-a
```

Git displayed the following error:

```text
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then
commit the result.
```

## Resolving the Conflict

I opened README.md in VS Code and reviewed the
conflicting versions of the title.

I resolved the conflict by combining both titles
into one:

**A Practical Beginner's Guide to Git, GitHub,
and Version Control**

After removing the conflict markers and saving
the file, I staged the changes:

```bash
git add README.md
```

I then committed the resolution:

```bash
git commit -m "Resolve README merge conflict"
```

## Verification

I used the following command to verify the
merge history:

```bash
git log --oneline --graph -6
```

The Git history showed both branches connecting
to the merge commit.

Merge commit: 5d67b37

## Conclusion

This exercise helped me understand how Git
identifies conflicting changes when multiple
branches modify the same section of a file.

I learned how to review conflicting changes,
remove conflict markers, and commit a successful
merge resolution.
