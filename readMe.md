# first test Erwan Duchêne

## Compte rendu commandes git

### commandes de bases

    git config --global user.name "El Maknati Abdellatif"
    git config --global user.email "abdellatif.elmaknati@gmail.com"

ces deux commandes successives permettent de configurer localement les paramètres du répo local.

    git clone [https link/ssh link]

` Cloning into 'testGitlab'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.`

clone le repo distant vers le repo local.

**on ajoute un fichier texte
<br>
<br>
<br>
<br>
<br>

    * git add [nom du fichier]

`$ git commit -m "new text file"
[main 4ea7d0d] new text file
 1 file changed, 1 insertion(+)
 create mode 100644 hello.txt
`

ajoute les modification à l'index

<br>
<br>
<br>
<br>
<br>

    git commit -m "[texte du message]"
    ou
    git commit -a


`[main 4ea7d0d] new text file
 1 file changed, 1 insertion(+)
 create mode 100644 hello.txt
`

enregistre sous un commit les changements indexés

<br>
<br>
<br>
<br>
<br>

    git push -u origin [nom de la branche]

`Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 284 bytes | 284.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://gitlab.com/margouillat/testGitlab.git
   9fbd20f..4ea7d0d  main -> main
branch 'main' set up to track 'origin/main'.`

pousse les changements en commit sur le repo distant
<br>
<br>


### Corriger des erreurs

    git log

`commit e926db95502314a6d4f962d643b0668ebda2ccee (HEAD -> main)
Author: margouillat <erwanduchene@gmail.com>
Date:   Mon Oct 7 12:04:50 2024 +0200
ajout erreur
commit 4ea7d0d424d8bfce5ff25bf3f942ffbfd5ab7654 (origin/main, origin/HEAD)
Author: margouillat <erwanduchene@gmail.com>
Date:   Mon Oct 7 12:02:31 2024 +0200
new text file
commit 9fbd20f0ca947d85b333ddb549729e44ed336595
Author: Erwan DUCHENE (Margouillat) <erwanduchene@gmail.com>
Date:   Mon Oct 7 09:59:41 2024 +0000
Update README.md
commit 6524ec5fe73ad374719dcfc222fee0a0745ebf92
Author: Erwan DUCHENE (Margouillat) <erwanduchene@gmail.com>
Date:   Mon Oct 7 09:56:11 2024 +0000
Initial commit
`

affiche les commits enregistrés sur la branche

<br>
<br>
<br>
<br>

    git commit --amend

permet de modifier le texte du commit

    git reset [id_du_commit]

retourne à la version du commit spécifié dans la commandes
<br>
<br>
<br>
<br>
<br>

### Résolution de conflits
Si lors d'un 

    git pull

des conflits apparaissent, il faut vérifier et corriger les conflits sur l'IDE de votre choix

Ensuite , __comit__ les changements validés

### Ajouter des tags

    git tag v0.1 [id_du_commit]

ajoute un tag au commit spécifié

pour vérifier le tag, faire un git log

    git push --tags

pousse les tags sur le répo distant


### Créer et supprimer des branches

    git branch [nom_de_la_branche]

    git checkout -b

Créer une nouvelle branche (le git checkout -b permet de créer et de se déplacer directement sur la branche créée)

    git checkout [nom_de_branche]

permet de se déplacer sur les différentes branches

    git branch -d [nom_de_branche]

supprime la branche spécifié (__ne pas être sur la dite branche__)
