---
title: Cuadros de lista
description: Con un cuadro de lista, los usuarios pueden seleccionar entre un conjunto de valores que aparecen en una lista que siempre está visible.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3db0bbb07ed6cea18b7d8fb29fd4e329840590d5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361821"
---
# <a name="list-boxes"></a>Cuadros de lista

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con un cuadro de lista, los usuarios pueden seleccionar entre un conjunto de valores que aparecen en una lista que siempre está visible. Con un cuadro de lista de selección única, los usuarios seleccionan un elemento de una lista de valores mutuamente excluyentes. Con un cuadro de lista de selección múltiple, los usuarios seleccionan cero o más elementos de una lista de valores.

![captura de pantalla del cuadro de lista de selección única ](images/ctrl-list-boxes-image1.png)

Cuadro de lista de selección única típico.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) y las [vistas de lista](ctrl-list-views.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿La lista presenta datos, en lugar de opciones de programa?** En cualquier caso, un cuadro de lista es una opción adecuada independientemente del número de elementos. Por el contrario, los [botones de radio](ctrl-radio-buttons.md) o las [casillas](ctrl-check-boxes.md) solo son adecuadas para un número pequeño de opciones de programa.
-   **¿Los usuarios deben cambiar las vistas, agrupar, ordenar por columnas o cambiar el orden y el ancho de las columnas?** Si es así, use una [vista de lista](ctrl-list-views.md) en su lugar.
-   **¿El control debe ser un origen de arrastre o un destino de colocación?** Si es así, use una vista de lista en su lugar.
-   **¿Es necesario copiar o pegar los elementos de la lista desde el portapapeles?** Si es así, use una vista de lista en su lugar.

**Listas de selección única**

-   **¿Se usa el control para elegir una opción de una lista de valores mutuamente excluyentes?** Si no es así, usa otro control. Para elegir varias opciones, use una lista de selección múltiple estándar, lista de casillas, generador de listas o agregar o quitar lista en su lugar.
-   **¿Hay una opción predeterminada recomendada para la mayoría de los usuarios en la mayoría de las situaciones?** ¿Está viendo la opción seleccionada mucho más importante que ver las alternativas? Si es así, considere la posibilidad de usar una [lista desplegable](/windows/desktop/uxguide/ctrl-drop) si no desea animar a los usuarios a realizar cambios ocultando las alternativas.

![captura de pantalla de la calidad máxima como botón predeterminado ](images/ctrl-list-boxes-image2.png)

En este ejemplo, la calidad de color más alta es la mejor opción para la mayoría de los usuarios, por lo que una lista desplegable es una buena opción para minimizar las alternativas.

-   **¿La lista requiere interacción constante?** Si es así, use una lista de selección única para simplificar la interacción.

![captura de pantalla de la lista de opciones, como texto sin formato ](images/ctrl-list-boxes-image3.png)

En este ejemplo, los usuarios cambian constantemente el elemento seleccionado en la lista Mostrar elementos para establecer los colores de primer plano y de fondo. El uso de una lista desplegable en este caso sería muy tedioso.

-   **¿La configuración parece una cantidad relativa? ¿Los usuarios se beneficiarán de los comentarios instantáneos** sobre el efecto de los cambios de configuración? Si es así, considere la posibilidad de usar un [control deslizante](ctrl-sliders.md) en su lugar.
-   **¿Hay una relación jerárquica significativa entre los elementos de la lista?** Si es así, utilice en su lugar un control de [vista de árbol](ctrl-tree-views.md) .
-   **¿El espacio de pantalla es Premium?** Si es así, use una lista desplegable en su lugar porque el espacio de pantalla utilizado es fijo e independiente del número de elementos de lista.

**Listas de selección múltiple estándar y listas de casillas**

-   **¿Es esencial la selección múltiple de la tarea o se usa habitualmente?** Si es así, use una lista de casillas para hacer que la selección múltiple sea obvia, especialmente si los usuarios de destino no están avanzados. Muchos usuarios no saben que una lista de selección múltiple estándar admite la selección múltiple. Use una lista de selección múltiple estándar si las casillas dibujan mucha atención en la selección múltiple o el resultado es demasiado confuso.
-   **¿Es importante la estabilidad de la selección múltiple?** Si es así, use una lista de casillas, un generador de listas o agregar o quitar lista, porque al hacer clic en solo se cambian los elementos de uno en uno. Con una lista de selección múltiple estándar, es muy fácil borrar todas las selecciones incluso accidentalmente.
-   **¿Se usa el control para elegir cero o más elementos de una lista de valores?** Si no es así, usa otro control. Para elegir un elemento, utilice en su lugar una lista de selección única.

**Listas de vista previa**

-   **¿Son más fáciles de seleccionar las opciones con imágenes que solo con texto?** Si es así, use una lista de vista previa.

**Enumerar generadores y agregar o quitar listas**

-   **¿Se usa el control para elegir cero o más elementos de una lista de valores?** Si no es así, usa otro control. Para elegir un elemento, utilice en su lugar una lista de selección única.
-   **¿Es importante el orden de los elementos seleccionados?** En ese caso, el generador de listas y agregar o quitar patrones de lista admiten el orden, mientras que los otros patrones de selección múltiple no lo hacen.
-   **¿Es importante para los usuarios ver un resumen de todos los elementos seleccionados?** Si es así, el generador de listas y los patrones de la lista Agregar o quitar muestran solo los elementos seleccionados, mientras que los otros patrones de selección múltiple no lo hacen.
-   **¿Las opciones posibles son sin restricciones?** Si es así, use una lista de agregar o quitar para que los usuarios puedan elegir valores que no están actualmente en la lista.
-   **¿Se va a agregar un valor a la lista para requerir un cuadro de diálogo especializado para elegir objetos?** Si es así, use una lista Agregar o quitar y muestre el cuadro de diálogo cuando los usuarios haga clic en Agregar.
-   **¿El espacio de pantalla es Premium?** Si es así, use una lista de agregar o quitar en su lugar porque utiliza menos espacio de pantalla y no muestra siempre el conjunto de opciones.

En los cuadros de lista, **el número de elementos de la lista no es un factor para elegir el control** , ya que se escalan de miles de elementos hasta uno para las listas de selección única (y ninguno para las listas de selección múltiple). Dado que los cuadros de lista se pueden usar para los datos, es posible que el número de elementos no se conozca de antemano.

**Nota:** A veces, un control que se parece a un cuadro de lista se implementa mediante una vista de lista y viceversa. En tales casos, aplique las directrices basadas en el uso, no en la implementación.

## <a name="usage-patterns"></a>Patrones de uso

Los cuadros de lista tienen varios patrones de uso:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Listas de selección única</strong> Permitir a los usuarios seleccionar un elemento cada vez. <br/></td>
<td><img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br/> En este ejemplo, los usuarios solo pueden seleccionar un elemento para mostrar.<br/></td>
</tr>
<tr class="even">
<td><strong>Listas de selección múltiple estándar</strong> Permitir a los usuarios seleccionar cualquier número de elementos, incluido ninguno.<br/></td>
<td>Las listas de selección múltiple estándar tienen exactamente la misma apariencia que las listas de selección única, por lo que no hay ninguna pista visual de que un cuadro de lista admita la selección múltiple. Dado que los usuarios tienen que detectar esta capacidad, este patrón de lista se utiliza mejor para las tareas en las que la selección múltiple no es esencial y rara vez se usa. <br/> Hay dos modos diferentes de selección múltiple: <a href="glossary.md">varios</a> y <a href="glossary.md">extendidos</a>. El <strong>modo de selección extendida</strong> es mucho más común, donde la selección se puede extender arrastrando o presionando Mayús + clic y Ctrl + clic para seleccionar grupos de valores contiguos y no adyacentes, respectivamente. En el <strong>modo de selección múltiple</strong>, al hacer clic en cualquier elemento, se alterna su estado de selección independientemente de las teclas Mayús y Ctrl. Dado este comportamiento inusual, el modo de selección múltiple está en desuso y, en su lugar, se deben utilizar listas de casillas.<br/> <img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br/> En este ejemplo, los usuarios pueden seleccionar cualquier número de elementos mediante el modo de selección múltiple.<br/></td>
</tr>
<tr class="odd">
<td><strong>Listas de casillas</strong> Como los cuadros de lista de selección múltiple estándar, las listas de casillas permiten a los usuarios seleccionar cualquier número de elementos, incluido ninguno.<br/></td>
<td>A diferencia de las listas de selección múltiple estándar, las casillas indican claramente que es posible la selección múltiple. Use este patrón de lista para las tareas en las que la selección múltiple es fundamental o se usa con frecuencia. <br/> <img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br/> En este ejemplo, los usuarios suelen seleccionar más de un elemento para que se utilice una lista de casillas.<br/> Dada esta indicación clara de selección múltiple, podría suponer que las listas de casillas son preferibles a las listas de selección múltiple estándar. En la práctica, pocas tareas requieren selección múltiple o la usan en gran medida. el uso de una lista de casillas en tales casos da mucha atención a la selección. Por consiguiente, <strong>las listas de selección múltiple estándar son mucho más comunes.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>Listas de vista previa</strong> Puede ser una selección única o múltiple, pero muestran una vista previa del efecto de la selección en lugar de solo texto.<br/></td>
<td><img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br/> En este ejemplo, una vista previa de cada opción muestra claramente el efecto de la elección, que es más eficaz que usar solo texto.<br/></td>
</tr>
<tr class="odd">
<td><strong>Enumerar generadores</strong> Permitir a los usuarios crear una lista de opciones agregando un elemento a la vez y, opcionalmente, estableciendo el orden de la lista.<br/></td>
<td>Un generador de listas consta de dos listas de selección única: la lista de la izquierda es un conjunto fijo de opciones y la lista de la derecha es la lista que se está compilando. Hay dos botones de comando entre las listas: <br/>
<ul>
<li>Botón <strong>Agregar</strong> que mueve la opción seleccionada actualmente a la lista que se va a compilar, insertada antes del elemento seleccionado. (Hacer doble clic en un elemento de opción tiene el mismo efecto).</li>
<li>Botón <strong>quitar</strong> que quita el elemento seleccionado de la lista de elementos compilados y lo devuelve a la lista de opciones. (Hacer doble clic en un elemento de la lista de compilación tiene el mismo efecto). La lista compilada puede tener opcionalmente comandos <strong>subir</strong> y <strong>bajar</strong> para ordenar los elementos de la lista.</li>
</ul>
<img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br/> En este ejemplo, se utiliza un generador de listas para crear una barra de herramientas seleccionando elementos de un conjunto de opciones disponibles y estableciendo su orden.<br/></td>
</tr>
<tr class="even">
<td><strong>Agregar o quitar listas</strong> Permite a los usuarios crear una lista de opciones mediante la adición de uno o varios elementos a la vez y, opcionalmente, establecer el orden de la lista (como los generadores de listas).<br/></td>
<td>A diferencia de un generador de listas, al hacer clic en <strong>Agregar</strong> se muestra un cuadro de diálogo para seleccionar los elementos que se van a agregar a la lista. El uso de un cuadro de diálogo independiente permite una gran flexibilidad a la hora de elegir elementos. puede utilizar un selector de objetos especializado o incluso un cuadro de diálogo común. En comparación con el generador de listas, esta variación es más compacta, pero requiere un poco más de esfuerzo para agregar elementos. <br/> <img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br/> En este ejemplo, los usuarios pueden agregar o quitar herramientas de un menú, así como establecer el orden.<br/> Aunque el generador de listas y agregar o quitar patrones de lista son significativamente más pesados que las otras listas de selección múltiple, ofrecen dos ventajas únicas:<br/>
<ul>
<li>Los usuarios tienen control sobre el orden de la lista, tanto al compilar la lista como después.</li>
<li>Los usuarios pueden revisar un resumen de los elementos seleccionados, lo que puede suponer una ventaja significativa si el número de opciones es grande.</li>
</ul>
Sus desventajas son que requieren mucho más espacio en la pantalla y pueden resultar difíciles de usar al crear una lista grande de elementos desde cero. Por lo tanto, se usan mejor para crear listas cortas o modificar listas que ya existen.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Ordenar los elementos de la lista en un orden lógico,** como agrupar las opciones relacionadas, colocando los elementos que se usan con más frecuencia primero o usando el orden alfabético. Ordenar nombres en orden alfabético, números en orden numérico y fechas en orden cronológico. Las listas con 12 o más elementos se deben ordenar alfabéticamente para facilitar la búsqueda de elementos.

**Correcto:** ![ captura de pantalla de la alineación (izquierda, centro, derecha) ](images/ctrl-list-boxes-image10.png)

En este ejemplo, los elementos del cuadro de lista se ordenan por su relación espacial.

**Incorrecto:** ![ captura de pantalla de lista desorganizada ](images/ctrl-list-boxes-image11.png)

En este ejemplo, hay muchos elementos de lista que se deben ordenar en orden alfabético.

**Correcto:** ![ captura de pantalla de la lista alfabética ](images/ctrl-list-boxes-image12.png)

En este ejemplo, los elementos de lista son más fáciles de encontrar porque se ordenan en orden alfabético. Sin embargo, el elemento "todos los productos de Windows" se encuentra al principio de la lista, independientemente de su criterio de ordenación.

-   **Coloque las opciones que representan todos o ninguno al principio de la lista**, independientemente del criterio de ordenación de los elementos restantes.
-   **Incluya las opciones de meta entre paréntesis.**

![captura de pantalla de la lista desplegable con ninguno seleccionado ](images/ctrl-list-boxes-image13.png)

En este ejemplo, "(None)" es una metaopción porque no es un valor válido para la opción, sino que indica que no se está usando la opción en sí.

-   **No tener elementos de lista en blanco use las opciones meta-Options.** Los usuarios no saben cómo interpretar los elementos en blanco, mientras que el significado de las metaopciones es explícito.

**Incorrecto:** ![ captura de pantalla de la lista desplegable con la opción en blanco seleccionada ](images/ctrl-list-boxes-image14.png)

En este ejemplo, el significado del elemento en blanco no está claro.

**Correcto:** ![ captura de pantalla de la lista desplegable con ninguno seleccionado ](images/ctrl-list-boxes-image13.png)

En este ejemplo, se utiliza la metaopción "(None)" en su lugar.

### <a name="interaction"></a>Interacción

-   **Considere la posibilidad de proporcionar un comportamiento de doble clic.** Hacer doble clic debe tener el mismo efecto que seleccionar un elemento y ejecutar el comando predeterminado.
-   **Haga que el comportamiento de doble clic sea redundante.** Siempre debe haber un botón de comando o un comando de menú contextual que tenga el mismo efecto.
-   **Si los usuarios no pueden hacer nada con los elementos seleccionados, no permita la selección.**

**Correcto:** ![ captura de pantalla de la lista de cambios del asistente completada ](images/ctrl-list-boxes-image15.png)

Este cuadro de lista muestra una lista de solo lectura de cambios; no es necesario seleccionar.

-   **Al deshabilitar un cuadro de lista, deshabilite también las etiquetas y los botones de comando asociados.**
-   **No use el cambio del elemento seleccionado en un cuadro de lista para:**
    -   Ejecutar comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar de forma dinámica otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar dichos eventos). **Excepción:** Puede cambiar de forma dinámica el texto estático que se usa para describir el elemento seleccionado.

**Aceptable:** ![ captura de pantalla de los detalles del elemento de lista seleccionado ](images/ctrl-list-boxes-image16.png)

En este ejemplo, el cambio del elemento seleccionado cambia la descripción.

-   **Evite el desplazamiento horizontal.** Las listas de varias columnas se basan en el desplazamiento horizontal, que suele ser más difícil de usar que el desplazamiento vertical. Las listas de varias columnas que requieren desplazamiento horizontal se pueden usar cuando se tienen muchos elementos ordenados alfabéticamente y suficiente espacio de pantalla para un control ancho.

**Aceptable:** ![ captura de pantalla de la lista de carpetas en el explorador de Windows ](images/ctrl-list-boxes-image17.png)

En este ejemplo, se usan varias columnas que requieren desplazamiento horizontal porque hay muchos elementos y una gran cantidad de espacio de pantalla disponible para un control ancho.

### <a name="multiple-selection-lists"></a>Listas de selección múltiple

-   **Considere la posibilidad de mostrar el número de elementos seleccionados debajo de la lista,** especialmente si es probable que los usuarios seleccionen varios elementos. Esta información no solo proporciona comentarios útiles, sino que también indica claramente que el cuadro de lista admite varias selecciones.

![captura de pantalla del cuadro de lista con cuatro elementos seleccionados ](images/ctrl-list-boxes-image5.png)

En este ejemplo, el número de elementos seleccionados se muestra debajo de la lista.

-   Puede proporcionar otras métricas de selección que podrían ser más significativas, como los recursos necesarios para las selecciones.

![captura de pantalla de la lista de las características de Windows ](images/ctrl-list-boxes-image18.png)

En este ejemplo, el espacio en disco necesario para instalar los componentes es más significativo que el número de elementos seleccionados.

-   Si hay muchos elementos de lista y selecciona o borra todos ellos, es probable que se agreguen los botones de comando Seleccionar todo y borrar todo.
-   En el caso de las listas de selección múltiple estándar, no use el modo de selección múltiple porque este modo de selección está en desuso. Para un comportamiento equivalente, use una lista de casillas en su lugar.

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y la opción más segura de forma predeterminada.** Si seguridad y seguridad no son factores, seleccione la opción más probable o cómoda.

**Excepción:** No seleccione ningún elemento si el control representa una propiedad en un [Estado mixto](glossary.md), lo que sucede cuando se muestra una propiedad para varios objetos que no tienen la misma configuración.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de tamaño y espaciado de cuadro de lista ](images/ctrl-list-boxes-image19.png)

Ajuste de tamaño y espaciado recomendados para los cuadros de lista.

-   **Elija un ancho de cuadro de lista adecuado para los datos válidos más largos.** Los cuadros de lista estándar no se pueden desplazar horizontalmente, de modo que los usuarios solo pueden ver lo que está visible en el control.
-   **Incluya un 30% adicional** (hasta el 200 por ciento para el texto más corto) para cualquier texto (pero no para los números) que se traducirá.
-   **Elija un alto de cuadro de lista que muestre un número entero de elementos.** Evite truncar elementos verticalmente.
-   **Elija un alto del cuadro de lista que elimine el desplazamiento vertical innecesario.** Los cuadros de lista deben mostrarse entre 3 y 20 elementos sin necesidad de desplazarse. Considere la posibilidad de hacer un cuadro de lista ligeramente mayor si al hacerlo se elimina la barra de desplazamiento vertical. Las listas con potencialmente muchos elementos deben mostrar al menos cinco elementos para facilitar el desplazamiento al mostrar más elementos a la vez y facilitar la posición de la barra de desplazamiento.
-   **Si los usuarios se benefician de aumentar el tamaño del cuadro de lista, haga que el cuadro de lista y su ventana primaria sean ajustables.** Esto permite a los usuarios ajustar el tamaño del cuadro de lista según sea necesario. Sin embargo, los cuadros de lista de tamaño variable no deben mostrar menos de tres elementos.

## <a name="labels"></a>Etiquetas

**Etiquetas de control**

-   Todos los cuadros de lista necesitan etiquetas. Escribir la etiqueta como una palabra o frase, no como una oración; Use un signo de dos puntos al final de la etiqueta.

**Excepción:** Omita la etiqueta si es simplemente una resituación de la [instrucción principal](glossary.md)de un cuadro de diálogo. En este caso, la instrucción principal toma el signo de dos puntos (a menos que sea una pregunta) y una clave de acceso.

**Aceptable:** ![ captura de pantalla de la lista con una etiqueta redundante ](images/ctrl-list-boxes-image20.png)

En este ejemplo, la etiqueta del cuadro de lista solo reindica la instrucción principal.

**Mejor:** ![ captura de pantalla de la lista de sin etiqueta redundante ](images/ctrl-list-boxes-image21.png)

En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma el signo de dos puntos y la tecla de acceso.

-   Si un cuadro de lista está subordinado a un botón de radio o una casilla y se introduce en la etiqueta de ese control y termina con un signo de dos puntos, no incluya una etiqueta adicional en el control de cuadro de lista.

![captura de pantalla de un botón y una lista con la misma etiqueta ](images/ctrl-list-boxes-image22.png)

En este ejemplo, el cuadro de lista está subordinado a un botón de radio y comparte su etiqueta.

-   Asigne una [clave de acceso](glossary.md)única. Para obtener instrucciones, consulte [teclado](inter-keyboard.md).
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Coloque la etiqueta a la izquierda o encima del control y alinee la etiqueta con el borde izquierdo del control.
    -   Si la etiqueta está a la izquierda, alinee verticalmente el texto de la etiqueta con la primera línea de texto del control.

**Correcto:** ![ captura de pantalla de la lista con la etiqueta alineada a la izquierda sobre la ](images/ctrl-list-boxes-image23.png)![ captura de pantalla de la lista con la etiqueta alineada de texto a la izquierda ](images/ctrl-list-boxes-image24.png)

En estos ejemplos, la etiqueta en la parte superior se alinea con el borde izquierdo del cuadro de lista y la etiqueta de la izquierda se alinea con el texto del cuadro de lista.

**Incorrecto:** ![ captura de pantalla de la lista con la etiqueta alineada de texto encima ](images/ctrl-list-boxes-image25.png)![ de la captura de pantalla de la lista con la etiqueta alineada en la parte izquierda ](images/ctrl-list-boxes-image26.png)

En estos ejemplos incorrectos, la etiqueta en la parte superior se alinea con el texto del cuadro de lista y la etiqueta de la izquierda se alinea con la parte superior del cuadro de lista.

-   En el caso de los cuadros de lista de selección múltiple, use una etiqueta que indique claramente que se puede seleccionar varias. Las etiquetas de la lista de casillas pueden ser menos explícitas.

**Correcto:** ![ captura de pantalla de la lista con seleccionar una o más etiquetas ](images/ctrl-list-boxes-image27.png)

En este ejemplo, la etiqueta indica claramente que es posible la selección múltiple.

**Incorrecto:** ![ captura de pantalla del cuadro de lista con etiqueta de complementos ](images/ctrl-list-boxes-image28.png)

En este ejemplo, la etiqueta no proporciona información obvia sobre la selección múltiple.

**Lo mejor:** ![ captura de pantalla de la lista de cosillas con etiqueta de complementos ](images/ctrl-list-boxes-image29.png)

En este ejemplo, las casillas de verificación indican claramente que la selección múltiple es posible, por lo que la etiqueta no tiene que ser explícita.

-   Puede especificar unidades (segundos, conexiones, etc.) entre paréntesis después de la etiqueta.

**Texto de la opción**

-   Asigne un nombre único a cada opción.
-   Use [mayúsculas y minúsculas](glossary.md), a menos que un elemento sea un nombre adecuado.
-   Escriba la etiqueta como una palabra o frase, no como una frase, y no use ningún signo de puntuación final.
-   Use frases paralelas e intente mantener la longitud sobre el mismo para todas las opciones.

**Texto de instrucciones y complementos**

-   Si necesita agregar texto informativo sobre un cuadro de lista, agréguelo encima de la etiqueta. Use frases completas con una puntuación final.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   La información adicional que sea útil pero no necesaria debe mantenerse en breve. Coloque este texto entre paréntesis entre la etiqueta y el signo de dos puntos, o sin paréntesis debajo del control.

![captura de pantalla de la lista de casillas y el texto descriptivo ](images/ctrl-list-boxes-image30.png)

En este ejemplo, el texto complementario se coloca debajo de la lista.

## <a name="documentation"></a>Documentación

Al hacer referencia a los cuadros de lista:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso o el signo de dos puntos. Incluya la lista de palabras. No haga referencia a un cuadro de lista como un cuadro de lista o un campo.
-   En el caso de los elementos de lista, use el texto exacto del elemento, incluido el uso de mayúsculas.
-   En programación y otra documentación técnica, consulte cuadros de lista como cuadros de lista. En cualquier otro lugar, use List.
-   Para describir la interacción del usuario, use Select.
-   Siempre que sea posible, dé formato a la etiqueta y a los elementos de lista usando texto en negrita. De lo contrario, coloque la etiqueta y los elementos entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la lista **ir a** , seleccione **marcador**.

