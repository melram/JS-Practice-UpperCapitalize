### Features

- Ejercicio Practico de JavaScript.
- Uso de Uppercase - Capitalize en CSS.
- Funciones y evento.


####Javascript　

```javascript
mensajefrom.addEventListener("submit", (event) => {
  //valor del mensaje
  let textmensaje = document.getElementById("mensaje").value;
  addElement(textmensaje); // llamo a la función para llamar en la lista
  event.preventDefault(); // para que no se recarge la pagina :D
});

function addElement(text) {
  // crea un nuevo li
  var newLi = document.createElement("li");
  // y añade text
  var newContent = document.createTextNode(text);
  //añade texto al li
  newLi.appendChild(newContent);

  // seleccionar la lista mensajes
  var currentLi = document.getElementById("mensajes-list");
  // añadir mensaje la lista :D
  currentLi.appendChild(newLi);
}

listmayuscula.addEventListener("click", () => {
  //selecciona la lista y le asigno la clase de css :D
  document.getElementById("mensajes-list").className = "capi-text";
});

```

####HTML code

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Ejercicio JavaScript</title>
        <link rel="stylesheet" href="index.css">
    </head>
    <body>

        <p class="upper-text">Dato este Texto, conviertelo todo en mayuscula</p>
        <p class="capi-text">dato este texto, convierta la primera palabra a mayuscula</p>

        <form id="mensajefrom">
            <label for="mensaje">Ingrese un mensaje</label>
            <input id="mensaje"/>
            <button type="submit" id="guardar">Guardar</button>
        </form>
        <ul id="mensajes-list">
            <li>Tus mensajes son</li>
        </ul>
        <!--De de los mensajes anteriores-->
        <button id="listmayuscula">Convertir primera letra de cada palabra en mayuscula</button>
        <!--Realizar un boton anterior de 2 maneras, con y sin hacer modificaciones al texto ingresando por el usuario al insertarlo-->
    </body>
    <script src="index.js"></script>
</html>
```

####CSS　
```CSS
.upper-text {
  text-transform: uppercase;
}

.capi-text {
  text-transform: capitalize;
}

body {
  background-color: black;
  color: white;
}

```
