git init: sirve para inicializar el repositorio
git add <nombre_archivos>: añadir los archivos al staging area
git commit -m "mensaje": sirve guardar los cambios realizados en los archivos y añadir un mensaje
git diff <archivo>: sirve para comparar los cambios entre dos archivos (la version actual y su ultima actualización)
git diff  <hash> <archivo>: sirve para comprar el archivo actual con una verisón en especifico utilizando el tag hash.
git branch <nombre_rama>: crea una nueva rama.
git status: verificar los archivos modificados, si están en el staging area.
git checkout <nombre_rama>: sirve para viajar entre ramas.
git checkout <id_commit>: viajar a un commit en especifico utilizando su ID.
git merge <nombre_rama>: unir dos ramas (la rama actual y la rama que se especifica en el comando).
git revert <id_commit>: viajar a un punto de la misma rama anterior y los archivos de los commits posteriores a ese punto regresan al staging area.
git reset: viajar a un punto de la misma rama anterior, con dos variantes:
	--hard: elimina todos los commits posteriores a ese punto de la rama (no recuerda que existen esos commits)
	--soft: el sistema asume que no existen los commits posteriores a ese punto, sin embargo (sabe que existieron esos commits)

-- REPOSITORIOS REMOTOS --
Un repositorio remoto es aquel alojado en un servidor remoto.
Comando para su uso: git remote add <nombre_del_repo> <URL_repositorio>

-- PETICION DE CAMBIOS --
La petición de cambios o Pull Request consiste en solicitarle a un colaborador/compañero que revise y apruebe los cambios que has hecho en el código.


