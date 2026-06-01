PS C:\today-i-learned> cd git

PS C:\today-i-learned\git> cd git-tutorial

PS C:\today-i-learned\git\git-tutorial> code .

PS C:\today-i-learned\git\git-tutorial> git init

PS C:\today-i-learned\git\git-tutorial> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../

nothing added to commit but untracked files present (use "git add" to track)
PS C:\today-i-learned\git\git-tutorial> git add config.js
PS C:\today-i-learned\git\git-tutorial> git add src
PS C:\today-i-learned\git\git-tutorial> git add .
PS C:\today-i-learned\git\git-tutorial> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md
        new file:   config.js
        new file:   git-github-reference.pdf
        new file:   src/index.js

PS C:\today-i-learned\git\git-tutorial> git commit -m "Version 1"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'iamti@acer.(none)')
PS C:\today-i-learned\git\git-tutorial>   git config --global user.email "iamtilou@gmail.com"
PS C:\today-i-learned\git\git-tutorial>   git config --global user.name "tilouu"        
PS C:\today-i-learned\git\git-tutorial> git commit -m "Version 1"
[main 3458af1] Version 1
 4 files changed, 11 insertions(+)
 create mode 100644 git/git-tutorial/README.md
 create mode 100644 git/git-tutorial/config.js
 create mode 100644 git/git-tutorial/git-github-reference.pdf
 create mode 100644 git/git-tutorial/src/index.js
PS C:\today-i-learned\git\git-tutorial> git log
commit 3458af13b657491a0691a288fb407617690be936 (HEAD -> main)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 07:37:43 2026 +0000

    Version 1

commit c5d9a97c45c0352c1fb0d4c17d0959aa683418f0 (origin/main, origin/HEAD)
Author: tilou <iamtilou@gmail.com>
Date:   Sun May 31 11:56:36 2026 +0000

    Initial commit
PS C:\today-i-learned\git\git-tutorial> git add .
PS C:\today-i-learned\git\git-tutorial> git commit -m "Version 1" --amend
[main 31d7ceb] Version 1
 Date: Mon Jun 1 07:37:43 2026 +0000
 5 files changed, 12 insertions(+)
 create mode 100644 git/git-tutorial/README.md
 create mode 100644 git/git-tutorial/change.js
 create mode 100644 git/git-tutorial/config.js
 create mode 100644 git/git-tutorial/git-github-reference.pdf
 create mode 100644 git/git-tutorial/src/index.js
PS C:\today-i-learned\git\git-tutorial> git log
commit 31d7ceb7891bd7cad5a1711a565141e77511c056 (HEAD -> main)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 07:37:43 2026 +0000

    Version 1

commit c5d9a97c45c0352c1fb0d4c17d0959aa683418f0 (origin/main, origin/HEAD)
Author: tilou <iamtilou@gmail.com>
Date:   Sun May 31 11:56:36 2026 +0000

    Initial commit
PS C:\today-i-learned\git\git-tutorial> git reset .
Unstaged changes after reset:
M       git/git-tutorial/change.js
M       git/git-tutorial/config.js
M       git/git-tutorial/src/index.js
PS C:\today-i-learned\git\git-tutorial> git checkout -- .
PS C:\today-i-learned\git\git-tutorial> git add .
PS C:\today-i-learned\git\git-tutorial> git commit -m "Version 2"
[main 2e50040] Version 2
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\today-i-learned\git\git-tutorial> git add .
PS C:\today-i-learned\git\git-tutorial> git commit -m "Version 3"
[main c5c09c4] Version 3
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\today-i-learned\git\git-tutorial> git log
commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (HEAD -> main)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 08:00:22 2026 +0000

    Version 3

commit 2e500401072b5d501fff9c4e521ea235c1c0de93
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 07:58:02 2026 +0000

    Version 2

commit 31d7ceb7891bd7cad5a1711a565141e77511c056
PS C:\today-i-learned\git\git-tutorial> git checkout 2e500401072b5d501fff9c4e521ea235c1c0de93
Note: switching to '2e500401072b5d501fff9c4e521ea235c1c0de93'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 2e50040 Version 2
PS C:\today-i-learned\git\git-tutorial> git log
commit 2e500401072b5d501fff9c4e521ea235c1c0de93 (HEAD)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 07:58:02 2026 +0000

    Version 2

commit 31d7ceb7891bd7cad5a1711a565141e77511c056
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 07:37:43 2026 +0000

    Version 1

commit c5d9a97c45c0352c1fb0d4c17d0959aa683418f0 (origin/main, origi
PS C:\today-i-learned\git\git-tutorial> git log --all
commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (main)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 08:00:22 2026 +0000

    Version 3

commit 2e500401072b5d501fff9c4e521ea235c1c0de93 (HEAD)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 07:58:02 2026 +0000

    Version 2

commit 31d7ceb7891bd7cad5a1711a565141e77511c056
PS C:\today-i-learned\git\git-tutorial> git checkout 31d7ceb7891bd7cad5a1711a565141e77511c056
Previous HEAD position was 2e50040 Version 2
HEAD is now at 31d7ceb Version 1
PS C:\today-i-learned\git\git-tutorial> git log --all
commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (main)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 08:00:22 2026 +0000

    Version 3

commit 2e500401072b5d501fff9c4e521ea235c1c0de93
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 07:58:02 2026 +0000

    Version 2

commit 31d7ceb7891bd7cad5a1711a565141e77511c056 (HEAD)
PS C:\today-i-learned\git\git-tutorial> git add .
PS C:\today-i-learned\git\git-tutorial> git commit -m "Version 1 updated"
[detached HEAD f8d1e79] Version 1 updated
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\today-i-learned\git\git-tutorial> git log --all
commit f8d1e798bfae37be5283c154057e864543f0e683 (HEAD)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 08:11:41 2026 +0000

    Version 1 updated

commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (main)
Author: tilouu <iamtilou@gmail.com>
Date:   Mon Jun 1 08:00:22 2026 +0000

    Version 3

commit 2e500401072b5d501fff9c4e521ea235c1c0de93
PS C:\today-i-learned\git\git-tutorial> git log --all --graph
* commit f8d1e798bfae37be5283c154057e864543f0e683 (HEAD)
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 08:11:41 2026 +0000
| 
|     Version 1 updated
|   
| * commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (main)
| | Author: tilouu <iamtilou@gmail.com>
| | Date:   Mon Jun 1 08:00:22 2026 +0000
| | 
| |     Version 3
| | 
| * commit 2e500401072b5d501fff9c4e521ea235c1c0de93
:...skipping...
* commit f8d1e798bfae37be5283c154057e864543f0e683 (HEAD)
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 08:11:41 2026 +0000
| 
|     Version 1 updated
|   
| * commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (main)
| | Author: tilouu <iamtilou@gmail.com>
| | Date:   Mon Jun 1 08:00:22 2026 +0000
| | 
| |     Version 3
| | 
| * commit 2e500401072b5d501fff9c4e521ea235c1c0de93
|/  Author: tilouu <iamtilou@gmail.com>
|   Date:   Mon Jun 1 07:58:02 2026 +0000
|   
|       Version 2
| 
* commit 31d7ceb7891bd7cad5a1711a565141e77511c056
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 07:37:43 2026 +0000
| 
|     Version 1
| 
* commit c5d9a97c45c0352c1fb0d4c17d0959aa683418f0 (origin/main, origin/HEAD)
  Author: tilou <iamtilou@gmail.com>
  Date:   Sun May 31 11:56:36 2026 +0000
  
      Initial commit
~
~
~
~
~
~
~
~
PS C:\today-i-learned\git\git-tutorial> git checkout master
error: pathspec 'master' did not match any file(s) known to git
PS C:\today-i-learned\git\git-tutorial> git checkout main
Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  f8d1e79 Version 1 updated

If you want to keep it by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> f8d1e79

Switched to branch 'main'
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)
PS C:\today-i-learned\git\git-tutorial> git log --all --graph
* commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (HEAD -> main)
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 08:00:22 2026 +0000
| 
|     Version 3
| 
* commit 2e500401072b5d501fff9c4e521ea235c1c0de93
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 07:58:02 2026 +0000
| 
|     Version 2
| 
* commit 31d7ceb7891bd7cad5a1711a565141e77511c056
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 07:37:43 2026 +0000
| 
|     Version 1
| 
* commit c5d9a97c45c0352c1fb0d4c17d0959aa683418f0 (origin/main, origin/HEAD)
  Author: tilou <iamtilou@gmail.com>
  Date:   Sun May 31 11:56:36 2026 +0000
  
      Initial commit
PS C:\today-i-learned\git\git-tutorial> git checkout 31d7ceb7891bd7cad5a1711a565141e77511c056 .        
Updated 1 path from 8270b0b
PS C:\today-i-learned\git\git-tutorial> git log --all --graph
* commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a (HEAD -> main)
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 08:00:22 2026 +0000
| 
|     Version 3
| 
* commit 2e500401072b5d501fff9c4e521ea235c1c0de93
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 07:58:02 2026 +0000
| 
|     Version 2
| 
* commit 31d7ceb7891bd7cad5a1711a565141e77511c056
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 07:37:43 2026 +0000
| 
|     Version 1
| 
* commit c5d9a97c45c0352c1fb0d4c17d0959aa683418f0 (origin/main, origin/HEAD)
  Author: tilou <iamtilou@gmail.com>
  Date:   Sun May 31 11:56:36 2026 +0000
  
      Initial commit
PS C:\today-i-learned\git\git-tutorial> git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   config.js

PS C:\today-i-learned\git\git-tutorial> git commit -m "Version 1 restored"
[main 8c284a6] Version 1 restored
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\today-i-learned\git\git-tutorial> git log --all --graph
* commit 8c284a6d22e99102b5cceee4b73d124419a82c5f (HEAD -> main)
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 08:24:55 2026 +0000
| 
|     Version 1 restored
| 
* commit c5c09c4e3379fdfee8f2ad7081322a5e65f4016a
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 08:00:22 2026 +0000
| 
|     Version 3
| 
* commit 2e500401072b5d501fff9c4e521ea235c1c0de93
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 07:58:02 2026 +0000
| 
|     Version 2
| 
* commit 31d7ceb7891bd7cad5a1711a565141e77511c056
| Author: tilouu <iamtilou@gmail.com>
| Date:   Mon Jun 1 07:37:43 2026 +0000
| 
|     Version 1
| 
* commit c5d9a97c45c0352c1fb0d4c17d0959aa683418f0 (origin/main, origin/HEAD)
  Author: tilou <iamtilou@gmail.com>
  Date:   Sun May 31 11:56:36 2026 +0000
  
      Initial commit
PS C:\today-i-learned\git\git-tutorial> git status
On branch main
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\today-i-learned\git\git-tutorial> git s
git: 's' is not a git command. See 'git --help'.

The most similar commands are
        show
        status
        switch
        lfs
PS C:\today-i-learned\git\git-tutorial> git config --global alias.s "status"
PS C:\today-i-learned\git\git-tutorial> git s
On branch main
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\today-i-learned\git\git-tutorial> git config --global alias.cm "commit -m"
PS C:\today-i-learned\git\git-tutorial> git config --global alias.co "checkout"
PS C:\today-i-learned\git\git-tutorial> git status
On branch main
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
PS C:\today-i-learned\git\git-tutorial> git add .
PS C:\today-i-learned\git\git-tutorial> git cm "Add git ignore"
[main cb128f7] Add git ignore
 1 file changed, 1 insertion(+)
 create mode 100644 git/git-tutorial/.gitignore

PS C:\today-i-learned\git\git-tutorial> git log

PS C:\today-i-learned\git\git-tutorial> rm -rf .git

PS C:\today-i-learned\git\git-tutorial> git log

PS C:\today-i-learned\git\git-tutorial> git add . 
PS C:\today-i-learned\git\git-tutorial> git cm "Add README.md"
[main c78153d] Add README.md
 1 file changed, 396 insertions(+), 1 deletion(-)
PS C:\today-i-learned\git\git-tutorial> git push
info: please complete authentication in your browser...
Enumerating objects: 32, done.
Counting objects: 100% (32/32), done.
Delta compression using up to 8 threads
Compressing objects: 100% (22/22), done.
Writing objects: 100% (31/31), 2.13 MiB | 958.00 KiB/s, done.
Total 31 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), done.
To https://github.com/tilouu/today-i-learned.git
   c5d9a97..c78153d  main -> main