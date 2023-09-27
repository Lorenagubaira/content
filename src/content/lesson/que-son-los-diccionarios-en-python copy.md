---
title: "Introducción a los diccionarios en Python: Estructuras clave-valor para organizar y acceder a datos"
subtitle: "Descubre qué son los diccionarios en Python y cómo se utilizan. Aprende cómo aprovechar estas estructuras de datos para organizar y acceder eficientemente a información."
tags: ["python"]
authors: ["DF27ARTS"]

---

## Exploring Python Dictionaries

Dictionaries in [Python](https://4geeks.com/es/lesson/como-programar-en-python) are a data structure that allows us to store large amounts of data and access them in a very efficient way. In this article you will learn how to create, access and modify data in a Python dictionary, in the following example we will see a small demonstration of how you can use a dictionary to store a collection of data.

```py
city = {
    #Key Value
    "city_id": 1,
    "city_name": "New York",
    "population": 8,468,
    "currency": "dollar"
}

city["city_id"] = 1000 # Replace data within the dictionary.
city["city_name"] = city["city_name"].upper() # Modify data inside the dictionary
from city["currency"] # Delete data within the dictionary

print(city)
```
> output city: 

```bash
{
    'city_id': 1000, 
    'city_name': 'NEW YORK', 
    'population': 8,468
}
```

In this example, we create a dictionary with data to represent a city, in the example we access to the property `city_id` and we replace its original value **50** with a new value **1000**, also we modify the property `city_name` with the same value but in capital letters **NEW YORK** and finally we eliminate the property `currency` of the dictionary. In this code we can see the most basic examples on how to access to a property, how to modify data and how to delete properties in dictionary.

## ¿Qué es un diccionario en Python?

Un diccionario en Python es una estructura de datos donde puedes almacenar información de forma organizada. Piénsalo como un verdadero diccionario, pero en lugar de encontrar definiciones de palabras, ¡tendrás valores asociados a claves únicas! Cada elemento del diccionario es un par clave-valor, donde la clave es única y nos permite acceder a su valor correspondiente. Así podemos encontrar rápidamente lo que necesitamos.

En el siguiente video se muestra mejor cómo funcionan los diccionarios en Python, cómo acceder a sus propiedades, cómo actualizar sus valores y muchas cosas más.

<iframe 
    width="650" 
    height="350" src="https://www.youtube.com/embed/DSzqe4Rb5YY" 
    title="YouTube video player" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    allowfullscreen>
</iframe>

## ¿Cómo declarar un diccionario?

Para declarar un diccionario en Python puedes hacerlo de dos formas, la primera es crear una variable y asignarle como valor un par de llaves `{}` esto creará un diccionario por defecto, otra forma de declarar un diccionario es crear una variable y asignarle como valor el constructor `dict()`, en los siguientes ejemplos verás un poco mejor cómo funciona.

```py
objeto_uno = {
    "clave_uno": "objeto uno valor uno",
    "clave_dos": "objeto uno valor dos",
}

objeto_dos = dict(
    clave_uno = "objeto dos valor uno",
    clave_dos = "objeto dos valor dos",
)

print(objeto_uno)
print(objeto_dos)
```
> output:
```bash
{
    'clave_uno': 'objeto uno valor uno', 
    'clave_dos': 'objeto uno valor dos'
}
{
    'clave_uno': 'objeto dos valor uno', 
    'clave_dos': 'objeto dos valor dos'
}
```

Como puedes ver, crear un diccionario en Python es muy sencillo, primero creas una variable y le asignas un par de llaves `{}`, luego dentro de las llaves creamos una clave y a esta clave le asignamos un valor, por ejemplo: `{ "academia": "4Geeks" }`.

> Aunque es posible declarar un diccionario con el constructor `dict()`, te recomiendo que utilices las llaves `{}` ya que se considera una buena práctica y hace el código más sencillo de leer.

## ¡Accediendo a los datos!

Para acceder a los datos adentro un diccionario usa la sintaxis `nombre_diccionario[clave]`, o también puedes usar el método `get()` con la siguiente sintaxis `nombre_diccionario.get(clave)` como se muestra en el siguiente ejemplo:

```py
persona = {
    "nombre": "Axel",
    "edad": 32,
    "email": "axel@mail.com",
    "teléfono": "(123) 456-7890"
}

print(persona["nombre"])  # output:  Axel
print(persona["edad"])    # output:  32

print(persona.get("email"))     # output:  axel@mail.com
print(persona.get("teléfono"))  # output:  (123) 456-7890

print(persona["peso"])      # output:  Arroja un error (KeyError: 'peso') y detiene la ejecución porque la clave (peso) no existe en el objeto persona
print(persona.get("peso"))  # output:  Aunque la clave (peso) no existe en el objeto persona el método get() no detiene la ejecución y retorna: None
```

Como se muestra en este ejemplo, para acceder al valor de la un diccionario puedes usar los corchetes y dentro de los corchetes el nombre de la clave de ese valor `variable[clave]` o también puedes usar el método `get()` y le pasas como parámetro el nombre de la clave que contiene es valor `variable.get(clave)`. 

> Es importante resaltar que si tratas de acceder a la clave de un diccionario que no contiene esa clave usando los corchetes te va a arrojar un error de tipo `KeyError` y va a detener la ejecución del código mientra que si usas el metodo `get()` este no detiene la ejecución del código y te retorna el valor `None`.

## ¡Añadiendo nuevos datos! 

Para añadir un nuevo elemento a un diccionario existen varias formas, puedes usar la sintaxis `nombre_diccinario[nueva clave] = nuevo valor` para añadir un nuevo elemento o también puedes usar el método `update()` para añadir varios elementos a la vez como se muestra en el siguiente ejemplo:

```py
objeto_uno = { "clave_1": 1, "clave_2": 2 }
objeto_dos = { 1: "A", 2: "B", 3: "C" }

objeto_uno["clave_3"] = 3
objeto_uno["clave_4"] = 4

objeto_dos.update({ 4: "D", 5: "E" })

print(objeto_uno)
print(objeto_dos)
```
> output:
```bash
{ 'clave_1': 1, 'clave_2': 2, 'clave_3': 3, 'clave_4': 4}

{ 1: 'A', 2: 'B', 3: 'C', 4: 'D', 5: 'E' }
```

Como vemos en este ejemplo, puedes usar la sintaxis de llaves `{}` y dentro de las llaves el nombre de la nueva clave para crear un nuevo valor dentro de un diccionario, pero si necesitas crear más de un valor puedes usar el método `update()` y le pasas como parámetro un diccionario con los nuevos valores.

## ¡Eliminando datos! 

Para eliminar una clave-valor de un diccionario, puedes usar la sintaxis `del nombre_diccionario[clave]` o también puedes usar el método `pop()` y le pasas como parámetro el nombre de la clave del valor que deseas eliminar como se muestra en el siguiente ejemplo:

```py
persona = {
    "nombre": "Axel",
    "edad": 32,
    "email": "axel@mail.com",
    "teléfono": "(123) 456-7890",
    "peso": 80
} 

del persona["peso"]
edad = persona.pop("edad")

print(edad) # output: 32
print(persona)
```
> output persona:
```bash
{
    'nombre': 'Axel', 
    'email': 'axel@mail.com', 
    'teléfono': '(123) 456-7890'
}
```

Como se muestra en el ejemplo, puedes usar la palabra reservada `del` y luego accedes a la clave del diccionario `persona["peso"]` para eliminarla. Otra forma en la puedes eliminar una clave-valor de un diccionario es haciendo uso método `pop()`, este método recibe como parámetro el nombre de la clave, elimina esa clave-valor del diccionario y retorna el valor que eliminó que en el ejemplo se guarda en la variable `edad`.

## ¡Recorriendo un diccionario!

Para recorrer un diccionario puedes hacerlo de muchas maneras, en el siguiente ejemplo veremos un caso sencillo haciendo uso de la estructura de bucle `for`:

```py
persona = {
    "nombre": "Axel",
    "edad": 32,
    "email": "axel@mail.com",
    "teléfono": "(123) 456-7890",
    "peso": 80
}

for clave in persona:
    valor = persona[clave]
    print(f"Clave: '{clave}', valor: '{valor}'")
```
> output: 
```bash
Clave: 'nombre',  valor: 'Axel'
Clave: 'edad',  valor: '32'
Clave: 'email',  valor: 'axel@mail.com'
Clave: 'teléfono',  valor: '(123) 456-7890'
Clave: 'peso',  valor: '80'
```

Como vemos en este ejemplo, recorrer un diccionario es muy sencillo puedes hacerlo con un bucle `for` y unas pocas líneas de código. En este ejemplo recorremos el diccionario y mostramos en la consola el nombre de la clave y el valor del esa clave en cada iteración.

## ¡Métodos de diccionarios!

En el siguiente videotutorial podrás ver algunas de los métodos más importantes de los diccionarios y además abajo del video podrás ver una tabla con algunos métodos más.

<iframe 
    width="650" 
    height="350" src="https://www.youtube.com/embed/Ycu5Re7bEUE" 
    title="YouTube video player" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    allowfullscreen>
</iframe>

Estos son algunos de los métodos más relevantes de los diccionarios.

| Método        | Descripción                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------|
|`clear()`      | Elimina todos los elementos del diccionario.                                                                   |
|`copy()`       | Crea una copia superficial del diccionario.                                                                    |
|`get()`        | Devuelve el valor asociado a una clave específica.                                                             |
|`items()`      | Devuelve una vista de tuplas `(clave, valor)` para cada par clave-valor en el diccionario.                     |
|`keys()`       | Devuelve una vista de las claves en el diccionario.                                                            |
|`values()`     | Devuelve una vista de los valores en el diccionario.                                                           |
|`pop()`        | Elimina y devuelve el valor asociado a una clave específica.                                                   |
|`popitem()`    | Elimina y devuelve un par `(clave, valor)` arbitrario del diccionario.                                         |
|`setdefault()` | Devuelve el valor asociado a una clave específica. Si la clave no existe, se crea una nueva entrada con valor. |
|`update()`     | Actualiza el diccionario con los pares clave-valor de otro diccionario o de una secuencia de tuplas.           |

## Conclusión

En conclusión, los diccionarios son una excelente estructura de almacenamiento que te permite almacenar grandes cantidades de datos cada uno con una clave y un valor, puedes usar cualquier tipo de dato como clave para un diccionario excepto por otros diccionarios, listas o tuplas. Espero que este artículo te sea de gran utilidad para aprender más sobre diccionarios y cómo trabajar con ellos. Si quieres conocer más sobre este lenguaje de programación te invito a que leas el siguiente [tutorial de Python](https://4geeks.com/es/lesson/como-programar-en-python) en el Blog de [4Geeks](https://4geeks.com/es).
