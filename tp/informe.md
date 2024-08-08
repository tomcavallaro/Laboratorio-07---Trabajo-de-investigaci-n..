# Informe sobre manipulacion de cadenas en C++

> ## Ⅰ. Introducción ☜ ( ͡👁️ ͜ʖ ͡👁️)
Las cadenas de caracteres en C++ son secuencias de caracteres utilizados para representar texto. Existen dos formas principales de manejar cadenas:

➤char[]: Arreglos de caracteres, una forma más clásica pero que requiere una gestión manual de la memoria y es propensa a errores si no se maneja correctamente.

➤std::string: Una clase de la biblioteca estándar que encapsula la funcionalidad de las cadenas, ofreciendo una interfaz más segura y fácil de usar.


> ## Ⅱ. Declaración e Inicialización de Cadenas ☜ ( ͡👁️ ͜ʖ ͡👁️)

```cpp

//char[]
char cadena1[] = "Hola, mundo!";

///std::string
std::string cadena2 = "Hola, mundo!";

```

  char[] cadena1[] = "Hola, mundo!";

➤ char[]: Esto declara un arreglo de caracteres. Un arreglo de caracteres en C++ se utiliza para representar cadenas de texto.
➤ cadena1: Este es el nombre que le damos a este arreglo específico.
➤ "Hola, mundo!": Esta es la cadena de texto que se almacena en el arreglo cadena1. Las comillas dobles indican que se trata de una cadena literal.

 std::string cadena2 = "Hola, mundo!";

➤ std::string: Esta es una clase de la biblioteca estándar de C++ que se utiliza para representar cadenas de texto de manera más segura y flexible que los arreglos de caracteres.
➤ cadena2: Este es el nombre que le damos a un objeto de la clase std::string.
➤ "Hola, mundo!": Al igual que antes, esta es la cadena de texto que se asigna al objeto cadena2.



> ## Ⅲ. Concatenación de Cadenas ☜ ( ͡👁️ ͜ʖ ͡👁️)

```cpp

// char[]
char cadena1[] = "Hola";
char cadena2[] = " mundo";
char resultado[50];
strcat(resultado, cadena1);
strcat(resultado, cadena2);

// std::string
std::string cadena3 = "Hola";
std::string cadena4 = " mundo";
std::string resultado2 = cadena3 + cadena4;
 
 ```



### 🔹Explicación:
#### ➤char []
char cadena1[] = "Hola"; y char cadena2[] = " mundo"; declaran dos arreglos de caracteres, que representan las cadenas "Hola" y " mundo".
char resultado[50]; reserva un espacio de memoria de 50 caracteres para almacenar el resultado de la concatenación.
strcat(resultado, cadena1); y strcat(resultado, cadena2); utilizan la función strcat para concatenar las cadenas cadena1 y cadena2 al final de resultado.

#### ➤std::string
std::string cadena3 = "Hola"; y std::string cadena4 = " mundo"; declaran dos objetos de tipo std::string, que representan las mismas cadenas.
std::string resultado2 = cadena3 + cadena4; utiliza el operador + sobrecargado para concatenar las cadenas cadena3 y cadena4 y asignar el resultado a resultado2.

### 🔹Facilidad de uso:

#### ➤char []
Menor nivel de abstracción: Requiere un manejo más manual de la memoria y de las operaciones con cadenas.
Mayor propensión a errores: Si no se reserva suficiente espacio para el resultado, se produce un desbordamiento de búfer, lo que puede llevar a comportamientos inesperados o incluso a la vulnerabilidad a ataques.

#### ➤std::string
Mayor nivel de abstracción: Oculta la gestión de la memoria y proporciona una interfaz más intuitiva para trabajar con cadenas.
Más seguro: Maneja automáticamente el tamaño de la cadena y evita desbordamientos de búfer.


### 🔹Eficiencia:

#### ➤char []
Potencialmente más eficiente: En algunos casos, puede ser ligeramente más eficiente que std::string debido a la menor sobrecarga, pero esta diferencia suele ser insignificante en la mayoría de las aplicaciones.
Depende de la implementación: La eficiencia de strcat puede variar según el compilador y la arquitectura.

#### ➤std::string
Generalmente más eficiente en términos de seguridad: Al manejar automáticamente la memoria, reduce el riesgo de errores y facilita la depuración.
Puede tener una ligera sobrecarga: Debido a las comprobaciones de límites y otras características, puede ser ligeramente menos eficiente que char[] en algunos casos muy específicos.

 
> ## Ⅳ. Longitud de una Cadena ☜ ( ͡👁️ ͜ʖ ͡👁️)

```cpp

// char[]
int longitud1 = strlen(cadena1);

// std::string
int longitud2 = cadena2.length();
 
```
### ➤ char []

int longitud1 = strlen(cadena1);

✦   strlen(cadena1) : Esta parte del código utiliza la función strlen para calcular la longitud de la cadena cadena1.

✦ cadena1: Es un arreglo de caracteres (C-style string) definido previamente.

✦ strlen: Es una función de la biblioteca estándar de C que devuelve la longitud de una cadena de caracteres. La ✦ longitud es el número de caracteres antes del carácter nulo final (\0).

✦ int longitud1: Aquí se declara una variable entera llamada longitud1 para almacenar el resultado del cálculo de la longitud.



### ➤ std::string

int longitud2 = cadena2.length();

✦cadena2.length();: Esta parte del código utiliza el método length() para obtener la longitud de la cadena cadena2.

✦cadena2: Es un objeto de tipo std::string definido previamente.

✦length(): Es un método miembro de la clase std::string que devuelve la longitud de la cadena como un entero.


> ## Ⅴ. Subcadenas
 ```cpp

std::string subcadena = cadena2.substr(0, 5); // "Hola "

```

✦ Esta línea de código toma la cadena almacenada en cadena2 y extrae los primeros 5 caracteres a partir del índice 0. La subcadena resultante ("Hola ") se almacena en la variable subcadena.


> ## Ⅵ. Comparación de Cadenas

  ``` cpp

// char[]
int resultado = strcmp(cadena1, cadena2); 

// std::string
bool igual = (cadena3 == cadena4);

  ```
✦Función strcmp: Esta función de la biblioteca estándar de C se utiliza para comparar dos cadenas de caracteres (C-style strings).

✦ strcmp es más bajo nivel y requiere un manejo más cuidadoso, pero ofrece mayor flexibilidad al devolver un valor numérico que indica la relación entre las cadenas.

✦ para std::string es más alto nivel y fácil de usar, ya que directamente indica si las cadenas son iguales o no. Es la opción preferida en la mayoría de los casos debido a su mayor seguridad y facilidad de uso.


<div style="border: 2px solid black; padding: 10px; background-color: #FFD3D3D3; color:black; border-radius: 15px; "> En la mayoría de los casos, es recomendable utilizar el operador == para comparar objetos std::string, ya que es más seguro y fácil de entender. Sin embargo, strcmp puede ser útil en situaciones específicas donde se requiere un control más preciso sobre la comparación de cadenas. </div>


## Ⅶ. Comparación de Cadenas ☜ ( ͡👁️ ͜ʖ ͡👁️)

✦ Ejemplo de cómo convertir una cadena a mayúsculas o minúsculas usando std::string y las funciones toupper y tolower:

  ``` cpp

  #include <iostream>
#include <string>
#include <cctype>

int main() {
    std::string str = "Hola Mundo";
    for (char &c : str) {
        c = std::toupper(c);
    }
    std::cout << str << std::endl;  // Output: HOLA MUNDO
    return 0;
}

  ```




✦ Convertir una cadena a minúsculas:

 ``` cpp

#include <iostream>
#include <string>
#include <cctype>

int main() {
    std::string str = "Hola Mundo";
    for (char &c : str) {
        c = std::tolower(c);
    }
    std::cout << str << std::endl;  // Output: hola mundo
    return 0;
}

 ```



✦ Ejemplo de cómo buscar caracteres o subcadenas en una std::string usando el método find
Buscar una subcadena:

``` cpp

#include <iostream>
#include <string>

int main() {
    std::string str = "Hola Mundo";
    std::size_t found = str.find("Mundo");
    if (found != std::string::npos) {
        std::cout << "Subcadena encontrada en la posición: " << found << std::endl;
    } else {
        std::cout << "Subcadena no encontrada" << std::endl;
    }
    return 0;
}

```




✦ conversión de una cadena a un número entero (int):

``` cpp

#include <iostream>
#include <string>

int main() {
    std::string str = "123";
    int num = std::stoi(str);
    std::cout << "El número es: " << num << std::endl;  // Output: 123
    return 0;
}

```


✦ Convertir una cadena a un número de punto flotante (double):

``` cpp

#include <iostream>
#include <string>

// Función que convierte una cadena a double y la imprime
void imprimirNumeroDesdeCadena(const std::string& cadena) {
    double numero = std::stod(cadena);
    std::cout << "El número es: " << numero << std::endl;
}

// Función que retorna una cadena representando un número
std::string obtenerCadenaNumerica() {
    return "123.456";
}

int main() {
    // Crear una cadena
    std::string miCadena = "456.789";
    
    // Pasar la cadena a una función que convierte y la imprime
    imprimirNumeroDesdeCadena(miCadena);
    
    // Obtener una cadena desde una función y convertirla
    std::string nuevaCadena = obtenerCadenaNumerica();
    imprimirNumeroDesdeCadena(nuevaCadena);
    
    return 0;
}

```

✦ Pasaje de Cadenas a Funciones usando char[]:

``` cpp

#include <iostream>
#include <cstring>

// Función que toma una cadena como argumento y la imprime
void imprimirCadena(const char* cadena) {
    std::cout << "La cadena es: " << cadena << std::endl;
}

// Función que retorna una cadena
const char* obtenerCadena() {
    return "Hola, mundo!";
}

int main() {
    // Crear una cadena
    char miCadena[] = "Hola desde main!";
    
    // Pasar la cadena a una función
    imprimirCadena(miCadena);
    
    // Obtener una cadena desde una función
    const char* nuevaCadena = obtenerCadena();
    imprimirCadena(nuevaCadena);
    
    return 0;
}

```

✦ Pasaje de Cadenas Usando std::string:

``` cpp

#include <iostream>
#include <string>

// Función que toma una cadena como argumento y la imprime
void imprimirCadena(const std::string& cadena) {
    std::cout << "La cadena es: " << cadena << std::endl;
}

// Función que retorna una cadena
std::string obtenerCadena() {
    return "Hola, mundo!";
}

int main() {
    // Crear una cadena
    std::string miCadena = "Hola desde main!";
    
    // Pasar la cadena a una función
    imprimirCadena(miCadena);
    
    // Obtener una cadena desde una función
    std::string nuevaCadena = obtenerCadena();
    imprimirCadena(nuevaCadena);
    
    return 0;
}


```


### 🔹Explicación general:

✦ Conversión de cadenas a mayúsculas/minúsculas:

Utilizamos un bucle for para recorrer cada carácter de la cadena y aplicamos las funciones std::toupper y std::tolower de la biblioteca <cctype> para convertir cada carácter a su equivalente en mayúscula o minúscula.

✦ Búsqueda de caracteres o subcadenas:

Utilizamos el método find de std::string para buscar la posición de una subcadena. Si la subcadena no se encuentra, find devuelve std::string::npos.

✦ Conversión de cadenas a números:

Usamos las funciones std::stoi y std::stod de la biblioteca <string> para convertir cadenas a números enteros y de punto flotante, respectivamente.

✦ Pasaje de cadenas a funciones:

Demostramos cómo pasar cadenas a funciones usando tanto arreglos de caracteres (char[]) como std::string. En el caso de std::string, es buena práctica pasar la cadena como una referencia constante (const std::string &) para evitar copias innecesarias.

## Ⅷ. Conclusion ☜ ( ͡👁️ ͜ʖ ͡👁️)
Resumen de las principales diferencias entre char[] y std::string

✦ char[] es un arreglo de caracteres de tamaño fijo y es parte de la biblioteca estándar de C. Se utiliza comúnmente en programación de bajo nivel.

✦ std::string es una clase de la biblioteca estándar de C++ que proporciona una interfaz más conveniente y segura para manejar cadenas de caracteres. Ofrece una variedad de funciones miembro para manipular cadenas.

### 🔹Ventajas y desventajas de usar cada uno

### char[]

🔹Ventajas

✦Control de memoria:

Permite un control más fino sobre la asignación y liberación de memoria.
Útil en entornos donde los recursos son limitados (por ejemplo, sistemas embebidos).

✦Rendimiento:

En ciertos casos, puede ser más rápido ya que no hay sobrecarga asociada a la gestión de memoria automática.

✦ Compatibilidad con C:

Mayor compatibilidad con código C y con APIs que esperan arreglos de caracteres.

✦ Simplicidad:

Para cadenas de longitud fija y simple, char[] puede ser más sencillo y directo.

🔹Desventajas

✦ Gestión de memoria:

El programador es responsable de la asignación y liberación de memoria, lo que puede llevar a errores como fugas de memoria (memory leaks) y desbordamientos de búfer (buffer overflows).

✦ Limitaciones de tamaño:

El tamaño de la cadena debe ser conocido de antemano y es fijo, lo que puede ser poco flexible.

✦ Funcionalidad limitada:

No proporciona métodos integrados para la manipulación de cadenas como concatenación, búsqueda, etc.

std::string

🔹Ventajas

✦ Gestión automática de memoria:

La clase std::string maneja automáticamente la asignación y liberación de memoria, reduciendo la probabilidad de errores de memoria.
Flexibilidad:

El tamaño de la cadena puede cambiar dinámicamente, adaptándose a las necesidades del programa.

✦ Funciones y métodos incorporados:

Proporciona una amplia gama de funciones y métodos para la manipulación de cadenas, como concatenación, búsqueda, comparación, etc.

✦ Seguridad:

Reduce el riesgo de errores como desbordamientos de búfer y fugas de memoria.

🔹Desventajas

✦ Sobrecarga de rendimiento:

Puede ser más lento debido a la gestión automática de memoria y otras características adicionales.

✦ Mayor consumo de memoria:

Puede consumir más memoria debido a la sobrecarga de la clase y las operaciones internas.

✦ Compatibilidad con C:

Menos compatible con código C y APIs que esperan char[].

### Ⅸ. Referencias ☜ ( ͡👁️ ͜ʖ ͡👁️)

🔹 [CHATGPT](https://chatgpt.com/)

🔹 [GEMINI](https://gemini.google.com/app)
