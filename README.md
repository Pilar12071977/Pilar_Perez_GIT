#PRÁCTICA DE GIT 

A -  Los ejerccios resueltos
B -  El diagrama pedido en el apartado de 25

**A**

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




