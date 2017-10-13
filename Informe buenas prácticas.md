
#  Buenas prácticas de la programación en Java

  Al crear un programa o aplicación, hay muchas formas distintas de llegar al mismo resultado. Cada programador tiene un estilo personal
y ha aprendido distintas técnicas de distintas fuentes. Es muy fácil aprender a programar con la variedad de cursos que existen hoy en día,
pero el gran volumen de aprendizaje no supervisado genera deficiencia en la calidad del software.

La calidad puede medirse en 3 grandes aspectos:
* Que el programa funcione.
* Que sea legible.
* Que sea mantenible.

  En el primer punto, no hay grandes problemas, de una forma u otra el programa cumple con su tarea. El foco está en cómo se llega a
ese resultado. En el sistema llamado software "artesanal" el programador sigue un proceso de prueba y error constante hasta obtener el
funcionamiento deseado y esto genera que el código sea poco legible para otros programadores o usuarios y hace casi imposible su
mantenibilidad.
  Para evitar estos problemas que afectan tanto el tiempo de producción como el costo y el rendimiento de la aplicación, se deben seguir
ciertas convenciones para crear un código de buena calidad, que no sólo cumpla con su tarea sino que lo haga de la mejor forma posible.
Estas buenas prácticas pueden dividirse en 2 grandes grupos: convenciones sobre sintaxis o forma de escritura y convenciones sobre programación
que influyen en el rendimiento del software.


##**SINTAXIS:**

Un código Java tiene la siguiente estructura:
1. Comentario de comienzo.
2. Sentencias *Package* e *import*.
3. Declaraciones de Clases e interfaces.

1. Los códigos deberían comenzar con un comentario que contenga datos sobre sus características.
2. La primer línea no comentada en un código es la sentencia Package, despúes puede haber tantas sentencias import como sea necesarias.
3. Las declaraciones de clases y/o interfaces debentener el siguiente orden:
  * Comentario de documentación.
  * Sentencia Class o Interface (se recomienda una declaración por línea).
  * Comentario sobre su implementación (solo si son necesarios).
  * Variables estáticas de clase (Public, Protected, Private). Se recomienda inicializar las variables cuando se declaran.
  * Variables de instancia (Public, Protectes, Private).
  * Constructores
  * Métodos

 Es importante, además, respetar un estilo de indentación a lo largo de todo el código, lo cual lo hace más legible para una persona.
 No existe una covención sobre la cantidad de espacios, pero lo más usado es un tabulador de 8 espacios.
 Las sentencias return no deben usar parentesis a menos que hagan el contenido más claro para la lectura
 Las sentencias IF siempre llevan llave {}.
 Usar líneas en blanco, separando secciones de código relacionadas para mejorar la lectura.
 Los nombres de clase, variables y métodos siempre deben ser representativos, si son compuestos, la primer letra de cada palabra debe ser mayúscula.

**Convenios de Nombrado:**
Los nombres de las clases y las interfaces deben ser sustantivos. Evitar abreviaturas salvo en el caso de que sean más
conocidas y usadas que el nombre completo.
Los nombres de los métodos deben ser verbos y comenzar siempre con una letra minúscula.
Las variables nunca deben comenzar con "_"_ o "$" y si se refieren a una operación, utilizar mnemónicos. Si se trata de constantes,
siempre deben estar completamente en mayúscula con sus palabras separadas por un guion bajo.

**Uso de Paréntesis:**
Se recomienda utilizar "()" para separar expresiones en una sentencia lógica para que quede claro el órden de precedencia de los operadores.

##**RENDIMIENTO:**

* Crear o inicializar objetos solo en el momento en el que serán requeridos en el código para minimizar el uso de memoria de su
correspondiente impacto en el rendimiento.
* Las variables de una clase no deben ser públicas a menos que exista un buen motivo para ello. Siempre se deben definir como privadas o protegidas
y crear los correspondientes métodos de acceso.
* Para las variables locales siempre declararlas justo antes de ser usadas para que el código sea mas legible, menos propenso a errores y mantenible.
* Siempre utilizar librerias estándar en lugar de desperdiciar tiempo creando propias, facilitando el reuso de código.
* Tener cuidado al utilizar objetos del tipo *String* ya que pueden afectar la memoria y reducir el rendimiento.
* Evitar sentencias *"System.out"* en metodos de clases.
* Siempre que se conozca, iniciar las colecciones con el tamaño que van a requerir.
* Utilizar llamadas a métodos dentro de las condiciones de un bucle solo cuando sea necesario, ya que consumen mucha memoria.
* Evitar el uso de bloques *Try* anidados. Los boloques *Catch* siempre van de lo más específico a lo más genérico.
* Analizar si conviene utilizar un *If* o un *Switch* según el caso. If será mejor para los casos complejos y los anidamientos mientras que
Switch es más ventajoso para el rendimeinto cuando las opciones no son complejas.
* Evitar el uso de sentencias que rompan el flujo secuencial de ejecución (Goto, Break, Continue). Estas sentencias dificultan la
legibilidad, depuración, y verificación de programas.
* Utilizar un único Return por método, colocado como sentencia final.
* Evitar métodos y funciones demasiado largas ya que dificultan su legibilidad, comprensión y mantenimiento.
* Evitar el reuso de código, encapsular éstos bloques en una función o método e invocarla cuando se necesite.
* La función Main siempre se ubica en una clase o módulo separado e independiente, ya que representa el punto de entrada de la
aplicación y su funcionalidad no pertenece a ninguno de los módulos o clases que  la conforman. Se recomienda nombrar a esta clase Runner
o Launcher.
* Colocar al lado de una llave de cierre de bloque un comentario que indique qué tipo de bloque esta cerrando o el nombre del metodo
o clase cuando corresponda.
* No utilizar caracteres propios del castellano, sino codificar en inglés o sustituir por adaptaciones (ñ = ni).

## **BIBLIOGRAFÍA**

http://mmc.geofisica.unam.mx/acl/Herramientas/Java/ConvencionesCodigoJava1.pdf
http://personales.unican.es/sanchezbp/teaching/faqs/programming.html
http://www.decodigo.com/2013/04/mejores-practicas.html
https://unpocodejava.com/2012/03/16/buenas-practicas-de-codificacion-en-java/
