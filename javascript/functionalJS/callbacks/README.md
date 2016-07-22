#Ejercicios de Callbacks

##Resumen

Javascript es un lenguaje en donde las funciones se denominan como `First class citizens` esto quiere decir que las podemos utilizar como lo harias con cualquier otro tipo de datos. Podemos pasarlas como argumentos a otras funciones o podemos asignarlas a variables.

Esta propiedad de las funciones en Javascript nos permite hacer cosas muy interesantes. Una de esas cosas se llaman funciones de alto nivel o `higher order functions`. Una funcion de alto nivel es simplente una funcion que recibe otra funcion como argumento. Esta otra funcion recibe el nombre de `callback` por que efectivamente la funciton de alto nivel va a decidir cuando llamarla despues.

Cuando estes creando aplicaciones de javascript te vas a dar cuenta de que hay callbacks por todos lados y que la mayor parte del tiempo estamos pasando funciones como argumetos a otras funciones. Es por esto que es de vital importancia entender como funciona este mecanismo.


##Pasos

###Paso 0:

Escribe una funcion `funcCaller` que reciba `callback` (una funcion) como primer argumento y `arg` (cualquier tipo de datos) como segundo argumento. `funcCaller` debe devolver `func` llamada con `arg`.


###Paso 1:

Escribe una funcion `firstVal` que recibe un arreglo `arr` como primer argumento y una funcion `callback` como segundo. Esta funcion debe devolver llamar a `callback` con el primer elmento de `arr`.


###Paso 2:

Escribe una funcion `once`, que recibe una funcion `callback` como primer argumento, y devuelve otra funcion que es una version del `callback` que solo puede ser invocada una vez. TIP: necesitas hacer un closure.

Por ejmemplo podriasmos usar `once` para evitar hacer un cargo a una tarjeta dos veces, como en el sigeuinte ejemplo:

  ```javascript
    var chargeCreditCard = function(num, price){
      //charges credit card for a certain price
    };
    var processPaymentOnce = once(chargeCreditCard);
    processPaymentOnce(123456789012, 200);
  ```



