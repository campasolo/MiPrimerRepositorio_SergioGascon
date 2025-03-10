# Práctica para Entornos de Desarrollo RA4
# Proyecto MiPrimerRepositorio_SergioGascon

Este repositorio va a contener los documentos relacionados con la práctica RA4 de la asignatura Entornos de Desarrollo con la documentación de lo realizado en dicha práctica.

## Comandos utilizados

### Parte 1: Introducción y configuración inicial

git config --global user.name "campasolo"
git config --global user.email "campasolo.developments+github@gmail.com"
Los comandos anteriores configuran GIT en modo global con el nombre de usuario y correo electrónico.

git config --list
El comando anterior muestra en la consola la configuración introducida.

### Parte 2: Trabajando con un repositorio local 


Creo el directorio del proyecto
Me posiciono en el siguiente directorio:
/c/Proyectos/DAM/Entornos_de_Desarrollo/RA4/MiPrimerRepositorio_SergioGascon

Y creo el directorio para el repositorio:
mkdir MiPrimerRepositorio_SergioGascon

Me posiciono en el anterior directorio.

git init
El comando anterior inicializa el repositorio local

Creo el archivo README.md con los textos indicados.

git add REAME.md
El comando anterior añade el archivo en el área de staging

git commit -m "Primer commit: Creación del README"
El comando anterior ejecuta un commit de lo que esté en staging, en este caso el fichero README.md

### Parte 3: Subir un repositorio a GitHub

Creo el repositorio en la web de GitHub.

git remote add origin https://github.com/campasolo/MiPrimerRepositorio_SergioGascon.git
El anterior comando, vincula el repositorio remoto al local.

git push origin master
El anterior comando sirve para subir los cambios locales al repositorio remoto.


He ejecutado el comando git branch -m main y a continuación git push --set-upstream origin main, para ir haciendo el resto de la práctica desde la rama main. Al actualizar la web del repositorio ya se ve el cambio y aparece la rama main.

### Parte 4: Trabajando con ramas

git branch dev
Con el comando anterior creo la rama dev

git checkout dev
Con el comando anterior me cambio a la rama dev

Creo el archivo script.js con el comando touch script.js y lo edito en VS Code

git add .
Agrego a la rama dev los ficheros nuevos

git commit -m “Subiendo los cambios a la rama dev”
Con el comando anterior ejecuto un commit de los cambios

git push –set-upstream origin dev
Con el comando anterior subo al repositorio remoto

Si actualizo la web de Github, se indica que se ha creado una nueva rama, me posiciono sobre la rama dev y puedo ver los nuevos archivos.

git checkout main
Con el comando anterior nos posicionamos en la rama dev

### Parte 5: Descargar cambios 

En la web de GitHub, edito el fichero README.md y agrego la siguiente línea:
"Este es un cambio hecho desde GitHub por Sergio Gascón, desde el editor de archivos de GitHub."

Pulso el botón de "commit changes" y se muestra un diálogo para escribir un mensaje para el commit. Vuelvo a pulsar "commit changes" y todo queda almacenado en la rama.

git pull
Con el comando anterior traigo los cambios al repositorio local.
Voy al editor VS COde y verifico los cambios en el archivo correspondiente.

### Parte 6: Resolución de comflictos

git branch main
Con el comando anterior nos posicionamos en la rama main

Editamos el archivo script.js cambiando el texto de salida del console.log al siguiente texto:
console.log("Hola desde la rama main");

git commit -m "Modificación rama main"
Con el comando anterior ejecutamos un commit en la rama actual, main

git push –set-upstream origin main
Con el comando anterior subo al repositorio remoto

git branch dev
Con el comando anterior nos posicionamos en la rama dev

Editamos el archivo script.js cambiando el texto de salida del console.log al siguiente texto:
console.log("Hola desde la rama dev");

git commit -m "Modificación rama dev"
Con el comando anterior ejecutamos un commit en la rama actual, main

git push –set-upstream origin dev
Con el comando anterior subo al repositorio remoto

git checkout main
Con el comando anterior nos posicionamos en la rama main

git merge dev
Con el comando anterior realizamos la fusión de las ramas. GIT nos informa de que hay un conflicto que resolver. Y nos indica que lo resolvamos con la yuda de un editor.

Abrimos VS Code y nos indica ala bris scrip.js que podemos resolver el conflicto con su herramienta, que abre a tres bandas, el contenido de dev, el de main y debajo el contenido final del archivo.

Escribimos en la sección final cómo queremos resolver y guardamos.

git add .
Con el comando anterior, agregamos los cambios a la rama main

git commit -m "Conflicto resuelto en el merge"
Con el comando anterior guardamos el cambio en la rama.

git push
Con el comando anterior subimos los cambios a remoto.

