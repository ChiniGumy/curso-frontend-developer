<style>
h1 {margin-top: 45px; color: #6C3483}
h2, h3 {margin-top: 45px; color: #3498DB}
</style>

# Motores de Renderizado
Nosotros escribimos toda la sintaxis, pero el navegador no lo entiende, para esto existen los motores de renderizado, que permiten transformar nuestro codigo a el lenguaje que el navegador entienda y tambien transformarlo a pixeles para que nosotros lo podamos ver.


## Los navegadores tienen motores: <br>
Chrome 	→  blink\
Edge 	→  Edge HTML\
Safari 	→  Webkit\
Firefox →  Gecko


## El navegador hace 5 pasos

1. Transformar HTML en objetos que puedan entender (DOM) - DOM = Document Object Model, mismo HTML transformado en objetos entendibles por el motor.

2. Coge cada estilo y los anade a cada elemento de los nodos.

3. Calcular dimensiones de cada nodo, donde van, su tamano.

4. Pintar las diferentes cajas.

5. Coger cada cosa pintada y tomar una foto, esa foto se renderizara el en navegador.


# Anatomia un documento HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Mi portafolio</title>
</head>
<body>
	<header></header>
	<nav></nav>
	<section></section>
	<footer></footer>
</body>
</html>
```
Head → fabicon (icono), titulo, enlaces que necesitemos para usar en el documento.

Body → Todo lo que vamos a mostrar en nuestra pagina.


# Anatomia de un elemento HTML

## Elemento

```html
<h1> Platzi </h1>
```

<kbd>\<etiqueta de apertura></kbd> <kbd>contenido</kbd> <kbd>\<etiqueta de cierre></kbd>


## Atributos

```html
<h1 class="title"> Platzi </h1>
```


## Anidamiento

```html
<section>
	<h1>Platzi</h1>
	<p>Tiene una comunidad</p>
	<ul>
		<li>increible</li>
		<li>Maravillosa</li>
		<li>Inigualable</li>
	</ul>
<section>
```

## Elementos Vacios

```html
<img src="dolly.png" alt="dolly">
```
No necesariamente tiene que tener una etiqueta de cierre.


# HTML Semantico

No siempre uses <kbd>\<div></kbd> , utiliza etiquetas adecuadas a nuestro codigo.

## Etiquetas con significado:

- Ayuda a tu sitio a ser accesible.
- Mejora tu pocisionamiento SEO.
- Codigo mas claro.


Si vamos a usar un navbar, usa la etiqueta nav.
si vamos a escribir una seccion, usa la etiqueta section. si vamos a escribir en el footer, usa la etiqueta footer.

### Lo que no se debe hacer:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>

	<div>
		<h1>Aqui deberia ir un header</h1>
	</div>
	
	<div>
		<ul>Aqui deberia ir un navbar</ul>
	</div>

	<div>
		<p>Aqui deberia ir un section</p>
	</div>

	<div>Aqui deberia ir un footer</div>

</body>
</html>
```


### Lo que se debe hacer:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>

	<header>
		<h1>Aqui hay un header</h1>
	</header>

	<nav>
		<ul>Aqui hay un navbar</ul>
	</nav>

	<section>
		<p>Aqui hay un section</p>
	</section>

	<footer>Aqui hay un footer</footer>

</body>
</html>
```

# Etiquetas mas usadas en HTML

## Layouts
Estructura principal de nuestro documento.

- <kbd>\<header>
- <kbd>\<nav>
- <kbd>\<section>
- <kbd>\<article>
- <kbd>\<aside>
- <kbd>\<footer

## Enlances
Podemos colocar enlaces para poder redigir a otras paginas.

- <kbd>\<a>

## Textos
Textos que se veran en la pagina.

- <kbd>\<h1>, \<h2>, \<h3>, \<h4>, \<h5>, \<h6>
- <kbd>\<p>
- <kbd>\<span>


## Imagenes y videos
Mostrar imagenes y videos en la pagina.

- <kbd>\<img>
- <kbd>\<svg>
- <kbd>\<iframe>
- <kbd>\<video>


## Formularios
Formularios de la pagina web.

- <kbd>\<form>
- <kbd>\<input>
- <kbd>\<label>
- <kbd>\<button>


## Listas
Listas

- <kbd>\<li>
- <kbd>\<ul>
- <kbd>\<ol>


## Codigo
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=, initial-scale=1.0">
	<title>Etiquetas</title>
</head>
<body>

	<nav>
		<ul>
			<li>About us</li>
			<li>Contact us</li>
		</ul>
	</nav>

	<section>
		<div>
			<img src="https://images.pexels.com/photos/617278/pexels-photo-617278.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" alt="Gato">
		</div>
		<div>
			<h1>Gatos</h1>
			<p>Los gatos son hermosos.</p>
		</div>
	</section>

	<form action="">
		<label for="name">Nombre del gato: </label>
		<input type="text" id="name">
	</form>
	<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Free V-Bucks</a>
</body>
</html>
```

## Documentacion de HTML
Aqui podremos encontrar todos las etiquetas de HTML: https://htmlreference.io/