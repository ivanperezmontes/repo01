# Creación de repositorio en Git

1. Creación de carpeta e iniciar Git
   
   - `mkdir`para crear una carpeta  
   - `git init` para iniciar git i crear un repositorio

        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/iniciar_repo01.PNG "Iniciar repo01")

 - Vemos que hemos iniciado el repositorio con éxito al hacer `git status`

2. Staging area
   
   - Con `git add .`añadimos el readme.md y la imagen en el *staging area*
  

      ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/staging_area.PNG "readme.md a staging area")

 
    - Hago `git commit -m "Añado el readme.md y las imagenes"` para hacer el snapshot y vemos que tenemos un fichero untracked por la captura que acabo de hacer y no he añadido a *staging area* 
    
       ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/commit.PNG "Commit")

    - Añado las imagenes que faltan al *staging area* 
    - ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/añadir_staging.PNG "Añadir lo que queda a Staging area")

3. Push 
   
     - Hacemos push pero como no hemos indicado el repositorio remoto al que hay que subir los cambios, vamos a crear uno en git-hub para enlazarlo
    
        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/push_fallido.PNG "Push fallido")

    - En git-hub añadimos un nuevo repositorio y lo llamamos como lo tenemos en local para respetar la coherencia 
     
        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/new_repo.PNG "New repo")

        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/crear_repo.PNG "New repo")

    - Añadimos la dirección del origen: `git remote add origin https://github.com/ivanperezmontes/repo01.git`  
    -  Cambiamos el nombre de la rama ***master*** a ***main***: `git branch -M main` 
    - Hacemos push: `git push -u origin main`

         ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/añadimos_origen.PNG "Añadimos origen")
        ![Este contenido se mostrará cuando la imagen no se pueda cargar, como texto alternativo](./img/push_correcto.PNG "Añadimos origen")
