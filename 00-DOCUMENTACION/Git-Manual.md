Git Manual - Capítulo 1

Guárdalo porque será tu referencia para cualquier proyecto futuro.

1. Configurar Git (solo una vez por computadora)
git config --global user.name "David Vara"

git config --global user.email "davidvara.dev@gmail.com"

Verificar:

git config --global --list
2. Crear un repositorio nuevo

Ir a la carpeta del proyecto.

git init
3. Ver el estado del proyecto
git status

Este comando lo usarás prácticamente todos los días.

4. Agregar archivos al Staging Area

Agregar un archivo:

git add Diario.md

Agregar todos los archivos:

git add .

Importante: git add . agrega todos los cambios de la carpeta actual. Más adelante aprenderemos cuándo conviene usarlo y cuándo no.

5. Crear un commit
git commit -m "docs: iniciar Proyecto 3000"

Ejemplos:

git commit -m "feat: agregar formulario"

git commit -m "fix: corregir error de login"

git commit -m "docs: actualizar README"
6. Ver historial
git log

Versión resumida:

git log --oneline

Esta última será muy útil cuando el historial crezca.

7. Cambiar la rama principal a main

Antes se usaba master.

Ahora el estándar es:

main

Comando:

git branch -M main

Verificar:

git branch

Resultado esperado:

* main
8. Configurar SSH (solo una vez por computadora)

Crear clave SSH:

ssh-keygen -t ed25519 -C "davidvara.dev@gmail.com"

Mostrar la clave pública:

cat ~/.ssh/id_ed25519.pub

Comprobar la conexión:

ssh -T git@github.com

Resultado esperado:

Hi davidvara-dev!
You've successfully authenticated...
9. Conectar un proyecto con GitHub

Agregar el repositorio remoto:

git remote add origin git@github.com:davidvara-dev/Proyecto-3000.git

Verificar:

git remote -v
10. Subir el proyecto por primera vez
git push -u origin main

Solo la primera vez usamos -u.

Después simplemente:

git push
11. Descargar cambios del repositorio remoto
git pull
Flujo de trabajo que seguiremos SIEMPRE

Cada vez que programes, seguirás este ciclo:

Modificar archivos
        │
        ▼
git status
        │
        ▼
git add .
        │
        ▼
git commit -m "mensaje"
        │
        ▼
git push

Este será tu hábito desde el primer proyecto.