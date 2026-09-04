# Git Commands Reference

## Repository Setup and Cloning
- `git init` — Initialize a new Git repository in the current directory.
- `git clone <repository-url>` — Clone a remote repository to your local machine.
- `git clone <repository-url> <folder-name>` — Clone into a specific folder name.
- `git remote -v` — Show configured remote repositories.
- `git remote add origin <repository-url>` — Add a new remote named `origin`.

## Basic Workflow
- `git status` — Show current branch, staged/unstaged files, and untracked files.
- `git add <file>` — Stage a specific file.
- `git add .` — Stage all changed files in the current directory.
- `git restore <file>` — Discard unstaged changes in a file.
- `git restore --staged <file>` — Unstage a file without losing local changes.
- `git commit -m "message"` — Create a commit with a message.
- `git commit -am "message"` — Stage tracked file changes and commit in one step.
- `git log` — View commit history.
- `git log --oneline` — View compact one-line commit history.

## Branching
- `git branch` — List local branches.
- `git branch <branch-name>` — Create a new branch.
- `git switch <branch-name>` — Switch to an existing branch.
- `git switch -c <branch-name>` — Create and switch to a new branch.
- `git checkout <branch-name>` — Switch branches (older but widely used command).
- `git branch -d <branch-name>` — Delete a merged local branch.
- `git branch -D <branch-name>` — Force-delete a local branch.

## Syncing with Remote
- `git fetch` — Download changes from remote without merging.
- `git pull` — Fetch and merge remote changes into the current branch.
- `git pull --rebase` — Fetch and rebase local commits on top of remote changes.
- `git push` — Push local commits to the tracked remote branch.
- `git push -u origin <branch-name>` — Push and set upstream tracking branch.
- `git push origin --delete <branch-name>` — Delete a remote branch.

## Merging and Rebasing
- `git merge <branch-name>` — Merge another branch into the current branch.
- `git rebase <branch-name>` — Reapply current branch commits on top of another branch.
- `git rebase -i HEAD~<n>` — Interactively edit, squash, or reorder last `n` commits.
- `git merge --abort` — Abort an in-progress merge.
- `git rebase --abort` — Abort an in-progress rebase.

## Comparing Changes
- `git diff` — Show unstaged changes.
- `git diff --staged` — Show staged changes.
- `git diff <branch1>..<branch2>` — Compare differences between two branches.
- `git show <commit-hash>` — Show details of a specific commit.

## Stashing
- `git stash` — Temporarily save uncommitted changes.
- `git stash list` — List all stashes.
- `git stash apply` — Reapply the most recent stash (keep it in stash list).
- `git stash pop` — Reapply and remove the most recent stash.
- `git stash drop` — Delete a specific stash.
- `git stash clear` — Delete all stashes.

## Undo and Recovery
- `git reset <file>` — Unstage a file (legacy approach).
- `git reset --soft HEAD~1` — Undo last commit, keep changes staged.
- `git reset --mixed HEAD~1` — Undo last commit, keep changes unstaged.
- `git reset --hard HEAD~1` — Undo last commit and discard local changes.
- `git revert <commit-hash>` — Create a new commit that reverses a previous commit.
- `git reflog` — Show reference log to recover lost commits or branch states.

## Tags
- `git tag` — List tags.
- `git tag <tag-name>` — Create a lightweight tag.
- `git tag -a <tag-name> -m "message"` — Create an annotated tag.
- `git push origin <tag-name>` — Push a specific tag.
- `git push origin --tags` — Push all local tags.

## Inspection and Configuration
- `git config --global user.name "Your Name"` — Set global Git username.
- `git config --global user.email "you@example.com"` — Set global Git email.
- `git config --list` — View all Git configuration values.
- `git remote show origin` — Show detailed info for remote `origin`.
- `git blame <file>` — Show who changed each line in a file.

## Useful Cleanup Commands
- `git clean -n` — Preview untracked files/folders that would be removed.
- `git clean -f` — Remove untracked files.
- `git clean -fd` — Remove untracked files and directories.

---
This README provides a practical set of commonly used Git commands with short descriptions.