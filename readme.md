Tabla de contenido
- [Creación de repositorio en Git](#creación-de-repositorio-en-git)
  - [1. Creación de carpeta e iniciar Git en local](#1-creación-de-carpeta-e-iniciar-git-en-local)
  - [2. Staging area](#2-staging-area)
  - [3. Push](#3-push)
  - [4. Repositorio remoto](#4-repositorio-remoto)
  - [5. Iniciar repositorio desde GitHuB](#5-iniciar-repositorio-desde-github)

# Creación de repositorio en Git

## 1. Creación de carpeta e iniciar Git en local
   
   - `mkdir`para crear una carpeta  
   - `git init` para iniciar git i crear un repositorio
   - Vemos que hemos iniciado el repositorio con éxito al hacer `git status`

        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/iniciar_repo01.PNG "Iniciar repo01")

 

## 2. Staging area
   
   - Con `git add .`añadimos el readme.md y la imagen en el *staging area*
  

      ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/staging_area.PNG "readme.md a staging area")

 
- Hago `git commit -m "Añado el readme.md y las imagenes"` para hacer el snapshot y vemos que tenemos un fichero untracked por la captura que acabo de hacer y no he añadido a *staging area* 
    
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/commit.PNG "Commit")

- Añado las imagenes que faltan al *staging area* 
- ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/añadir_staging.PNG "Añadir lo que queda a Staging area")

## 3. Push 
   
- Hacemos push pero como no hemos indicado el repositorio remoto al que hay que subir los cambios, vamos a crear uno en GitHub para enlazarlo
    
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/push_fallido.PNG "Push fallido")

- En GitHub añadimos un nuevo repositorio y lo llamamos como lo tenemos en local para respetar la coherencia 
     
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/new_repo.PNG "New repo")

    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/crear_repo.PNG "New repo")

- Añadimos la dirección del origen: `git remote add origin https://github.com/ivanperezmontes/repo01.git`  
-  Cambiamos el nombre de la rama ***master*** a ***main***: `git branch -M main` 
- Hacemos push: `git push -u origin main`

    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/añadimos_origen.PNG "Añadimos origen")
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/push_correcto.PNG "Añadimos origen")

## 4. Repositorio remoto
-  Veo que en GitHub se han subido el fichero readme.md y las imagenes
  
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/resultado_push.PNG "github")
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/resultado_push2.PNG "github")
- Hay un problema, no se han subido el fichero readme.md que estaba editando
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/resultado_push3.PNG "github")
- Guardo el ***readme.md***, lo añado al staging area, commit y push
  
     ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/resultado_push4.PNG "github")

- Finalmente vemos el readme en GitHub
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/readmemd.PNG "github")

## 5. Iniciar repositorio desde GitHuB
   - Creo el repositorio desde GitHub
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/crear_repo_github.PNG "github")
    ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/crear_repo_github2.PNG "github")
    
      - He usado regex para cambiar la forma en la que estaba escribiendo "git-hub" a GitHub
        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/git.PNG "github")
- Clono el repositorio repo02
        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/clone_repo2.PNG "github")
- Creo readme.md en repo02
        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/readme_repo2.PNG "github")
- Añado al staging area, `git add .`. Hago el commit, `git commit -m "Añado el readme.md"`. Hago push, `git push`
        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/push_repo2.PNG "github")