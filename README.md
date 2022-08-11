# Test Javascript Platzi 🚀
## Herald Flores Solution:

### **Variables y operaciones**
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
**¿Qué es una variable y para qué sirve?**
las variables son espacios reservados en memoria que se utilizan para almacenar diferentes tipos datos y convertirlos en información al ser procesados por nuestras aplicaciones.
**¿Cuál es la diferencia entre declarar e inicializar una variable?**
Declarar una variable es el proceso que realizamos para reservar un espacio en memoria, que al ser inicializado se define el tipo de dato a almacenar y el valor inicial o por defecto.
**¿Cuál es la diferencia entre sumar números y concatenar strings?**
Sumar números es una operación aritmética que requiere realizar cálculos en la aplicación, por otra parte concatenar es una acción que permite unir dos o más cadenas de caracteres y formar una sola cadena con toda la información.


```
// arithmetic operation
const numberOne = 5;
const numberTwo = 10;

const sum = numberOne + numberTwo;
console.log("Result: ", sum);

// Concatenation
const stringOne = "Hi everyOne, ";
const stringTwo = "I study here at Platzi, never stop learning!";

const epicString = stringOne + stringTwo;
console.log(epicString);
```

**¿Cuál operador me permite sumar o concatenar?**
El operador de suma ( + )

```
const fullName = "Herald " + "Flores";
```


2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:
Nombre “String”
Apellido“String”
Nombre de usuario en Platzi “String”
Edad "Integer"
Correo electrónico “String”
Mayor de edad "Boolean"
Dinero ahorrado "Float"
Deudas "Float"

3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.
```
let name = "Herald";
let lastName = "Flores";
let user_name = "h-flores";
let age = 27;
let mail = "example@gmail.com"
let adult = true;
let savedMoney = 3000.99;
let debtMoney = 1999.50;
```
4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)

- Dinero real (dinero ahorrado menos deudas)


```
const fullName = name + " " + lastName;
// Calc
let money = savedMoney - debtMoney;

console.log(`Hello ${fullName} your statement of account is: $${money}`);
```

### **Funciones**
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
**¿Qué es una función?**
Es una porción de código reusable, se conforma de un conjunto de declaraciones y devuelven un resultado.
**¿Cuándo me sirve usar una función en mi código?**

1. Cuándo se quiere evitar reescribir código

1. Para modularizar una aplicación

1. Para realizar operaciones repetitivas

**¿Cuál es la diferencia entre parámetros y argumentos de una función?**
Un argumento representa el valor que se pasa a un parámetro, Un parámetro representa un valor que espera la función al ser llamada.


**2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:**
```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");

//Solution
const myFunction = (name, lastName, nickName) =>  `Mi nombre es:  ${name} ${lastName}, pero prefiero que me digas ${nickName}.`;

console.log(myFunction("Herald ", "Flores", "herald"));
```

### **Condicionales**
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
¿Qué es un condicional?
Es una expresión que nos permite evaluar dos o más valores y poder realizar acciones en base al resultado de la expresión.

¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
**if .. else...**
se usa pasa evaluar una condición, si esta condición es verdadera ejecuta las acciones dentro del bloque del if en caso contrario ejecuta las acciones del bloque else
**if .. else if...**
Se usa para evaluar más de  una condición, si esta condición es verdadera ejecuta las acciones dentro del bloque del if, en caso contrario comprueba que la condición de la sentencia else if se cumple y de ser verdadera ejecuta las acciones de ese bloque.
**switch**
Permite evaluar multiples escenarios y tener una acción por default en caso de que no se cumplan las condiciones evaluadas.
**Ternary operator ()? : ;**
Es una pequeña sintaxis que prueba una condición y devuelve un valor, si es true, y otro si es false
¿Puedo combinar funciones y condicionales?
2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}


// ----- Solution ----------
if ( tipoDeSuscripcion === "Free" ) {
	console.log("Solo puedes tomar los cursos gratis");
} else if(  tipoDeSuscripcion === "Basic" ) {
	console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if(  tipoDeSuscripcion === "Expert" ) {
	 console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if(  tipoDeSuscripcion === "ExpertPlus" ) {
	console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
} else {
	console.log("Necesitas una suscripción válida")
}
```

3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).
💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏



```
let  suscriptions = [ 
	{	
		type:"Free",
		message: "solo puedes tomar los cursos gratis"
	},
	{	
		type:"Basic",
		message: "puedes tomar casi todos los cursos de Platzi durante un mes"
	},
	{	
		type:"Expert",
		message: "puedes tomar casi todos los cursos de Platzi durante un año"
	},
	{	
		type:"ExpertPlus",
		message: "tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
	}
];

const mySub = "Basic";

const findSub = suscriptions.find( sub => sub.type === mySub );
const result = findSub !== undefined? findSub.message: "Necesitas una suscripción válida";
console.log(result);

```

### **Ciclos**
**1️⃣ Responde las siguientes preguntas en la sección de comentarios:**
**¿Qué es un ciclo?**
son bucles utilizados para realizar tareas repetitivas con base en una condición
**¿Qué tipos de ciclos existen en JavaScript?**

- for
- foreach
- for...of
- while
- do ... while

**¿Qué es un ciclo infinito y por qué es un problema?**
Es un ciclo que se repite n cantidad de veces, podemos decir que es un ciclo infiinito por que la condición que lo detiene no se cumple, esto puede generar problemas de rendimiento y colapsar la memoria de los equipos donde se ejecuta este bucle.
**¿Puedo mezclar ciclos y condicionales?**
Si los ciclos y las condiciones se utilizan comúnmente en combinación para lograr una lógica de programación especifica.

**2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:**
```
for (let i = 0; i < 5; i++) {
     console.log("El valor de i es: " + i);
}

// While 
let i = 0;
while ( i < 5 ) {
 	console.log("El valor de i es: " + i);
  	i++;
}


for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

// While
let i = 10;
while ( i >= 2 ) {
 	console.log("El valor de i es: " + i);
  	i--;
}
```

3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
💡 Pista: puedes usar la función prompt de JavaScript.


```
//Quiz
let valOne = 2;
let valTwo = 2;
const result = valOne + valTwo;

function quiz() {
	let userInput = prompt( `Cuanto es ${num} + ${num2}` );

  	if (userInput == result) {
   		alert("Felicitaciones, respondiste correctamente el desafio");
  	} else {
    		alert("lamentablemente, tu respuesta es incorrecta, sigue practicando!");
  	}
}

quiz();
```

### **Listas**
**1️⃣ Responde las siguientes preguntas en la sección de comentarios:**
**¿Qué es un array?**
Los arreglos son estructuras de datos, estos pueden ser una colección de elementos de cualquier tipo de dato (String , Boolean, Number, Objects).
**¿Qué es un objeto?**
un objeto es un entidad independiente con propiedades y tipos
**¿Cuándo es mejor usar objetos o arrays?**
Se recomienda usar arreglos cuando se trabaja con valores del mismo tipo, mientras que un objeto puede contener múltiples variables con sus valores
**¿Puedo mezclar arrays con objetos o incluso objetos con arrays?**
Si es posible crear estructuras de datos que contentan array de objetos y que los objetos a su vez tengan claves con valores de tipo array.


```
const employies = [
	{
		"id": "xr2932",
		"type": "Developer",
		"name": "Herald",
		"workPhone":"555-555-5555",
		"skills": [ "html", "css", "js" ]
	},
 	{
		"id": "xr2933",
		"type": "Designer",
		"name": "Juan",
		"workPhone":"555-555-5555",
		"skills": [ "html", "css", "XD" ]
	},
];
```

2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.


```
let frameworks = [ 'react', 'angular', 'vue js' ];

function firsElement( arr ){
	if( arr.length !== 0 ) {
		console.log(arr[0])
	}  
}

firsElement(frameworks);
```

3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).


```
let frameworks = [ 'react', 'angular', 'vue js' ];

function printElements( arr ) {
  	arr.forEach( function ( item ) {
  		console.log( item );
	})
}

printElements( frameworks);
```

4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).


```
const obj = {
	name: "Herald",
	lastName: "Flores",
	age: 27
}

function elementsObject( obj ) {
  	Object.values(obj).forEach( val => {
	 	console.log(val);
	});
 }

elementsObject( obj );
```
