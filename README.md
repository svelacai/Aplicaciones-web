# Aplicaciones-web

# Fundamentos de la Web: HTML, CSS, JavaScript y DevTools

## 1) ¿Qué es HTML y cuál es su función en la web?
**HTML (HyperText Markup Language)** es el lenguaje de marcas que define la **estructura** y el **contenido** de una página web: textos, imágenes, enlaces, formularios, tablas, etc. Los navegadores leen HTML para construir el **DOM** (árbol de nodos) que luego se presenta al usuario.

## 2) ¿Qué es una etiqueta HTML y etiquetas comunes?
Una **etiqueta HTML** (tag) delimita y describe un tipo de contenido dentro del documento. Normalmente tiene **apertura** `<etiqueta>` y **cierre** `</etiqueta>`.
**Comunes**:
- Estructura: `<!doctype html>`, `<html>`, `<head>`, `<body>`, `<meta>`, `<title>`
- Texto: `<h1>`…`<h6>`, `<p>`, `<span>`, `<strong>`, `<em>`, `<br>`, `<hr>`
- Agrupación/maquetación: `<div>`, `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
- Enlaces/medios: `<a>`, `<img>`, `<video>`, `<audio>`, `<source>`, `<picture>`
- Listas/tablas: `<ul>`, `<ol>`, `<li>`, `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`
- Formularios: `<form>`, `<input>`, `<label>`, `<button>`, `<select>`, `<option>`, `<textarea>`
- Scripts/estilos: `<script>`, `<link>`, `<style>`

## 3) ¿Qué es un atributo en HTML y los más comunes?
Un **atributo** añade información extra o configura el comportamiento de una etiqueta mediante **pares nombre="valor"**.
**Comunes**:
- Globales: `id`, `class`, `style`, `title`, `data-*`, `hidden`, `tabindex`
- Accesibilidad: `aria-*`, `role`, `alt` (en `img`)
- Enlaces/medios: `href` (`a`), `src` (`img`, `script`), `target`, `rel`
- Imágenes/responsive: `width`, `height`, `srcset`, `sizes`, `loading="lazy"`
- Formularios: `name`, `type`, `value`, `placeholder`, `required`, `min`, `max`, `step`, `checked`, `disabled`

## 4) ¿Qué es CSS y cómo se utiliza para el diseño web?
**CSS (Cascading Style Sheets)** define la **presentación**: colores, tipografías, espaciados, tamaños, posiciones y diseño responsivo. Se aplica:
- **Externo**: `<link rel="stylesheet" href="styles.css">` (recomendado)
- **Interno**: `<style> ... </style>` en el `<head>`
- **Inline**: `style="..."` directamente en una etiqueta (evitar salvo casos puntuales)

## 5) ¿Qué es una propiedad en CSS y las más comunes?
Una **propiedad CSS** especifica qué aspecto estilístico modificar (con un valor). Ej.: `color: red;`
**Comunes**:
- Texto/tipografía: `color`, `font-family`, `font-size`, `font-weight`, `line-height`, `text-align`
- Caja/espaciado: `margin`, `padding`, `border`, `border-radius`, `box-shadow`
- Tamaño/posición: `width`, `height`, `max-width`, `display`, `position`, `top/right/bottom/left`, `z-index`
- Layout moderno: `flex`, `flex-direction`, `justify-content`, `align-items`, `gap`, `grid`, `grid-template-columns`, `grid-template-rows`, `grid-gap`
- Fondo: `background`, `background-color`, `background-image`, `background-size`
- Otros útiles: `overflow`, `opacity`, `transition`, `transform`

## 6) ¿Qué es un selector en CSS y qué tipos existen?
Un **selector** indica a qué elementos del DOM se les aplican reglas.
**Tipos**:
- **Básicos**: de **tipo** (`div`), de **clase** (`.card`), de **id** (`#header`), **universal** (`*`)
- **Combinadores**: descendiente (`div p`), hijo directo (`ul > li`), adyacente (`h1  p`), hermanos (`h1 ~ p`)
- **Atributo**: `[type="email"]`, `[href^="https"]`, `[data-role~="tag"]`
- **Pseudoclases**: `:hover`, `:focus`, `:active`, `:visited`, `:checked`, `:disabled`, `:nth-child(n)`, `:first-child`, `:last-child`
- **Pseudoelementos**: `::before`, `::after`, `::placeholder`, `::selection`
- **Específicos modernos**: `:is()`, `:where()`, `:not()`, `:has()` (soporte reciente)

## 7) ¿Qué es JavaScript y cómo añade interactividad?
**JavaScript** es el lenguaje de programación del navegador (y también del servidor con Node.js). Permite **manipular el DOM**, **manejar eventos** (click, input, teclas), **cargar datos** vía **fetch/AJAX**, **validar formularios**, reproducir multimedia y más, haciendo que las páginas respondan a las acciones del usuario **sin recargar** completamente.

## 8) Tipos de datos primitivos en JavaScript
`string`, `number` (incluye `NaN` e infinitos), `boolean`, `null`, `undefined`, `symbol`, `bigint`.

## 9) Estructuras de control (if/else, switch, bucles)
- **if / else if / else**: ejecutan bloques en función de condiciones booleanas.
- **switch**: compara una expresión contra múltiples **case**; usar `break` para evitar *fall-through*.
- **Bucles**:
  - `for (inicio; condición; actualización) { ... }`
  - `while (condición) { ... }`
  - `do { ... } while (condición);`
  - **Iterables**: `for...of` recorre valores de arrays/iterables; `for...in` recorre **claves** de objetos (útil con cuidado).
  - **Array helpers** (declarativos): `forEach`, `map`, `filter`, `reduce`, `some`, `every`.

## 10) ¿Por qué usar nombres significativos para variables y métodos?
Mejoran la **legibilidad**, reducen **errores**, facilitan el **mantenimiento** y la **colaboración**. Nombres claros comunican propósito y evitan comentarios innecesarios. Preferir **sustantivos** para datos (`userEmail`) y **verbos** para funciones/métodos (`sendInvoice`).

## 11) ¿Qué es una variable de entorno y por qué es importante?
Una **variable de entorno** es un valor configurado fuera del código (p.ej., en el sistema o archivo `.env`) que el programa lee en tiempo de ejecución: **claves API**, **URLs**, **modos** (`NODE_ENV=production`). Permiten:
- Separar **configuración** de **código**
- Evitar exponer **secretos** en el repositorio
- Cambiar comportamientos entre **desarrollo**, **pruebas** y **producción**

## 12) ¿Qué son las DevTools de Chrome y cómo se accede?
Son herramientas integradas del navegador para **inspeccionar**, **depurar**, **medir rendimiento** y **analizar red**.
Acceso: **F12**, **CtrlShiftI** (Windows/Linux) o **CmdOptionI** (macOS), o clic derecho → **Inspect/Inspeccionar**.

## 13) ¿Qué se puede hacer en el panel *Elements*?
- Inspeccionar y **editar el DOM** en vivo
- Modificar **estilos CSS**, ver **reglas**, **especificidad**, estados (`:hover`, `:active`)
- Visualizar el **box model** (margen, borde, padding, tamaño)
- Comprobar **clases**, **atributos**, **event listeners** y **propiedades de accesibilidad**

## 14) ¿Cómo usar el panel *Console* y para qué es útil?
Permite **ejecutar JavaScript** en la página, ver **logs** (`console.log`, `error`, `warn`, `table`), **errores y trazas**, probar expresiones, medir tiempos (`console.time`/`timeEnd`) y depurar con `debugger`. Útil para **diagnóstico rápido** y **experimentos** sin editar archivos.

## 15) ¿Qué información ofrece el panel *Network* y por qué importa?
Muestra cada **petición** (HTML, CSS, JS, imágenes, XHR/fetch):
- **URL**, **método**, **código de estado**
- **Request/Response headers**, **payload**, **respuesta**, **tamaño**
- **Timing** (DNS, conexión, TTFB, descarga) y efecto de **caché**
Sirve para detectar **errores de API**, tiempos lentos, recursos pesados y problemas de **caching** o **CORS**.
