# jPaginate
Plugin Jquery encontrado en la red para crear la paginación, es muy fácil de usar y ofrece varias ventajas, ya que puede paginar controles o grupo de controles. 

```html
<table>
<tbody id="example-1">
    <tr>        <td>1</td>        <td>5</td>        <td>Dispersado</td></tr>
    <tr>        <td>1</td>        <td>5</td>        <td>Dispersado</td></tr>
    <tr>        <td>1</td>        <td>5</td>        <td>Dispersado</td></tr>
    <tr>        <td>1</td>        <td>5</td>        <td>Dispersado</td></tr>
</tbody>
</table>
<div id="paginator1"></div>
```

## Usar


1. cargar el jQuery library en tu `<head>`:

  ```html
  <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.2/jquery.min.js"></script>
  ```

2. cargar el plugin, antes de cerrar el `<body>` .

  ```html
<script language="JavaScript" type="text/javascript" src="Assets/js/jpaginate.js"></script>
  ```

  1. Inicializa el plugin.

  ```javascript
  $("#example-1").jPaginate();
  ```

### Multiple instancia

Para poder usar mas de un JPaginate en un documento, se debe declarar la inicialización del plugin con los parametros más importantes: namecookies,tablecontent,basenumerador, los cuales identifican a cada uno, tal y como se puede ver en los ejemplos.

```javascript
$(document).ready(function()
{
    var parametros = {
            namecookies:"tabla",
            tablecontent:"example-1",
            basenumerador:"paginator1",
        };
    $("#example-1").jPaginate(parametros);

    $("#example-2").jPaginate({
            namecookies:"cards",
            tablecontent:"example-2",
            basenumerador:"paginator2",
    });
});
  ```

  ## Opciones

El plugin se puede inicializar con las distintas opciones:

Option             | Type    |  Default   | Description
:----------------- | ------- | :--------: | ------------------------------------
`pagination_class` | string  | pagination | La clase de estilos
`items`            | int     |     10     | Numero de items por página
`next`             | string  |    'Next'  | Lo que muestra en siguiente
`previous`         | string  | 'Previous' | Lo que muestra en previo
`inicial`          | string  |    'first' | Lo que muestra al inicio
`final`            | string  |    'end'   | Lo que muestra al final
`minimize`         | string  |    'false' | cuando muchas paginas se simplifica
`nav_items`        | int     |    '6'     | numero de botones
`cookies`          | boolean |   'trur'   | si trabaja con cookies
`namecookies`      | string  | 'current'  | el nombre de esa cookie
`tablecontent`     | string  | 'content'  | nombre del Id donde estan los items
`basenumerador`    | string  | 'paginator'| nombre del Id donde se muestra el paginador
`ocultarinicialfinal` | boolean | 'false' | Si se muestra o no los botones inicio y final


Un ejemplo con los paramtros pos default:

```javascript
$( '#example-1' ).jpaginate( {
            items: 10,
            next: "Next",
            previous: "Previous",
            inicial:"first",
            final:"end",
            active: "active",
            pagination_class: "pagination",
            minimize: false,
            nav_items: 6,
            cookies: true,
            namecookies:"current",
            tablecontent:"content",
            basenumerador:"paginator",
            ocultarinicialfinal:false,
  } );
```
