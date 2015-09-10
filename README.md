# gitCommands

**Renaming a branch in github**
```
git branch -m oldname newname
```
**Mergin**
digamos que estoy en un branch propio por ejemplo, TICKET-123, y quiero traerme las cosas que los demas desarolladores ya mergearon a la rama DEVELOP tendriamos primero que pararnos en nuestra rama.
```
git checkout TICKET-123
```
y luego traernos los cambios ejecutando el comando _merge_, en este comando lo que se indica es:
git trae a mi rama (en la cual estoy poscisionado) los cambios que hay en la rama [TARGET] (en nuestro caso DEVELOP)
```
git merge DEVELOP
```
**Renombrar un Branch**
If you want to rename a branch while pointed to any branch, simply do :
```
git branch -m <oldname> <newname>
```
If you want to rename the current branch, you can simply do:
```
git branch -m <newname>
```
