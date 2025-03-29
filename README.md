# **#7DaysOfCode** :rocket:

+ [Día 1: Comparación de valores](#día-1-comparación-de-valores-en-javascript)
+ [Día 2: Variables](#día-2-variables)

---

## Día 1: Comparación de valores

Este primer día es muy importante. Al final de él, tendrás un nuevo conocimiento que es esencial para los próximos desafíos.

Existe una situación muy común para quienes usan **JavaScript**: problemas con los **tipos de variables** al comparar los valores de dos variables entre sí. ¡A mí me ha pasado mucho!

En lenguajes de programación compilados, como **Java** y **C#**, este problema se detecta en tiempo de compilación, y tienes un aviso claro del error mientras desarrollas el código.

En **JavaScript**, estos errores pasan desapercibidos, ya que el código no pasa por un compilador. Es decir, los errores solo aparecen en **tiempo de ejecución**.

La parte más confusa para quienes están comenzando a aprender lógica con JavaScript es la operación de **igualdad entre valores**. Dependiendo de cómo escribas tu código, JavaScript hará una **conversión de tipo** a un tipo booleano de manera **implícita** (automática), y esto afectará a variables que eran `String`, `Number`, `Object`, etc.

Esto causa algunos comportamientos extraños, como estos ejemplos que retornan `true`:

```javascript
console.log( false == '0' );
console.log( null == undefined );
console.log( " \t\r\n" == 0 );
console.log( ' ' == 0 );
```

Lo cual no tiene necesariamente mucho sentido. 🤯

Puedes probar todo esto yendo a tu navegador, haciendo clic con el botón derecho, eligiendo la opción **“Inspeccionar”** y accediendo a la pestaña **“Consola”**.  
En esa pestaña, basta con copiar y pegar cada una de las líneas anteriores para confirmar que todas realmente retornan `true`.

---

### 🚀 Desafío

Tu tarea de hoy es reescribir el siguiente código para que imprima la información de manera correcta, tenga sentido y no contenga errores:

```javascript
let numeroUn = 1;
let stringUn = '1';

let numeroTreinta = 30;
let stringTreinta = '30';

let numeroDiez = 10;
let stringDiez = '10';

if (COMPARAR numeroUn y stringUn) {
  console.log('Las variables numeroUn y stringUn tienen el mismo valor, pero tipos diferentes');
} else {
  console.log('Las variables numeroUn y stringUn no tienen el mismo valor');
}

if (COMPARAR numeroTreinta y stringTreinta) {
  console.log('Las variables numeroTreinta y stringTreinta tienen el mismo valor y el mismo tipo');
} else {
  console.log('Las variables numeroTreinta y stringTreinta no tienen el mismo tipo');
}

if (COMPARAR numeroDiez y stringDiez) {
  console.log('Las variables numeroDiez y stringDiez tienen el mismo valor, pero tipos diferentes');
} else {
  console.log('Las variables numeroDiez y stringDiez no tienen el mismo valor');
}
```

---

### 💡 Consejo

También puedes utilizar el **navegador** para ejecutar este programa si aún no tienes familiaridad con editores de código como **Visual Studio Code**.

Para hacerlo, como mencioné antes, basta con hacer clic con el botón derecho del mouse en cualquier página, seleccionar la opción **“Inspeccionar”**, ir a la pestaña **“Consola”** y escribir tu código. ¡Muy simple, verdad? 😊

Si deseas cambiar los nombres de las variables y los valores, **siéntete libre de hacerlo**.  
Pero **nunca imprimas algo que no sea verdadero**, ¿eh? 😉

✅ [***Solución***](./day-1.html) 👈

[🔝 Índice](#7daysofcode-rocket)

---

## Día 2: Variables

¿Sabes cuando te registras en un site y, justo después, al iniciar sesión, te llama por tu nombre? Eso es lo que harás en el desafío de hoy.

Cuando creas un sistema, sitio o aplicación, es común querer agregar algunos toques personalizados para hacer la experiencia en tu aplicación más rica y dinámica.

Hacer esto mediante programación puede no ser una tarea fácil. Dependiendo del nivel de personalización que quieras implementar, la cantidad de código que necesitarás escribir puede ser inmensa.

Pero, por supuesto, puedes comenzar de una manera más sencilla. Para ello, lo importante es entender cómo capturar y almacenar valores dentro de variables. ¡Y en eso te voy a ayudar hoy!

Las variables son los bloques básicos de construcción de cualquier sistema y son esenciales para procesar cualquier tipo de información, ya sea de una persona que ha iniciado sesión en el sistema o incluso para mostrar detalles de productos en un catálogo de comercio electrónico.

### 🚀 Desafío
Por eso, hoy te voy a enseñar a desarrollar un programa simulando una de esas aplicaciones. Debe pedir al usuario responder 3 preguntas:

- **¿Cuál es tu nombre?**  
- **¿Cuántos años tienes?**  
- **¿Qué lenguaje de programación estás estudiando?**  

A medida que se hagan las preguntas, la persona que esté usando el programa debe responder cada una de ellas.

Al final, el sistema mostrará el mensaje:

> **"Hola [nombre], tienes [edad] años y ya estás aprendiendo [lenguaje]!"**

Observa que cada información entre `[]` es una de las respuestas dadas por la persona.

---

### ✨ Ejercicio opcional

Si deseas profundizar en el tema de hoy, tengo otro ejercicio para ti.  
Pero es **100% opcional**.

Vas a complementar el código para que, después de mostrar el mensaje anterior, el programa pregunte:

> **¿Te gusta estudiar [lenguaje]? Responde con el número 1 para SÍ o 2 para NO.**

Y luego, dependiendo de la respuesta, debería mostrar uno de los siguientes mensajes:

- `1` → **¡Muy bien! Sigue estudiando y tendrás mucho éxito.**  
- `2` → **Oh, qué pena... ¿Ya intentaste aprender otros lenguajes?**  

---

### 💡 Consejo

Puedes agregar tantas preguntas como desees y aprovechar las respuestas de los usuarios en el mensaje que se mostrará.

Para imprimir y recibir valores, puedes usar tanto `console.log`, `prompt` y `alert`, como también **HTML y CSS** si ya tienes conocimiento en estas dos tecnologías.

Puedes usar la estructura condicional `if` para resolver el **Ejercicio Opcional**. Algo como:

```javascript
if (respuesta == 1) {
    // da la respuesta positiva
}

if (respuesta == 2) {
    // da la respuesta negativa
}
```

---

### 🔍 Extra

Tanto `alert()` como `prompt()` se utilizan para crear cuadros de diálogo e interactuar con el usuario, pero son diferentes entre sí.

- **El `alert()`** se utiliza para mostrar un mensaje simple al usuario.  
  **Ejemplo:**
  ```javascript
  alert("¡Hola, todos!");
  ```

- **El `prompt()`** requiere que el usuario ingrese algún valor, que podrás manipular.  
  **Ejemplo:**
  ```javascript
  const ciudad = prompt("Escribe tu ciudad:");
  const msg = `¡Eres de ${ciudad}!`;
  alert(msg);
  ```

Prueba los códigos anteriores e intenta adaptarlos a tu programa.

✅ [***Solución***](./day-2.html) 👈

[🔝 Índice](#7daysofcode-rocket)

---
