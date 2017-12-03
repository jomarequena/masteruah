# Master IoT 
## Primera Practica
"En Este documento vamos a ir poniendo los comandos que hemos tenido que utilizar durante los ejercicios y las explicaciones y capturas de pastalla que consideremos necesarias"

### Clonacion repositorio remoto
Clonamos nuestro repositorio remoto en el local
```
git clone https://github.com/jomarequena/masteruah.git
```

### Levantamos el Git
Nos cambiamos al directorio de trabajo y levantamos nuestro git
```
cd masteruah.git
git init
```

### Confirmamos, primer commit
Una vez en el vemos que tenemos un fichero README.md, que es este fichero. Lo vamos a editar. Y hacemos el primer commit.
```
vi README.md
git commit -m "commit inicial"
```

### Ver los repositorios remotes.
Al ejecutar el commit vemos que nuestro branch confirmado es origin/master y en el esta el HEAD. Vemos los remote repository asociados hasta ahora y su nombre.
```
git remote -v
```

### Lo publicamos a nuestro repositorio remoto.
Subimos los cambios al repositorio remote, en nuestro caso origin. Master es nuestro branch a subir y como se almacenará en el origin.
```
git push origin master
```

### Cambios sobre nuestro entorno de trabajo.
Creamos en el repositorio local los ficheros privado.txt y la carpeta privada. Y las ignoramos.
```
vi privado.txt
mkdir privada
```
### Fichero de exclusion.
Tendremos que editar el .gitignore. Vemos con el git status los ficheros que estan en untacked
```
git status
vi .gitignore -> privado.txt
		 privada/*
git status
```
### Añadir nuevos ficheros y los añadimos.
Creamos el fichero 1.txt y lo añadimos a nuestro repositorio local.
```
touch 1.txt
git add 1.txt
git commit -a "Añadimos nuevos Cambios"
```
### Creacion de Tags
Creamos un tag a nuestro commit y vemos los tags.
```
git tag v0.1
git tag
```
### Publicación de TAGs
Subimos los cambios al remote.
```
git push origin v0.1
```
### Creacion de Tablas
| NOMBRE | GITHUB |
| ------ | ------ |
| Lourdes | [Enlace](https://github.com/LourdesRD) |
| Evamuhe | [Enlace](https://github.com/Evamuhe) |
| Juan Pablo | [Elnace](https://github.com/jpinto7) |

## Ejercicios Avanzados
### Creacion de RAMAS y posicionamiento en el
```
git branch v0.2
git checkout v0.2
```

### Añadir un nuevo fichero.
```
touch 2.txt
git add 2.txt
```
### Subir cambios al remoto, creando una rama remota.
```
git commit -a "Cambios sobre la rama v0.2"
git push origin v0.2
```

### Merge directo
Nos cambiamos a la rama MASTER y hacemos un merge de la rama v0.2
```
git checkout master
git merge v0.2
```

### Merge con Conflito
1. En MASTER, editamos 1.txt y ponemos Hola, hacemos un commit.
```
vi 1.txt
git add 1.txt
git commit -m "Merge Conflicto"
```

2. Nos cambiamos a la rama v0.2 y ponemos Adios en el fichero 1.txt, hacemos commit.
```
git checkout v0.2
vi 1.txt
git add 1.txt
git commit -m "Merge Conflicto v0.2"
```

3. Cambiamos a MASTER y hacemos MERGE.
```
git checkout master
git merge v0.2
```

### Ver lista de ramas
```
git branch --merged
git branch --no-mergeg
```

### Finalmente arreglamos el conflicto a mano y hacemos un commit
```
git commit -m "FINAL"
git push origin master
```
