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

#### Exercise 2

```bash

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git add home.html

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash
Saved working directory and index state WIP on dev: 13b1

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git add about.html

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash
Saved working directory and index state WIP on dev: 13b1

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash list
stash@{0}: WIP on dev: 13b1b7b deleted stuff
stash@{1}: WIP on dev: 13b1b7b deleted stuff

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git add team.html

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash
Saved working directory and index state WIP on dev: 13b1

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash list
stash@{0}: WIP on dev: 13b1b7b deleted stuff
stash@{1}: WIP on dev: 13b1b7b deleted stuff
stash@{2}: WIP on dev: 13b1b7b deleted stuff

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (014cfff83c1fda9da39e6bf4188d50888af6dce1)

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (e1c87f9499a24fecc4001a71135de9543713c388)

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git add --all

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git commit -m "setup the home and about page"
[dev 27c63f1] setup the home and about page
 2 files changed, 11 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 492 bytes | 246.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Jess-xca/git-exercise.git
   13b1b7b..27c63f1  dev -> dev
branch 'dev' set up to track 'origin/dev'.

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash list
stash@{0}: WIP on dev: 13b1b7b deleted stuff

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (bdc0b41aba09ac37d9b1977c2899fdcf25cdd7db)

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE (dev)
$ git reset --hard
HEAD is now at 27c63f1 setup the home and about page

```
