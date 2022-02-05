Modelo de caja
=============

#### **Brenda Yudsil Rivera Lopez**
#### **19100241**

<div style="text-align: justify">
El modelo de cajas o "box model" es seguramente la característica más importante del lenguaje de hojas de estilos CSS, ya que condiciona el diseño de todas las páginas web. El modelo de cajas es el comportamiento de CSS que hace que todos los elementos de las páginas se representen mediante cajas rectangulares.

Las cajas de una página se crean automáticamente. Cada vez que se inserta una etiqueta HTML, se crea una nueva caja rectangular que encierra los contenidos de ese elemento. La siguiente imagen muestra las tres cajas rectangulares que crean las tres etiquetas HTML que incluye la página: 


![](https://uniwebsidad.com/static/libros/imagenes/css/f0402.gif "Las cajas se crean automáticamente al definir cada elemento HTML")

 
El modelo de cajas CSS completo se aplica a cajas que presentan comportamiento en bloque; las cajas con comportamiento en línea solo usan una parte del comportamiento definido en el modelo de cajas. El modelo define cómo funcionan juntas las diferentes partes de una caja (margen, borde, relleno y contenido) para crear una caja que puedas ver en tu página

## Partes de una caja
Al hacer una caja de tipo bloque en CSS tenemos los elementos siguientes:
+ **El contenido de la caja (o content box)**: El área donde se muestra el contenido, cuyo tamaño puede cambiarse utilizando propiedades como width y height.
+ **El relleno de la caja (o padding box)**: El relleno es espacio en blanco alrededor del contenido; es posible controlar su tamaño usando la propiedad padding y otras propiedades relacionadas.
+ **El borde de la caja (o border box)**: El borde de la caja envuelve el contenido y el de relleno. Es posible controlar su tamaño y estilo utilizando la propiedad border y otras propiedades relacionadas.
+ **El margen de la caja (o margin box)**: El margen es la capa más externa. Envuelve el contenido, el relleno y el borde como espacio en blanco entre la caja y otros elementos. Es posible controlar su tamaño usando la propiedad margin y otras propiedades relacionadas.

El diagrama siguiente muestra estas capas:

![](https://media.prod.mdn.mozit.cloud/attachments/2019/03/19/16558/29c6fe062e42a327fb549a081bc56632/box-model.png)

El relleno y el margen son transparentes, por lo que en el espacio ocupado por el relleno se muestra el color o imagen de fondo (si están definidos) y en el espacio ocupado por el margen se muestra el color o imagen de fondo de su elemento padre (si están definidos). Si ningún elemento padre tiene definido un color o imagen de fondo, se muestra el color o imagen de fondo de la propia página (si están definidos).

Fuentes:
- [1.MDN WEB DOCS](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/The_box_model)
- [2. uniwebsidad](https://uniwebsidad.com/libros/css/capitulo-4)