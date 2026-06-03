# [Start Bootstrap - Freelancer](https://startbootstrap.com/theme/freelancer/)

[Freelancer](https://startbootstrap.com/theme/freelancer/) is a one page, freelancer portfolio theme built with [Bootstrap](https://getbootstrap.com/) created by [Start Bootstrap](https://startbootstrap.com/). This theme features several content sections, a responsive portfolio grid, modal windows for each portfolio item, and a working PHP based contact form.

## Preview

[![Freelancer Preview](https://assets.startbootstrap.com/img/screenshots/themes/freelancer.png)](https://startbootstrap.github.io/startbootstrap-freelancer/)

**[View Live Preview](https://startbootstrap.github.io/startbootstrap-freelancer/)**

## Status

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/StartBootstrap/startbootstrap-freelancer/master/LICENSE)
[![npm version](https://img.shields.io/npm/v/startbootstrap-freelancer.svg)](https://www.npmjs.com/package/startbootstrap-freelancer)

## Download and Installation

To begin using this template, choose one of the following options to get started:

- [Download the latest release on Start Bootstrap](https://startbootstrap.com/theme/freelancer/)
- Install using npm: `npm i startbootstrap-freelancer`
- Clone the repo: `git clone https://github.com/StartBootstrap/startbootstrap-freelancer.git`
- [Fork, Clone, or Download on GitHub](https://github.com/StartBootstrap/startbootstrap-freelancer)

## Usage

### Basic Usage

After downloading, simply edit the HTML and CSS files included with `dist` directory. These are the only files you need to worry about, you can ignore everything else! To preview the changes you make to the code, you can open the `index.html` file in your web browser.

### Advanced Usage

Clone the source files of the theme and navigate into the theme's root directory. Run `npm install` and then run `npm start` which will open up a preview of the template in your default browser, watch for changes to core template files, and live reload the browser when changes are saved. You can view the `package.json` file to see which scripts are included.

#### npm Scripts

- `npm run build` builds the project - this builds assets, HTML, JS, and CSS into `dist`
- `npm run build:assets` copies the files in the `src/assets/` directory into `dist`
- `npm run build:pug` compiles the Pug located in the `src/pug/` directory into `dist`
- `npm run build:scripts` brings the `src/js/scripts.js` file into `dist`
- `npm run build:scss` compiles the SCSS files located in the `src/scss/` directory into `dist`
- `npm run clean` deletes the `dist` directory to prepare for rebuilding the project
- `npm run start:debug` runs the project in debug mode
- `npm start` or `npm run start` runs the project, launches a live preview in your default browser, and watches for changes made to files in `src`

You must have npm installed in order to use this build environment.

### Contact Form

The contact form available with this theme is prebuilt to use [SB Forms](https://startbootstrap.com/solution/contact-forms).
SB Forms is a simple form solution for adding functional forms to your theme. Since this theme is prebuilt using our
SB Forms markup, all you need to do is sign up for [SB Forms on Start Bootstrap](https://startbootstrap.com/solution/contact-forms).

After signing up you will need to set the domain name your form will be used on, and you will then see your
access key. Copy this and paste it into the `data-sb-form-api-token='API_TOKEN'` data attribute in place of
`API_TOKEN`. That's it! Your forms will be up and running!

If you aren't using SB Forms, simply delete the custom data attributes from the form, and remove the link above the
closing `</body>` tag to SB Forms.

## Bugs and Issues

Have a bug or an issue with this template? [Open a new issue](https://github.com/StartBootstrap/startbootstrap-freelancer/issues) here on GitHub or leave a comment on the [theme overview page at Start Bootstrap](https://startbootstrap.com/theme/freelancer/).

## About

Start Bootstrap is an open source library of free Bootstrap themes and templates. All of the free themes and templates on Start Bootstrap are released under the MIT license, which means you can use them for any purpose, even for commercial projects.

- <https://startbootstrap.com>
- <https://twitter.com/SBootstrap>

Start Bootstrap was created by and is maintained by **[David Miller](https://davidmiller.io/)**.

- <https://davidmiller.io>
- <https://twitter.com/davidmillerhere>
- <https://github.com/davidtmiller>

Start Bootstrap is based on the [Bootstrap](https://getbootstrap.com/) framework created by [Mark Otto](https://twitter.com/mdo) and [Jacob Thorton](https://twitter.com/fat).



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
