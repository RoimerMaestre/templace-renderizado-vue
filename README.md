
![alt](./public/Captura%20de%20pantalla%202024-07-02%20190239.png)

# DESAFIO TEMPLATE-RENDERING

## Descripción

Este proyecto es una sencilla aplicación Vue.js que permite a los usuarios personalizar un cuadro dinámico. Los usuarios pueden ajustar varias propiedades del cuadro, como el color de fondo, color del texto, opacidad, tamaño del borde, tipo de letra, y tamaño de la letra. Además, pueden mostrar u ocultar el texto dentro del cuadro y cambiar el contenido del texto.

## Características

<ul>
<li>Color de fondo: Permite cambiar el color de fondo del cuadro.</li>
<li>Color de texto: Permite cambiar el color del texto dentro del cuadro.</li>
<li>Mostrar/Ocultar texto: Permite mostrar u ocultar el texto dentro del cuadro.</li>
<li>Tamaño del borde: Permite ajustar el radio del borde del cuadro.</li>
<li>Contenido actual: Permite cambiar el contenido del texto dentro del cuadro.</li>
<li>Tipografía: Permite seleccionar entre varias fuentes para el texto dentro del cuadro.</li>
<li>Opacidad: Permite ajustar la opacidad del cuadro.
Tamaño de letra: Permite seleccionar entre varios tamaños de letra (pequeño, mediano, grande).</li>
</ul>

### Estructura del Proyecto

<ul>
<li>template: Contiene la estructura HTML de la aplicación.</li>
<li>script: Contiene la lógica Vue.js de la aplicación.</li>
<li>style: Contiene los estilos CSS para la aplicación.</li>
</ul>

## Detalle

Aunque no es un detalle como tal se le debe dar click al checkbox(Mostrar texto) para que aparezca,de lo contrario no se vera.
En la tipogracia en principio usamos v-model, dando de manera explicita el valor en la opcion, sin embargo no cubriamos la rubrica por ello decidimos usar bucle for en esa seccion.

# Dificultades

Personalmente me cuesta mucho entender el key en el bucle for, debo profundizar mas en ese caso.
aun me cuesta entender un poco el v-for, sin embargo no se ve complicado.

## templates-rendering-vue

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
