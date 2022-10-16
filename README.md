# Portfolio Práctica1
Para hacer la página web de los cuadros de Velázquez, he dividido la estructura en 4 divs principalmente, el titulo o cabecera, el menu de las imagenes para seleccionar el cuadro que quisieramos ver, el propio cuadro y la zona donde se encontraba la explicación de cada cuadro, precio, año y tamaño.

## HTML
Para el HTML no hay mucho que explicar, unicamente la estructura que dependia de las imagenes y de las clases o ids para que conectara con CSS y JS, también para que funcionaran los tipos de letras he tenido que añadir unos links, y dos scripts, uno para CSS y otro para JS
```
    <link rel="stylesheet" href="styles.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@200;700&display=swap" rel="stylesheet">
    <script src="/js/jquery-3.6.0.js"></script>
```

## CSS

### 1. Menú
Para hacer el menú de las imágenes he metido un div  con todas las imágenes y unicamente le he dado el tamaño que queria, además con el overflow he hecho que no salgan todas y puedas elegir cual ver, además las fotos son en blanco y negro y cuando se acerca el raton con el hover se colorean con una transición. 
```
#Menu{
text-align: center;
margin-top: 10px;
width: 200px ;
height: 540px;
overflow-y: auto;

.miniatura{
    width: 150px;
    height: 180px;
    transition: 1s;
    filter: grayscale(100%);
}

.miniatura:hover{
    filter: grayscale(0%);
}
```
### 2. Cabecera
El título también se encontraba en un div y le he puesto la letra Monserrat 
```
header{
    height: 100px;
    width: auto;
    text-align: center;
}

.titulo{
    font-family: 'Montserrat', sans-serif;
    font-size: xx-large;
}
```
### 3. Cuadro
Para el cuadro unicamente he dado forma al div y ya dependiendo de cada cuadro he puesto unas caracteristicas u otras
```
.cuadro{
    text-align: center;
    margin: 203px;
    margin-top: -575px;
    width: 510px;
    height: 600px;
}
```

### 4. Descripción
Ya para terminar he escrito las características de cada cuadro y a cada párrafo le he puesto el tamaño y tipo de letra que se pedía
```
.texto{
    text-align: center;
    margin-left: 50%;
    margin-top: -780px;
    width: auto ;
    height: 570px;
}

.titulo_c{
    font-family: 'Montserrat', sans-serif;
    font-size: xxx-large;
    margin-top:250px;
}
.precio_c{
    font-family: 'Montserrat', sans-serif;
    font-size: large;
}
.descripcion_c{
    font-family: 'Montserrat', sans-serif;
    font-size: large;
}
.fecha_c{
    font-family: 'Montserrat', sans-serif;
    font-size: large;
}
```

## JavaScript
Para terminar el .js es el que me ha sido mas dificil, he intentado hacer que sea todo en la misma página pero al no  he tenido qye crear mas index y conectarlas entre ellas
```
let imgchange = document.getElementById("imgchange");
let breda = document.getElementById("breda");
let inocencio = document.getElementById("inocencio");
let meninas = document.getElementById("meninas");
let vulcano = document.getElementById("vulcano");
let venus = document.getElementById("venus");

breda.onclick = function() {
    imgchange.src = "img/breda.jpg"
}
inocencio.onclick = function() {
    imgchange.src = "img/inocencio.jpg"
}
meninas.onclick = function() {
    imgchange.src = "img/meninas.jpg"
}
vulcano.onclick = function() {
    imgchange.src = "img/vulcano.jpg"
}
venus.onclick = function() {
    imgchange.src = "img/venus.jpg"
}
```

#### Luis Rebollo Castellanos 2ºASIR