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
