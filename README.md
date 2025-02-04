# Git Essential Commands
Git is a version control system. Git helps you keep track of code changes.

A — Files added to stage
M — Modified files
D — Deleted files

### 1. Update local current feature branch with Develop/Master branch

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git stash  ---------- save you local changes / untracked files
$ git pull origin develop -------- if want to pull from develop branch
$ git stash apply -------- apply you local changes on develop branch's changes

resolve merge conflict if you have
```
 
</p>
</details>

---

### 2. Push local repository content to a remote repository

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git status
$ git add . ---------------------------------------- move your local working directory changes to staging are
$ git commit -m "commit msg"  ---------------------- commit your all changes

commit few particular files
============================================================
git commit file1 file2 file5 -m "commit message"

Note: git reset  -------- opposit of "git add .". revet your staging changes to local working directory

if remote repository already exists in git
===========================================================
$ git push 
if remote repository not exists in git
===========================================================
$ git push --set-upstream origin <your branch name>
OR
$ git push -u origin <your branch name>
```

Let me explain you using VS code. In VS code, we have changes & stage changes section in left panel. Will be easy to relate with VS Code.
```
git add .   ------------ Move all local changed files to stage changes
git add scm-provider-category.png --------- only move particular file to stage changes
```
![stage changes]([http://url/to/img.png](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*og7TRCo3IOQ1iWUCwPNU1w.png))

if you want to un-stage the file (scm-provide-category.png)
```
git reset ------------- unstage all stage changes file & move back to changes section
git reset scm-provider-category.png -------- unstage only a particular file
```
 
</p>
</details>

---

### 3. Checkout command uses

<details><summary><b>Answer</b></summary>
<p>

#### 
Let’s say, you already pushed a file contact.html with your codes. now someone mistakenly change/delete your contact.html file. Then using git status you can see your modified files details like the following way.

![checkout](https://miro.medium.com/v2/resize:fit:828/format:webp/1*VdyI7NXLOsH_DmrykakGxw.png)

Now how you will get your already pushed contact.html file? Here checkout command comes to help. The checkout command retrieve the already pushed contact.html file with changes.

```
git checkout commands match your working directory with the last commit

match contact.html file of working directory with your last commited contact.html file
======================================================================
$ git checkout contact.html 

match all files of working directory with your last commit
======================================================================
$git checkout -f
```
![checkout final](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*OReZbMr3lPuyzTZAxzFhhQ.png)

</p>
</details>

---

### 4. Git Diff

<details><summary><b>Answer</b></summary>
<p>

#### 
git diff compares working tree with staging area.

git diff command allows us to track the changes that are staged but not committed

Let’s say, i have changed a file file.txt of my working directory. I want to compare my latest changed file.txt with my staging file.txt file. staging file not committed file.
```
Compare all current working directory changes with Staging area or previous commited changes one by one
=====================================================================
$ git diff


Compare one particular file of current working directory with Staging area or previous commited change
========================================================================
$ git diff contact.html
```
red color highlights replaced text, green color newly added text

![color highlight](https://miro.medium.com/v2/resize:fit:828/format:webp/0*RuRXz1jahSk7YKPN.png)

if you run command “git add file.txt”, now again run command “git diff”. It will not show anything. Because “git add file.txt” already pushed my changed file to stage.
If i want to compare staging area with last commit : `git diff — staged`

</p>
</details>

---

### 5. Git configure for first time in your local

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git config --global user.name "Firstname Lastname"
$ git config --global user.email "myemail@example.com"
```
 
</p>
</details>

---

### 6. Want to display global name & email already stored in you local Git

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git config --global user.name "Firstname Lastname"
$ git config --global user.email "myemail@example.com"
```
 
</p>
</details>

---

### 7. Git Initialize

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git init --------- initialize empty git repo
$ ls -lart --------- show all hidden folders of the current folder. you can see .git folder
```
 
</p>
</details>

---

### 8. Clone a repository

<details><summary><b>Answer</b></summary>
<p>

#### 
create a folder -> go inside the folder -> run git bash
```
git clone <clone repo url>
```
 
</p>
</details>

---

### 9. Merge local branch to master

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git checkout master
$ git merge <local branch name>
$ git push -u origin master
```
 
</p>
</details>

---

### 10. Delete Local Branch

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git branch -D <branch-name>
```
 
</p>
</details>

---

### 11. Delete Remote Branch

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git checkout master
$ git push origin --delete <local branch name>
```
 
</p>
</details>

---

### 12. Display all local branches. For current branch, display with * In front of the branch name & green color for black git background

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git branch
```
 
</p>
</details>

---

### 13. Create Branch

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git branch <branch name>
```
 
</p>
</details>

---

### 14. Create & switching a New branch

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git checkout -b <feature-branch>
```
 
</p>
</details>

---

### 15. Change Branch

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git checkout <existing branch name>
```
 
</p>
</details>

---

### 16. Pull changes from existing current branch

<details><summary><b>Answer</b></summary>
<p>

#### 
let’s say that you are in a branch (feature-user). if you want to pull changes of that
```
git pull
```
 
</p>
</details>

---

### 17. Pull changes from other branch in current branch

<details><summary><b>Answer</b></summary>
<p>

#### 
let’s say that you are in a branch (feature-user). if you want to pull changes of that
```
git pull origin <other branch name>
```
 
</p>
</details>

---

### 18. Pull all remote branches

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git pull — all
```
 
</p>
</details>

---

### 19. Display untacked files in you local

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git status
```
 
</p>
</details>

---

### 20. Remove File

<details><summary><b>Answer</b></summary>
<p>

#### 
git rm command deletes files both from the Git repository as well as the filesystem.
```git rm <file name>```

git rm — cached removes the file only from the Git repository, but not from the filesystem.
```git rm — cached <file name>```
 
</p>
</details>

---

### 21. Fetching Remote repository data

<details><summary><b>Answer</b></summary>
<p>

#### 
git pull copies changes from a remote repository directly into your working directory, while git fetch does not. The git fetch command only copies changes into your local Git repo.
```
git fetch
``` 
</p>
</details>

---

### 22. Ignoring by GIT

<details><summary><b>Answer</b></summary>
<p>

#### 
Git will not track files and folders specified in .gitignore. When sharing your code with others, there are often files or parts of your project, you do not want to share.

Examples

log files
temporary files
hidden files
personal files
etc.
</p>
</details>

---

### 23. Git logger details (how many commits with files info like author’s email, date)

<details><summary><b>Answer</b></summary>
<p>

#### 
```
git log  --------- all previous commits details
git log -p -5 --------- will display only last 5 commits

press Q to quit to excapse from displaying git log details
```
</p>
</details>

---

### 24. Display list of all Git configurations

<details><summary><b>Answer</b></summary>
<p>

#### 
```
$ git config - global - list
user.name=Firstname Lastname
user.pasword=Admin@12      -------------------- demo test password
user.email=myemail@example.com

git config --global --get user.name -------------------- shows your username.
git config --global --get user.email -------------------- displays your email.
git config --global credential.helper -------------------- verify credentials.
git config --global    
```
</p>
</details>

---
