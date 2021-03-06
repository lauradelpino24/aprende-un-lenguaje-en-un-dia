﻿# Aprende un lenguaje de programación en un día (ejercicio voluntario para subir nota).

## Introducción

Cuando te sacaste el carnet de conducir, aprendiste las normas de circulación así como los fundamentos básicos para manejar un coche: volante, marchas, freno, acelerador, embrague, retrovisores... Seguramente, el coche que conduces ahora es diferente al que utilizaste para aprender a conducir, no obstante, lo puedes llevar sin problema. Cada coche tiene sus peculiaridades, pero quien sabe manejar un automóvil, puede adaptarse a las medidas, tacto y comportamiento de un vehículo en cuestión de horas.

Aprender a programar es como aprender a conducir. Si tienes una base sólida de programación y sabes manejar con soltura los tipos de datos, bucles, arrays, clases, métodos, etc. podrás pasar de un lenguaje a otro en un período relativamente corto, simplemente tendrás que adaptarte a la sintaxis y a las peculiaridades del nuevo lenguaje.

Con este ejercicio se pretende despertar el interés por otros lenguajes de programación distintos al que el alumno está estudiando como primer lenguaje.

Sigue los pasos que se indican a continuación.

## Creación del equipo

Este ejercicio se debe hacer en grupos de 3 alumnos. Uno de ellos será el representante del grupo.

## Forkea forkea

El representante del grupo debe hacer un *fork* de este repositorio para utilizarlo como base.

## Añadiendo colaboradores

El encargado del grupo deberá añadir como colaboradores del repositorio *forkeado* a los otros dos miembros, para trabajar todos sobre los mismos archivos. Cuando alguien es colaborador en un repositorio, puede hacer *push* a él sin necesidad de pedir permiso o hacer *pull request*.

Para añadir colaboradores hay que hacer click en la pestaña *Settings* y seleccionar luego *Collaborators* en el menú.

## Miembros del grupo

Escribe aquí los miembros del grupo. El primero es el representante o encargado.

* Alvaro Campos Vega
* Laura del Pino Heredia
* Alejandro García Serrano

## Lenguaje de programación

El profesor llevará una cajita llena de papelitos con los nombres de distintos lenguajes de programación. Los encargados de cada grupo meterán la mano en la caja y sacarán dos papelitos, de los cuales el grupo elegirá uno. Se permite hacer intercambio de papelitos entre grupos.

Escribe el lenguaje de programación elegido por el grupo.

* Javascript

Los papelitos se han recortado de este [documento](lenguajes_de_programacion.pdf).

## Información sobre el lenguaje

JavaScript se diseñó con una sintaxis similar a C, aunque adopta nombres y convenciones del lenguaje de programación Java. Sin embargo, Java y JavaScript tienen semánticas y propósitos diferentes. 

Todos los navegadores modernos interpretan el código JavaScript integrado en las páginas web. Para interactuar con una página web se provee al lenguaje JavaScript de una implementación del Document Object Model (DOM). 

## Herramientas de desarrollo

Para la redacción de los comandos hemos usado el VisualCode Studio, y para su ejecución la consola de Google Chrome.

## Poniendo en práctica el lenguaje

Pon en práctica el lenguaje de programación realizando los siguientes ejercicios. Para cada uno de los ejercicios, pega el código fuente de la solución y una captura de pantalla.

### 1. ¡Hola mundo!

Realiza un programa que muestre por pantalla la frase **¡Hola mundo!**.

Creado el archivo HolaMundo.js

```javascript
console.log('Hola mundo');
```

![imagen hola mundo](/Imágenes/holamundo.png)

### 2. Pirámide

Dada una altura introducida por el usuario, realiza un programa que pinte una pirámide a base de asteriscos con la altura indicada.

Creado el archivo Piramide.js

```javascript
var altura = prompt("Dime la altura de la piramide: ");
document.write( altura );
    
var piso = 1;
var longitud = 1;
var espacios = altura-1;
var resultado = "";
      
while (piso <= altura) {
     
    for (var i = 1; i <= espacios; i++) {
        resultado += " ";
    }

    for (var i = 1; i <= longitud; i++) {
        resultado += "*";
    }

    console.log(resultado);
    resultado = "";
    piso++;
    espacios--;
    longitud += 2;
}
```

![imagen hola mundo](/Imágenes/peticionAltura.png)
![imagen hola mundo](/Imágenes/piramide.png)

### 3. Arrays y números aleatorios

Realiza un programa que rellene un array (o una estructura similar) con 20 números enteros aleatorios entre 1 y 100 y que seguidamente los muestre por pantalla. A continuación, se deben pasar los números primos a las primeras posiciones del array y los no primos a las posiciones restantes. Muestra finalmente el array resultado.

Creado el archivo arrays.js

```javascript
var num = [];
var resultado = "";

console.log('Array original: ');

for(var i = 0; i < 20; i++){
    num.push(Math.floor(Math.random()*100)+1);
    resultado += (num[i] + " ");
}

console.log(resultado);

console.log('Array ordenado: ');

resultado = "";

var esPrimo;

for(var i = 0; i < 20; i++){
    esPrimo = true;
    for (var j = 2; j < num[i]; j++) {
        if ((num[i] % j) == 0) {
            esPrimo = false;
        }
    }

    if (esPrimo) {
        resultado += num[i] + " ";
    }
}

for(var i = 0; i < 20; i++){
    esPrimo = true;
    for (var j = 2; j < num[i]; j++) {
        if ((num[i] % j) == 0) {
            esPrimo = false;
        }
    }

    if (!esPrimo) {
        resultado += (num[i] + " ");
    }
}

console.log(resultado);
```

![imagen hola mundo](/Imágenes/arrays.png)

## Presentación de resultados

Cada equipo explicará al resto de la clase lo aprendido durante la realización del ejercicio. Todos los miembros de cada equipo deben participar en la explicación. Se puede utilizar como material de base para la presentación el repositorio de GitHub.

## Recompensa

* Todos los alumnos que realicen correctamente la actividad tendrán 0'25 puntos extra en la nota del trimestre.

* Los miembros del equipo más votado ganarán un premio.

:star: Si te ha gustado este ejercicio, dale una estrellita al [repositorio original](https://github.com/LuisJoseSanchez/aprende-un-lenguaje-en-un-dia).

