
1. Ya tenes instalado Git y, la primera vez que lo usas, vas a tener que configurar tu nombre completo y tu email con los siguientes comandos:

  ```bash
  git config --global user.name  "TU NOMBRE"
  git config --global user.email "TU DIRECCION DE EMAIL"
  ```

1. Si vas a trabajar en grupo necesitás un repositorio remoto al cual todos los integrantes tengan acceso. Hay varios servicios para esto, tres de los más conocidos son:

    * [Github](https://github.com) - Personalmente el que más me gusta
      * Cómo crear un [repositorio](https://help.github.com/articles/create-a-repo).
      * Si sos alumno de una entidad educativa, podes pedir [repositorios privados](https://education.github.com).
    * [Bitbucket](https://bitbucket.com)
      * Repositorios privados con límite de 5 usuarios.
    * [Gitlab](https://gitlab.com/)
      * Repositorios privados sin restricciones.

1. Una vez creada la cuenta y un repositorio en alguno de estos servicios, tenés que bajarte la información del repositorio remoto a tu computadora. Para eso vamos a utilizar el comando `git clone «url_repositorio_remoto»`

  ```bash
  federico@DESKTOP-538S3NF:~$ git clone https://github.com/fedescarpa/example.git
  Cloning into 'example'...
  remote: Counting objects: 3, done.
  remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  Unpacking objects: 100% (3/3), done.
  Checking connectivity... done.
  https://github.com/fedescarpa/example.git
  ```
  > _Nota_: Una vez realizado esto, habrá una carpeta con el mismo nombre que el repositorio remoto, allí se encontrará nuestro repositorio local y es donde podrás crear/modificar/eliminar archivos para versionarlos.
.name  "TU NOMBRE"
  git config --global user.email "TU DIRECCION DE EMAIL"
  ```

1. Ya tenes instalado Git y, la primera vez que lo usas, vas a tener que configurar tu nombre completo y tu email con los siguientes comandos:

  ```bash
  git config --global user.name  "TU NOMBRE"
  git config --global user.email "TU DIRECCION DE EMAIL"
  ```

1. Si vas a trabajar en grupo necesitás un repositorio remoto al cual todos los integrantes tengan acceso. Hay varios servicios para esto, tres de los más conocidos son:

    * [Github](https://github.com) - Personalmente el que más me gusta
      * Cómo crear un [repositorio](https://help.github.com/articles/create-a-repo).
      * Si sos alumno de una entidad educativa, podes pedir [repositorios privados](https://education.github.com).
    * [Bitbucket](https://bitbucket.com)
      * Repositorios privados con límite de 5 usuarios.
    * [Gitlab](https://gitlab.com/)
      * Repositorios privados sin restricciones.

1. Una vez creada la cuenta y un repositorio en alguno de estos servicios, tenés que bajarte la información del repositorio remoto a tu computadora. Para eso vamos a utilizar el comando `git clone «url_repositorio_remoto»`

  ```bash
  federico@DESKTOP-538S3NF:~$ git clone https://github.com/fedescarpa/example.git
  Cloning into 'example'...
  remote: Counting objects: 3, done.
  remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  Unpacking objects: 100% (3/3), done.
  Checking connectivity... done.
  https://github.com/fedescarpa/example.git
  ```
  > _Nota_: Una vez realizado esto, habrá una carpeta con el mismo nombre que el repositorio remoto, allí se encontrará nuestro repositorio local y es donde podrás crear/modificar/eliminar archivos para versionarlos.
