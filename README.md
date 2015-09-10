# gitCommands

###Renaming a branch in github
If you want to rename a branch while pointed to any branch, simply do :
```
git branch -m <oldname> <newname>
```
If you want to rename the current branch, you can simply do:
```
git branch -m <newname>
```
###Listing Remote Branches
La forma más fácil de listar las ramas disponibles en un repositorio es utilizando las distintas opciones del comando
 _git branch -a_, por ejemplo, muestra todas las ramas locales y remotas, mientras que _git branch -r_ muestra unicamente las ramas remotas.
 ```
$ git branch
* master

$ git branch -a
* master
  origin/1-2-stable
  origin/2-0-stable
  origin/3-0-unstable
  origin/HEAD
  origin/master

$ git branch -r
  origin/1-2-stable
  origin/2-0-stable
  origin/3-0-unstable
  origin/HEAD
  origin/master
```

###Fetching branches
You can fetch one branch from all remotes like this:
```
git fetch --all
```
**Delete a Git branch both locally and remotely**
To remove a local branch from your machine:
```
git branch -d the_local_branch
```
To remove a remote branch from the server:
```
git push origin :the_remote_branch
```

or also As of Git v1.7.0, you can delete a remote branch using
```
git push origin --delete <branchName>
```
which is easier to remember than
```
git push origin :<branchName>
```
###Mergin
digamos que estoy en un branch propio por ejemplo, TICKET-123, y quiero traerme las cosas que los demas desarolladores ya mergearon a la rama DEVELOP tendriamos primero que pararnos en nuestra rama.
```
git checkout TICKET-123
```
y luego traernos los cambios ejecutando el comando _merge_, en este comando lo que se indica es:
git trae a mi rama (en la cual estoy poscisionado) los cambios que hay en la rama [TARGET] (en nuestro caso DEVELOP)
```
git merge DEVELOP
```
