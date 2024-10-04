#PRÁCTICA DE GIT 

A -  Los ejerccios resueltos

B -  El diagrama pedido en el apartado de 25

**A**

- ¿Qué comandos utilizaste en el paso 11? ¿Por qué?

  En el paso 11 he utilizadó el comando "git reset --soft HEAD~1". Porque este comando se utiliza para deshacer el último commit manteniendo los cambios en el área de preparación . Se usa cuando quieres revertir un commit pero deseas mantener el trabajo realizado para corregirlo o modificarlo antes de volver a hacer commit.
  
- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

  En el paso 12 he utilizadó el comando "git merge master". Porque, este comando intenta fusionar la rama master en la rama actual. Se usa para integrar los cambios que se han hecho en master a la rama en la que estás trabajando, en este caso, styled. Esto es importante para mantener la rama actualizada con los últimos cambios realizados en master.

- El merge del paso 13. ¿Causó algún conflicto? ¿Por qué?

  El merge en el paso 12 causó un conflicto, porque cuando hay cambios en el mismo archivo en ambas ramas (git-nuestro.md) que no se pueden fusionar automáticamente. Git requiere que el conflicto sea resuelto manualmente.

  
- El merge del paso 19. ¿Causó algún conflicto? ¿Por qué?

  No, el merge en el paso 19 no causó conflictos porque en este paso se resolvió el conflicto previamente encontrado al elegir el contenido de la rama styled para mantener. Se hizo un commit después de resolver el conflicto, por lo que no había más conflictos que resolver.
  
- El merge del paso 21. ¿Causó algún conflicto? ¿Por qué?

  No hay conflicto, porque aqui creo una nueva rama llamada title y, posteriormente, se hacen cambios en git-nuestro.md. 
  
- ¿Qué comando o comandos utilizaste en el paso 25?

  git log –graph
    
- El merge del paso 26. ¿Podría ser fast forward? ¿Por qué?

  git merge --no-ff title. En este caso, no se puede porque hay commits adicionales en main que no permiten que se mueva directamente la referencia sin un commit de fusión explícito.
  
- ¿Qué comando o comnados utilzaste en el paso 27?

  git checkout -- git-nuestro.md. Este comando lo utilice para descartar los cambios en git-nuestro.md, restaurándolo al último estado confirmado (commit). No afecta a otros archivos, solo al que se especifica.
  
- ¿Qué comando o comnados utilzaste en el paso 28?

  git branch -d title. Intenté usar git branch -d title para eliminar la rama title, pero me dio un error porque estaba en esa rama. No puedo eliminar una rama si estoy dentro de ella, así que tuve que cambiar a otra primero.
  
- ¿Qué comando o comnados utilzaste en el paso 29?

  git checkout 209203f.En este paso, usé git checkout 209203f para cambiar a un commit específico, esto me permite ver cómo estaba todo en ese momento de la historia del proyecto
  
- ¿Qué comando o comnados utilzaste en el paso 30?

  git checkout master // git branch -d htmlify // git branch -d styled // git branch -d title. Aquí, cambié a la rama master y traté de eliminar las ramas htmlify, styled y title. 

- ¿Qué comando o comnados utilzaste en el paso 32?

  git checkout 3a5c76d // git tag -a inicial -m "en el primer commit". Aquí, commit específico (3a5c76d) y etiqueto ese commit como inicial, añadiendo un mensaje descriptivo.
  
- ¿Qué comando o comnados utilzaste en el paso 33?

  git tag -a styled -m "modificacion del paso 10". En este paso, usé git tag -a styled -m "modificacion del paso 10" para crear otra etiqueta llamada styled, así puedo recordar qué cambios hice en el paso 10.




1.	git clone https://github.com/Pilar12071977/Pilar_Perez_GIT.git
2.	nano git-nuestro.md
3.	git add git-nuestro.md     /// git commit
4.	git push
5.	git branch styled
6.	git branch
7.	git checkout styled
8.	git branch
9.	nano git-nuestro.md   
10.	git add git-nuestro.md // git commit -m "Primer cambio dentro del fichero git-nuestro"   //    git push origin styled
11.	git reset --soft HEAD~1
12.	git merge master
13.	git checkout master // git branch
14.	git branch htmlify
15.	git checkout htmlify
16.	nano git-nuestro.md
17.	git add git-nuestro.md // git commit -m "Modificado el el fichero git-nuestro.md por tercera vez"
18.	git checkout styled // git merge htmlify
 
Auto-merging git-nuestro.md
CONFLICT (content): Merge conflict in git-nuestro.md
Automatic merge failed; fix conflicts and then commit the result.

19.	Hacemos un nano de git-nuestro.md y me quedo con el contenido con la rama de “styled” // git add git-nuestro.md // git commit -m "Resolvemos el conflicto y quedamos con contenido styled"
20.	git checkout master //   git merge styled
21.	git branch title // git checkout title
22.	nano git-nuestro.md // git add git-nuestro.md // git commit -m "Añadimos título al archivo git_nuestro"
23.	git checkout master
24.	git log –graph
25.	git merge --no-ff title
26.	git reset HEAD~1
27.	git checkout -- git-nuestro.md  (Con este commando dejó el resto de los archivos sin tocar, eliminando los cambios únicamente del archivo que necesito)
28.	git branch -d title // error: Cannot delete branch 'title' checked out at '/Users/jorgegonzalezsaenz/Desktop/Pilar_Perez_GIT' // git checkout master // git branch -d title // error: The branch 'title' is not fully merged.If you are sure you want to delete it, run 'git branch -D title'. // git branch -D title
29.	git checkout 209203f // git checkout -b title
30.	git checkout master // git branch -d  htmlify //  git branch -d  styled // git branch -d  title // error: The branch 'title' is not fully merged.If you are sure you want to delete it, run 'git branch -D title'. // git branch -D  title
31.	git checkout 3a5c76d
32.	git checkout 209203f
33.	git checkout 3a5c76d // git tag -a inicial -m "en el primer commit" //  git show inicial // git checkout a40d94f // git tag -a styled -m "modificacion del paso 10" // git show styled // git reflog// git checkout 6ac974a // git tag -a htmlify  -m "mofificacion del paso 17-18" // git checkout 209203f // git tag -a title  -m "modificacion del paso 30"
34.	git checkout htmlify
35.	git checkout master
36.	git push origin inicial // git push origin styled // git push origin htmlify // git push origin title. Para cada rama git log -g // git branch htmlify 6ac974a01687437b1f15ed434491f04a2643126a// git checkout htmlify//

**B**
## Gráfo 

git log –graph
|\  Merge: a40d94f 6ac974a
| | Author: Pilar Perez <pilarperez7@hotmail.com>
| | Date:   Sat Sep 14 22:27:18 2024 +0200
| |
| |     Resolvemos el conflicto y quedamos con contenido styled
| |
| * commit 6ac974a01687437b1f15ed434491f04a2643126a (htmlify)
| | Author: Pilar Perez <pilarperez7@hotmail.com>
| | Date:   Sat Sep 14 22:19:10 2024 +0200
| |
| |     Modificado el el fichero git-nuestro.md por tercera vez
| |
* | commit a40d94fd7b6c6b5c5666e09ead2af450117d6b2a (origin/styled, refs/original/HEAD)
|/  Author: Pilar Perez <pilarperez7@hotmail.com>
|   Date:   Fri Sep 13 20:38:33 2024 +0200
|
|       Primer cambio dentro del fichero git-nuestro
|
* commit 3a5c76dc4a50714d2b9a43b3473a8340091aa97f (origin/master)




