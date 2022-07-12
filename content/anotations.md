# Anotaciones Javascript

## Tabla de contenido

- [Anotaciones Javascript](#anotaciones-javascript)
  - [Tabla de contenido](#tabla-de-contenido)
  - [Aspectos importantes del lenguaje](#aspectos-importantes-del-lenguaje)
  - [Tipos de Datos](#tipos-de-datos)
    - [Variables: var VS let](#variables-var-vs-let)
  - [Estructuras de Control](#estructuras-de-control)
  - [Progrmacion Orientada a Objetos](#progrmacion-orientada-a-objetos)
  - [Objetos y funciones del lenguaje](#objetos-y-funciones-del-lenguaje)
  - [Programación Asíncrona](#programación-asíncrona)
    - [Set](#set)
    - [Map](#map)
    - [WeakSet & WeakMap](#weakset--weakmap)
  - [Nuevos Tipos y Características](#nuevos-tipos-y-características)
  - [La instrucción this en Javascript](#la-instrucción-this-en-javascript)
  - [Javascript Object Notation (JSON)](#javascript-object-notation-json)
  - [Document Object Model (DOM)](#document-object-model-dom)
  - [Asynchronous Javascript and XML (AJAX)](#asynchronous-javascript-and-xml-ajax)
  - [APIs Rest](#apis-rest)
  - [Single Page Aplication (SPA)](#single-page-aplication-spa)
  - [Reactividad](#reactividad)

## Aspectos importantes del lenguaje

Hoy JavaScript, es el único lenguaje capaz de ejecutarse en las 3 capas de una aplicación:

- Frontend (con JavaScript).
- Backend (con Node.js).
- Persistencia de Datos (con MongoDB, Couch DB, Firebase, etc).

Con JavaScript puedes:

- Diseño y Desarrollo Web.
- Hacer Videojuegos.
- Experiencias 3D, Realidad Aumentada, Realidad Virtual.
- Controlar Hardware (drones, robots, electrodomésticos, wearables, etc).
- Aplicaciones Híbridas y Móviles.
- Aprendizaje Automático.
- etc.

## Tipos de Datos

### Variables: var VS let

La sentencia _var_ declara una variable, opcionalmente inicializándola con un valor.
_Su ámbito es global._

```javascript
var nombreDeVariable1 [= valor1] [, nombreDeVariable2 [= valor2] ... [, nombreDeVariableN [=valorN]]];
```

## Estructuras de Control

## Progrmacion Orientada a Objetos

## Objetos y funciones del lenguaje

## Programación Asíncrona

### Set

### Map

### WeakSet & WeakMap

Weak: débil. Significa que solo van a poder almacenar referencias débiles, es decir que las llaves sean de tipo objeto. Esto le permite al recolector de basura que al momento que alguna de las referencias débiles que tengan estos WeakSets o WeaksMaps se hayan limpiado dentro de la logica de nuestra programación, cuando el recolector de basura del navegador ejecute su proceso, es decir que limpia lo que el navegador no necesite en la sesion que estes trabajando, todas estas referencias débiles al ya no existir las va a limpiar y eso mejora el rendimiento de nuestra aplicacién.

**Carencias:**

- No se pueden iterar, es decir recorrer cada elemento con un bucle como el for of, ya que no son propieades iterables.
- No se pueden eliminar todos los elementos y propiedades directamente con el metodo clear
- No podemos verificar su tamaño, es decir no tienen la propiedad size
- No se pueden agregar los valores directamente como un set normal:
  `const ws = new WeakSet([1, 2, 3, true, false, false, {}, {}, "HOLA", "HOla"])`

## Nuevos Tipos y Características

## La instrucción this en Javascript

## Javascript Object Notation (JSON)

## Document Object Model (DOM)

## Asynchronous Javascript and XML (AJAX)

## APIs Rest

## Single Page Aplication (SPA)

## Reactividad

```

```
