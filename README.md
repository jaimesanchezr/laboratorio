## 29/03/2023 DÍA 1
# INICIALIZAR REPOSITORIO --
- `git init`: sirve para inicializar el repositorio

# AÑADIR ARCHIVOS --
- `git add <nombre_archivos>`: añadir los archivos al staging area

# COMMIT --
- `git commit -m "mensaje"`: sirve guardar los cambios realizados en los archivos y añadir un mensaje

# DIFF --
- `git diff <archivo>`: sirve para comparar los cambios entre dos archivos (la version actual y su ultima actualización)
	-hash: sirve para comprar el archivo actual con una verisón en especifico utilizando el tag hash.

# RAMAS --
- `git branch <nombre_rama>`: crea una nueva rama.

# STATUS --
- `git status`: verificar los archivos modificados, si están en el staging area.

# CHECKOUT --
- `git checkout <nombre_rama>`: sirve para viajar entre ramas.
- `git checkout <id_commit>`: viajar a un commit en especifico utilizando su ID.
- `git checkout -b`: crear un branch desde el punto en donde estoy parado

# MERGE
- `git merge <nombre_rama>`: unir dos ramas (la rama actual y la rama que se especifica en el comando).

# REVER Y RESET --
- `git revert <id_commit>`: viajar a un punto de la misma rama anterior y los archivos de los commits posteriores a ese punto regresan al staging area.
- `git reset`: viajar a un punto de la misma rama anterior, con dos variantes:
	--hard: elimina todos los commits posteriores a ese punto de la rama (no recuerda que existen esos commits)
	--soft: el sistema asume que no existen los commits posteriores a ese punto, sin embargo (sabe que existieron esos commits)

# REPOSITORIOS REMOTOS --
Un repositorio remoto es aquel alojado en un servidor remoto.
Comando para su uso:
- `git remote add <nombre_del_repo> <URL_repositorio>`

# PETICION DE CAMBIOS --
La petición de cambios o Pull Request consiste en solicitarle a un colaborador/compañero que revise y apruebe los cambios que has hecho en el código.

# MERGE ENTRE RAMAS Y RESOLUCIÓN DE PROBLEMAS --
El merge entre ramas puede darse de dos tipos: manual o automática.
- Automática si: Git determina que no hay ningún entre ramas, por lo tanto, el merge se hará de forma automática.
- Manual si: Git determina que hay conflictos entre las ramas a "mergear", indicandole al usuario que debe resolver el conflicto de forma manual.

# GESTIÓN DE RAMAS --
Gestion de todas las ramas derivadas de la rama principal (main/master)

# FORKS en control de versiones -- 
Permite clonar el repositorio sin dañar el original; permite a los desarrolladores a contribuir.

## 30/02/2023 - DÍA 2
# TAGS
Son identificadores que se le asocian a una versión especifica de un repo. Se utilizan para taggear versiones importantes.
- `git tag v1.0`
- `git tag -s v1.0`
- `git push -tags`
- git show v1.0: es un git log de un tag.

# GIT FETCH, PULL AND PUSH 
- `git fetch`: descarga los cambios de un repo. remoto a tu repo. local.
- `git pull`: git pull es un alias de fetch y merge. El es una combinación entre fetch y merge; sincroniza la rama actual del repo. local con la del remoto.
- `git push`: envia los cambios en la rama actual del repo. local al repo. remoto.
NEVER use: git push --force (-f)

# FLUJOS DE TRABAJO DE AVANZADOS
Como se gestiona el ciclo de vida de la aplicación.
- Archivo .gitignore: archivo donde se indican que archivos de texto o binario no quiero que estén en mi repositorio; puede contener rutas, dependencias...
- Archivo .README.md: archivo donde se va a detallar toda la documentación necesaria de la aplicación.
- Archivo changelog.md: archivo que documenta los tags

# CONVENCIONES PARA COMENTAR COMMIT
- La oración sea imperativa: debe ser clara y concisa.
- La longitud del mensaje: directo al grano y de forma funcional.
- Detalles adicionales: historias de usuario
- Incluir número de tarea 
- Usar verbos precesos 

# CONVENCIONES PARA NOMBRAR BRANCHS
- Nombres cortos y descriptivos: feature/id_historia
- Nombre en minúsculas y separadados por "/" o "-"
- Utilizar prefijos para el tipo de branch: 
- No usar nombres genéricos: dev, feature1, nuevo...

# DOCUMENTACIÓN DE UNA SOLICITUD DE CAMBIO (PULL REQUEST)
- Título: nombres cortos y descriptivos
- Descripción: detallada de lo que espera que se resuelva y los motivos del cambio. 
- Capturas de pantalla: hacer capturas para ilustrar.
- Problemas relacionados: dar un "enlace" al prolema.
- Etiquetas: etiquetar la solicitud de cambio.

# CODE REVIEW
- Verificación y validación del código para reducir errores.

# GIT EN MULTIPLES ENTORNOS DE TRABAJO
- `git clean`:  eliminar archivos no rastreados en un directorio local. en git, un archivo no rastreado es que no ha sido añadido por primera vez.
- `git rebase`: integra cambios de una rama a otra de forma mas ordenada (es como un merge).

# GIT stash
- `git stash`: guarda temporalmente los cambios en un estado intermedio para trabajar en otra cosa sin tener que hacer commit de los cambios actuales.
- Se puede seguir trabajando desde el estado guardado.

# Comandos de emergencia
- `git reset`:  permite mover la rama y head del repo a un commit anterior.
- `git reflog`: muestra historial detallado del head del repositorio. 

# Commit Ammend
- `git commit --amend`: es utilizado para modificar el commit anterior (que no se ha sincronizado con el repositorio )si se nos olvida un archivo o el mensaje de confirmación e inclusive para fusionar confirmaciones.

# Uso avanzado del checkout
- `git checkout -- <file>`: con su uso podemos volver a la ultima versión de un archivo y descartar los cambios.
- `git checkout <branch> - <file>`: restaura el archivo de una rama especifica a nuestra rama actual.

# GIT Blame
- `git blame`: es un comando utilizado en forma de autoría, ya que muestra quién y cuándo se realizaron cambios en un archivo.

# GIT GREP y LOG
- `git grep`: buscar cadenas de texto dentro de un archivo; buscar de las salidas de los logs. 
- `git log`: comando que se utiliza para mostrar las confirmaciones en un repositorio.

# Repositorio dentro de otros repositorios
- Submódulos: es una forma de poder versionar o permitirle a un proyecto saber que checkout de los submódulos para el punto de la historia en que estás trabajando.
- permiten incluir un repositorio de Git dentro de otro repositorio, como una subcarpeta.
- Es una opción de mantener y utlizar proyectos relacionados o dependientes.


