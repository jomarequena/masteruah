<<<<<<< HEAD
#masteruah

##Master IoT

"En Este documento vamos a ir poniendo los comandos que hemos tenido que utilizar durante los ejercicios y las explicaciones y capturas de pastalla que consideremos necesarias"

##Clonamos nuestro repositorio remoto en el local

git clone https://github.com/jomarequena/masteruah.git

##Nos cambiamos al directorio de trabajo y levantamos nuestro git

cd masteruah.git

git init

##Una vez en el vemos que tenemos un fichero README.md, que es este fichero. Lo vamos a editar. Y hacemos el primer commit.

vi README.md

git commit -m "commit inicial"

##Al ejecutar el commit vemos que nuestro branch confirmado es origin/master y en el esta el HEAD
##Vemos los remote repository asociados hasta ahora y su nombre.

git remote -v

##Subimos los cambios al repositorio remote, en nuestro caso origin.
###master es nuestro branch a subir y como se almacenará en el origin.

git push origin master

##Creamos en el repositorio local los ficheros privado.txt y la carpeta privada. Y las ignoramos.

vi privado.txt

mkdir privada

##Tendremos que editar el .gitignore
###Vemos con el git status los ficheros que estan en untacked

git status

vi .gitignore -> privado.txt
		 
		 privada/*

git status

##Creamos el fichero 1.txt y lo añadimos a nuestro repositorio local.

touch 1.txt

git add 1.txt

##Creamos un tag a nuestro commit y vemos los tags.

git tag v0.1

git tag

##Subimos los cambios al remote.

git push origin v0.1

##Aqui tendremos lo del ultimo commit. Pero tenemos que subir todos los cambios que hemos creado hasta ahora. Para ello, creo un nuevo commit y tag v0.2 y lo publico.

git commit -a "Subir tag v0.2 con cambios"

git tag v0.2

##Si edito el README.md desde el remote y el local, tendré un conflicto, tendré que solucionarlo. 

git pull 

##Me sacará todos los errores y los tengo que solucionar a mano.

git add README.md

git commit -m "Subir tag v0.5 sin tag en push"

git push origin master
