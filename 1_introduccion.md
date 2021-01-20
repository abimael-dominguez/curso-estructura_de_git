# 1. Introducción
----
## Comandos de porcelana
Para realizar tareas de alto nievel utilizamos comandos de usuario amigables tales como:

- git status
- git commit
- git log
- git add
- git init
- git checkout
- git branch

## Comandos de fontanería

Para realizar tareas de bajo nievel utilizamos comandos de "plomero" tales como:

- git hash-object
- git cat-file 
- git show-ref

## Carpeta .git 
Cuando se ejecuta el comando `git init` se crea una carpeta oculta llamada .git. Esta carpeta es utilizada por Git para almacenar y gestionar el contenido del usuario.

Contenido inicial de la carpeta .git:

```bash

>> tree .git/
.git/
├── branches
├── config
├── description
├── HEAD
├── hooks
│   ├── applypatch-msg.sample
│   ├── commit-msg.sample
│   ├── fsmonitor-watchman.sample
│   ├── post-update.sample
│   ├── pre-applypatch.sample
│   ├── pre-commit.sample
│   ├── prepare-commit-msg.sample
│   ├── pre-push.sample
│   ├── pre-rebase.sample
│   ├── pre-receive.sample
│   └── update.sample
├── info
│   └── exclude
├── objects
│   ├── info
│   └── pack
└── refs
    ├── heads
    └── tags


```

En este curso nos enfocaremos  principalmente en las siguientes partes:

- **Archivos**
	- _HEAD_
		- Apunta a la rama activa (checked out)
	- _index_ (se crea hasta ejecutar un `git add` )
		- Almacena información del área de preparación (staging area)

- **Carpetas**
	- _objects_
		- Guarda contenido.
	- _refs_
		- Guarda apuntadores hacia las ramas (branches)
		
		
# Ejercicios
---
#

- Crear una carpeta nueva llamada "repositorio_de_aprendizaje"

```bash
>> mkdir repositorio_de_aprendizaje
>> cd repositorio_de_aprendizaje
```
- Inicializar el repositorio

```bash
git init
```
- Ubicar cada una de las carpetas y archivos que utilizaremos en este curso (anotar la dirección en donde se localiza cada uno)

	- _HEAD_:
	- _index_ (por ahora no aparece, pero estar atento para saber donde se ubicará en los capítulos siguientes):
	- _objects_:
	- _refs_: 

Otros comandos que te pueden ser de utilidad:

```bash
# Si cometiste un error puedes borrar el repositorio con el siguiente comando y volver a comenzar
>> rm .git -rf

# si quieres visualizar qué carpetas ocultas tienes 
>> ls --all

# Te sirve para visualizar desde la terminal el contenido de un archivo
>> cat <nombre-del-archivo>

# El programa "tree" te puede ayudar a visualizar y navergar entre las carpetas; prueba con estos:
>> tree .git
>> tree .git/objects

# También puedes listar los directorios con "ls"
>> ls .git -F1

# Para listar el árbol de directorios de forma recursiva ejecuta:
>> ls -R .git
```

------
