## Explicación

Este ejercicio simulará un sistema de gestión de libros.
Crearemos tres módulos:

- Uno para gestionar la lista de libros.
- Otro para manejar operaciones relacionadas con autores.
- Y un último módulo principal que utiliza los dos primeros para realizar algunas acciones.

1. Crea un archivo llamado `bookList.js` para gestionar la lista de libros:
   El objetivo es manejar una lista de libros y realizar operaciones básicas como agregar libros y obtener todos los libros.

**PASOS PARA IMPLEMENTAR bookList.js:**

### Definir la Estructura de Datos:

- Decide cómo representarás un libro en tu aplicación. Puede ser un objeto con propiedades como title, author, isbn, etc.
- Piensa en cómo almacenarás la lista de libros. Puede ser un array donde cada elemento es un libro.
  Agregar Funciones:
- Implementa una función para agregar un nuevo libro a la lista. Esta función debería tomar parámetros como el título y el autor del libro y agregarlo a la lista.
  Implementa una función para obtener todos los libros. Esta función debería devolver la lista completa de libros.

### Exportar Funciones:

- Exporta las funciones que has implementado para que puedan ser utilizadas en otros módulos o en el archivo principal (index.js en este caso).
- Antes de utilizar este módulo en tu aplicación principal, puedes probarlo de forma aislada para asegurarte de que las funciones funcionan correctamente.

2. Crea otro archivo llamado `authorUtils.js` para manejar operaciones relacionadas con autores:

**PASOS PARA IMPLEMENTAR authorUtils.js:**

### Definir la Funcionalidad:

Decide qué funcionalidad específica relacionada con autores deseas implementar. En este caso, asumamos que deseas obtener una lista de todos los autores únicos presentes en la lista de libros.

### Agregar Funciones:

- Implementa una función que toma la lista de libros como parámetro y devuelve una lista de autores únicos.
- Puedes utilizar un conjunto (Set) para almacenar los autores únicos y luego convertirlo en una lista.

### Exportar Funciones:

- Exporta la función que has implementado para que pueda ser utilizada en otros módulos o en el archivo principal (index.js).

3. Ahora, crea un archivo principal `index.js` que utiliza los dos módulos anteriores:

**PASOS PARA IMPLEMENTAR index.js:**

## Importar Módulos:

Importa los módulos bookList y authorUtils al principio de tu archivo.

## Utilizar Funciones de bookList:

Utiliza las funciones del módulo `bookList` para agregar libros y obtener la lista completa de libros.
Puedes hacer algo parecido a esto:

`bookList.addBook('The Great Gatsby', 'F. Scott Fitzgerald');`
`bookList.addBook('To Kill a Mockingbird', 'Harper Lee');`
`bookList.addBook('1984', 'George Orwell');`

## Utilizar Funciones de authorUtils:
Utiliza las funciones del módulo `authorUtils` para obtener la lista de autores únicos a partir de la lista de libros.

4. Ejecuta el programa:

Desde la línea de comandos, ejecuta `node index.js` para ver el resultado. Este programa simplemente agrega algunos libros, muestra todos los libros y luego muestra todos los autores.

EL resultado debe ser algo similar a esto:

Todos los libros: [
{ title: 'The Great Gatsby', author: 'F. Scott Fitzgerald' },
{ title: 'To Kill a Mockingbird', author: 'Harper Lee' },
{ title: '1984', author: 'George Orwell' },
{ title: 'The Catcher in the Rye', author: 'J.D. Salinger' },
{ title: 'Brave New World', author: 'Aldous Huxley' }
]
Todos los autores: [
'F. Scott Fitzgerald',
'Harper Lee',
'George Orwell',
'J.D. Salinger',
'Aldous Huxley'
]

Este es un ejemplo simple, pero puedes expandirlo y agregar más funcionalidades según tus necesidades. El diseño modular permite que cada módulo se centre en una tarea específica, lo que hace que el código sea más modular y fácil de entender y mantener.

## Pista:

Si comenzar modularmente te resulta más complejo, haz todo en el documento index.js y después refactoriza modularmente una vez funcione.
