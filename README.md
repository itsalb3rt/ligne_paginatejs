# Ligne PaginateJs
Librería ligera en vanilla javascript para crear paginación y filtros sobre tablas HTML.
Con unas configuraciones mínimas puedes tener una paginación increíble.

- Sin Frameworks
- Sin dependencias

### DEMO

## https://itsalb3rt.github.io/ligne_paginatejs/

### Uso basico

Descarga del directorio `js` el archivo `paginate.js` y agregalo a tu proyecto con las etiqueta `script`

```html
<script type="text/javascript" src="js/paginate.js"></script>
```
Opcionalmente puedes agregar una hoja de estilos que hará que tu paginación luzca fenomenal, esta hoja esta en el directorio `css` llamada `paginate.css`

```html
<link rel="stylesheet" href="css/paginate.css">
```
---
Una vez incluido en tu proyecto puedes indicar el selector de tu tabla el cual puede ser una `clase` o un `id` ambos son validos.

```javascript
paginate.init('.myTable');
```

**Resultado;**

[![](https://i.imgur.com/ykzd7Lu.png)](https://i.imgur.com/ykzd7Lu.png)

### Opciones

Puedes establecer algunas opciones en el segundo parámetro como son;

- **numberPerPage:** Cantidad de filas por pagina
- **goBar:** Barra donde puedes digitar el numero de la pagina al que quiere ir
- **pageCounter:** Contador de paginas, en cual estas, de cuantas paginas

Te recomiendo crees una variable para establecer estas opciones;

```javascript
    let options = {
        numberPerPage:5, 
        goBar:true, 
        pageCounter:true
    };
	
paginate.init('.myTable',options);
```

**Resultado;**

[![](https://i.imgur.com/crlUHrS.png)](https://i.imgur.com/crlUHrS.png)

### Filtrar

Es posible agregar un tercer parámetro para establecer el elemento con el que quieres que se filtre, ósea la caja de texto donde escribe el usuario. Nuevamente te recomiendo crees una variable para esto.

**el:** Caja de texto para filtrar, puede ser una clase o un ID

```javascript
    let options = {
        numberPerPage:5,
        goBar:false, 
        pageCounter:false,
    };

    let filterOptions = {
        el:'#searchBox'
    };

    paginate.init('.myTable',options,filterOptions);
```
