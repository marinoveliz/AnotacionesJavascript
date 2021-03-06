# forEach vs forOf vs forIn

## ForEach

El método _forEach()_ ejecuta la función indicada una vez por cada elemento del array.

Se debe usar cuando por cada iteracion se desee ejecutar una funcion en particupar, es similar al bucle for...of pero con la limitante de que solo ejecuta funciones.

### Sintaxis

```
arr.forEach(function callback(currentValue, index, array) {
   // tu iterador
    }[, thisArg]);
```

**Ejemplos**

```javascript
const array1 = ["a", "b", "c"];

array1.forEach((element) => console.log(element));

// expected output: "a"
// expected output: "b"
// expected output: "c"
```

> **Nota:** recomendado para trabajar con arreglos.

---

## for...in

La instrucción for-in itera sobre todas las propiedades enumerables de un objeto que está codificado por cadenas (ignorando los codificados por Símbolos, incluidas las propiedades enumerables heredadas.

Un bucle for...in solo itera sobre propiedades enumerables que no son símbolo. Los objetos creados a partir de constructores integrados como Array y Object han heredado propiedades no enumerables de Object.prototype y String.prototype, como el método indexOf() de String o el método toString() de Object. El bucle iterará sobre todas las propiedades enumerables del objeto en sí y aquellas que el objeto hereda de su cadena de prototipos (las propiedades de los prototipos más cercanos tienen prioridad sobre las de los prototipos más alejados del objeto en su cadena de prototipos).

A mi parecer se debe usar cuando queramos trabajar con las propiedades de los objetos para ver como estas se comportan, pero siempre es preferible trabajar con el metodo for..of.

### Propiedades deleted, modified, added

En general, es mejor no agregar, modificar o eliminar propiedades del objeto durante la iteración, aparte de la propiedad que se está visitando actualmente. No hay garantía de si se visitará una propiedad agregada, si se visitará una propiedad modificada (distinta de la actual) antes o después de que se modifique, o si se visitará una propiedad eliminada antes de eliminarla.

**Ejemplos**

```javascript
const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```

### Sintaxis

```
for (variable in objeto)
  instrucción
```

**variable:** Asigna un nombre de propiedad diferente a la variable en cada iteración.

**objeto:** Objeto cuyas propiedades enumerables que no son símbolos se iteran.

> **Nota:** for...in no se debe usar para iterar sobre un Array donde el orden del índice es importante.

---

## for ... of

La sentencia sentencia for...of ejecuta un bloque de código para cada elemento de un objeto iterable, como lo son: String, Array, objetos similares a array (por ejemplo, arguments or NodeList), TypedArray, Map, Set e iterables definidos por el usuario.

A diferencia del bucle for ..in este bucle se centra en su index como el valor del objeto iterable y no su posicion o propiedad.

### Sintaxis

```
for (variable of iterable) {
  statement
}
```

**variable:** En cada iteración el elemento (propiedad enumerable) correspondiente es asignado a variable.

**iterable:** Objeto cuyas propiedades enumerables son iteradas.

**Ejemplos**

Iterando un Array

```javascript
let iterable = [10, 20, 30];

for (let value of iterable) {
  value += 1;
  console.log(value);
}
// 11
// 21
// 31
```

### Diferencia entre for...of y for...in

El bucle for...in iterará sobre todas las propiedades de un objeto. Más tecnicamente, iterará sobre cualquier propiedad en el objeto que haya sido internamente definida con su propiedad [[Enumerable]] configurada como true.

La sintaxis de for...of es específica para las colecciones, y no para todos los objetos. Esta Iterará sobre cualquiera de los elementos de una colección que tengan la propiedad [Symbol.iterator].

El siguiente ejemplo muestra las diferencias entre un bucle for...of y un bucle for...in.

```javascript
let arr = [3, 5, 7];
arr.foo = "hola";

for (let i in arr) {
  console.log(i); // logs "0", "1", "2", "foo"
}

for (let i of arr) {
  console.log(i); // logs "3", "5", "7"
}
```
