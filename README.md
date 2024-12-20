# Git exercise project

## Bundle 1

### Exercise 1

```bash

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ git add README.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ git commit -m "init project"
[main (root-commit) 57e5930] init project
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ git remote add origin https://github.com/Jess-xca/git-exercise.git


user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 239 bytes | 59.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)To https://github.com/Jess-xca/git-exercise.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ git push
Everything up-to-date

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ git checkout -b dev
Switched to a new branch 'dev'

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git status
On branch dev
nothing to commit, working tree clean

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Jess-xca/git-exercise/pull/new/dev
remote:
To https://github.com/Jess-xca/git-exercise.git
 * [new branch]      dev -> dev

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git checkout -b test
Switched to a new branch 'test'

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Jess-xca/git-exercise/pull/new/test
remote:
To https://github.com/Jess-xca/git-exercise.git
remote:
To https://github.com/Jess-xca/git-exercise.git
To https://github.com/Jess-xca/git-exercise.git
 * [new branch]      test -> test

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (test)
$ git checkout dev
Switched to branch 'dev'

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git branch -D test
Deleted branch test (was 57e5930).

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git push origin --delete test
To https://github.com/Jess-xca/git-exercise.git
 - [deleted]         test

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.


```
