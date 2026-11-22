# Mi Proyecto

Proyecto individual de DevOps para practicar Git y GitHub: crear un repositorio, versionar cambios, subirlos a GitHub y deshacer errores.

## Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/jgarces-lang/mi-proyectoDev-git.git
   ```
2. Entrar a la carpeta:
   ```bash
   cd mi-proyectoDev-git
   ```

## Comandos usados y qué hace cada uno

| Comando | Qué hace |
| --- | --- |
| `git init` | Convierte una carpeta normal en un repositorio de Git. Crea la carpeta oculta `.git`, que guarda todo el historial. |
| `git status` | Muestra en qué estado están los archivos: si son nuevos (untracked), si están modificados o si ya están listos para el commit. |
| `git add` | Pasa los cambios al área de staging, que es como una "sala de espera" con lo que va a entrar en el próximo commit. |
| `git commit -m "mensaje"` | Toma una foto de los cambios que están en staging y la guarda en el historial con un mensaje que explica qué se hizo. |
| `git remote add origin URL` | Conecta el repositorio local con el repositorio de GitHub y le pone el nombre `origin`. |
| `git push` | Sube los commits locales a GitHub. La primera vez se usa `git push -u origin main` para dejar enlazada la rama. |
| `git diff` | Muestra línea por línea qué cambió respecto al último commit. En verde lo agregado y en rojo lo borrado. |
| `git log` | Muestra el historial de commits con su autor, fecha y mensaje. Con `--oneline --graph` se ve resumido y en forma de árbol. |
| `git restore archivo` | Descarta los cambios que aún no tienen commit y deja el archivo como estaba en el último commit. |
| `git restore --staged archivo` | Saca el archivo del staging sin perder los cambios: el archivo sigue modificado, pero ya no entra en el próximo commit. |
| `git reset --soft HEAD~1` | Deshace el último commit, pero conserva los cambios para corregirlos o volver a hacer el commit. |
| `git checkout <hash> -- archivo` | Devuelve un archivo exactamente a como estaba en un commit anterior, usando el código (hash) de ese commit. |