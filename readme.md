# GIT

## New repository in Git

To create a repository and commit new change - command: git commit (c0)-(c1)-(c2)
_перехід (c0)-(c1)
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
----------------------------------




