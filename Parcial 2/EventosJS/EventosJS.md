
EventosJS
=============

#### **Brenda Yudsil Rivera Lopez**
#### **19100241**



### ¿Qué es Event Bubbling en JavaScript?

Básicamente, el Event Bubbling es una técnica en la que se llama a los controladores de eventos cuando un elemento está anidado en otro elemento y debe ser del mismo evento. Es similar a la encapsulación.

Cuando un evento ocurre en un elemento, este primero ejecuta los manejadores que tiene asignados, luego los manejadores de su padre, y así hasta otros ancestros.
Digamos que tenemos 3 elementos anidados FORM > DIV > P con un manejador en cada uno de ellos:
```
<style>
  body * {
    margin: 10px;
    border: 1px solid blue;
  }
</style>

<form onclick="alert('form')">FORM
  <div onclick="alert('div')">DIV
    <p onclick="alert('p')">P</p>
  </div>
</form>
```

Un clic en el elemento del interior p primero ejecuta onclick:
+ En ese p.
+ Luego en el div de arriba.
+ Luego en el form de más arriba.
+ Y así sucesivamente hasta el objeto document.

Así si hacemos clic en <, entonces veremos 3 alertas: p → div → form.

Este proceso se conoce como “propagación” porque los eventos “se propagan” desde el elemento más al interior, a través de los padres, como una burbuja en el agua.

### Captura de eventos
Hay otra fase en el procesamiento de eventos llamada “captura”. Es raro usarla en código real, pero a veces puede ser útil.

El estándar de eventos del DOM describe 3 fases de la propagación de eventos:

Fase de captura – el evento desciende al elemento.
Fase de objetivo – el evento alcanza al elemento.
Fase de propagación – el evento se propaga hacia arriba del elemento.
#### Captura y burbujeo de eventos #### 
![](https://images2.programmerclick.com/490/ea/eab193225307618e164cea62258d6f32.png) 

Se explica así: por un clic en td el evento va primero a través de la cadena de ancestros hacia el elemento (fase de captura), luego alcanza el objetivo y se desencadena ahí (fase de objetivo), y por último va hacia arriba (fase de propagación), ejecutando los manejadores en su camino.

Para atrapar un evento en la fase de captura, necesitamos preparar la opción capture como true en el manejador:
```
elem.addEventListener(..., {capture: true})
// o, solo "true" es una forma más corta de {capture: true}
elem.addEventListener(..., true)
```
Hay dos posibles valores para la opción capture:

Si es false (por defecto), entonces el manejador es preparado para la fase de propagación.
Si es true, entonces el manejador es preparado para la fase de captura.