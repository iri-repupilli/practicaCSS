# Practica CSS
## Ejercitacion 1
1.	CSS son las siglas de hojas de estilo en cascada. Las hojas de estilo es una tecnología que permite controlar la apariencia de una pagina web. Además, describe como los elementos dispuestos en la pagina son presentados al usuario. Se pueden especificar estilos como el tamaño, fuentes, color, espaciado entre textos y recuadros, así como el lugar donde disponer texto e imágenes en la página.
Es importante aclarar que no es un lenguaje de programación sino un lenguaje de hojas de estilo que permite aplicarlos de manera selectiva a elementos en documentos HTML.
2.	Las reglas de CSS para dar estilo se componen de un selector y una declaración. El selector identifica el elemento HTML al que se aplica el estilo, y la declaración contiene la propiedad y el valor que definen el estilo. 
3.	Las 3 formas de dar estilo a un documento son: directamente a la marca, en el head de la pagina o agrupar las reglas de estilo en un archivo independiente con extensión *.css
4.	Los tipos de selectores CSS más utilizados son: 
Selector universal: Selecciona todos los elementos, por ejemplo: * { } 
- Selector de clase: Selecciona los elementos que tienen una clase determinada, por ejemplo: .box { } 
- Selector de ID: Selecciona el elemento que tiene un ID determinado, por ejemplo: #unique { } 
- Selector de atributo: Selecciona los elementos que tienen un atributo determinado, por ejemplo: a[title] { } 
- Selector de elemento: Selecciona todos los elementos HTML de un tipo determinado, por ejemplo: p
5.	Una pseudo-clase es una palabra clave que se añade a los selectores de CSS para definir un estilo específico a un elemento. Se utilizan para aplicar estilos cuando el elemento se encuentra en un estado determinado. 
Las pseudoclases más utilizadas para aplicar estilos a los vínculos son: 
•	:link: Selecciona los enlaces no visitados
•	:visited: Selecciona los enlaces visitados
•	:hover: Aplica un estilo cuando el usuario pasa el ratón sobre el enlace
Algunos ejemplos de uso de pseudoclases son: cambiar el estilo de un botón de gris a verde al pasar el ratón sobre él, mostrar los enlaces no visitados en azul, pero una vez visitados, se vuelven morados.
6.	La herencia es el proceso por el cual algunas propiedades CSS aplicadas a una etiqueta se pasan a las etiquetas anidadas. Si un elemento no tiene un valor en cascada para una determinada propiedad, puede heredar uno de un elemento antecesor. 
7.	El proceso denominado cascada CSS es el algoritmo que determina cómo se combinan los valores de propiedades de diferentes fuentes. Esto se hace para resolver conflictos entre reglas CSS que se aplican a un mismo elemento. 
¿Cómo funciona? El navegador interpreta la hoja de estilos CSS y resuelve los conflictos entre las declaraciones. Cada vez que se escribe una regla CSS, el navegador la coloca en la cascada. La regla que esté al principio de la cascada tiene más posibilidades de ser el estilo final. Se calcula el valor de especificidad de cada regla para determinar cuál prevalece. La regla que se aplica es la del selector de mayor especificidad. 
## Ejercicio 2
p#normal { <br/>
font-family: arial,helvetica; <br/>
font-size: 11px; <br/>
font-weight: bold; <br/>
} <br/>
*#destacado { <br/>
border-style: solid; <br/>
border-color: blue; <br/>
border-width: 2px; <br/>
} <br/>
#distinto { <br/>
background-color: #9EC7EB; <br/>
color: red; <br/>
} <br/>
<p id="normal">Este es un párrafo</p> 
<p id="destacado">Este es otro párrafo</p> 
<table id="destacado"><tr><td>Esta es una tabla</td></tr></table> 
<p id="distinto">Este es el último párrafo</p>
(ver el codigo)
El primer párrafo tiene como id “normal”, entonces el estilo que se le aplicara es el primero que hace referencia que es para párrafos (p) que tengan como id “normal” (#normal). La fuente será arial o helvética, el tamaño de 11px y estará en negrita. 
El segundo párrafo tiene como id “destacado”, entonces el estilo que se le aplicara es el segundo que hace referencia a todo lo que tenga id “destacado” (#destacado). Va a tener un borde solido, en color azul de 2px. 
La tabla tiene como id “destacado”, por lo tanto el estilo que se le aplicara es el segundo. Va a tener un borde solido, en color azul de 2px. 
El tercer párrafo tiene id=”distinto”, entonces el estilo que se le aplicara es el tercero ya que hace referencia a todo lo que tenga por id="distinto". Va a tener un fondo de color medio celestito y la letra será en color rojo.

## Ejercicio 3
p.quitar {
color: red; 
}
*.desarrollo { 
font-size: 8px; 
.importante { 
font-size: 20px; 
}
<p class="desarrollo"> 
En este primer párrafo trataremos lo siguiente: 
<br />xxxxxxxxxxxxxxxxxxxxxxxxx 
</p> 
<p class="quitar"> 
Este párrafo debe ser quitado de la obra… 
<br />xxxxxxxxxxxxxxxxxxxxxxxxx 
</p> 
<p > 
En este otro párrafo trataremos otro tema:<br /> 
xxxxxxxxxxxxxxxxxxxxxxxxx 
</p> 
<p class="importante"> 
Y este es el párrafo más importante de la obra… 
<br />xxxxxxxxxxxxxxxxxxxxxxxxx 
</ p> 
<h1 class="quitar">Este encabezado también debe ser quitado de la obra</h1> 
<p class="quitar importante">Se pueden aplicar varias clases a la vez</p>
(ver el codigo)
Otra forma de identificar es usar clases, como en este ejercicio. 
El primer párrafo tiene class=”desarrollo”, entonces el estilo que se le aplicara es el segundo ya que es aplicable a todo lo que tenga esa clase. Dice que tendrá una fuente de 8px. 
El segundo párrafo tiene class="quitar", entonces el estilo será el primero ya que es aplicable a párrafos (p) que tengan como clase quitar (.quitar). La fuente será en color rojo. 
El tercer párrafo tendrá un estilo predeterminado. 
El cuarto párrafo tiene class="importante", entonces el estilo será el tercero y tendrá una fuente de 20px. 
El titulo h1 se vera con el estilo predeterminado ya que aunque tenga class="quitar" el estilo relacionado para esa clase solo esta definido para párrafos.
El ultimo párrafo tiene class="quitar importante", por lo tanto se combinan dos estilos y se vera con fuente roja y de 20px. 

## Ejercicio 4 
Dadas las siguientes declaraciones: 
* {color:green; } <br/>
a:link {color:gray } <br/>
a:visited{color:blue } <br/>
a:hover {color:fuchsia } <br/>
a:active {color:red } <br/>
p {font-family: arial,helvetica;font-size: 10px;color:black; } <br/>
.contenido{font-size: 14px;font-weight: bold; } <br/>

Analizar los siguientes códigos y comparar sus efectos. Explicar:
<body> 
<p class="contenido" style="font-weight: normal;"> 
Este es un texto ...............</p> 
<table> 
<tr> 
<td>Y esta es una tabla.......</td> 
</tr> 
<tr> 
<td><a href="http://www.google.com.ar">con un 
enlace</a></td> 
</tr> 
</table> 
</body> 
(ver el codigo)
El primer párrafo aplicara los estilos desde lo mas general a lo mas especifico. Tomara el estilo p pero luego de .contenido tomara el tamaño de la fuente es la negrita y por ultimo del estilo definido en el elemento cambiara la negrita a normal. 
La primer celda de la tabla tendrá fuente verde, ya que el primer estilo se aplica a todo.
Luego en la segunda celda de la tabla hay un enlace, para esto hay varios estilos definidos. a:link indica que si el enlace aun no fue visitado se mostrara en color gris, a:visited indica que si ya fue visitado se mostrara en azul y a:active indica que si ponemos el mouse sobre el cambiara de color a fuchsia.
<body class="contenido"> 
<p> Este es un texto................</p> 
<table> 
<tr> 
<td>Y esta es una tabla.......</td> 
</tr> 
<tr> 
<td><a href="http://www.google.com.ar">con un enlace</a></td> 
</tr> 
</table> 
</body> 
(ver el codigo)
Al parrafo se le aplica el estilo p, la primer celda de la tabla va a tener el estilo .contenido ya que se encuenta dentro del body y no tiene un estilo mas especifico definido. Por ultimo, en la segunda celda de la tabla hay un enlace, para esto hay varios estilos definidos. a:link indica que si el enlace aun no fue visitado se mostrara en color gris, a:visited indica que si ya fue visitado se mostrara en azul y a:active indica que si ponemos el mouse sobre el cambiara de color a fuchsia.

## Ejercicio 5 
En cada caso, declarar una regla CSS que produzca el siguiente efecto: 
1.	Los textos enfatizados dentro de cualquier título deben ser rojos. <br/>
h1, h2, h3, h4, h5, h6 { color:red;}

2.	Cualquier elemento que tenga asignado el atributo "href" y que esté dentro de cualquier párrafo que a su vez esté dentro de un bloque debe ser color negro. <br/>
*p [href] {
  color: black;
}

3.	El texto de las listas no ordenadas que estén dentro del bloque identificado como “ultimo” debe ser amarillo pero si es un enlace a otra página debe ser azul. <br/>

#ultimo ul { color: yellow;} <br/>
#ultimo ul li a {color:blue; } <br/>
4.	Los elementos identificados como “importante” dentro de cualquier bloque deben ser verdes, pero si están dentro de un título deben ser rojos. <br/>
#importante {color:green;} <br/>
h1, h2, h3, h4, h5, h6 #importante {color:red} <br/>

5.	Todos los elementos h1 que especifique el atributo title, cualquiera que sea su valor, deben ser azules. <br/>
h1[title] {color:blue;}

6.	El color de los enlaces en las listas ordenadas debe ser azul para los enlaces aún no visitados, y violeta para los ya visitados y, además, no deben aparecer subrayados. <br/>

ol li a:link {color:blue; 
	        text-decoration: none;
} <br/>
ol li a:visited{color:violet; 
	         text-decoration: none;
}


## Ejercicio 6
(ver el codigo o los archivos subidos)
<!DOCTYPE html
  PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3c.org/TR/1999/REC-html401-19991224/loose.dtd">
<html lang="es">

<HEAD>
  <TITLE>Página Principal</TITLE>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="estilo2.css"> <!—cambio-- >
</HEAD>

<BODY>
  <DIV id=encabezado> <!—cambio-- >
    <H1>ASIGNATURA ELECTIVA</H1>
  </DIV>
  <DIV id=contenido>
    <H2>Contenido</H2>
    <p>En esta asignatura ...........................<BR></p>
    <P>El objetivo fundamental ..................</P>
    <P>etc., etc., ...........................................</P>
    <P>etc., etc., ...........................................</P>
    <P>Adem&aacute;s, ...........................................</P>
    <P>etc., etc., ...........................................</P>
    <P class="resaltado">Pero, lo más importante es ..............................</P>
    <P class="resaltado">etc., etc., ...........................................</P>
    <P>Y, entonces, podemos continuar con ..................</P>
    <P>etc., etc., ...........................................</P>
    <P>&nbsp;</P>
  </DIV>
  <DIV id=menu>
    <H3>Enlaces</H3>
    <UL class="vineta"> <!—cambio-- >
      <LI><A href="http://www.e-style.com.ar/moodle" target=_blank>Curso Actual</A>
      <LI><A href="http://www.e-style.com.ar/logica" target=_blank>Curso anterior</A> </LI>
      <LI><A href="http://www.e-style.com.ar/ntedu/consultas.htm" target=_blank>Contacto</A></LI>
    </UL>
  </DIV>
  <DIV id=pie class="estilopie">Ingeniería en Sistemas de Información - Universidad Tecnológica Nacional Rosario</DIV> <!—cambio-- >
  <p>&nbsp;</p>
</BODY>
