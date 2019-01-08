Librería ligera en vanilla javascript para crear paginación y filtros sobre tablas.
Con unas configuraciones mínimas puedes tener una paginación increíble.

### DEMO



### Uso basico

Puedes indicar que es una `clase` o un `id` ambos son validos.

```javascript
paginate.init('.myTable');
```

**Resultado;**

[![](https://i.imgur.com/v5vfjPZ.png)](https://i.imgur.com/v5vfjPZ.png)

### Opciones

Puedes establecer algunas opciones en el segundo parámetro como son;

-         **numberPerPage: **Cantidad de filas por pagina
-         **goBar:** Barra donde puedes digitar el numero de la pagina al que quiere ir
-         **pageCounter:** Contador de paginas, en cual estas, de cuantas paginas

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

[![](https://i.imgur.com/CPRiiN2.png)](https://i.imgur.com/CPRiiN2.png)

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
