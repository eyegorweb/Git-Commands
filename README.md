Git Commands
============

A list of my commonly used Git commands

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git add -u` | Add only changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git fetch origin` | Fetch and update files from remote repository |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote -v` | List remote repository urls |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Revert and reset (cancel, undo, unchange...)

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### Notes à ajouter au fichier README.md

Créer une branche en local => git checkout -b release-2.10.0 
et écouter la branche distante => origin/release-2.10.0 
en une commande : 
git checkout -b release-2.10.0 origin/release-2.10.0 
équivaut à 
git branch --set-upstream-to=origin/develop develop 

git checkout permet de savoir quelle branche on écoute 
Your branch is up-to-date with 'origin/release-2.10.0’. 

git checkout -b nameOfTheBranch permet de créer une branche 

• git fetch is the command that says "bring my local copy of the remote repository up to date." 
• git pull says "bring the changes in the remote repository where I keep my own code. » 

git checkout -b feature-sprint-5.2 git branch --set-upstream-to=origin/feature-sprint-5.2 feature-sprint-5.2 

Type : git checkout -b feature-sprint-5.2 origin/feature-sprint-5.2 => Branch feature-sprint-5.2 set up to track remote branch feature-sprint-5.2 from origin. 
=> Switched to a new branch 'feature-sprint-5.2’ 

git reset --hard : revenir sur le dernier commit 

git reset idcommit : revenir sur le id commit 

git clone http://prafatfsat1:8080/tfs/Web10/AF.Espace_Client/_git/vsup-back-config 
git branch -a 
git checkout -b develop origin/develop git branch -vv 
||
Voir les configuration d’upstream : git branch -vv
git fetch && git checkout mabranche
git branch --set-upstream-to=origin/feature-sprint-4.3 feature-sprint-4.3
git push --set-upstream origin ORION-2338
RACCOURCI: 
git branch -u origin/feature-sprint-4.3

REMISE à plus tard une modification 
git stash 
git stash list 
git stash apply 

git pull —rebase 
git add -u 
git rebase —continue 

quand il y a un conflit après!s un git pull sur un fichier par exemple: 
CONFLICT (content): Merge conflict in e-retrait-front-ui/jcr_root/etc/designs/axa/withdrawal/clientlib_base/js/scripts/components/controllers/withdrawal-otp.controller.js 

il faut aller sur le fichier et fixer les modifications puis en ligne de commande faire git add . ou git add -u et git rebase —continue git rebase —continue 

et on est à jour sans conflit 

git log --pretty=oneline 

git log —oneline 

http://stackoverflow.com/questions/12876350/diff-returning-entire-file-for-identical-files 

git checkout -b feature-sprint-5.4 
git fetch 

git branch --set-upstream-to=origin/feature-sprint-5.4  feature-sprint-5.4 

wstorm espace-client-front/ 

nano bash_profile 
mv bash_profile /Users/igortrifunovic/.bash_profile 
mv m2 /Users/igortrifunovic/.m2 

pwd 

git fetch -a -p 
Met à jour les branches (recul et suppression par rapport à la remote)

git branch -a 
Montre les branches en local et en remote 

alias => permet de lire tous ces alias ;-) 

git fetch —all 

git checkout -b feature-sprint-5.6 origin/feature-sprint-5.6 

Faire un git fetch —all puis un git status permet de voir un message de mise à jour par rapport à la remote distante 

ESLINT 
eslint en ligne de commande puis tab deux fois pour lire les dossiers et trouver son chemin 

Depuis iMac-de-Igor:e-retrait-front-ui igortrifunovic$ 
eslint jcr_root/etc/designs/axa/withdrawal/clientlib_base/js/scripts/*/*.js 

BASH_PROFILE: 
Exécuter un .bash_profile => ./.bash_profile 
cd ; => va à la racine de la machine 
sudo nano .bash_profile => ouvre le fichier .bash_profile 

http://stackoverflow.com/questions/7726131/git-add-a-is-not-adding-all-modified-files-in-directories 

http://defeo.lu/in202/classes/class6/ 
git rm --cached repository/Resources/js/external/next-player 

Lister les fichiers modifiés lors du dernier commit 
git show --pretty="" --name-only id-sha-commit 

Git: Delete a branch (local or remote)

To delete a local branch
git branch -d the_local_branch
To remove a remote branch (if you know what you are doing!)
git push origin :the_remote_branch

Bonjour,

Le déploiement sur la recette est incomplet. https://stackoverflow.com/questions/424071/how-to-list-all-the-files-in-a-commit
Les projets suivants sont à mettre à jour: 

Projet : backbee/videobundle

* Les tickets suivants sont à mettre à jour ( Procédure GIT ) : 		•	#ORION-2260 ( Igor Trifunovic ) est en conflit avec le(les) ticket(s) suivants :		▪	#ORION-2372 ( Igor Trifunovic )		•	
    * Voici les fichiers impactés :		▪	Templates/scripts/partials/PlayerBrightcoveHtml5.html.twig
	Merci
	Sur ma branche	git checkout origin/developer path-file-conflict	ou git reset origin/developer path-file-conflict


git diff origin/ORION-1991 developer repository/Templates/scripts/Article/Article.twig 
Différence entre un fichier sur remote et local avec applicatifs:
git diff HEAD repository/Templates/scripts/Article/Article.twig
 

Configurer les exclude:

nano .git/info/exclude

http://stackoverflow.com/questions/10879783/git-doesnt-ignore-2-specifically-named-files

use "git checkout -- <file>..." to discard changes in working directory

git reflog
Reference logs, or "reflogs", record when the tips of branches and other references were updated in the local repository.

git rebase origin/developer ORION-2258 depuis branche locale ORION-2258

Compresser via line command (attention, ici le dossier sera enregistré dans le path où cette commande est lancée)
tar zcvf node_modules.tar.gz /Users/igortrifunovic/Desktop/node_modules/
 
One of the more helpful options is -p, which shows the difference introduced in each commit.
git log -p

Rebase
Rebaser une branche avec l’originale
git rebase developer
Au départ, on a une branche develop/master. Puis à partir de cette branche on crée une autre branche pour assurer une tâche/ticket (on dit que l’on fait une synchro). Le temps passe, et il se peut que develop ait été modifié par les autres. Du coup, on fait sur la branche develop un git fetch origin
, puis un git pull origin developer
Puis on se remet sur notre branche et on fait un git rebase origin, ce qui va nous montrer les conflits à résoudre depuis notre dernière création de la branche locale, jusqu’au plus récent commit sur developer. On résout les conflits et on git add, puis on git rebase —continue jusqu’à ce qu’il n'y ait plus de conflits. On va parcourir chaque commit qu’il y a eu sur developer et comparer avec notre branche les éventuels conflits avec nos fichiers. Ainsi, on se met à jour avec developer et notre branche que l’on déploiera sur recette n’aura plus de conflits avec les autres tickets/branches.
Sur gitlab, on peut comparer les deux branches et voir leurs derniers deversions. Comme on a créés notre branche à partir de developer, on a gardé l’historique de leur dernier commit en commun. En se positionnant sur notre branche créée à partir de developer, on recherche l’id du dernier commit de Jenkins User et on le voit apparaître à la suite de tous nos derniers commits. Sur la branche developer, on voit aussi que ce commit n’est plus le dernier depuis longtemps et qu’un tas de commits a été effectué depuis notre création de branche. Rebaser nous permet de remonter tous les commits en réglant les conflits et de terminer par refaire une mise à niveau avec la branche developer sur son dernier commit.
Une fois les conflits fixés, le rebase est fini et il faut forcer le push avec ses modification en faisant git push origin ORION-XXX --force

Annuler et effacer le dernier commit:
git reset --hard HEAD~ 

Delete remote branch:

git push origin --delete ORION-2446 

Copier un fichier depuis une branche vers sa branche courante: https://stackoverflow.com/questions/307579/how-do-i-copy-a-version-of-a-single-file-from-one-git-branch-to-another

git show ffd6bb3cb99b3d900f06cec8d0af55aa54ce7de0:repository/Templates/scripts/Article/Article.twig > repository/Templates/scripts/Article/Article.twig 

Se mettre sur ta branche (OIRON-1906) et tu copies mon fichier avec cette commande (mon dernier commit_hash est le: d425191aed63f107e88f74d84f2b5c038582c710)
git show <commit_hash>:repository/Templates/scripts/partials/footer-scripts.twig > repository/Templates/scripts/partials/footer-scripts.twig 

git show ebabadb4922b63ecfd0ad4f2df4a28e845ab4b51:repository/Templates/scripts/Article/Article.twig > repository/Templates/scripts/Article/Article.twig 

git reset -- composer.json 
 
gck — composer.json 

Pull instead rebase:
On branch ORION-2446, git pull origin developer puis merge diff files and if conflict, git proposes us to fix them. So, in PHPStorm, click right > Git > Resolve conflicts and double click on the file(s). And select what to add/delete from mine or server’s branch. git commit and git push 

Voir un conflit « caché »: on crée une branche test à partir de sa branche, on pull la branch en conflit  (git pull origin ORION-XXX) et on va sur phpstorm, git, resolve conflict et on voit ainsi clairement ce qui se cache comme conflit ! 

Ne pas commiter un fichier, ni le pusher
git reset -- composer.json
gck -- composer.json 

revert to a desired commit that was pushed(https://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit)
git checkout idcommit . (attention à bien mettre le point), puis git commit

Undo a git push:
git push -f origin last_known_good_commit:branch_name
Undo a rebase or a push (make a revert so)
git reset --hard HEAD@{XX}
git push -f origin ma_branche

List all the files in a commit
https://stackoverflow.com/questions/424071/how-to-list-all-the-files-in-a-commit

List the logs:
git log --pretty=format:"%h - %an, %ar : %s"

Git - Reset
https://git-scm.com/book/fr/v2/Utilitaires-Git-Reset-d%C3%A9mystifi%C3%A9

Rechercher (https://git-scm.com/book/fr/v2/Utilitaires-Git-Recherche)
Rechercher une expression régulière dans le répertoire, => rechercher Où l’expression apparait
git grep -n expression
Rechercher quand l’expression apparaît:
git log -Sexpression —online
Rechercher l’historique d’une ligne:
git log -L :expression:chemin°fichier

