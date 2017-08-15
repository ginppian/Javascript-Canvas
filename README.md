Canvas 
=====

<p align="center">
	<img src="https://github.com/ginppian/Javascript-Canvas/blob/master/imgs/img1.png" width="681" height="340">
</p>

## Descripción

<p align="justify">
	Debído a que estamos trabajando con los Google Maps Web, queremos hacer uso de <i>MARKS</i> personalizados. Para hacer ésto usamos <i>CANVAS</i>.
</p>

<p align="justify">
	Según <a href="https://es.wikipedia.org/wiki/Canvas_(HTML)">wikipedia</a> <i>"Canvas (o lienzo traducido al español) es un elemento HTML incorporado en HTML5 que permite la generación de gráficos dinámicamente por medio del scripting. Entre otras cosas, permite la renderización interpretada dinámica de gráficos 2D y mapas de bits, asi como animaciones con estos gráficos. Se trata de un modelo de procedimiento de bajo nivel, que actualiza un mapa de bits y no tiene una gráfica de escena integrada."</i>
</p>

<p align="justify">
	<i>CANVAS</i> en ingles significa <i>LIENZO</i> y efectivamente como los pintores nos otros hacemos uso de un lienzo el cual lo indicamos en nuestro <i>HTML</i> especificando <i>ANCHO</i> y <i>ALTO</i>, entonces empezamos a pintar.
</p>

## Desarrollo

<p align="justify">
	Hay varios diferentes tipos dibujar lineas en <i>CANVAS</i> podemos dibujar lineas rectas, curvas, o curvas de Bezier. Para nuestro ejemplo básta con lineas rectas, para más información podemos consultar <a href="https://developer.mozilla.org/es/docs/Web/Guide/HTML/Canvas_tutorial/Dibujando_formas">aquí</a>
</p>

<ol>
	<li>
		Primer paso es dibujar nuestro diseño a papel y lápiz.
		<p align="center">
			<img src="https://github.com/ginppian/Javascript-Canvas/blob/master/imgs/img2.jpg" width="504" height="378">
		</p>
	</li>
	<li>
		En nuestro código
	</li>
</ol>

* HTML

```html
<p align="center">
  <canvas id="myCanvas" width="400" height="400">
</p>
```

* CSS

```css
#myCanvas{
  border:5px
  solid #d3d3d3;
}
```

* Javascript-Canvas

```javascript
var c = document.getElementById("myCanvas");
if(c.getContext){
  var s = 5;
  var ctx = c.getContext("2d");
  ctx.fillStyle = "rgba(230,2,25,1)";
  ctx.beginPath();
  ctx.moveTo(35*s,35*s);//Init
  ctx.lineTo(45*s,25*s);//A
  ctx.lineTo(45*s,15*s);//B 
  ctx.lineTo(35*s,5*s);//C 
  ctx.lineTo(35*s,5*s);//D
  ctx.lineTo(20*s,5*s);//E 
  ctx.lineTo(10*s,15*s);//F 
  ctx.lineTo(10*s,25*s);//G
  ctx.lineTo(20*s,35*s);//H 
  ctx.lineTo(23*s,35*s);//I 
  ctx.lineTo(27.5*s,70*s);//J
  ctx.lineTo(32*s,35*s);//K 
  ctx.fill(); 
  ctx.closePath();
  ctx.stroke();
  
  ctx.fillStyle = "rgba(0,0,0,1)";
  ctx.font = "89px Helvetica";
  ctx.fillText("1",22*s,20.5*s);
  
  ctx.font = "21px Helvetica";
  ctx.fillText("11/08/2017",17*s,26.5*s);
  ctx.fillText("08:34",21.5*s,31.5*s);
  
}
```

<p align="justify">
	Aquí obtenemos el elemento <i>CANVAS</i> generamos un <i>CONTEXTO</i> (el contexto indicamos la dimención 2D o 3D). Si podemos obtener un contexto, módificamos a que sea <i>2D</i> a continuación cambiamos el color a rojo, y empezamos a dibujar indicando lo con <i>beginPath</i>, movemos la pluma a las coordenadas <i>(35,35)</i> y empezamos a dibujar. Copiamos todos nuestros puntos que habíamos hecho en nuestro <i>BOCETO</i> anterior y la propiedad <i>S</i> indica que es un <i>ESCALAR</i> es decir si queremos que la figura sea más grande o pequeña.
</p>

<p align="justify">Ya para finalizar hacemos <i>FILL</i> para rellenar y <i>STROKE</i> para marcar el contorno.</p>
<p align="justify">Como queremos agregar texto, modificamos el color a <i>NEGRO</i> le asignamos un tipo de letra, y a continuación agregamos el texto, pasando le una coordenada para ajustar éste a nuestro diseño.</p>

<p align="center">
	<img src="https://github.com/ginppian/Javascript-Canvas/blob/master/imgs/img3.png" width="263" height="351">
</p>


## Demo

<a href="https://codepen.io/guitarrkurt/pen/YxENmE">Live</a>

## Fuente

* <a href="https://gist.github.com/viktorkelemen/1451945/cb94c2aa2d24d60209a896506c438f8e754d08dd">Custom canvas google maps marker</a>
* <a href="https://paul.kinlan.me/using-canvas-to-create-beautiful-custom-marke/">Using Canvas to create beautiful custom markers in Google Maps</a>
* <a href="https://stackoverflow.com/questions/2436484/how-can-i-create-numbered-map-markers-in-google-maps-v3">How can I create numbered map markers in Google Maps V3?</a>
* <a href="http://js-bits.blogspot.mx/2010/07/canvas-rounded-corner-rectangles.html">JavaScript Bits</a>
* <a href="https://developer.mozilla.org/es/docs/Web/Guide/HTML/Canvas_tutorial/Dibujando_formas">Dibujando formas con canvas</a>
* <a href="https://www.w3schools.com/tags/canvas_fill.asp">HTML canvas fill() Method</a>
* <a href="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_canvas_tut_path">html5_canvas_tut_path</a>
* <a href="https://stackoverflow.com/questions/12449904/how-to-use-the-helvetica-neue-bold-condensed-in-the-html5-canvas">How to use the “Helvetica Neue Bold Condensed” in the HTML5 Canvas</a>

