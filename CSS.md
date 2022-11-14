<style>
h1 {margin-top: 45px; color: #6C3483}
h2, h3 {margin-top: 45px; color: #3498DB}
</style>


# Selectores basicos en CSS

De Tipo → <kbd> div {...} </kbd>

De Clase → <kbd> .elemento {...} </kbd>

De ID → <kbd> #id-del-elemento </kbd>

De Atributo → <kbd> a[href="..."] {...} </kbd>

Universal → <kbd> * {...} </kbd>


# Pseudoclases y Pseudoelementos

## Pseudoclases
<kbd>:pseudoclase</kbd> 1 dos puntos

- <kbd>:active</kbd>
- <kbd>:focus</kbd>
- <kbd>:hover</kbd>
- <kbd>:nth-child(n)</kbd>

## Pseudoelementos
<kbd>::pseudoelemento</kbd> 2 dos punto

- <kbd>::after</kbd>
- <kbd>::before</kbd>
- <kbd>::first-letter</kbd>
- <kbd>::placeholder</kbd>


# Especificidad

## Valores de especificidad

```
1 0 0 0 0 	!important (!important)

  1 0 0 0 	Estilos en linea (<style color="tomato">)

    1 0 0	#ID ( #boton-enviar )

      1 0   Clases, Atributos y PseudoClases ( .clase , font-color , :pseudoclase )

	    1   Elementos y PseudoElementos ( p , ::pseudoelementos)

		0	Selector universal ( * {...} )

```

```

#ID h1::first-letter		( ID[#] + Elemento[h1] + Pseudoelemento[::] )

	1 0 0 	#ID
	    1 	h1
	    1 	::first-letter
	-----
	1 0 2	!Mas Especifico!


p .sidemenu div:hover		( Elemento[p] + Clase[.sidemenu] + Elemento + Pseudoclase[:])

	    1 	p
	  1 0   .sidemenu
	    1   div
	  1 0   :hover
    -----
	  2 2   Menos Especifico :(

```

# Tipos de display mas usados: block, inline e inline-block

- block
- inline
- inline-block


# Flexbox

https://css-tricks.com/snippets/css/complete-guide-grid/


# Modelo de caja

<kbd>Margin</kbd> → Generar espacio entre los otros elementos.

<kbd>Border</kbd> → Borde.

<kbd>Padding</kbd> → Margen interna entre el borde y el contenido.

<kbd>Content</kbd> → El contenido al cual le podemos modificar el height y width.


# Colapso de imagenes



# Pocisionamiento en CSS

<kbd>relative</kbd> → Alinear nuestros elementos y tener nuestros elementos internos con position: relative, para que se puedan mover al rededor del container.

<kbd>absolute</kbd> → Al decirle que sea absouluto, indica que su espacio en donde se va a mover, sera solo en el container.

<kbd>fixed</kbd> → Se nos quedara fijo en la pantalla en donde nosotros indiquemos. El uso mas comun es como navbar, osea arriba.

<kbd>sticky</kbd> → Esto hara que cada que llegue a cierto punto, se quedara pegado.

<kbd>static</kbd> → No dio ejemplo xd.

<kbd>initial</kbd> → No dio ejemplo xd.

<kbd>inherit</kbd> → No dio ejemplo xd.


# Index y el contexto de apilamiento

Al cambiar el orden de los elementos de HTML, uno estaria encima del otro, entonces el orden de los elementos de HTML si importa en el eje Z


# Propiedades de CSS mas usadas

## Layout
<kbd>display</kbd>

## Textos
<kbd>font-size</kbd>

<kbd>font-weight</kbd>

<kbd>font-family</kbd>

<kbd>text-align</kbd>

<kbd>color</kbd>

## Modelo de Cajas

<kbd>margin</kbd>

<kbd>padding</kbd>

<kbd>border</kbd>

## Colores de fondo

<kbd>background-color</kbd>

## Tamanos

<kbd>width</kbd>

<kbd>height</kbd>


# Tipos de medidas

## Absolutas
* px
* pt
* pc
* in
* cm
* mm

## Relativos
* rem
* em
* vw
* vh
* vmin
* vmax
* ex
* ch


# Diseno Responsive

Media queries 

```css
@media screen { max-width: 375px;
	.clase{
		propiedad: valor;
	}
}
```


# Arquitecturas CSS

**objetivos:** ser predecible, reutilizable, mantenible, escalable.

**buenas practicas:** lineamentos, documentacion, estandares, componentes


# OOCSS, BEM, SMACSS, ITCSS Y ATOMIC DESIGN

## oocss

Separar la estructura y la piel

	objeto: estructura base

	mascara: elementos visuales iguales

## bem

Bloque - Elemento - Modificador

```elemento--modificador--bloque```


## smacss

base + layout + module + state + theme


## itcss

1. ajustes
1. herramientas
1. generico
1. elementos
1. objetos
1. comopnentes
1. utilidades


## Atomica Design

atomos = input, boton.

moleculas = grupo de atomos, input y boton.

organismos = varios, como un formulario.