# Cómo subir este repo a GitHub (sin exponer tokens)

Repo destino: amorporloshierros-lab/rim-herreria (público)

## Opción A — con GitHub CLI (lo más rápido)
Requiere tener `gh` instalado y haber hecho `gh auth login` una vez.

    cd ruta/a/rim-herreria
    gh repo create amorporloshierros-lab/rim-herreria --public --source=. --remote=origin --push

Listo. Eso crea el repo y sube todo.

## Opción B — con git clásico
1) Primero creá el repo VACÍO en la web: https://github.com/new
   - Owner: amorporloshierros-lab
   - Repository name: rim-herreria
   - Public
   - NO marques "Add a README" (ya hay uno)
   - Create repository

2) Después, en tu PC:

    cd ruta/a/rim-herreria
    git init
    git add .
    git commit -m "Web R.I.M Herrería en General"
    git branch -M main
    git remote add origin https://github.com/amorporloshierros-lab/rim-herreria.git
    git push -u origin main

Cuando te pida usuario/contraseña, la "contraseña" es un token NUEVO
(generado en tu PC, no el viejo). O usá `gh auth login` y se resuelve solo.

## Después: Vercel (para verla online)
1) vercel.com -> Add New -> Project
2) Importá el repo rim-herreria
3) Deploy -> te da un link tipo rim-herreria.vercel.app
Cada push a GitHub actualiza la web sola.
