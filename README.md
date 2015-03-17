# Git Resources

Resources for learning git. Checkout [Git Cheat Sheet](Git Cheat sheet.md) and 
[Getting Started With Git](Getting Started With Git.md).

### Git Cheat Sheet ###

| Scenario                              | Commands
|---------------------------------------|---------------------------------------------------------------
| Get the source code onto my machine   | `git clone https://github.com/dawsK/git-resources.git`
| Do a fresh GET                        | `git pull`
| Check what files I've changed         | `git status`
| Change Branches                       | `git checkout <name_of_branch>`
| Undo changes to a specific file       | `git checkout -- <path_to_file>`
| Undo all changes in current branch    | `git checkout .`
| Commit changes locally                | `git add -A`, `git commit`
| Check what files are staged           | `git status`
| Check for updates                     | `git fetch`, `git status`
| Push changes to GitHub                | `git push`
| Setup mergetool                       | `git config --global merge.tool kdiff3`
| Setup difftool                        | `git config --global diff.tool kdiff3`
| Create a new branch                   | `git checkout -b <new_branch_name>`
| Merge others' changes with yours      | `git add -A`, `git commit`, `git fetch`, `git rebase`
| Cancel a rebase                       | `git rebase --cancel`
| Push a new branch to GitHub           | `git push -u origin <new_branch_name>`
| Merge changes from master             | `git rebase master`
| Merge changes into master             | `git merge <other_branch>`
| Stash changes                         | `git stash`
| Unstash changes                       | `git stash pop`

### Resources ###

 * Readable Git Documentation - [http://git-scm.com/](http://git-scm.com/)
 * Try Git tutorial - [https://try.github.io/](https://try.github.io/)
 * git-tfs plugin - [https://github.com/git-tfs/git-tfs](https://github.com/git-tfs/git-tfs)
 * git-tf plugin - [https://gittf.codeplex.com/](https://gittf.codeplex.com/)
 * git-svn - [https://www.kernel.org/pub/software/scm/git/docs/git-svn.html](https://www.kernel.org/pub/software/scm/git/docs/git-svn.html)
 * GitHub for Windows - [https://windows.github.com/](https://windows.github.com/)
 * This document - [https://github.com/dawsK/git-resources](https://github.com/dawsK/git-resources)

### Aliases ###

Use these aliases to simplify the commands you type at the command prompt. They are mostly for convenience except for `git hist` and `git hista`,
which provide a very nice listing of your recent history, but are essentially impossible to remember.

Add these alias commands to git by editing your global `.gitconfig` file. You can open this file from git
by running `git config -e --global`, or just find the file in your root user directory.

```
[alias]
	aa = add --all
	br = branch
	ci = commit
	cl = clone
	co = checkout
	cp = cherry-pick
	dc = diff --cached
	diff = diff --word-diff
	hist = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --max-count=20
	hista = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
	ls = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate
	st = status -s
	alias = config --get-regexp ^alias\\.
	scorch = clean -xdie *.suo
```

#### Examples ####

##### git hist #####
```
daws@laptop /c/Code/GitHub/git-resources (master)
$ git hist
* 2bc6181 - (HEAD, origin/master, origin/HEAD, master) Add another link (14 hours ago) <Dawson Kroeker>
* 68593f9 - Add link to this document (14 hours ago) <Dawson Kroeker>
* 7681380 - Initial commit (14 hours ago) <Dawson Kroeker>
* bd41712 - Initial commit (15 hours ago) <dawsK>
```

##### git st #####
```
daws@laptop /c/Code/GitHub/git-resources (master)
$ git st
 M README.md
```

##### git ls #####
```
daws@laptop /c/Code/GitHub/git-resources (master)
$ git ls
2bc6181 (HEAD, origin/master, origin/HEAD, master) Add another link [Dawson Kroeker]
68593f9 Add link to this document [Dawson Kroeker]
7681380 Initial commit [Dawson Kroeker]
bd41712 Initial commit [dawsK]
```

##### git alias #####
```
daws@laptop /c/Code/GitHub/git-resources (master)
$ git alias
alias.aa add --all
alias.br branch
alias.ci commit
alias.cl clone
alias.co checkout
alias.cp cherry-pick
alias.dc diff --cached
alias.diff diff --word-diff
alias.hist log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --max-count=20
alias.hista log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
alias.ls log --pretty=format:%C(yellow)%h%Cred%d\ %Creset%s%Cblue\ [%cn] --decorate
alias.st status -s
alias.alias config --get-regexp ^alias\.
alias.scorch clean -xdie *.suo
```

