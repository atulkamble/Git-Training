# Git-Training
Git Training and Git Cheatsheet by Atul Kamble

Git Commands
============

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

## Tasks

All these commands are tested on  version 2.44.0.windows.1.

* [Everyday Git in twenty commands or so](#everyday-git-in-twenty-commands-or-so)
* [Show helpful guides that come with Git](#show-helpful-guides-that-come-with-git)
* [Search change by content](#search-change-by-content)
* [Show changes over time for specific file](#show-changes-over-time-for-specific-file)
* [Remove sensitive data from history, after a push](#remove-sensitive-data-from-history-after-a-push)
* [Sync with remote, overwrite local changes](#sync-with-remote-overwrite-local-changes)
* [List of all files till a commit](#list-of-all-files-till-a-commit)
* [Git reset first commit](#git-reset-first-commit)
* [Reset: preserve uncommitted local changes](#reset-preserve-uncommitted-local-changes)
* [List all the conflicted files](#list-all-the-conflicted-files)
* [List of all files changed in a commit](#list-of-all-files-changed-in-a-commit)
* [Unstaged changes since last commit](#unstaged-changes-since-last-commit)
* [Changes staged for commit](#changes-staged-for-commit)
* [Show both staged and unstaged changes](#show-both-staged-and-unstaged-changes)
* [List all branches that are already merged into master](#list-all-branches-that-are-already-merged-into-master)
* [Quickly switch to the previous branch](#quickly-switch-to-the-previous-branch)
* [Remove branches that have already been merged with master](#remove-branches-that-have-already-been-merged-with-master)
* [List all branches and their upstreams, as well as last commit on branch](#list-all-branches-and-their-upstreams-as-well-as-last-commit-on-branch)
* [Track upstream branch](#track-upstream-branch)
* [Delete local branch](#delete-local-branch)
* [Delete remote branch](#delete-remote-branch)
* [Create local tag](#create-local-tag)
* [Delete local tag](#delete-local-tag)
* [Delete remote tag](#delete-remote-tag)
* [Undo local changes with the last content in head](#undo-local-changes-with-the-last-content-in-head)
* [Revert: Undo a commit by creating a new commit](#revert-undo-a-commit-by-creating-a-new-commit)
* [Reset: Discard commits, advised for private branch](#reset-discard-commits-advised-for-private-branch)
* [Reword the previous commit message](#reword-the-previous-commit-message)
* [See commit history for just the current branch](#see-commit-history-for-just-the-current-branch)
* [Amend author.](#amend-author)
* [Reset author, after author has been changed in the global config.](#reset-author-after-author-has-been-changed-in-the-global-config)
* [Changing a remote's URL](#changing-a-remotes-url)
* [Get list of all remote references](#get-list-of-all-remote-references)
* [Get list of all local and remote branches](#get-list-of-all-local-and-remote-branches)
* [Get only remote branches](#get-only-remote-branches)
* [Stage parts of a changed file, instead of the entire file](#stage-parts-of-a-changed-file-instead-of-the-entire-file)
* [Get git bash completion](#get-git-bash-completion)
* [What changed since two weeks?](#what-changed-since-two-weeks)
* [See all commits made since forking from master](#see-all-commits-made-since-forking-from-master)
* [Pick commits across branches using cherry-pick](#pick-commits-across-branches-using-cherry-pick)
* [Find out branches containing commit-hash](#find-out-branches-containing-commit-hash)
* [Git Aliases](#git-aliases)
* [Saving current state of tracked files without commiting](#saving-current-state-of-tracked-files-without-commiting)
* [Saving current state of unstaged changes to tracked files](#saving-current-state-of-unstaged-changes-to-tracked-files)
* [Saving current state including untracked files](#saving-current-state-including-untracked-files)
* [Saving current state with message](#saving-current-state-with-message)
* [Saving current state of all files (ignored, untracked, and tracked)](#saving-current-state-of-all-files-ignored-untracked-and-tracked)
* [Show list of all saved stashes](#show-list-of-all-saved-stashes)
* [Show the contents of any stash in patch form](#show-the-contents-of-any-stash-in-patch-form)
* [Apply any stash without deleting from the stashed list](#apply-any-stash-without-deleting-from-the-stashed-list)
* [Apply last stashed state and delete it from stashed list](#apply-last-stashed-state-and-delete-it-from-stashed-list)
* [Delete all stored stashes](#delete-all-stored-stashes)
* [Grab a single file from a stash](#grab-a-single-file-from-a-stash)
* [Show all tracked files](#show-all-tracked-files)
* [Show all untracked files](#show-all-untracked-files)
* [Show all ignored files](#show-all-ignored-files)
* [Create new working tree from a repository (git 2.5)](#create-new-working-tree-from-a-repository-git-25)
* [Create new working tree from HEAD state](#create-new-working-tree-from-head-state)
* [Untrack files without deleting](#untrack-files-without-deleting)
* [Before deleting untracked files/directory, do a dry run to get the list of these files/directories](#before-deleting-untracked-filesdirectory-do-a-dry-run-to-get-the-list-of-these-filesdirectories)
* [Forcefully remove untracked files](#forcefully-remove-untracked-files)
* [Forcefully remove untracked directory](#forcefully-remove-untracked-directory)
* [Update all the submodules](#update-all-the-submodules)
* [Show all commits in the current branch yet to be merged to master](#show-all-commits-in-the-current-branch-yet-to-be-merged-to-master)
* [Rename a branch](#rename-a-branch)
* [Rebases 'feature' to 'master' and merges it in to master ](#rebases-feature-to-master-and-merges-it-in-to-master)
* [Archive the `master` branch](#archive-the-master-branch)
* [Modify previous commit without modifying the commit message](#modify-previous-commit-without-modifying-the-commit-message)
* [Prunes references to remove branches that have been deleted in the remote.](#prunes-references-to-remove-branches-that-have-been-deleted-in-the-remote)
* [Delete local branches that has been squash and merged in the remote.](#delete-local-branches-that-has-been-squash-and-merged-in-the-remote)
* [Retrieve the commit hash of the initial revision.](#retrieve-the-commit-hash-of-the-initial-revision)
* [Visualize the version tree.](#visualize-the-version-tree)
* [Visualize the tree including commits that are only referenced from reflogs](#visualize-the-tree-including-commits-that-are-only-referenced-from-reflogs)
* [Deploying git tracked subfolder to gh-pages](#deploying-git-tracked-subfolder-to-gh-pages)
* [Adding a project to repo using subtree](#adding-a-project-to-repo-using-subtree)
* [Get latest changes in your repo for a linked project using subtree](#get-latest-changes-in-your-repo-for-a-linked-project-using-subtree)
* [Export a branch with history to a file.](#export-a-branch-with-history-to-a-file)
* [Import from a bundle](#import-from-a-bundle)
* [Get the name of current branch.](#get-the-name-of-current-branch)
* [Ignore one file on commit (e.g. Changelog).](#ignore-one-file-on-commit-eg-changelog)
* [Stash changes before rebasing](#stash-changes-before-rebasing)
* [Fetch pull request by ID to a local branch](#fetch-pull-request-by-id-to-a-local-branch)
* [Show the most recent tag on the current branch.](#show-the-most-recent-tag-on-the-current-branch)
* [Show inline word diff.](#show-inline-word-diff)
* [Show changes using common diff tools.](#show-changes-using-common-diff-tools)
* [Don’t consider changes for tracked file.](#dont-consider-changes-for-tracked-file)
* [Undo assume-unchanged.](#undo-assume-unchanged)
* [Clean the files from `.gitignore`.](#clean-the-files-from-gitignore)
* [Restore deleted file.](#restore-deleted-file)
* [Restore file to a specific commit-hash](#restore-file-to-a-specific-commit-hash)
* [Always rebase instead of merge on pull.](#always-rebase-instead-of-merge-on-pull)
* [List all the alias and configs.](#list-all-the-alias-and-configs)
* [Make git case sensitive.](#make-git-case-sensitive)
* [Add custom editors.](#add-custom-editors)
* [Auto correct typos.](#auto-correct-typos)
* [Check if the change was a part of a release.](#check-if-the-change-was-a-part-of-a-release)
* [Dry run. (any command that supports dry-run flag should do.)](#dry-run-any-command-that-supports-dry-run-flag-should-do)
* [Marks your commit as a fix of a previous commit.](#marks-your-commit-as-a-fix-of-a-previous-commit)
* [Squash fixup commits normal commits.](#squash-fixup-commits-normal-commits)
* [Skip staging area during commit.](#skip-staging-area-during-commit)
* [Interactive staging.](#interactive-staging)
* [List ignored files.](#list-ignored-files)
* [Status of ignored files.](#status-of-ignored-files)
* [Commits in Branch1 that are not in Branch2](#commits-in-branch1-that-are-not-in-branch2)
* [List n last commits](#list-n-last-commits)
* [Reuse recorded resolution, record and reuse previous conflicts resolutions.](#reuse-recorded-resolution-record-and-reuse-previous-conflicts-resolutions)
* [Open all conflicted files in an editor.](#open-all-conflicted-files-in-an-editor)
* [Count unpacked number of objects and their disk consumption.](#count-unpacked-number-of-objects-and-their-disk-consumption)
* [Prune all unreachable objects from the object database.](#prune-all-unreachable-objects-from-the-object-database)
* [Instantly browse your working repository in gitweb.](#instantly-browse-your-working-repository-in-gitweb)
* [View the GPG signatures in the commit log](#view-the-gpg-signatures-in-the-commit-log)
* [Remove entry in the global config.](#remove-entry-in-the-global-config)
* [Checkout a new branch without any history](#checkout-a-new-branch-without-any-history)
* [Extract file from another branch.](#extract-file-from-another-branch)
* [List only the root and merge commits.](#list-only-the-root-and-merge-commits)
* [Change previous two commits with an interactive rebase.](#change-previous-two-commits-with-an-interactive-rebase)
* [List all branch is WIP](#list-all-branch-is-wip)
* [Find guilty with binary search](#find-guilty-with-binary-search)
* [Bypass pre-commit and commit-msg githooks](#bypass-pre-commit-and-commit-msg-githooks)
* [List commits and changes to a specific file (even through renaming)](#list-commits-and-changes-to-a-specific-file-even-through-renaming)
* [Clone a single branch](#clone-a-single-branch)
* [Create and switch new branch](#create-and-switch-new-branch)
* [Ignore file mode changes on commits](#ignore-file-mode-changes-on-commits)
* [Turn off git colored terminal output](#turn-off-git-colored-terminal-output)
* [Specific color settings](#specific-color-settings)
* [Show all local branches ordered by recent commits](#show-all-local-branches-ordered-by-recent-commits)
* [Find lines matching the pattern (regex or string) in tracked files](#find-lines-matching-the-pattern-regex-or-string-in-tracked-files)
* [Clone a shallow copy of a repository](#clone-a-shallow-copy-of-a-repository)
* [Search Commit log across all branches for given text](#search-commit-log-across-all-branches-for-given-text)
* [Get first commit in a branch (from master)](#get-first-commit-in-a-branch-from-master)
* [Unstaging Staged file](#unstaging-staged-file)
* [Force push to Remote Repository](#force-push-to-remote-repository)
* [Adding Remote name](#adding-remote-name)
* [List all currently configured remotes](#list-all-currently-configured-remotes)
* [Show the author, time and last revision made to each line of a given file](#show-the-author-time-and-last-revision-made-to-each-line-of-a-given-file)
* [Group commits by authors and title](#group-commits-by-authors-and-title)
* [Forced push but still ensure you don't overwrite other's work](#forced-push-but-still-ensure-you-dont-overwrite-others-work)
* [Show how many lines does an author contribute](#show-how-many-lines-does-an-author-contribute)
* [Revert: Reverting an entire merge](#revert-reverting-an-entire-merge)
* [Number of commits in a branch](#number-of-commits-in-a-branch)
* [Alias: git undo](#alias-git-undo)
* [Add object notes](#add-object-notes)
* [Show all the git-notes](#show-all-the-git-notes)
* [Apply commit from another repository](#apply-commit-from-another-repository)
* [Specific fetch reference](#specific-fetch-reference)
* [Find common ancestor of two branches](#find-common-ancestor-of-two-branches)
* [List unpushed git commits](#list-unpushed-git-commits)
* [Add everything, but whitespace changes](#add-everything-but-whitespace-changes)
* [Edit [local/global] git config](#edit-localglobal-git-config)
* [blame on certain range](#blame-on-certain-range)
* [Show a Git logical variable.](#show-a-git-logical-variable)
* [Preformatted patch file.](#preformatted-patch-file)
* [Get the repo name.](#get-the-repo-name)
* [logs between date range](#logs-between-date-range)
* [Exclude author from logs](#exclude-author-from-logs)
* [Generates a summary of pending changes](#generates-a-summary-of-pending-changes)
* [List references in a remote repository](#list-references-in-a-remote-repository)
* [Backup untracked files.](#backup-untracked-files)
* [List all git aliases](#list-all-git-aliases)
* [Show git status short](#show-git-status-short)
* [Checkout a commit prior to a day ago](#checkout-a-commit-prior-to-a-day-ago)
* [Push the current branch to the same name on the remote repository](#push-the-current-branch-to-the-same-name-on-the-remote-repository)
* [Push a new local branch to remote repository and track](#push-a-new-local-branch-to-remote-repository-and-track)
* [Change a branch base](#change-a-branch-base)
* [Use SSH instead of HTTPs for remotes](#use-ssh-instead-of-https-for-remotes)
* [Update a submodule to the latest commit](#update-a-submodule-to-the-latest-commit)
* [Prevent auto replacing LF with CRLF](#prevent-auto-replacing-lf-with-crlf)


## Everyday Git in twenty commands or so
```sh
git help everyday
```

## Show helpful guides that come with Git
```sh
git help -g
```

## Search change by content
```sh
git log -S'<a term in the source>'
```

## Show changes over time for specific file
```sh
git log -p <file_name>
```

## Remove sensitive data from history, after a push
```sh
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch <path-to-your-file>' --prune-empty --tag-name-filter cat -- --all && git push origin --force --all
```

## Sync with remote, overwrite local changes
```sh
git fetch origin && git reset --hard origin/master && git clean -f -d
```

## List of all files till a commit
```sh
git ls-tree --name-only -r <commit-ish>
```

## Git reset first commit
```sh
git update-ref -d HEAD
```

## Reset: preserve uncommitted local changes
```sh
git reset --keep <commit>
```

## List all the conflicted files
```sh
git diff --name-only --diff-filter=U
```

## List of all files changed in a commit
```sh
git diff-tree --no-commit-id --name-only -r <commit-ish>
```

## Unstaged changes since last commit
```sh
git diff
```

## Changes staged for commit
```sh
git diff --cached
```


__Alternatives:__
```sh
git diff --staged
```

## Show both staged and unstaged changes
```sh
git diff HEAD
```

## List all branches that are already merged into master
```sh
git branch --merged master
```

## Quickly switch to the previous branch
```sh
git checkout -
```


__Alternatives:__
```sh
git checkout @{-1}
```

## Remove branches that have already been merged with master
```sh
git branch --merged master | grep -v '^\*' | xargs -n 1 git branch -d
```


__Alternatives:__
```sh
git branch --merged master | grep -v '^\*\|  master' | xargs -n 1 git branch -d # will not delete master if master is not checked out
```

## List all branches and their upstreams, as well as last commit on branch
```sh
git branch -vv
```

## Track upstream branch
```sh
git branch -u origin/mybranch
```

## Delete local branch
```sh
git branch -d <local_branchname>
```

## Delete remote branch
```sh
git push origin --delete <remote_branchname>
```


__Alternatives:__
```sh
git push origin :<remote_branchname>
```


```sh
git branch -dr <remote/branch>
```

## Create local tag
```sh
git tag <tag-name>
```

## Delete local tag
```sh
git tag -d <tag-name>
```

## Delete remote tag
```sh
git push origin :refs/tags/<tag-name>
```

## Undo local changes with the content in index(staging)
```sh
git checkout -- <file_name>
```

## Revert: Undo a commit by creating a new commit
```sh
git revert <commit-ish>
```

## Reset: Discard commits, advised for private branch
```sh
git reset <commit-ish>
```

## Reword the previous commit message
```sh
git commit -v --amend
```

## See commit history for just the current branch
```sh
git cherry -v master
```

## Amend author.
```sh
git commit --amend --author='Author Name <email@address.com>'
```

## Reset author, after author has been changed in the global config.
```sh
git commit --amend --reset-author --no-edit
```

## Changing a remote's URL
```sh
git remote set-url origin <URL>
```

## Get list of all remote references
```sh
git remote
```


__Alternatives:__
```sh
git remote show
```

## Get list of all local and remote branches
```sh
git branch -a
```

## Get only remote branches
```sh
git branch -r
```

## Stage parts of a changed file, instead of the entire file
```sh
git add -p
```

## Get git bash completion
```sh
curl -L http://git.io/vfhol > ~/.git-completion.bash && echo '[ -f ~/.git-completion.bash ] && . ~/.git-completion.bash' >> ~/.bashrc
```

## What changed since two weeks?
```sh
git log --no-merges --raw --since='2 weeks ago'
```


__Alternatives:__
```sh
git whatchanged --since='2 weeks ago'
```

## See all commits made since forking from master
```sh
git log --no-merges --stat --reverse master..
```

## Pick commits across branches using cherry-pick
```sh
git checkout <branch-name> && git cherry-pick <commit-ish>
```

## Find out branches containing commit-hash
```sh
git branch -a --contains <commit-ish>
```


__Alternatives:__
```sh
git branch --contains <commit-ish>
```

## Git Aliases
```sh
git config --global alias.<handle> <command> 
git config --global alias.st status
```

## Saving current state of tracked files without commiting
```sh
git stash
```


__Alternatives:__
```sh
git stash push
```

## Saving current state of unstaged changes to tracked files
```sh
git stash -k
```


__Alternatives:__
```sh
git stash --keep-index
```


```sh
git stash push --keep-index
```

## Saving current state including untracked files
```sh
git stash -u
```


__Alternatives:__
```sh
git stash push -u
```


```sh
git stash push --include-untracked
```

## Saving current state with message
```sh
git stash push -m <message>
```


__Alternatives:__
```sh
git stash push --message <message>
```

## Saving current state of all files (ignored, untracked, and tracked)
```sh
git stash -a
```


__Alternatives:__
```sh
git stash --all
```


```sh
git stash push --all
```

## Show list of all saved stashes
```sh
git stash list
```

## Show the contents of any stash in patch form
```sh
git stash show -p <stash@{n}>
```

## Apply any stash without deleting from the stashed list
```sh
git stash apply <stash@{n}>
```

## Apply last stashed state and delete it from stashed list
```sh
git stash pop
```


__Alternatives:__
```sh
git stash apply stash@{0} && git stash drop stash@{0}
```

## Delete all stored stashes
```sh
git stash clear
```


__Alternatives:__
```sh
git stash drop <stash@{n}>
```

## Grab a single file from a stash
```sh
git checkout <stash@{n}> -- <file_path>
```


__Alternatives:__
```sh
git checkout stash@{0} -- <file_path>
```

## Show all tracked files
```sh
git ls-files -t
```

## Show all untracked files
```sh
git ls-files --others
```

## Show all ignored files
```sh
git ls-files --others -i --exclude-standard
```

## Create new working tree from a repository (git 2.5)
```sh
git worktree add -b <branch-name> <path> <start-point>
```

## Create new working tree from HEAD state
```sh
git worktree add --detach <path> HEAD
```

## Untrack files without deleting
```sh
git rm --cached <file_path>
```


__Alternatives:__
```sh
git rm --cached -r <directory_path>
```

## Before deleting untracked files/directory, do a dry run to get the list of these files/directories
```sh
git clean -n
```

## Forcefully remove untracked files
```sh
git clean -f
```

## Forcefully remove untracked directory
```sh
git clean -f -d
```

## Update all the submodules
```sh
git submodule foreach git pull
```


__Alternatives:__
```sh
git submodule update --init --recursive
```


```sh
git submodule update --remote
```

## Show all commits in the current branch yet to be merged to master
```sh
git cherry -v master
```


__Alternatives:__
```sh
git cherry -v master <branch-to-be-merged>
```

## Rename a branch
```sh
git branch -m <new-branch-name>
```


__Alternatives:__
```sh
git branch -m [<old-branch-name>] <new-branch-name>
```

## Rebases 'feature' to 'master' and merges it in to master 
```sh
git rebase master feature && git checkout master && git merge -
```

## Archive the `master` branch
```sh
git archive master --format=zip --output=master.zip
```

## Modify previous commit without modifying the commit message
```sh
git add --all && git commit --amend --no-edit
```

## Prunes references to remove branches that have been deleted in the remote.
```sh
git fetch -p
```


__Alternatives:__
```sh
git remote prune origin
```

## Delete local branches that has been squash and merged in the remote.
```sh
git branch -vv | grep ': gone]' | awk '{print <!-- @doxie.inject start -->}' | xargs git branch -D
```

## Retrieve the commit hash of the initial revision.
```sh
 git rev-list --reverse HEAD | head -1
```


__Alternatives:__
```sh
git rev-list --max-parents=0 HEAD
```


```sh
git log --pretty=oneline | tail -1 | cut -c 1-40
```


```sh
git log --pretty=oneline --reverse | head -1 | cut -c 1-40
```

## Visualize the version tree.
```sh
git log --pretty=oneline --graph --decorate --all
```


__Alternatives:__
```sh
gitk --all
```


```sh
git log --graph --pretty=format:'%C(auto) %h | %s | %an | %ar%d'
```

## Visualize the tree including commits that are only referenced from reflogs
```sh
git log --graph --decorate --oneline $(git rev-list --walk-reflogs --all)
```

## Deploying git tracked subfolder to gh-pages
```sh
git subtree push --prefix subfolder_name origin gh-pages
```

## Adding a project to repo using subtree
```sh
git subtree add --prefix=<directory_name>/<project_name> --squash git@github.com:<username>/<project_name>.git master
```

## Get latest changes in your repo for a linked project using subtree
```sh
git subtree pull --prefix=<directory_name>/<project_name> --squash git@github.com:<username>/<project_name>.git master
```

## Export a branch with history to a file.
```sh
git bundle create <file> <branch-name>
```

## Import from a bundle
```sh
git clone repo.bundle <repo-dir> -b <branch-name>
```

## Get the name of current branch.
```sh
git rev-parse --abbrev-ref HEAD
```

## Ignore one file on commit (e.g. Changelog).
```sh
git update-index --assume-unchanged Changelog; git commit -a; git update-index --no-assume-unchanged Changelog
```

## Stash changes before rebasing
```sh
git rebase --autostash
```

## Fetch pull request by ID to a local branch
```sh
git fetch origin pull/<id>/head:<branch-name>
```


__Alternatives:__
```sh
git pull origin pull/<id>/head:<branch-name>
```

## Show the most recent tag on the current branch.
```sh
git describe --tags --abbrev=0
```

## Show inline word diff.
```sh
git diff --word-diff
```

## Show changes using common diff tools.
```sh
git difftool [-t <tool>] <commit1> <commit2> <path>
```

## Don’t consider changes for tracked file.
```sh
git update-index --assume-unchanged <file_name>
```

## Undo assume-unchanged.
```sh
git update-index --no-assume-unchanged <file_name>
```

## Clean the files from `.gitignore`.
```sh
git clean -X -f
```

## Restore deleted file.
```sh
git checkout <deleting_commit> -- <file_path>
```

## Restore file to a specific commit-hash
```sh
git checkout <commit-ish> -- <file_path>
```

## Always rebase instead of merge on pull.
```sh
git config --global pull.rebase true
```


__Alternatives:__
```sh
#git < 1.7.9
git config --global branch.autosetuprebase always
```

## List all the alias and configs.
```sh
git config --list
```

## Make git case sensitive.
```sh
git config --global core.ignorecase false
```

## Add custom editors.
```sh
git config --global core.editor '$EDITOR'
```

## Auto correct typos.
```sh
git config --global help.autocorrect 1
```

## Check if the change was a part of a release.
```sh
git name-rev --name-only <SHA-1>
```

## Dry run. (any command that supports dry-run flag should do.)
```sh
git clean -fd --dry-run
```

## Marks your commit as a fix of a previous commit.
```sh
git commit --fixup <SHA-1>
```

## Squash fixup commits normal commits.
```sh
git rebase -i --autosquash
```

## Skip staging area during commit.
```sh
git commit --only <file_path>
```

## Interactive staging.
```sh
git add -i
```

## List ignored files.
```sh
git check-ignore *
```

## Status of ignored files.
```sh
git status --ignored
```

## Commits in Branch1 that are not in Branch2
```sh
git log Branch1 ^Branch2
```

## List n last commits
```sh
git log -<n>
```


__Alternatives:__
```sh
git log -n <n>
```

## Reuse recorded resolution, record and reuse previous conflicts resolutions.
```sh
git config --global rerere.enabled 1
```

## Open all conflicted files in an editor.
```sh
git diff --name-only | uniq | xargs $EDITOR
```

## Count unpacked number of objects and their disk consumption.
```sh
git count-objects --human-readable
```

## Prune all unreachable objects from the object database.
```sh
git gc --prune=now --aggressive
```

## Instantly browse your working repository in gitweb.
```sh
git instaweb [--local] [--httpd=<httpd>] [--port=<port>] [--browser=<browser>]
```

## View the GPG signatures in the commit log
```sh
git log --show-signature
```

## Remove entry in the global config.
```sh
git config --global --unset <entry-name>
```

## Checkout a new branch without any history
```sh
git checkout --orphan <branch_name>
```

## Extract file from another branch.
```sh
git show <branch_name>:<file_name>
```

## List only the root and merge commits.
```sh
git log --first-parent
```

## Change previous two commits with an interactive rebase.
```sh
git rebase --interactive HEAD~2
```

## List all branch is WIP
```sh
git checkout master && git branch --no-merged
```

## Find guilty with binary search
```sh
git bisect start                    # Search start 
git bisect bad                      # Set point to bad commit 
git bisect good v2.6.13-rc2         # Set point to good commit|tag 
git bisect bad                      # Say current state is bad 
git bisect good                     # Say current state is good 
git bisect reset                    # Finish search 

```

## Bypass pre-commit and commit-msg githooks
```sh
git commit --no-verify
```

## List commits and changes to a specific file (even through renaming)
```sh
git log --follow -p -- <file_path>
```

## Clone a single branch
```sh
git clone -b <branch-name> --single-branch https://github.com/user/repo.git
```

## Create and switch new branch
```sh
git checkout -b <branch-name>
```


__Alternatives:__
```sh
git branch <branch-name> && git checkout <branch-name>
```

```sh
git switch -c <branch-name>
```

## Ignore file mode changes on commits
```sh
git config core.fileMode false
```

## Turn off git colored terminal output
```sh
git config --global color.ui false
```

## Specific color settings
```sh
git config --global <specific command e.g branch, diff> <true, false or always>
```

## Show all local branches ordered by recent commits
```sh
git for-each-ref --sort=-committerdate --format='%(refname:short)' refs/heads/
```

## Find lines matching the pattern (regex or string) in tracked files
```sh
git grep --heading --line-number 'foo bar'
```

## Clone a shallow copy of a repository
```sh
git clone https://github.com/user/repo.git --depth 1
```

## Search Commit log across all branches for given text
```sh
git log --all --grep='<given-text>'
```

## Get first commit in a branch (from master)
```sh
git log --oneline master..<branch-name> | tail -1
```


__Alternatives:__
```sh
git log --reverse master..<branch-name> | head -6
```

## Unstaging Staged file
```sh
git reset HEAD <file-name>
```

## Force push to Remote Repository
```sh
git push -f <remote-name> <branch-name>
```

## Adding Remote name
```sh
git remote add <remote-nickname> <remote-url>
```

## List all currently configured remotes
```sh
git remote -v
```

## Show the author, time and last revision made to each line of a given file
```sh
git blame <file-name>
```

## Group commits by authors and title
```sh
git shortlog
```

## Forced push but still ensure you don't overwrite other's work
```sh
git push --force-with-lease <remote-name> <branch-name>
```

## Show how many lines does an author contribute
```sh
git log --author='_Your_Name_Here_' --pretty=tformat: --numstat | gawk '{ add += <!-- @doxie.inject start -->; subs += <!-- @doxie.inject end -->; loc += <!-- @doxie.inject start --> - <!-- @doxie.inject end --> } END { printf "added lines: %s removed lines: %s total lines: %s
", add, subs, loc }' -
```


__Alternatives:__
```sh
git log --author='_Your_Name_Here_' --pretty=tformat: --numstat | awk '{ add += <!-- @doxie.inject start -->; subs += <!-- @doxie.inject end -->; loc += <!-- @doxie.inject start --> - <!-- @doxie.inject end --> } END { printf "added lines: %s, removed lines: %s, total lines: %s
", add, subs, loc }' - # on Mac OSX
```

## Revert: Reverting an entire merge
```sh
git revert -m 1 <commit-ish>
```

## Number of commits in a branch
```sh
git rev-list --count <branch-name>
```

## Alias: git undo
```sh
git config --global alias.undo '!f() { git reset --hard $(git rev-parse --abbrev-ref HEAD)@{${1-1}}; }; f'
```

## Add object notes
```sh
git notes add -m 'Note on the previous commit....'
```

## Show all the git-notes
```sh
git log --show-notes='*'
```

## Apply commit from another repository
```sh
git --git-dir=<source-dir>/.git format-patch -k -1 --stdout <SHA1> | git am -3 -k
```

## Specific fetch reference
```sh
git fetch origin master:refs/remotes/origin/mymaster
```

## Find common ancestor of two branches
```sh
git merge-base <branch-name> <other-branch-name>
```

## List unpushed git commits
```sh
git log --branches --not --remotes
```


__Alternatives:__
```sh
git log @{u}..
```


```sh
git cherry -v
```

## Add everything, but whitespace changes
```sh
git diff --ignore-all-space | git apply --cached
```

## Edit [local/global] git config
```sh
git config [--global] --edit
```

## blame on certain range
```sh
git blame -L <start>,<end>
```

## Show a Git logical variable.
```sh
git var -l | <variable>
```

## Preformatted patch file.
```sh
git format-patch -M upstream..topic
```

## Get the repo name.
```sh
git rev-parse --show-toplevel
```

## logs between date range
```sh
git log --since='FEB 1 2017' --until='FEB 14 2017'
```

## Exclude author from logs
```sh
git log --perl-regexp --author='^((?!excluded-author-regex).*)

```

## Generates a summary of pending changes
```sh
git request-pull v1.0 https://git.ko.xz/project master:for-linus
```

## List references in a remote repository
```sh
git ls-remote git://git.kernel.org/pub/scm/git/git.git
```

## Backup untracked files.
```sh
git ls-files --others -i --exclude-standard | xargs zip untracked.zip
```

## List all git aliases
```sh
git config -l | grep alias | sed 's/^alias\.//g'
```


__Alternatives:__
```sh
git config -l | grep alias | cut -d '.' -f 2
```

## Show git status short
```sh
git status --short --branch
```

## Checkout a commit prior to a day ago
```sh
git checkout master@{yesterday}
```

## Push the current branch to the same name on the remote repository
```sh
git push origin HEAD
```

## Push a new local branch to remote repository and track
```sh
git push -u origin <branch_name>
```

## Change a branch base
```sh
git rebase --onto <new_base> <old_base>
```

## Use SSH instead of HTTPs for remotes
```sh
git config --global url.'git@github.com:'.insteadOf 'https://github.com/'
```

## Update a submodule to the latest commit
```sh
cd <path-to-submodule>
git pull origin <branch>
cd <root-of-your-main-project>
git add <path-to-submodule>
git commit -m "submodule updated"
```

## Prevent auto replacing LF with CRLF
```sh
git config --global core.autocrlf false
```
# Git Sildes

# Hello.

Welcome to Git!


---

# What is Git?

>> notes

Before we get started, lets talk a bit about what git is, and how it differes from some other forms of source control. I'll be comparing it a little bit to subversion, but similar comparsions can be applied to other source control systems also.

---

## Snapshots…everything

#### Subversion

Information is a set of files + **deltas** of changes over time.

#### Git

Information is a set of **snapshots**. For every committed change, Git takes another snapshot.

>> notes

In a system like Subversion - changes are tracked as a series of changes over time. When change is commited - it is the delta that the SVN will keep track of.

(make use of?) - http://git-scm.com/book/en/v2/book/01-introduction/images/deltas.png

With git - your changes are snapshots of whats happened. It is a full version of the file that changed - not just the changes to it. Git sort of acts like a filesystem with some tools on top.

By keeping snapshots of changes over time, this allows git to do most things locally.
---

## Local operations

#### Subversion

You can make local edits but you need **network access** to commit your changes to your database.

#### Git

The entire project history is on your **local disk**. You can do almost anything offline, including committing.

>>> Notes

With a CVS system, the general workflow is needing to connect to a server, pull down changes, commit changes - requiring a network connection. If you are trying to be a good developer - you might get latest again to ensure things still work before committing.

The difference with git - when you commit with a CVS system, you also need a network connection - and tends to promote 'larger and fewer' commits, because once the commit is done - it's on the server and another developer will pull it down, even if it's not ready.

With git, most operations are done locally.  This allows you to create branches, change branches, commit changes, revert changes without needing a network connection.

This also allows you to make smaller and more frequent commits - such as trying out new ideas, and easily being able to revert them, commiting work in progress to jump over to another branch for a hotfix.

"But, I don't want to see 1000 commits in my history" -- we will cover how to resolve this later on today when talking about merging and rebasing.

---

## Distributed

#### Subversion

**Centralized**. One repo and lots of clients.

#### Git

**Distributed**. One repo with lots of client repos, each with a user.

>>> notes
:TODO

---

## Lightweight branches

#### Subversion

Slow(er), network dependant, long urls, manual merges. To be used with care (especially pre-1.5).

#### Git

Fast(er), network independent, often automatic merges. To be used early and often.

>>> notes

At my previous company, we used TFS - and the general motto was 'less branches, less often - and if you need a branch, there best be a very, very good reason for it - and approved by someone else'.

With git, we are able to create branches locally, switch between them, commit changes all without needing a network connection. This also makes it really easy to do smaller branches that are more focused.

---

## Easily curated commits

#### Subversion

Diff to temporary files + reverting and partially applying those temporary files again.

#### Git

First-class and dedicated staging area + patch staging (which can be interactive).

>>> notes
TODO

---

## And so much more.

---

# The three states

---

## The .git directory (History)

Where the metadata and object database of the project is stored.

It's what's copied when you clone a repository.

---

## The working directory

A version of the project that is checked out and placed on disk.

Its files are pulled out of the compressed database in the .git directory.

---

## The staging area (Index)

A file, in the .git directory, that stores information about what will go into your next commit.

---

## All git commands operate over these three states.

---

# Basic commands

---
## Getting started, and making changes
---
## `git init`

Start tracking a project in Git.

This command creates the .git directory.

>>> notes: move this to above add / commit / etc

- if you are using git locally only
- if it's not on a remote (yet)
- simplest way is typically creating a repo on git, bitbucket, etc and then cloning


---
## `git status`

Show the status of modified files in the working directory.

These can be _untracked_, _unstaged_ or _staged_ for commit.

>>> notes
* go into new folder
* do git init
* do git status
* no files
* touch readme.md
* git status - see untracked files

---

## `git add <files>`

Copy snapshots of modified files to the staging area.

This command tracks new files

>>> notes

Git add will adds a change in the working directory, to the staging area. It lets git know that the next time a commit happens, that this file should be included.

Adding a file does not affect the repository in a major way, and the change is not recorded until we do a git commit which we will cover next.


---

## `git commit`

Save a snapshot of the staging area to the history as a commit.

>>>

Git commit is what will push changes from the staging area, to the history. The workflow for git is

- working directory
- staging
- comiting to history.

An important thing to note - is that every time a file changes, if you want to include that change with the next commit - you need to tell git to re-add it, as it is adding a snapshot of the file at the time the command is run.

-- edit file
-- git add
-- edit file again
-- need to add it again

You can avoid needing to always re-add a file by using git commit -a to automatically add files that are tracked.

** example with commit -a with tracked/untracked files?
---

## Undoing ....

* git revert
* git reset
* git checkout

>> notes:

Not every commit is perfect, and sometimes we make mistakes - either commited a change to soon, added something in error - and being able to restore to previous versions is imporant.

Git provides a few ways to work with your history - reset, revert and checkout.

---

## 'git revert <commit>'

>> notes:

Git revert is considered one of the safer ways of to undo a changes, as it does not rewrite the history of your project. Git will try to figure out how to undo a change, and create a new commit for that change.

---
## `git reset -- <files>`

Copy files from the latest commit to staging area.

Effectively undoes `git add <files>` by replacing files in the staging area by those last committed.

Omit `<files>` to unstage everything.

>> notes:

While git revert does not move the project back to a previous state, git reset does. Git revert also allows you to revert changes at any point in history, where git reset can only work backwards from the current commit.

Git reset can be considered a 'dangerous' command also, as it is possible to lose work as you are unable to recover your original work.

---

## `git checkout -- <files>`

Copy files from the staging area to the working directory.

Omit `<files>` to throw away all local changes.

---

## Basic commands visualized

![inline](http://marklodato.github.io/visual-git-guide/basic-usage.svg.png)

---

# Basic commands redux

---

## Interactive

Interactively select hunks a particular files to operate on.

`git add -p`
`git commit -p`
`git reset -p`
`git checkout -p`

>>>

The interactive/patch commands have quite a bit of power and flexability, but going over how to use the patch mode is outside the scope of todays session.

---

## Shortcuts

`git commit (file | -a)`
Add all tracked and changed files' contents to the staging area and then creates a commit.

`git`
Copy files from the latest commit into both the staging area and the working directory.

---

## Shortcuts visualized

![inline](http://marklodato.github.io/visual-git-guide/basic-usage-2.svg.png)

---

# More commands

---




## `git clone <url>`

Get a copy of an existing Git repository.

This command copies the .git directory of a remote Git repository to your local disk and checks out a working copy of the latest version of the default branch.

---

## `git diff`

See the exact lines added and removed in the working directory.

`--cached | --staged`: Compare your staged changes to those of your last commit.

---

## `git rm`

Remove files from the working directory and the staging area.

`--cached`: Remove files from the staging area only and keep them in the working directory.

---

## `git mv`

Track the movement (renaming) of files.

It essentially moves the file on the filesystem, `git rm`s and then `git add`s the moved file.

---

## `git log`

Browse and inspect the evolution of the project.

---

# Crafting commits

---

![original](http://imgs.xkcd.com/comics/git_commit.png)

---

## Do's

- keep commit changes as small as possible
- describe what was changed and why
- limit first line to 50 characters
- insert a blank line after first line
- wrap subsequent lines at 72 characters

---

## Don't

- mix whitespace with functional code changes
- mix unrelated functional code changes
- send large feature in a single commit

---

## Model Git commit message

```
Capitalized, short (50 chars or less) summary

More detailed explanatory text, if necessary.  Wrap it to about 72
characters or so.  In some contexts, the first line is treated as the
subject of an email and the rest of the text as the body.  The blank
line separating the summary from the body is critical (unless you omit
the body entirely); tools like rebase can get confused if you run the
two together.

Write your commit message in the imperative: "Fix bug" and not "Fixed bug"
or "Fixes bug."  This convention matches up with commit messages generated
by commands like git merge and git revert.

Further paragraphs come after blank lines.

- Bullet points are okay, too

- Typically a hyphen or asterisk is used for the bullet, preceded by a
  single space, with blank lines in between, but conventions vary here

- Use a hanging indent
```

---

## `git commit --amend`

Add any staged changes to the last commit and ammend the commit message (optional).

Useful for when you commit early and forget to add some files or when you make a mistake in the commit message.

---

## `git stash`

Save the uncommitted changes in the working directory and the staging area and go back to a clean working directory.


>>> notes:

* show git stash
* git stash ls
* git stash apply vs git stash pop --- apply applies it, pop applies it and removes it from the stack


---

# Remote branches

---

## `git remote`

List all remotes.

---

## `git remote add <shortname> <url>`

Add a remote git repository and reference it with a shortname.

---

## `git fetch <shortname>`

Get all the data from the remote repository unto your local disk.

---

## `git branch --set-upstream-to=<shortname>/<remote branch name> <local branch name>`

Set a local branch to track a remote branch.

---

## `git push <shortname> <branch>`

Push changes in your branch to its corresponding tracking branch on the remote repository.

*TIP: Use the `-u` flag when creating new local branches to automatically set their remote tracking branches.*

---

# Git configuration

---

## `git config --global user`

`.name <name>`: Setup your name.
`.email <email>`: Setup your email.

Set the name and email that will be attached to your commits.

---

## `git config --global alias`

Set short forms for frequently used commands.

Examples:

```
git config --global alias.st status
git config --global alias.ci commit
git config --global alias.br branch
git config --global alias.co checkout
git config --global alias.df diff
git config --global alias.lg 'log -p'
```

---

### Configurations can also be put in the ~/.gitconfig file

---

## `.gitignore`

A list of files in the project to ignore.

---

# Workflows

---

# Github Work Flow
![inline](http://lucamezzalira.files.wordpress.com/2014/03/screen-shot-2014-03-08-at-23-07-361.png?w=650&h=230)

A continuous deployment environment where everything in the `master` branch is deployable.

---

## Branching off

`git branch <name of branch> && git checkout <name of branch>`

`git checkout -b <name of branch>`

Create a new branch off of `master`, commit to that branch locally and push to the server frequently.

---

## Rebasing

`git rebase <name of branch to rebase off>`

As you work and even as you finish, integrate your changes with `master` regularly.

---

## Rebasing (continued)

Rebasing changes the base of your branch to the last commit found on another branch, `master` in this case, and replays your changes on top. In essence, the history is rewritten to make it appear that your work was always done after the latest master.

---

## Before a rebase

![inline](http://git-scm.com/figures/18333fig0327-tn.png)

---

## After a rebase

![inline](http://git-scm.com/figures/18333fig0328-tn.png)

---

## Squashing your commits

`git rebase -i <name of branch to rebase off>`

Pick the first commit on your feature branch and squash all subsequent ones on top of it.

This process combines them all into one commit.

---

## Pull requests

When a branch is ready to be merged, a pull request is made to start the review process.

---

## Review and discuss

Collaborators and stakeholders can review the commit together and any correction is made to the branch and pushed to update the pull request.

---

## Merging

`git merge --no-ff <name of branch to merge>`

Once the changes have passed the review process, they are merged to the `master` branch.

---

## Merging (continued)

### Before

      A---B---C topic
     /
    D---E---F---G master
### After

      A---B---C topic
     /         \
    D---E---F---G---H master

---

## Resolving merge conflicts

```
this presentation is

<<<<<<< HEAD
good
=======
great
>>>>>>> feature-improve-presentation
```

---

## Merge tools

`git mergetool`

Typically used after `git merge`, this command runs several built in tools to help resolve merge conflicts.

---

## Available tools for windows

- Araxis Merge
- Beyond Compare
- ExamDiff
- WinMerge (free)
- KDiff3 (free)

---

## Cherry Pick

`git cherry-pick <sha-1>`

Copy a commit from one branch and apply it to another.

---

# Git hooks

---

## What are Git hooks?

Built-in scripts Git executes before or after commits, pushes, and receives. These vary widely in functionality.

---

## How they work

Each Git repository comes with a `.git/hooks` folder where scripts for each hook that can be bound to.

To install a script, place any executable in the `.git/hooks` folder and name it according to the hook you mean to bind to.

---

## Client-side hooks

---

### `pre-commit`

Runs first, before the commit message prompt and allows you to inspect the snapshot that's about to be inspected.

Great for running tests, linting code and removing whitespaces.

---

### `prepare-commit-msg`

Runs before the commit message editor is launched but after the default message is created.

Great for editing the default message and templating.

---

### `commit-msg`

Runs after the commit message is saved.

Great for validating commit messages.

---

### `post-commit`

Runs after the entire commit is completed.

Great for notifications.

---

### `pre-rebase `

Runs before you rebase anything.

---

### `post-checkout`

Runs after a successful `git checkout`.

Great for setting up working environment, especially when large (untracked) binaries are involved.

---

### `post-merge`

Runs after a successful `git merge`.

---

## Server-side hooks

---

### `pre-receive`

Runs when handling a push from a client. Only

---

### `post-receive`

Runs after a push from a client is fully processed.

Great for notifying users and other systems such as the CI and IM applications.

---

### `update`

Very similar to the pre-receive hook but may run multiple times, depending on the amount of branches being pushed.

The `pre-receive` hook only runs once, no matter how many branches are pushed.

---

# Github Webhooks

---

## What is a Webhook?

Technical: An user defined HTTP callback that is triggered by a certain event that occurs at the source site.

Simple: A web service endpoint that listens to requests from a source and/or sends requests to a target.

Each hook can be configured to a specific service and any number of events.

---

## Setting up a Webhook

1. Go to the **Settings** page of your repository.
2. Click on **Webhooks & services**.
3. Click on **Add webhook**.

---

## Payload URL

This is the server endpoint that will handle the Webhook.

---

## Available events

commit\_comment | create | delete | deployment\_status | deployment | fork | gollum | issue\_comment | issues | member | page\_build | public | pull\_request\_review\_comment | pull\_request | push | release | status | team\_add watch

---

## Wildcard events

`*`

You'll receive every event.

---

## Payload

The POST request body, usually contains a JSON document.

Each event type has its own unique payload object.

---

## Sample Payload

```
POST /payload HTTP/1.1

Host: localhost:4567
X-Github-Delivery: 72d3162e-cc78-11e3-81ab-4c9367dc0958
User-Agent: GitHub Hookshot 044aadd
Content-Type: application/json
Content-Length: 6615
X-Github-Event: issue
```
```javascript
{
  "action": "opened",
  "issue": {
    "url": "https://api.github.com/repos/octocat/Hello-World/issues/1347",
    "number": 1347,
    ...
  },
  "repository" : {
    "id": 1296269,
    "full_name": "octocat/Hello-World",
    "owner": {
      "login": "octocat",
      "id": 1,
      ...
    },
    ...
  },
  "sender": {
    "login": "octocat",
    "id": 1,
    ...
  }
}
```

---

# One-button deployments

---

## Disclaimer

^ This is not prescriptive. YMMV.

---

## Stack

- Rundeck
- Github
- Jenkins
- New Relic
- Logstash & Kibana
- Slack

---

## Rundeck

Allows you to turn operations procedures into self-service jobs and safely give others control and visibility over the infrastructure.

---

![fit](http://rundeck.org/images/Rundeck-EditJob.png)

---

![fit](http://rundeck.org/images/Rundeck-JobExecution.png)

---

## Jenkins

A continuous integration server that allow you to run your test suite automatically everytime changes are commit and/or merged.

---

![fit](http://blog.octo.com/wp-content/uploads/2012/08/screenshot-dashboard-jenkins1.png)

---

![fit](https://s3.amazonaws.com/uploads.hipchat.com/68570/490459/eLKcPVAfVZesfcf/jenkins.png)

---

![fit](https://s3.amazonaws.com/uploads.hipchat.com/68570/490459/wtZQUHUhxIeVUSL/jenkinslog.png)

---

## Deployment overview

```
+---------+             +--------+            +-----------+        +-------------+
| Rundeck |             | GitHub |            |  Jenkins  |        | Your Server |
+---------+             +--------+            +-----------+        +-------------+
     |                      |                       |                     |
     |  Create Deployment   |                       |                     |
     |--------------------->|                       |                     |
     |                      |                       |                     |
     |  Deployment Created  |                       |                     |
     |<---------------------|                       |                     |
     |                      |                       |                     |
     |                      |   Deployment Event    |                     |
     |                      |---------------------->|                     |
     |                      |                       |     SSH+Deploys     |
     |                      |                       |-------------------->|
     |                      |                       |                     |
     |                      |   Deployment Status   |                     |
     |                      |<----------------------|                     |
     |                      |                       |                     |
     |                      |                       |   Deploy Completed  |
     |                      |                       |<--------------------|
     |                      |                       |                     |
     |                      |   Deployment Status   |                     |
     |                      |<----------------------|                     |
     |                      |                       |                     |
```

---

## New Relic

A real-time performance management and monitoring platform.

---

![fit](http://c179631.r31.cf0.rackcdn.com/newrelic_snapshot.jpg)

---

![fit](http://newrelic.com/assets/pages/application_monitoring/screens/screen_deployment-0cd60d04ed34f1c1063096efa945664e.jpg)

---

## Logstash

A tool for managing events and logs built on top of elasticsearch.

---

### Kibana

Visualization platform for elasticsearch.

---

![fit](http://www.elasticsearch.org/content/uploads/2014/03/Screen-Shot-2014-02-25-at-4.42.52-PM.png)

---

## Slack

Group communication tool with support for internal/private chat and instant messaging.

Integrates well with other tools in the stack.

---

![fit](https://s3.amazonaws.com/uploads.hipchat.com/68570/490459/PBVlrIpOsPmTrLK/slack.png)

---

# Thank you!

---

# References

[Pro Git](http://git-scm.com/book/en)
[A Visual Git Reference](http://marklodato.github.io/visual-git-guide/index-en.html)
[Git Hooks](http://githooks.com/)
[Git Gui](http://git-scm.com/docs/git-gui)

