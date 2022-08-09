# GIT

## New repository in Git
- _`'git init'`_ - to create a new repository 
- Add USER and EMAil _before_ to make a command "Git Commit"
1. "git config user.name"
2. "git config user.email"
----------------------------
## Commands to work in derictory
- _`touch main.js`_ - to create new file
- _`mkdir`_ - to create new repository
- _`ls`_ - to observe visible files in directory
- _`ls -a`_ - to observe all files in directory (unvisible also)
- _`cp foo.txt bar.txt`_ - to copy file in directory  => _cp ./foo.txt ./bar.txt_
- _`mv foo.txt ./folderName`_ - to move+copy file to upper directory  =>   _`mv foo.txt ../folderName`_ - to move files to down directoty                         
- _`cat foo.txt`_ - to observe the content of the file
- _`rm`_ - to deleta a file or repository

## Movement between directories
- _`cd`_ - to move to the base
- _`cd /d`_ to move to the disk d 
- _`cd /d/folderName` - to move to the directory on disk D
- _`cd /d/folderNam/folderProgect`_ - to move to the initial directory
- _`cd ../` - move to the down directory (previous directory which contains this foldre) => we will got the way 
from `cd /d/folderNam/folderProgect` to `cd /d/folderNam`

- _Before to do Git Commit - IS IMPORTANT to do command_'Git Status"
_After to do a commnad 'GIT ADD' - git starts to control the added files - it means that the files moved to STAGING AREA
1. _git status_
2. to move ALL changes/files from directory to _STAGING AREA
* command: _'git add . '_
* after this all changes/files from directory will move to _Staging Area_
3. _againe - git status
_THAN to do 'GIT COMMIT" - this allow to FIX (remember) CURRENT STATUS OF THE FILE_

!! to UnStage -to remove files from staging area _to use a command:
- git restore --stages _fileName

4. *git commit -m "second commit"
   '-m "_description"' - MASSEDGE; allow to make the DESCRIPTION direcltly / to do the commit DIRECTLY, without additional window to add the information about the file.
   
 ### to do COMMIT WITHOUT additional command 'git add' _should to do_:
 - command: _git commit -a -m "commitName"_ - allow to move files to staging area and to do commit - AT ONCE

### * ! _`git log`_ - to check the commit in the repository: it shows  _hash_  , _Autor_  , _Date_   of the commit;  
 
-----------------------
- To create a repository and commit new change - command: _git commit_ `(c0)-(c1)-(c2)`
_перехід `(c0)-(c1)`
-------------
To create a BRANCH - command: git branch newName - now the branche links to commit_(c1)
Before adding 'NEW commit' is important to MOVE to new (created) BRANCH - command: git checkout [nemName]
After that thr commit will be don on this New (created) BRANCH - git commit
To sum up: to create new branche and commit
1. git branch newName
2. git checkout newName 
3. git commit
-------------------
Branches and that MERGER: the approach to connect the information from a few or more branches  
1 - git merge 
merge - злипити 
This ALLOW to create the specific commit which containe TWO uniq 'parents'; it means that this commit involve information from both parents and predecessors (попередники)
This approach is beneficcial when we have few different branches wirh lesss work information
command: - git merge newName (останнє ім'я створене в істроії)
мерджити за останнім ім'ям що було створено з попередників (при мерджі за ім'ям попередника гілки зіль'ються але імя останнього не перейде до нової 'злитої' гілки
2 - git rebase
another way to combine the changes from different branches
- rebase_just take few commits - copy tham - and put tham into another plase 
IS USED TO cteate comfortable liniar consistency
Commit log and history on this way will be more CLEAR
на відміну від merge (злиття) за ім'ям комміту в одну гілку САМЕ REBASE переводить копью комміттів до вказаної гілки _git rebase brName_ 
-Але усі зміни (комміти) переходять попереду паренту (на гілку якого зроблений ребейз)
- Щоб просунути усі комміти на один стєйдж НЕОБХІДНО
-перетий до комміту паренту (на гілку якого робили ребейз) - _git checkout parentName
- з цього коміту робимо ребейз до 'створеного нащадку' - ПРОСУВАННЯ ГІЛКИ ВПЕРЕЛД В ІСТОРІЇ - _git rebase childName
To Sum Up
1. git rebase prName (main)
2. git checkout prName (main)
3. git rebase childName
--------------------------------
- HASH _is an individual namberName of a commit
- HAED of commit _means the strage/version of document which is in wrok currently
--------------------------------

# GIT to GitHub
Before is important:
* to add repository to GitHub (to create an accont on GitHub)
* to `'fork'` repository from GitH _`'eleks/fork-me'`_ to my account _`'Anna/fork-me'`_
* to `'clone'` repository from my own GitHub _account_ to my _local computer_

command: `'clone' + link (HTTPS/SSH)` for example _https://github.com/AnnaHuskova/fork-me.git_ (link from my GitHub FORKED repository 'code' buttom)

### HOW TO OPEN VS Code from GitBash Terminal
- in TERMINAL command: `'code .'`

= VS Code is opened

### HOW TO OPEN _TERMINAL_ in VS Code
`Ctrl + ~ 'tilda'`

----------------------
## REMOTE REPOSITORY connection (віддалений репозеторій)
before to do _`'git push'`_  `->`  it is neccesary to do _`'git token'`_.
before to do _`'git token'`_  `->`  it is important to do _`'git remote -v'`_
* _`'git remote'`_ - shows all remote repository which i manage
* 

- How to connect with GitHub :

!!! `Local repository` can send changes to `remote repository`

Щоб відправити дані на віддалений репозиторій - необхідно створити `token`

 - `token` створюється у GitHub аккаунті та працює з усіма моїми репозіторіями: my account -> `settings` -> `developer settings` -> `personal access tokens` -> `generate new token`

- command: `git remote add origin http://link of token @ link of githab repository .git` - або відредагувати оріджін всередені vs code
- command: `git remote -v` - to absorve all repository 


 1. command: _`'git push'`_ (means to move the chfnges somewhere)
 2. command: _`'git push origin brancheName'`_ - origin it is name of the terminal (means to move changes to DIRECT to DEFINE Remote and Branch - до визначеного віддал.репозиторію та папки) 

! To connect _main_ local branch with remote branche:
- commnad: _`git push -u origin main`_ - `-u` is upstream - для цієїж гілки `main` роблю зв'язок з такою ж гілкоюна віддаленому репозиторії;

















