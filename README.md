ninoniauri@Ninos-MacBook-Air Test % git checkout -b fix13
Switched to a new branch 'fix13'
ninoniauri@Ninos-MacBook-Air Test % git status
On branch fix13
On branch fix13
nothing to commit, working tree clean
zsh: command not found: On
ninoniauri@Ninos-MacBook-Air Test % touch Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % git add Fix13.txt
ninoniauri@Ninos-MacBook-Air Test %  git status
On branch fix13
On branch fix13
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Fix13.txt

zsh: command not found: On
ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit of fix13 branch"
[fix13 57f67ef] Initial commit of fix13 branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % git log --pretty=format:"%h %cd %an '%s'"
57f67ef Mon Mar 27 21:31:04 2023 +0400 Nino Niauri 'Initial commit of fix13 branch'
d1597b9 Mon Mar 27 21:20:16 2023 +0400 Nino Niauri 'Added README file content'
9fd3f3f Mon Mar 27 21:19:29 2023 +0400 Nino Niauri 'initial commit'
ninoniauri@Ninos-MacBook-Air Test % git checkout master         
Switched to branch 'master'
ninoniauri@Ninos-MacBook-Air Test %  ls -ltrh
total 8
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 21:19 README.txt
ninoniauri@Ninos-MacBook-Air Test % git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test %  ls -ltrh
total 8
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 21:19 README.txt
ninoniauri@Ninos-MacBook-Air Test % git merge fix13
Updating d1597b9..57f67ef
Fast-forward
 Fix13.txt | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 8
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 21:19 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 21:34 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % git log --pretty=format:"%h %cd %an '%s'"
57f67ef Mon Mar 27 21:31:04 2023 +0400 Nino Niauri 'Initial commit of fix13 branch'
d1597b9 Mon Mar 27 21:20:16 2023 +0400 Nino Niauri 'Added README file content'
9fd3f3f Mon Mar 27 21:19:29 2023 +0400 Nino Niauri 'initial commit'
ninoniauri@Ninos-MacBook-Air Test % git checkout -b fix14
Switched to a new branch 'fix14'
ninoniauri@Ninos-MacBook-Air Test % echo "It's Fix 14 branch"> fix14.txt
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 16
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 21:19 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 21:34 Fix13.txt
-rw-r--r--  1 ninoniauri  staff    19B Mar 27 21:35 fix14.txt
ninoniauri@Ninos-MacBook-Air Test % git add Fix14.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit of Fix 14 branch"
On branch fix14
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fix14.txt

nothing added to commit but untracked files present (use "git add" to track)
ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit of Fix 14 branch"
On branch fix14
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fix14.txt

nothing added to commit but untracked files present (use "git add" to track)
ninoniauri@Ninos-MacBook-Air Test %  git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 16
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 21:19 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 21:34 Fix13.txt
-rw-r--r--  1 ninoniauri  staff    19B Mar 27 21:35 fix14.txt
ninoniauri@Ninos-MacBook-Air Test % echo "Two branches was added to this repository" >
> README.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "Added the second line into README.txt"
[Master b029307] Added the second line into README.txt
 1 file changed, 1 insertion(+)
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all
* b029307 (HEAD, master) Added the second line into README.txt
* 57f67ef (fix14, fix13) Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test % git merge fix14
Already up to date.
ninoniauri@Ninos-MacBook-Air Test % git checkout -b fix15
Switched to a new branch 'fix15'
ninoniauri@Ninos-MacBook-Air Test % echo "It's Fix 15 branch" > fix15.txt
ninoniauri@Ninos-MacBook-Air Test % touch Fix15.txt
ninoniauri@Ninos-MacBook-Air Test % git add Fix15.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit for Fix15 branch"
On branch fix15
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fix14.txt
        fix15.txt

nothing added to commit but untracked files present (use "git add" to track)
ninoniauri@Ninos-MacBook-Air Test % git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test % echo "Fix 15 branch was added to the repository" >> README.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "added 3th line in README.txt file"
[Master 9cbeb72] added 3th line in README.txt file
 1 file changed, 1 insertion(+)
ninoniauri@Ninos-MacBook-Air Test % git checkout fix15
Switched to branch 'fix15'
ninoniauri@Ninos-MacBook-Air Test % echo "It's the second line of this file" >> fix15.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "2nd commit of Fix15 branch"
On branch fix15
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fix14.txt
ninoniauri@Ninos-MacBook-Air Test % git branch   
  master
ninoniauri@Ninos-MacBook-Air Test % git log
commit 9cbeb72e574d13a667bb3775bdb1d2af39956003 (HEAD, master)
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 21:40:20 2023 +0400

    added 3th line in README.txt file

commit b029307e458b66acf9b8f215d991cc3dbab8b476
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 21:38:19 2023 +0400

    Added the second line into README.txt

commit 57f67ef580bbcee58b02472c5c5725381a40b72c
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 21:31:04 2023 +0400

    Initial commit of fix13 branch

commit d1597b964eb1195ee183dc653972694007e68ecf
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 21:20:16 2023 +0400

ninoniauri@Ninos-MacBook-Air Test % git checkout -b fix13
Switched to a new branch 'fix13'
ninoniauri@Ninos-MacBook-Air Test % git status
On branch fix13
nothing to commit, working tree clean
ninoniauri@Ninos-MacBook-Air Test % touch Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % git add Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % git status
On branch fix13
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Fix13.txt

ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit of fix13 branch"
[fix13 febd544] Initial commit of fix13 branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test %  git log --pretty=format:"%h %cd %an '%s'"
febd544 Mon Mar 27 23:19:21 2023 +0400 Nino Niauri 'Initial commit of fix13 branch'
d1597b9 Mon Mar 27 21:20:16 2023 +0400 Nino Niauri 'Added README file content'
9fd3f3f Mon Mar 27 21:19:29 2023 +0400 Nino Niauri 'initial commit'
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 8
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 23:16 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 23:18 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test %  ls -ltrh
total 8
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 23:16 README.txt
ninoniauri@Ninos-MacBook-Air Test % git merge Fix13
Updating d1597b9..febd544
Fast-forward
 Fix13.txt | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 8
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 23:16 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 23:20 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % git log --pretty=format:"%h %cd %an '%s'"
febd544 Mon Mar 27 23:19:21 2023 +0400 Nino Niauri 'Initial commit of fix13 branch'
d1597b9 Mon Mar 27 21:20:16 2023 +0400 Nino Niauri 'Added README file content'
9fd3f3f Mon Mar 27 21:19:29 2023 +0400 Nino Niauri 'initial commit'
ninoniauri@Ninos-MacBook-Air Test % git checkout -b fix14
Switched to a new branch 'fix14'
ninoniauri@Ninos-MacBook-Air Test % echo "It's Fix 14 branch"> fix14.txt
ninoniauri@Ninos-MacBook-Air Test %  ls -ltrh
total 16
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 23:16 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 23:20 Fix13.txt
-rw-r--r--  1 ninoniauri  staff    19B Mar 27 23:21 fix14.txt
ninoniauri@Ninos-MacBook-Air Test %  git add
Nothing specified, nothing added.
hint: Maybe you wanted to say 'git add .'?
hint: Turn this message off by running
hint: "git config advice.addEmptyPathspec false"
ninoniauri@Ninos-MacBook-Air Test % touch Fix14.txt
ninoniauri@Ninos-MacBook-Air Test % git add Fix14.txt
ninoniauri@Ninos-MacBook-Air Test % echo "It's Fix 14 branch"> fix14.txt
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 16
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 23:16 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 23:20 Fix13.txt
-rw-r--r--  1 ninoniauri  staff    19B Mar 27 23:23 fix14.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit of Fix 14 branch"
On branch fix14
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fix14.txt

nothing added to commit but untracked files present (use "git add" to track)
ninoniauri@Ninos-MacBook-Air Test % git status
On branch fix14
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fix14.txt

nothing added to commit but untracked files present (use "git add" to track)
ninoniauri@Ninos-MacBook-Air Test % git add .
ninoniauri@Ninos-MacBook-Air Test % git status
On branch fix14
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   fix14.txt

ninoniauri@Ninos-MacBook-Air Test % commit -m "Initial commit of Fix 14 branch"
zsh: command not found: commit
ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit of Fix 14 branch"
[fix14 1969170] Initial commit of Fix 14 branch
 1 file changed, 1 insertion(+)
 create mode 100644 fix14.txt
ninoniauri@Ninos-MacBook-Air Test % git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 8
-rw-r--r--  1 ninoniauri  staff    26B Mar 27 23:16 README.txt
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 23:20 Fix13.txt
ninoniauri@Ninos-MacBook-Air Test % echo "Two branches was added to this repository" >>README.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "Added the second line into README.txt"
[Master 4cd596f] Added the second line into README.txt
 1 file changed, 1 insertion(+)
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all
* 4cd596f (HEAD, master) Added the second line into README.txt
| * 1969170 (fix14) Initial commit of Fix 14 branch
|/  
* febd544 (fix13) Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test % git merge fix14
hint: Waiting for your editor to close the file... error: cannot run mvim: No such file or directory
error: unable to start editor 'mvim'
Not committing merge; use 'git commit' to complete the merge.
ninoniauri@Ninos-MacBook-Air Test % git branch
  fix13
  fix14
  master
ninoniauri@Ninos-MacBook-Air Test % git merge Fix14
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.
ninoniauri@Ninos-MacBook-Air Test % git status
On branch Master
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        new file:   fix14.txt

ninoniauri@Ninos-MacBook-Air Test % git checkout fix14
Switched to branch 'fix14'
ninoniauri@Ninos-MacBook-Air Test % git log
commit 1969170f1ca2a386313e6e5478b0b103544ef5dd (HEAD -> fix14)
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 23:25:12 2023 +0400

    Initial commit of Fix 14 branch

commit febd5445e0069e81f06896e4463d97ebb2fd5ab1 (fix13)
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 23:19:21 2023 +0400

    Initial commit of fix13 branch

commit d1597b964eb1195ee183dc653972694007e68ecf
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 21:20:16 2023 +0400

    Added README file content

commit 9fd3f3f50cae8e2924734e0513f040ffd2331fd4
Author: Nino Niauri <ninoniauri3@gmail.com>
Date:   Mon Mar 27 21:19:29 2023 +0400

    initial commit
ninoniauri@Ninos-MacBook-Air Test % git checkout master
Switched to branch 'master'
ninoniauri@Ninos-MacBook-Air Test % git diff       
ninoniauri@Ninos-MacBook-Air Test % git status
On branch master
nothing to commit, working tree clean
ninoniauri@Ninos-MacBook-Air Test % git merge fix14
hint: Waiting for your editor to close the file... error: cannot run mvim: No such file or directory
error: unable to start editor 'mvim'
Not committing merge; use 'git commit' to complete the merge.
ninoniauri@Ninos-MacBook-Air Test % git merge fix14.txt
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "Added the second line into README.txt"
[master b27b438] Added the second line into README.txt
ninoniauri@Ninos-MacBook-Air Test % git merge fix14
Already up to date.
ninoniauri@Ninos-MacBook-Air Test % get checkout master
zsh: command not found: get
ninoniauri@Ninos-MacBook-Air Test % git checkout master
Already on 'master'
ninoniauri@Ninos-MacBook-Air Test % ls -ltrh
total 16
-rw-r--r--  1 ninoniauri  staff     0B Mar 27 23:20 Fix13.txt
-rw-r--r--  1 ninoniauri  staff    68B Mar 27 23:29 README.txt
-rw-r--r--  1 ninoniauri  staff    19B Mar 27 23:30 fix14.txt
ninoniauri@Ninos-MacBook-Air Test % echo "Two branches was added to this repository" >>
README.txt
zsh: parse error near `\n'
ninoniauri@Ninos-MacBook-Air Test % echo "Two branches was added to this repository" >>README.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "Added the second line into README.txt"
[master 19a2a23] Added the second line into README.txt
 1 file changed, 1 insertion(+)
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all
* 19a2a23 (HEAD -> master) Added the second line into README.txt
*   b27b438 Added the second line into README.txt
|\  
| * 1969170 (fix14) Initial commit of Fix 14 branch
* | 4cd596f Added the second line into README.txt
|/  
* febd544 (fix13) Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test % git merge fix14
Already up to date.
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all
* 19a2a23 (HEAD -> master) Added the second line into README.txt
*   b27b438 Added the second line into README.txt
|\  
| * 1969170 (fix14) Initial commit of Fix 14 branch
* | 4cd596f Added the second line into README.txt
|/  
* febd544 (fix13) Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test % git checkout -b fix15
Switched to a new branch 'fix15'
ninoniauri@Ninos-MacBook-Air Test % echo "It's Fix 15 branch" > fix15.txt
ninoniauri@Ninos-MacBook-Air Test % git add .
ninoniauri@Ninos-MacBook-Air Test % git commit -m "Initial commit for Fix15 branch"
[fix15 3318494] Initial commit for Fix15 branch
 1 file changed, 1 insertion(+)
 create mode 100644 fix15.txt
ninoniauri@Ninos-MacBook-Air Test % git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test % echo "Fix 15 branch was added to the repository" >>README.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "added 3th line in README.txt file"
[Master e3b5d91] added 3th line in README.txt file
 1 file changed, 1 insertion(+)
ninoniauri@Ninos-MacBook-Air Test % git checkout fix15
Switched to branch 'fix15'
ninoniauri@Ninos-MacBook-Air Test % echo "It's the second line of this file" >> fix15.txt
ninoniauri@Ninos-MacBook-Air Test % git commit -a -m "2nd commit of Fix15 branch"
[fix15 23e92a1] 2nd commit of Fix15 branch
 1 file changed, 1 insertion(+)
ninoniauri@Ninos-MacBook-Air Test % git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all -7
* 23e92a1 (fix15) 2nd commit of Fix15 branch
* 3318494 Initial commit for Fix15 branch
| * e3b5d91 (HEAD, master) added 3th line in README.txt file
|/  
* 19a2a23 Added the second line into README.txt
*   b27b438 Added the second line into README.txt
|\  
| * 1969170 (fix14) Initial commit of Fix 14 branch
* | 4cd596f Added the second line into README.txt
|/  
ninoniauri@Ninos-MacBook-Air Test % git rebase Fix15
Successfully rebased and updated refs/heads/Master.
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all
* 083517c (HEAD, master) added 3th line in README.txt file
* 23e92a1 (fix15) 2nd commit of Fix15 branch
* 3318494 Initial commit for Fix15 branch
* 19a2a23 Added the second line into README.txt
*   b27b438 Added the second line into README.txt
|\  
| * 1969170 (fix14) Initial commit of Fix 14 branch
* | 4cd596f Added the second line into README.txt
|/  
* febd544 (fix13) Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test %  git branch -a
  fix13
  fix14
  fix15
  master
ninoniauri@Ninos-MacBook-Air Test % git branch -D fix13 fix14 fix15
Deleted branch fix13 (was febd544).
Deleted branch fix14 (was 1969170).
Deleted branch fix15 (was 23e92a1).
ninoniauri@Ninos-MacBook-Air Test % git branch -a
  master
ninoniauri@Ninos-MacBook-Air Test %  git log --graph --oneline --decorate --all
* 083517c (HEAD, master) added 3th line in README.txt file
* 23e92a1 2nd commit of Fix15 branch
* 3318494 Initial commit for Fix15 branch
* 19a2a23 Added the second line into README.txt
*   b27b438 Added the second line into README.txt
|\  
| * 1969170 Initial commit of Fix 14 branch
* | 4cd596f Added the second line into README.txt
|/  
* febd544 Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test % 
