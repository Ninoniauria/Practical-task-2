# Practical-task-2
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
        fix15.txt

nothing added to commit but untracked files present (use "git add" to track)
ninoniauri@Ninos-MacBook-Air Test % git checkout Master
Switched to branch 'Master'
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all -7
* 9cbeb72 (HEAD, master) added 3th line in README.txt file
* b029307 (fix15) Added the second line into README.txt
* 57f67ef (fix14, fix13) Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test %  git rebase Fix15
Current branch Master is up to date.
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all
* 9cbeb72 (HEAD, master) added 3th line in README.txt file
* b029307 (fix15) Added the second line into README.txt
* 57f67ef (fix14, fix13) Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test % git branch -a
  fix13
  fix14
  fix15
  master
ninoniauri@Ninos-MacBook-Air Test % git branch -D fix13 fix14 fix15
Deleted branch fix13 (was 57f67ef).
Deleted branch fix14 (was 57f67ef).
Deleted branch fix15 (was b029307).
ninoniauri@Ninos-MacBook-Air Test % git branch -a
  master
ninoniauri@Ninos-MacBook-Air Test % git log --graph --oneline --decorate --all
* 9cbeb72 (HEAD, master) added 3th line in README.txt file
* b029307 Added the second line into README.txt
* 57f67ef Initial commit of fix13 branch
* d1597b9 Added README file content
* 9fd3f3f initial commit
ninoniauri@Ninos-MacBook-Air Test % 
