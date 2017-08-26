* Agregar, modificar o eliminar tus archivos.

  > Nota: Una carpeta vacía no se puede comitear. Debe tener al menos un archivo

* Saber si hay cambios que aún no commiteaste: `git status`

  ```bash
  federico@DESKTOP-538S3NF:~/example$ git status
  On branch master
  Your branch is up-to-date with 'origin/master'.

  Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git checkout -- <file>..." to discard changes in working directory)

          modified:   README.md

  Untracked files:
    (use "git add <file>..." to include in what will be committed)

          foo.txt

  no changes added to commit (use "git add" and/or "git commit -a")
  ```

  > _Nota_: Prestá atención a las ayudas que da git cuando ejecutas un comando.

* Decirle qué cambios hechos hasta el momento sobre un archivo deberían ser commiteados: `git add «archivo»`

  ```bash
  federico@DESKTOP-538S3NF:~/example$ git add foo.txt
  federico@DESKTOP-538S3NF:~/example$ git status
  On branch master
  Your branch is up-to-date with 'origin/master'.

  Changes to be committed:
    (use "git reset HEAD <file>..." to unstage)

          new file:   foo.txt

  Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git checkout -- <file>..." to discard changes in working directory)

          modified:   README.md
  ```

* Realizar el commit de los archivos a los que previamente le hiciste _git add_, haces: `git commit -m "MENSAJE"`

  ```bash
  federico@DESKTOP-538S3NF:~/example$ git commit -m "Agregando el archivo foo.txt"
  [master 2fbe591] Agregando el archivo foo.txt
  1 file changed, 1 insertion(+)
  create mode 100644 foo.txt
  ```

* Ver el historial de commits hechos hasta ahora, para esto tenes el comando: `git log`

  ```bash
  federico@DESKTOP-538S3NF:~/example$ git log
  commit 2fbe59175f2c0b038a2cd38d8568240e528fa022
  Author: Federico Scarpa <fedescarpa@gmail.com>
  Date:   Tue Aug 22 00:20:11 2017 -0300

      Agregando el archivo foo.txt

  commit 11980301cdc31eb4589c24734170678b55e74f8f
  Author: Federico Scarpa <fedescarpa@users.noreply.github.com>
  Date:   Mon Aug 21 23:13:12 2017 -0300

      Initial commit
  ```

* Hasta ahora sólo hicimos cambios manipulando nuestro repositorio local pero, en algún momento tengo que llevar mis cambios al repositorio remoto para que mis compañeros puedan ver lo que hice. Para hacer eso, solo debemos correr el siguiente comando: `git push origin HEAD`

  ```bash
  federico@DESKTOP-538S3NF:~/example$ git push origin HEAD
  Username for 'https://github.com': fedescarpa
  Password for 'https://fedescarpa@github.com':
  Counting objects: 4, done.
  Delta compression using up to 8 threads.
  Compressing objects: 100% (2/2), done.
  Writing objects: 100% (3/3), 321 bytes | 0 bytes/s, done.
  Total 3 (delta 0), reused 0 (delta 0)
  To https://github.com/fedescarpa/example.git
    1198030..2fbe591  HEAD -> master
  ```

  > _Nota 1_: Hay formas de evitar poner el usuario y la contraseña cada vez que corramos el comando `push`. Esa forma queda fuera del alcance de este apunte. Pero el que quiera configurarlo puede leerlo desde [este link](https://help.github.com/articles/connecting-to-github-with-ssh/).
  >
  > _Nota 2_: Hay veces que este comando puede fallar, eso se debe a que algún compañero subió cambios antes que vos, por lo que antes de re-ejecutar este comando tenés que ejecutar el comando que sigue en el próximo item.

* ¿Y si quiero bajarme cambios que hayan hecho mis compañeros? Fácil, sólo tenes que correr el comando `git pull`

  ```bash
  federico@DESKTOP-538S3NF:~/example$ git pull
  remote: Counting objects: 3, done.
  remote: Compressing objects: 100% (3/3), done.
  remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  Unpacking objects: 100% (3/3), done.
  From https://github.com/fedescarpa/example
    2fbe591..cf91a5d  master     -> origin/master
  Updating 2fbe591..cf91a5d
  Fast-forward
  foo.txt | 2 +-
  1 file changed, 1 insertion(+), 1 deletion(-)
  ```

  > _Nota_: Al hacer `pull` puede ser que se generen conflictos. Ese tema tampoco será aboradado por este apunte.