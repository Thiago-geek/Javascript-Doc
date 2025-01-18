# Javascript
JavaScript es un tema muy amplio, con muchas características, estilos y técnicas diferentes para aprender, y muchas API y herramientas creadas sobre él. Este módulo se centra principalmente en los aspectos esenciales del lenguaje principal, además de algunos temas clave relacionados; aprender estos temas le brindará una base sólida sobre la cual trabajar.

# ¿Qué es JavaScript?
JavaScript es un lenguaje de programación que permite implementar funciones complejas en páginas web. Cada vez que una página web hace algo más que simplemente estar ahí y mostrar información estática para que la mires (mostrar actualizaciones de contenido oportunas, mapas interactivos, gráficos animados 2D/3D, jukeboxes de video con desplazamiento, etc.), puedes apostar a que probablemente JavaScript esté involucrado. Es la tercera capa de la torta de capas de las tecnologías web estándar, dos de las cuales ( HTML y CSS ) hemos cubierto con mucho más detalle en otras partes del Área de aprendizaje.

![](images.png/torta3Capaz.png)
  
* `HTML` es el lenguaje de marcado que utilizamos para estructurar y dar significado a nuestro contenido web, por ejemplo, definiendo párrafos, encabezados y tablas de datos, o incrustando imágenes y vídeos en la página.

* `CSS` es un lenguaje de reglas de estilo que usamos para aplicar estilos a nuestro contenido HTML, por ejemplo, establecer colores de fondo y fuentes, y diseñar nuestro contenido en múltiples columnas.

* `JavaScript` es un lenguaje de programación que permite crear contenido que se actualiza de forma dinámica, controlar contenido multimedia, animar imágenes y prácticamente todo lo demás. (Bueno, no todo, pero es sorprendente lo que se puede lograr con unas pocas líneas de código JavaScript).

# Entonces, ¿qué puede hacer realmente?
El lenguaje principal del cliente JavaScript consta de algunas características de programación comunes que le permiten hacer cosas como:

* Almacenar valores útiles dentro de las variables. 

* Operaciones sobre fragmentos de texto (conocidos como "cadenas" en programación).

* `click` Ejecución de código en respuesta a determinados eventos que ocurren en una página web.

* ¡Y mucho más!

Pero lo que es aún más interesante es la funcionalidad desarrollada sobre el lenguaje JavaScript del lado del cliente. Las denominadas interfaces de programación de aplicaciones ( API ) le brindan superpoderes adicionales para usar en su código JavaScript.

Las API son conjuntos de bloques de código listos para usar que permiten a un desarrollador implementar programas que de otro modo serían difíciles o imposibles de implementar. Hacen lo mismo para la programación que los kits de muebles listos para usar para la construcción de viviendas: es mucho más fácil tomar paneles ya cortados y atornillarlos para hacer una estantería que elaborar el diseño uno mismo, buscar la madera correcta, cortar todos los paneles con el tamaño y la forma adecuados, encontrar los tornillos del tamaño correcto y luego unirlos para hacer una estantería.

![imagenAPI](images.png/imageAPI.png)

Las API del navegador están integradas en el navegador web y pueden exponer datos del entorno informático circundante o realizar tareas complejas y útiles. 

# ¿Qué hace JavaScript en tu página?
Aquí comenzaremos a mirar algo de código y, mientras lo hacemos, exploraremos lo que realmente sucede cuando ejecutas JavaScript en tu página.

Recapitulemos brevemente la historia de lo que sucede cuando cargas una página web en un navegador. Cuando cargas una página web en tu navegador, estás ejecutando tu código (HTML, CSS y JavaScript) dentro de un entorno de ejecución (la pestaña del navegador). Esto es como una fábrica que toma materias primas (el código) y produce un producto (la página web).

![laWeb](images.png/laweb.png)

Un uso muy común de JavaScript es modificar dinámicamente HTML y CSS para actualizar una interfaz de usuario, a través de la API del Modelo de objetos de documento (como se mencionó anteriormente).

# Seguridad del navegador
Cada pestaña del navegador tiene su propio contenedor independiente para ejecutar código (estos contenedores se denominan "entornos de ejecución" en términos técnicos); esto significa que, en la mayoría de los casos, el código de cada pestaña se ejecuta de forma completamente independiente y el código de una pestaña no puede afectar directamente al código de otra pestaña o de otro sitio web. Esta es una buena medida de seguridad; si no fuera así, los piratas podrían empezar a escribir código para robar información de otros sitios web y otras cosas malas similares.


# Orden de ejecución de JavaScript
Cuando el navegador encuentra un bloque de JavaScript, generalmente lo ejecuta en orden, de arriba hacia abajo. Esto significa que debes tener cuidado con el orden en el que colocas las cosas. Por ejemplo, volvamos al bloque de JavaScript

```javascript
const button = document.querySelector("button");

button.addEventListener("click", updateName);

function updateName() {
  const name = prompt("Enter a new name");
  button.textContent = `Player 1: ${name}`;
}
```

Aquí, primero seleccionamos un botón con document.querySelector, luego le adjuntamos un detector de eventos con addEventListener, de modo que cuando se haga clic en el botón, updateName()se ejecute el bloque de código (líneas 5 a 8). El updateName()bloque de código (estos tipos de bloques de código reutilizables se denominan "funciones") solicita al usuario un nuevo nombre y luego inserta ese nombre en el texto del botón para actualizar la pantalla.

Si cambiaras el orden de las dos primeras líneas de código, ya no funcionaría; en su lugar, obtendrías un error en la consola para desarrolladores del navegador .

# Código interpretado versus código compilado
Es posible que hayas oído hablar de los términos "interpretado" y "compilado" en el contexto de la programación. En los lenguajes interpretados, el código se ejecuta de arriba a abajo y el resultado de la ejecución del código se devuelve inmediatamente. No tienes que transformar el código en un formato diferente antes de que el navegador lo ejecute. El código se recibe en su formato de texto fácil de usar para el programador y se procesa directamente a partir de ahí.

Por otra parte, los lenguajes compilados se transforman (compilan) en otro formato antes de que el ordenador los ejecute. Por ejemplo, C/C++ se compilan en código de máquina que luego ejecuta el ordenador. El programa se ejecuta desde un formato binario, que se generó a partir del código fuente del programa original.

JavaScript es un lenguaje de programación interpretado ligero. El navegador web recibe el código JavaScript en su forma de texto original y ejecuta el script a partir de él. Desde un punto de vista técnico, la mayoría de los intérpretes de JavaScript modernos utilizan una técnica llamada compilación en tiempo real para mejorar el rendimiento; el código fuente de JavaScript se compila en un formato binario más rápido mientras se utiliza el script, de modo que se pueda ejecutar lo más rápido posible. Sin embargo, JavaScript todavía se considera un lenguaje interpretado, ya que la compilación se realiza en tiempo de ejecución, en lugar de antes.

Ambos tipos de lenguaje tienen ventajas, pero no las analizaremos ahora.
