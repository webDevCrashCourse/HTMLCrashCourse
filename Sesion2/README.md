# Sesion 2

## Header y Body Tags

### Estructura basica de una pagina Web 

Una página web, se compone de un conjunto de elementos individuales que se combinan para dar forma a un documento completo a continuacion se muestra una estructura simple de una página web:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <p>This is my page</p>
  </body>
</html>
```

En esta estructura podemos identifica las siguentes secciones:

1. **```<!DOCTYPE html>```:** El doctype. En sus inicios, cuando el HTML llevaba poco tiempo (alrededor de 1991/2), los doctypes servían como enlaces al conjunto de reglas que la página HTML debía seguir para considerarse buen HTML, lo que podía significar comprobación automática de errores y otras funcionalidades  útiles. <br> <br> En la actualidad se ignora y se considera un legado histórico que hay que incluir para que todo funcione correctamente. ```<!DOCTYPE html>``` es la secuencia de caracteres mas corta se acepta como doctype válido y esto es lo único que realmente necesitas saber.

1. **```<html></html>```:** El elemento ```<html>```. Este elemento engloba todo el contenido de la página y es conocido en ocasiones como el elemento raíz.

1. **```<head></head>```:** El elemento ```<head>``` (cabecera). Este elemento actúa como contenedor para todos los parámetros que quieras incluir en el documento HTML que **NO SERÁ visible** a los visitantes de la página. Incluye cosas como palabras clave y la descripción de la página que quieras mostrar en los resultados de búsqueda, así como la hoja de estilo para formatear nuestro contenido, declaraciones de codificación de caracteres y más. Aprenderás más acerca de esto en el siguiente artículo de la serie.

1. **```<meta charset="utf-8">```:** Este elemento establece que tu documento HTML usará la codificación uft-8, que incluye la gran mayoría de caracteres de todos los lenguajes humanos conocidos. En resumen: puede tratar cualquier contenido de texto que pongas en tu documento. No hay razón para no configurarlo y puede te ayudar a evitar problemas más adelante.

1. **```<title></title>```:** Este elemento establece el título de tu página, que aparece en la pestaña/ventana de tu navegador cuando la página se carga y se utiliza para describir la página cuando la agregas a tus marcadores o la marcas como favorita.

1. **```<body></body>```:** El elemento ```<body>```. Contiene todo el contenido que quieres mostrar a los usuarios cuando visitan tu página, ya sea texto, imágenes, vídeos, juegos, pistas de audio reproducibles o cualquier otra cosa.


## Head (cabecera)

La cabecera HTML está contenida por el elemento ```<head>```— a diferencia del contenido del elemento ```<body>``` (el cual es mostrado en la página cargada por el navegador), el contenido de la cabecera no es mostrada en la pantalla de la página. En su lugar, el trabajo de la cabecera es contener metadatos acerca del documento. 

### Titulo

Ya hemos visto el elemento ```<title>``` en acción: se puede usar para agregar un título al documento. Sin embargo, esto puede confundirse con el elemento ```<h1>```, que se utiliza para agregar un encabezado en el nivel superior del cuerpo de tu contenido, esto también se conoce como el título de la página. 

* El elemento ```<h1>``` aparece en una pagina cuando es cargado por el navegador — generalmente esto sucede una sola vez por pagina, para marcar el titulo del contenido de tu pagina (el titulo de la historia, el titulo de noticias o cualquier cosa que sea apropiado para su uso).

* El elemento ```<title>``` es un metadato que representa el titulo de todo el documento HTML (no el contenido del documento).

### Metadatos

Los Metadatos son datos que describen datos, y HTML tiene una forma "oficial" de agregar metadatos a un documento---el elemento  ```<meta>```.

En el ejemplo que vimos arriba, esta linea fue incluida:

```html
<meta charset="utf-8">
```

Este elemento simplemente especifica la codificación de caracteres del documento: el conjunto de caracteres que el documento puede usar. utf-8 es un juego de caracteres universal que incluye prácticamente cualquier caracter de cualquier idioma humano.

Muchos elementos ```<meta>``` incluyen atributos name y content :

* name especifica el tipo de elemento que es; qué tipo de información contiene.
* content especifica el contenido meta real.

Dos de esos metaelementos que son útiles para incluir en tu página definen a l autor de la página  y proporcionan una descripción concisa de la página. Veamos un ejemplo:

```html
<meta name="author" content="Eduardo Pavon">
<meta name="description" content=" Web Dev Crash course es un curso pensado en proporcionar 
las herramientas basicas para iniciar tu carrera de desarrollador web.">
```

Especificar una autor es útil de varias maneras: es útil saber quién escribió una página, si desean contactarnos con preguntas sobre el contenido. Algunos sistemas de gestión de contenido tienen facilidades para extraer automáticamente la información del autor de la página y ponerla a disposición parar tales fines.

Espeficar una descripción que incluya palabras clave relacionadas con el contenido de tu página es útil ya que tiene el potencial de hacer de la página aparezca más arriba en las búsquedas relevantes realizadas en los motores de búsqueda.

### Favicon

Para un mayor enriquecimiento del diseño de tu sitio, puedes añadir referencias para personalizar iconos en tus metadatos, y estos se mostrarán en determinados contextos.

El favicon, fue el primer icono de este tipo, un icono de 16 x 16 pixel usado en múltiples sitios. El favicon puede ser añadido a tu página:

1. Guardándolo en el mismo directorio que la página index de tu sitio, guardada en el formato .ico (la mayoria de los buscadores soportarán favicons en los formatos más comunes como .gif o .png, pero usar el formato ICO asegurará que funcionará desde Internet Explorer 6.)

1. Añadiendo la siguiente línea en tu HTML ```<head>``` para referenciarlo:

```html	
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
```

### Aplicando CSS y JavaScript a HTML

la mayoria de los sitios o páginas web utilizan términos CSS para que brindar un aspecto visual, así como los términos JavaScript para potenciar las funcionalidades interactivas, como reproductores de video, mapas, juegos y demás. Estas son las aplicaciones más comunes para una página web, usando el elemento ```<link>``` y el elemento ```<script>``` respectivamente.

* El elemento ```<link>``` siempre va dentro del ```<head>``` del documento, acompañado de dos atributos: ```rel="stylesheet"```, que indica que es la hoja de estilo del documento, y ```href```, que contiene la ruta del archivo de la hoja de estilo:
```html
<link rel="stylesheet" href="my-css-file.css">
```

* El elemento ```<script>``` no tiene por qué ir en el ```<head>```. De hecho, a menudo es mejor colocarlo al final del ```<body>``` del documento (justo antes de la etiqueta de cierre ```</body>```), para asegurarnos que todo el contenido HTML se ha leido por el navegador antes de que intente aplicarle JavaScript (si JavaScript intenta acceder a un elemento que ya no existe, el navegador lanzará un error).

```html
<script src="my-js-file.js"></script>
```

## Body tag

El Elemento HTML ```<body>``` representa el contenido que será directamente visible de un documento HTML o pagina web. Sólo puede haber un elemento ```<body>``` en un documento.

Es en esta seccion en donde debemos definir la estructura y contenidos del documento.


```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Mi pagina de prueba</title>
  </head>
  <body>
    <!-- <p>Este es el contenido de la pagina</p> -->
    <h1>Titulo del contenido </h1>
  </body>
</html>
```

## Texto Fundamentos

Uno de los trabajos principales de HTML es dar estructura de texto y significado (también conocida como semántica), de forma que un navegador pueda mostrarlo correctamente. 

Los textos más estructurados están compuestos por títulos y párrafos, independientemente de si estás leyendo una historia, un periódico, un libro de texto, una revista, etc.

El contenido estructurado facilita la experiencia de lectura y se disfruta más.

En HTML, cada párrafo tiene que ser envuelto en un elemento ```<p>```, como este:

```html 
<p>yo soy un parrafo.</p> 
```
Cada título tiene que ser envuelto en un elemento de título:

```html
<h1>Yo soy el titulo de la historia.</h1>
```
Hay seis elementos de título — ```<h1>```, ```<h2>```, ```<h3>```, ```<h4>```, ```<h5>```, y ```<h6>```. Cada elemento representa un nivel diferente de contenido en el documento; ```<h1>``` representa el título principal, ```<h2>``` representa el subtítulo, ```<h3>``` representa el subtítulo del subtítulo, y demás.

### Listas

Existen diferentes tipo de listas:

* Inordenadas: se usan para marcar listas de artículos cuyo orden no es importante <br>Cada lista inordenada comienza con un elemento ```<ul>``` que envolvería todos los artículos de la lista, cada artículo de la lista con un elemento ```<li>``` (list item):

```html
<ul>
  <li>leche</li>
  <li>huevos</li>
  <li>pan</li>
  <li>hummus</li>
</ul>
```
El resultado seria: 

<ul>
  <li>leche</li>
  <li>huevos</li>
  <li>pan</li>
  <li>hummus</li>
</ul>

* Ordenadas: se usan para marcar listas de artículos cuyo orden importa <br> la estructura de la lista es similar a la de la lista inordenada a excepcion de que la lista se envuelve el un elemento ```<ol>``` :

```html
<ol>
  <li>llegar al final de la calle</li>
  <li>Dar vuelta a la derecha</li>
  <li>Atravezar las siguientes dos rotondas</li>
  <li>dar vuelta a la izquierda en la tercera rotonda</li>
  <li>La escuela esta a 300 metros a la derecha</li>
</ol>
``` 
<ol>
  <li>llegar al final de la calle</li>
  <li>Dar vuelta a la derecha</li>
  <li>Atravezar las siguientes dos rotondas</li>
  <li>dar vuelta a la izquierda en la tercera rotonda</li>
  <li>La escuela esta a 300 metros a la derecha</li>
</ol>


### Enfasis e Importancia

en HTML usamos el elemento ```<em>``` para brindar enfasis a algunas palabras y cambiar ligeramente su significado, los navegadores colocan la palabra rodead en la etiqueta ```<em>``` en italicas, sin embargo no debe usarse el elemento solo para obtener esta estilizacion ya que esta puede obtenerse por medio de un elemento  ```<span>``` con estilos CSS  o con el elemento ```<i>```.

```html
<p>Estoy <em>contento</em> de que no hayas llegado <em>tarde</em>.</p>
```
<p>Estoy <em>contetento</em> de que no hayas llegado <em>tarde</em>.</p>


Para enfatizar palabras importantes en el lenguaje escrito usualmente la colocamos en **Negritas**, para hacer esto en HTML utilizamos el elemento ```<strong>``` 

```html
<p>Este liquido es <strong>Altamente toxico</strong>.</p>
```
<p>Este liquido es <strong>Altamente toxico</strong>.</p>


Ademas de estos elementos de enfasis e importancia tambien tenemos:

* ```<i>``` se usa para convenir significados tradicionalmente indicados por italicas: palabras extranjeras, designaciones taxonomicas, terminos tecnicos, pensamientos...
* ```<b>``` se usa para convenir significados tradicionalmente indicados por negritas: palabras clave, nombres de productos, enunciados principales...
* ```<u>``` se usa para convenir significados tradicionalmente indicados por subrayados: Nombres propios, errores de ortografia...




## Hyperlinks

Los hyperlinks o hipervinculos permiten enlazar nuestros documentos a cualquier otro documento (o recurso), hacer referencia a partes específicas de los mismos, podemos hacer las aplicaciones accesibles con una sencilla dirección web. Cualquier contenido web puede ser convertido en un link, para que al pulsarlo (lo activemos) el navegador se dirija a la dirección web a la que apunte el link. (URL.)

Una URL(uniform resouce locator) puede apuntar a ficheros HTML, ficheros de texto, imágenes, documentos de texto, archivos de audio o video, y cualquier otra cosa que pueda ser mostrada en la Web. Si el navegador no sabe cómo manejar el archivo, nos preguntará si lo queremos abrir (en cuyo caso la tarea de abrirlo y manejarlo será transferida a la aplicación nativa instalada en el dispositivo) o lo queremos descargar (en cuyo caso puedes ocuparnos de él más tarde).

Un link básico se crea incluyendo el texto (o cualquier otro contenido Block level links) que deseemos convertir en un link dentro de un elemento ancla ```<a>```, dándole un atributo href (también conocido como target - objetivo) que contendrá la dirección web hacia dónde deseemos que apunte el link.

```html
<p>I'm creating a link to
<a href="https://www.mozilla.org/en-US/">the Mozilla homepage</a>.
</p>
```
Este código producirá el siguiente resultado:

<p>I'm creating a link to
<a href="https://www.mozilla.org/en-US/">the Mozilla homepage</a>.
</p>

### Titulo del link

Otro atributo que podemos añadir a los links es el título (title); este ha sido concebido para proporcionar información útil sobre el destino, como el tipo de información que contiene la página, o cosas a tener en cuenta sobre el mismo. Por ejemplo:

```html
<p>I'm creating a link to
<a href="https://www.mozilla.org/en-US/"
   title="The best place to find more information about Mozilla's
          mission and how to contribute">the Mozilla homepage</a>.
</p>
```
Esté código producirá el siguiente resultado (el título se mostrará al pasar el ratón sobre el texto del link):

<p>I'm creating a link to
<a href="https://www.mozilla.org/en-US/"
   title="The best place to find more information about Mozilla's
          mission and how to contribute">the Mozilla homepage</a>.
</p>

Como hemos mencionado anteriormente, puedes convertir cualquier contenido en un link, incluso los bloques de contenido block level elements. Si dispones de una imagen que desees convertirla en un link, simplemente ánclala entre elementos ```<a></a>```.

```html
<a href="https://github.com">
  <img src="imagenes/Octocat.png" alt="The world's leading software development platform">
</a>
```

<a href="https://github.com">
  <img src="imagenes/Octocat.png" alt="The world's leading software development platform" width="100" >
</a>

### Rutas

Una URL (de las iniciales en inglés Uniform Resource Locator - localizador de recursos estandarizado) es simplemente una secuencia de caracteres de texto que definen donde está situado algo en la web. Por ejemplo la página de Mozilla en inglés está ubicada en https://www.mozilla.org/en-US/.

Las URLs utilizan las referencias para encontrar los archivos. Las referencias especifican donde se encuentra el archivo que buscas dentro del sistema de archivos. 

