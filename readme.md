# Bootcamp de Frontend: Guía del Alumno

Bienvenido al Bootcamp de Frontend. Esta guía proporciona información esencial sobre la manipulación del DOM en JavaScript, el uso de promesas y conceptos básicos de Git.

## 1. Manipulación del DOM con JavaScript

### ¿Qué es el DOM?

El DOM (Document Object Model) es una representación en memoria de la estructura de un documento HTML. Permite a los programadores acceder, modificar y actualizar el contenido y la estructura de una página web de manera dinámica.

### Selección de Elementos

En JavaScript, hay varias formas de seleccionar elementos del DOM:

```javascript
// Por ID
const elementoPorId = document.getElementById('miId');

// Por clase
const elementosPorClase = document.getElementsByClassName('miClase');

// Selector único
const elementoUnico = document.querySelector('.miSelector');

// Selector múltiple
const elementosMultiples = document.querySelectorAll('p');

```
### Manipulación de Contenido y Atributos

Para manipular el contenido de un elemento y sus atributos, puedes usar:

```javascript

// Manipulación de contenido
elementoPorId.innerHTML = 'Nuevo contenido';

// Manipulación de atributos
elementoPorId.setAttribute('nuevo-atributo', 'valor');
```

### Creación de Elementos y Anidación

Puedes crear nuevos elementos y anidarlos en el DOM:

```javascript
// Crear un nuevo elemento
const nuevoElemento = document.createElement('div');

// Anidar elementos
elementoPorId.appendChild(nuevoElemento);
```

## 2. Promesas en JavaScript

### ¿Qué son las Promesas?

Las promesas en JavaScript son objetos que representan el resultado eventual de una operación asíncrona.
Permiten manejar el código asíncrono de manera más limpia y legible.

### Sintaxis Básica de Promesas

```javascript
const miPromesa = new Promise((resolve, reject) => {
  // Operación asíncrona
  if (operacionExitosa) {
    resolve('Éxito');
  } else {
    reject('Error');
  }
});

// Uso de then, catch y finally
miPromesa
  .then((resultado) => {
    console.log(resultado);
  })
  .catch((error) => {
    console.error(error);
  })
  .finally(() => {
    console.log('Operación completa');
  });
```
### Uso de fetch con Promesas

Fetch es una función integrada en los navegadores que permite realizar solicitudes HTTP de manera asíncrona. Se integra bien con el uso de promesas para manejar las respuestas.

```javascript
// Ejemplo de uso de fetch
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json(); // Parsear la respuesta como JSON
  })
  .then(data => {
    console.log('Datos recibidos:', data);
  })
  .catch(error => {
    console.error('Hubo un problema con la petición Fetch:', error);
  });
```


## 3. Git Básico

### Introducción a Git

Git es un sistema de control de versiones que ayuda a rastrear los cambios en el código fuente durante el desarrollo de software.

### Inicializar un repositorio
```
git init
```

### Añadir archivos al área de preparación
```
git add nombre-del-archivo
```

### Realizar un commit
```
git commit -m "Mensaje descriptivo"
```

### Verificar el estado del repositorio
```
git status
```

### Ver el historial de commits
```
git log
```

