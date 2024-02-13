# 00-git :
Éste es el repositorio del Laboratorio de Git (en el Bootcamp JS de Lemoncode).

### En este archivo, describo los pasos que he seguido para realizar este primer laboratorio. 

1. Crear un repositorio en local:
    - Desde mi terminal en MacOS, me sitúo en el escritorio mediante el comando: *cd desktop*
    - A continuación creo la carpeta (a la que llamaré “Bootcamp JS”), utilizando: *md “Bootcamp JS”*
    - Ingreso a dicha carpeta con: *cd “Bootcamp JS”*
    - Doy inicio al repositorio de Git con el comando: *git init*
        - Como me ha creado la rama principal con el nombre de “master”, y yo prefiero denominarla “main”, le cambio el nombre usando: *git branch -m main*
        - Sin embargo, luego he recordado que puedo configurar Git de manera que siempre me nombre como “main” la rama principal de mis proyectos, por defecto. Así que lo configuro ahora, con el comando: *git config --global init.defaultBranch main*
    
    ![Captura Laboratorio Git 01](./content/Captura%20Laboratorio%20Git%2001.png)

    
2. Subir el repositorio a GitHub:
    - A continuación, me voy a mi perfil de **GitHub y desde allí creo un nuevo repositorio**. Lo he nombrado como “00-git”. Para ello, fui a la pestaña “Repositories”, cliqué en “New”, y rellené los datos tal y como muestro en la captura:

    ![Captura Laboratorio Git 02](./content/Captura%20Laboratorio%20Git%2002.png)
    
    - Ahora, copio la URL que me va a conectar mi repositorio de GitHub en la nube, con el repositorio que creé previamente en mi ordenador. Escojo la opción de hacerlo mediante el protocolo de SSH (ya que anteriormente creé una contraseña SSH y la conecté con GitHub). Aquí dejo algunas capturas de ese proceso (no de todos los pasos para no extenderme mucho):

    ![Captura proceso SSH 1](./content/Captura%20SSH%2001.png)

    ![Captura proceso SSH 5](./content/Captura%20SSH%2005.png)

    - Ésta es la URL SSH para conectar ambos repositorios: git@github.com:Laezne/00-git.git

    ![Captura Laboratorio Git 03](./content/Captura%20Laboratorio%20Git%2003.png)

    - Ahora conecto ambos repositorios. Para ello, vuelvo a mi terminal, y desde el repositorio local, lanzo el comando:
    *git clone git@github.com:Laezne/00-git.git*

    ![Captura Laboratorio Git 04](./content/Captura%20Laboratorio%20Git%2004.png)

    - Desde terminal, abro mi proyecto en Visual Studio Code, mediante el comando *code .*
    
    - Aquí puedo ver que está todo correcto y que, efectivamente, ya tengo en mi repo local la carpeta y el archivo .md del repositorio de GitHub.
    
    ![Captura Laboratorio Git 05](./content/Captura%20Laboratorio%20Git%2005.png)


3. Hacer un ***commit*** y un ***push***:
    - Desde Visual Studio Code, con la terminal, creo una nueva carpeta llamada “content” (donde añado las capturas de este ejercicio para luego añadirlas al readme.md). También creo el archivo .gitignore
    - Luego, reviso todos estos cambios con: *git status*
    - Y añado todo al área de staging con: *git add .*
    - Posteriormente, realizo un commit con: *git commit -am “Añado archivos”*
    - Y por último, subo los cambios a GitHub lanzando: *git push -u origin main*

     ![Captura Laboratorio Git 06](./content/Captura%20Laboratorio%20Git%2006.png)
    

4. Crear una rama:
    -  Creo una nueva rama llamada “development”, utilizando: *git branch development*
    - Me cambio para situarme en la nueva rama con: *git switch development* (aunque también podría usar git checkout).
    - Realizo cambios en la carpeta “content” y en el “readme.md”.
    - Para añadir y commitear, lanzo: *git add .* y *git commit -am “Primer commit en development”*
    - Inicialmente y por confusión, intento subir los cambios con *git push*
    - Pero como esta nueva rama aún no estaba creada en GitHub, me da error y entonces utilizo: *git push --set-upstream origin development*

     ![Captura Laboratorio Git 07](./content/Captura%20Laboratorio%20Git%2007.png)


5. Hacer un ***merge***:
- Regreso a la rama main escribiendo: *git switch main*
- Con un *git tree* (alias que configuré previamente), reviso el estado de todo.
- Ahora, hago un merge con: *git merge development*
- No ha avisado de ningún conflicto, así que procedo a lanzar: *git push*

![Captura Laboratorio Git 08](./content/Captura%20Laboratorio%20Git%2008.png)


## Por último, termino de editar el README, y commiteo y subo los cambios a GitHub. 

# ¡Gracias por leerme! 😊

---