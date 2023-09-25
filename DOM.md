## ¿Qué es DOM?

El modelo de objeto de documento (DOM) es una interfaz de programación para HTML este traduce el contenido de un documento HTML a un objeto estandarizado, al que los lenguajes de programación funcionales como JavaScript tienen facilidad de acceso y modificación. Debido a que la mayoría de los eventos de páginas web son impulsados por código que no es HTML, todas las páginas web dinámicas dependen del DOM para visualizarse y funcionar correctamente.

## Funciones para modificar el DOM

### 1.querySelector y querySelectorAll:
Estas funciones te permiten seleccionar elementos del DOM utilizando selectores CSS y luego puedes modificar los elementos seleccionados.

```javascript
// Seleccionar un elemento por su ID
const elemento = document.querySelector("#miElemento");

// Seleccionar múltiples elementos por su clase
const elementos = document.querySelectorAll(".claseElemento");

```

### 2.**getElementById:**
Puedes seleccionar un elemento por su ID utilizando esta función.
```javascript 
const elemento = document.getElementById("miElemento");

```

### 3.**createElement:**
Crea un nuevo elemento HTML que puedes agregar al DOM.
```javascript
const nuevoElemento = document.createElement("div");
nuevoElemento.textContent = "Nuevo elemento";
document.body.appendChild(nuevoElemento); // Agregar al final del body

```

### 4.**appendChil:**
Agrega un elemento como hijo de otro elemento en el DOM.
```javascript 
const padre = document.getElementById("contenedor");
const hijo = document.createElement("p");
hijo.textContent = "Este es un nuevo párrafo";
padre.appendChild(hijo);

```

### 5.**removeChild:**
Elimina un elemento hijo de otro elemento.
```javascript
const padre = document.getElementById("contenedor");
const hijo = document.getElementById("elementoAEliminar");
padre.removeChild(hijo);

```

### 6.**innerHTML:**
Modifica el contenido HTML de un elemento.
```javascript
const elemento = document.getElementById("miElemento");
elemento.innerHTML = "<p>Nuevo contenido</p>";
 
```

### 7.**setAttribute y removeAttribute:**
Estas funciones te permiten agregar o eliminar atributos de elementos.
```javascript
const elemento = document.getElementById("miElemento");
elemento.setAttribute("class", "nuevaClase");
elemento.removeAttribute("id");
 
```

### 8.**classList:**
La propiedad **classList** te permite agregar, eliminar y alternar clases CSS en un elemento
```javascript
const elemento = document.getElementById("miElemento");
elemento.classList.add("nuevaClase");
elemento.classList.remove("claseAntigua");
elemento.classList.toggle("claseToggle");
 
```

### 9.**style:**
Puedes modificar el estilo CSS de un elemento utilizando la propiedad **style**.
```javascript
const elemento = document.getElementById("miElemento");
elemento.style.color = "red";
elemento.style.fontSize = "20px";

```

### 10.**addEventListener:**
Agrega un evento a un elemento para que responda a eventos del usuario, como clics o cambios de teclado.
```javascript
const boton = document.getElementById("miBoton");
boton.addEventListener("click", function() {
    // Código a ejecutar cuando se haga clic en el botón
});

```




## ¿Qué es?
La expresión **document.getElementById()** es una función en JavaScript que se utiliza para seleccionar un elemento HTML específico en un documento web utilizando su atributo `id`. Sin embargo, no existe una propiedad **.valve** asociada directamente a **document.getElementById().**

```javascript
const inputElement = document.getElementById("miInput");
const valor = inputElement.value;
 
```

# JQUERY

## ¿Qué es?
jQuery es una biblioteca de JavaScript que simplifica la manipulación del DOM (Document Object Model) y proporciona una amplia gama de funciones y utilidades para interactuar con elementos HTML, realizar animaciones, gestionar eventos, realizar peticiones AJAX y muchas otras tareas comunes en el desarrollo web. Fue creado por John Resig y lanzado en 2006.

### Principales características y ventajas:
1. **Facilita la manipulación del DOM:** jQuery simplifica la selección y manipulación de elementos HTML en una página web, lo que hace que sea más fácil agregar, eliminar o modificar contenido dinámicamente.
    
2. **Cross-browser:** jQuery se encarga de las diferencias entre navegadores, lo que significa que el mismo código funciona de manera consistente en varios navegadores web, eliminando la necesidad de escribir código específico para cada uno.
    
3. **Event Handling:** jQuery simplifica la gestión de eventos, como clics, cambios, desplazamientos y otros eventos del usuario, permitiendo una programación más sencilla de la interacción en la página web.
    
4. **Animaciones:** jQuery proporciona funciones para crear animaciones suaves y efectos de transición en elementos HTML, lo que facilita la creación de interfaces de usuario atractivas.
    
5. **Ajax:** jQuery facilita la realización de peticiones Ajax, lo que permite cargar datos de manera asincrónica desde el servidor sin necesidad de recargar toda la página.
    
6. **Plugins:** jQuery cuenta con una gran cantidad de plugins desarrollados por la comunidad que amplían sus capacidades, lo que permite añadir funcionalidades adicionales a tu sitio web de manera sencilla.
    
7. **Documentación abundante:** jQuery tiene una amplia documentación y una comunidad activa que ofrece soporte y recursos para ayudarte a resolver problemas y aprender a utilizar la biblioteca de manera efectiva.

### Ejemplo de uso: 

```javascript 
$(document).ready(function() {
    // Seleccionar un elemento por su ID y ocultarlo
    $("#miElemento").hide();

    // Agregar un manejador de eventos al hacer clic en un botón
    $("#miBoton").click(function() {
        // Realizar alguna acción al hacer clic en el botón
        $("#miElemento").show();
    });
});

```
