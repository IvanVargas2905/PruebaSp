
wrumsoltest1@50C4WH3 MINGW64 ~/Downloads/Ivan/Prueba3
$ git init
Initialized empty Git repository in C:/Users/wrumsoltest1/Downloads/Ivan/Prueba3/.git/

wrumsoltest1@50C4WH3 MINGW64 ~/Downloads/Ivan/Prueba3 (master)
$ git remote add origin https://github.com/IvanVargas2905/Sistema.git

wrumsoltest1@50C4WH3 MINGW64 ~/Downloads/Ivan/Prueba3 (master)
$ git branch -M master

wrumsoltest1@50C4WH3 MINGW64 ~/Downloads/Ivan/Prueba3 (master)
$ git push -u origin master
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/IvanVargas2905/Sistema.git'

wrumsoltest1@50C4WH3 MINGW64 ~/Downloads/Ivan/Prueba3 (master)
$ git add .

wrumsoltest1@50C4WH3 MINGW64 ~/Downloads/Ivan/Prueba3 (master)
$ git commit -m "Primer commit"
[master (root-commit) 907e955] Primer commit
 Committer: solutions L1 <wrmsoltest1@copeland.com>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 11 files changed, 2193 insertions(+)
 create mode 100644 .vscode/settings.json
 create mode 100644 ESTRUCTURA.md
 create mode 100644 README.md
 create mode 100644 REFERENCIA_RAPIDA.md
 create mode 100644 css/styles.css
 create mode 100644 index.html
 create mode 100644 js/app.js
 create mode 100644 js/modules/actions.js
 create mode 100644 js/modules/auth.js
 create mode 100644 js/modules/roles.js
 create mode 100644 js/services/navigation.js

wrumsoltest1@50C4WH3 MINGW64 ~/Downloads/Ivan/Prueba3 (master)
$ git push -u origin master
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 14 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (18/18), 18.96 KiB | 1.18 MiB/s, done.
Total 18 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/IvanVargas2905/Sistema.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.




Necesito que desarrolles una aplicación web completa usando HTML, CSS y JavaScript puro (sin frameworks).

IMPORTANTE:
- El código debe estar organizado como un proyecto real.
- Cada parte debe estar en archivos separados.
- Usa una estructura de carpetas clara (como proyectos profesionales).

----------------------------------
1. ESTRUCTURA DEL PROYECTO
----------------------------------

Quiero que organices el proyecto así:

/project
│
├── index.html
├── /css
│     └── styles.css
├── /js
│     ├── app.js
│     ├── modules/
│     │      ├── auth.js
│     │      ├── roles.js
│     │      └── actions.js
│     └── services/
│            └── navigation.js

Explica qué hace cada archivo.

----------------------------------
2. DISEÑO (MUY IMPORTANTE)
----------------------------------

El diseño debe ser SIMPLE, como sistema interno.

Basado en esto:
- Login centrado
- Fondo gris claro
- Caja blanca con borde gris suave
- Inputs básicos
- Botón sencillo
- Sin sombras modernas ni estilos complejos

Debe verse como en la imagen:
- Título "Iniciar sesión"
- Texto "Ingresa tu ID"
- Campo "ID de usuario"
- Botón "Ingresar"

----------------------------------
3. LOGIN
----------------------------------

- Solo se usa un ID (sin contraseña)
- Validar que no esté vacío

Reglas:
- ID que empieza con "C" → CALIDAD
- ID que empieza con "P" → PRODUCCIÓN
- Otro → mostrar error: "ID no válido"

Después de iniciar sesión:
- Redirigir al panel correspondiente automáticamente

----------------------------------
4. PANEL PRINCIPAL
----------------------------------

Mostrar:

- Usuario: CALIDAD o PRODUCCIÓN
- 5 botones:

1. Eliminar caja
2. Borrar historial de pieza
3. Mover piezas de orden de trabajo (Retrabajado)
4. Botón sin asignar
5. Botón sin asignar

----------------------------------
5. PERMISOS
----------------------------------

CALIDAD:
- Puede ver todos los botones
- SOLO puede usar:
  ✔ Eliminar caja
- Si hace clic en otro:
  → Mostrar: "No tienes permitido acceder a esta opción"

PRODUCCIÓN:
- Puede usar:
  ✔ Eliminar caja
  ✔ Borrar historial de pieza
  ✔ Mover piezas
- Los otros 2:
  → Mostrar: "Botón sin asignar"

----------------------------------
6. FUNCIONALIDAD: RETRABAJADO
----------------------------------

Crear una pequeña interfaz con inputs:

- Orden original
- Nueva orden
- ID de pieza

Lógica:
- Simular que una pieza se devuelve
- Al reutilizarla, agregar "R" al inicio

Ejemplo:
Orden 20 → piezas 1,2,3
Se devuelve pieza 2
Nueva orden 45 → guardar como "R2"

Mostrar resultado en pantalla

----------------------------------
7. ARQUITECTURA DEL CÓDIGO
----------------------------------

modules:
- auth.js → lógica de inicio de sesión
- roles.js → permisos por tipo de usuario
- actions.js → funciones de cada botón

services:
- navigation.js → cambios de vista (login → panel)

app.js:
- archivo principal que conecta todo

----------------------------------
8. VALIDACIONES
----------------------------------

- Campos vacíos
- ID inválido
- Mostrar mensajes claros en pantalla (no solo alert)

----------------------------------
9. EXTRAS
----------------------------------

- No usar base de datos
- Todo en memoria (JavaScript)
- Código comentado línea por línea
- Explicar cómo funciona todo

----------------------------------

IMPORTANTE FINAL:
Entrega todo el código separado por archivos, indicando claramente:

--- index.html ---
--- css/styles.css ---
--- js/app.js ---
etc.

Hagamos un promt para claudea.ia
en donde temenos que hacer un programa y su pagina principal sea un inicio de sesion, la cual solo pueden acceder por un id, en este caso dependiendo del id puede que sean del departamento de calidad o de produccion

la cual las 2 pueden ver todas las opciones, calidad: vamos a decir que calidad solo tener la opcion de que puede eliminar caja, pero aun asi puede ver las otras 2 opciones, pero cuando el usuario de calidad le de click, le salga un mensaje en donde diga que no tiene permitido entrar

produccion: produccion puede hacer las 3 opciones

pero digamos que son 5 opciones, la cual produccion tiene las 3 que ya habiamos omentado y las otras 2 las tiene bloquedas, estas no hacen nada, solo dicen que boton sin asignar, necesito que sea en html, css y js

las opciones son:

eliminar caja

borrar historial de pieza (esto es aparte de lo de eliminar caja)

mover piezas de orden de trabajo (R de retrabajado) (aqui lo que se necesita es que si se usa una pieza en una orden y tiempo despues vuelve una pieza, poder ponerno en una Nueva orden, pero con una R al principio de su id de producto) ejemplo, si se crea la orden 20 y se lleva la pieza 1, 2 y 3, pero 2 fue devuelta porque no se uso y esa pieza sirve para la orden 45, entonces le pondremos a la pieza que se devolvio una "R", ejemplo: R2, fue asignada a la orden 45



se necesita que cuando se inicie sesion, ya lo meta al apartado de calidad o produccion, dependiendo de su ID

Que tiene que no tenga un diseño, solo sea css basico como esta en la foto que es un ejemplo de como lo quiero
necesito que cada cosa este separada, html, js, css, cada cosa separa en arhvivos separados, asi como que hay proyecos que usan carpetas como service, moduls y etc, quiero que tambien sea asi este proyecto, yo se que la carpeta service sirve para redirigir, es la que hace todos los procesos, entonces debe de ser asi con las demas 


## Copyright and License

Copyright 2013-2023 Start Bootstrap LLC. Code released under the [MIT](https://github.com/StartBootstrap/startbootstrap-freelancer/blob/master/LICENSE) license.
