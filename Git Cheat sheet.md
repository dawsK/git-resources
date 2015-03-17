# Git Cheat Sheet #

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

## Resources ##

 * Readable Git Documentation - [http://git-scm.com/](http://git-scm.com/)
 * Try Git tutorial - [https://try.github.io/](https://try.github.io/)
 * git-tfs plugin - [https://github.com/git-tfs/git-tfs](https://github.com/git-tfs/git-tfs)
 * git-tf plugin - [https://gittf.codeplex.com/](https://gittf.codeplex.com/)
 * git-svn - [https://www.kernel.org/pub/software/scm/git/docs/git-svn.html](https://www.kernel.org/pub/software/scm/git/docs/git-svn.html)
 * GitHub for Windows - [https://windows.github.com/](https://windows.github.com/)
 * This document - [https://github.com/dawsK/git-resources](https://github.com/dawsK/git-resources)
 