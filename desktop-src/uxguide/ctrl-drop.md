---
title: Cuadros combinados de listas desplegables
description: Con una lista desplegable o un cuadro combinado, los usuarios pueden elegir entre una lista de valores que se excluyen mutuamente.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 646fb569cf3a7861d68d0eb885107ba12978c101
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279753"
---
# <a name="drop-down-lists--combo-boxes"></a>Listas desplegables & cuadros combinados

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con una lista desplegable o un cuadro combinado, los usuarios pueden elegir entre una lista de valores que se excluyen mutuamente. Los usuarios pueden elegir una y solo una opción. Con una lista desplegable estándar, los usuarios se limitan a las opciones de la lista, pero con un cuadro combinado pueden escribir una opción que no está en la lista.

![captura de pantalla del cuadro combinado de tiempo de recordatorio ](images/ctrl-drop-image1.png)

Cuadro combinado típico.

Es importante comprender los siguientes términos a medida que lea este artículo:

-   Un cuadro de lista estándar es un cuadro que contiene una lista de varios elementos, con varios elementos visibles.
-   Una lista desplegable es una lista en la que el elemento seleccionado está siempre visible y los demás están visibles a petición haciendo clic en un botón desplegable.
-   Un cuadro combinado es una combinación de un cuadro de lista estándar o una lista desplegable y un [cuadro de texto](ctrl-text-boxes.md)editable, lo que permite a los usuarios especificar un valor que no está en la lista.
    -   Una lista desplegable editable es una combinación de una lista desplegable y un cuadro de texto editable.
    -   Un cuadro de lista modificable es una combinación de un cuadro de lista estándar y un cuadro de texto editable.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa el control para elegir una opción de una lista de valores mutuamente excluyentes?** Si no es así, usa otro control. Para elegir varias opciones, use una [lista de selección múltiple estándar](ctrl-list-boxes.md), lista de casillas, generador de listas o agregar o quitar lista en su lugar.
-   **¿Son los comandos de opciones?** Si es así, use un [botón de menú](ctrl-command-buttons.md) o un botón de expansión en su lugar. Use listas desplegables y cuadros combinados para objetos (sustantivos) o atributos (adjetivos), pero no comandos (verbos).
-   **¿La lista presenta datos, en lugar de opciones de programa?** En cualquier caso, una lista desplegable o un cuadro combinado es una opción adecuada. Por el contrario, los [botones de radio](ctrl-radio-buttons.md) solo son adecuados para un número reducido de opciones del programa.

**Listas desplegables**

-   **¿Hay una opción predeterminada recomendada para la mayoría de los usuarios en la mayoría de las situaciones?** ¿Está viendo la opción seleccionada mucho más importante que ver las alternativas? Considere la posibilidad de usar una lista desplegable si no desea animar a los usuarios a realizar cambios ocultando las alternativas. Si no es así, tenga en cuenta los botones de radio, una lista de selección única o un cuadro de lista editable, que dan más énfasis a las opciones alternativas.

    ![captura de pantalla de la calidad máxima como botón predeterminado ](images/ctrl-drop-image2.png)

    En este ejemplo, la calidad de color más alta es la mejor opción para la mayoría de los usuarios, por lo que una lista desplegable es una buena opción para minimizar las alternativas.

-   **¿Desea atraer la atención a la opción?** Si es así, considere la posibilidad de usar botones de radio, una lista de selección única o un cuadro de lista editable, que tiende a tomar más atención mediante la obtención de más espacio en la pantalla. Dado que las listas desplegables son compactas, son buenas opciones para las opciones que desea resaltar.
-   **¿El espacio de pantalla es Premium?** Si es así, use una lista desplegable porque el espacio de pantalla utilizado es fijo e independiente del número de opciones.
-   **¿Hay otras listas desplegables en la ventana?** Si es así, considere la posibilidad de usar una lista desplegable para la coherencia.

**Listas desplegables editables**

Además de los principios que se proporcionan para las listas desplegables, también se aplica lo siguiente:

-   **¿Las opciones posibles están limitadas?** Si es así, utilice en su lugar una lista desplegable normal. Los cuadros combinados son para entradas sin restricciones, en las que es posible que los usuarios tengan que escribir un valor que no se encuentre actualmente en la lista. Dado que la entrada no está restringida, si los usuarios escriben texto que no es válido, debe controlar el error con un mensaje de error.
-   **¿Puede enumerar las opciones más probables de antemano**? En caso contrario, utilice un cuadro de texto en su lugar.
-   **¿Se usa la lista desplegable para mostrar la entrada del usuario anterior?** A menos que los usuarios tengan que revisar la lista completa de entradas anteriores, en su lugar, use un cuadro de texto con la opción Autocompletar.

    ![captura de pantalla del cuadro de diálogo Ejecutar con lista desplegable ](images/ctrl-drop-image3.png)

    En este ejemplo, es posible que los usuarios necesiten revisar su entrada anterior, por lo que una lista desplegable editable es una buena elección.

    ![captura de pantalla de Outlook para la línea y Autocompletar ](images/ctrl-drop-image4.png)

    En este ejemplo, un cuadro de texto con Autocompletar es una buena elección.

-   **¿Los usuarios necesitarán ayuda para seleccionar valores válidos?** Si es así, use un cuadro de texto con un [botón examinar](ctrl-command-buttons.md) en su lugar.

    ![captura de pantalla de Outlook para el botón de línea y de exploración ](images/ctrl-drop-image5.png)

    En este ejemplo, los usuarios pueden hacer clic en "para" para ayudarles a seleccionar valores válidos.

-   **¿Es importante animar a los usuarios a revisar las opciones alternativas o invitar a cambiar?** Si es así, considere la posibilidad de usar en su lugar un cuadro de lista modificable. Con una lista desplegable editable, los usuarios no van a tener en cuenta las alternativas hasta que se quite la lista.
-   **¿Los usuarios necesitan localizar un elemento rápidamente en una lista grande?** (Solo Win32) Si es así, use un cuadro combinado, ya que los usuarios pueden seleccionar un elemento escribiendo su nombre completo. Por el contrario, la lista desplegable Win32 selecciona elementos basados solo en el último carácter escrito (por lo que escribir "Jun" en una lista de meses coincidiría con noviembre, no con junio). En este caso, use un cuadro combinado incluso si las opciones posibles están restringidas.

**Cuadros de lista modificables**

-   **¿Las opciones posibles están limitadas?** Si es así, utilice en su lugar una lista desplegable de selección única o normal. Los cuadros combinados son para entradas sin restricciones, donde es posible que los usuarios tengan que escribir un valor que no se encuentre actualmente en la lista. Dado que la entrada no está restringida, si los usuarios escriben texto que no es válido, debe controlar el error con un mensaje de error.
-   **¿Puede enumerar las opciones más probables de antemano?** En caso contrario, utilice un cuadro de texto en su lugar.
-   **¿Es importante animar a los usuarios a revisar las opciones alternativas o invitar a cambiar?** En caso contrario, considere una lista desplegable editable.
-   **¿Desea atraer la atención a la opción?** En caso contrario, considere una lista desplegable editable. Dado que las listas desplegables son compactas, son buenas opciones para las opciones que desea resaltar.
-   **¿El espacio de pantalla es Premium?** Si es así, utilice una lista desplegable editable porque el espacio de pantalla utilizado es fijo e independiente del número de opciones.

En las listas desplegables, **el número de elementos de la lista no es un factor para elegir el control** , ya que se escalan desde miles de elementos hasta uno. Las listas desplegables editables se escalan desde miles de elementos hasta ninguno, ya que los usuarios pueden escribir un valor que no está en la lista. Dado que las listas desplegables se pueden usar para los datos, es posible que el número de elementos no se sepa de antemano y quizás no se pueda garantizar. **Incluya siempre al menos tres elementos en los cuadros de lista editables para justificar el espacio de pantalla adicional.**

## <a name="usage-patterns"></a>Patrones de uso

Las listas desplegables y los cuadros combinados tienen varios patrones de uso:



|                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lista** desplegable muestra una lista desplegable estándar, con un conjunto fijo de valores predeterminados. <br/>                                 | Cuando se cierra, solo está visible el elemento seleccionado. Cuando los usuarios hagan clic en el botón desplegable, todas las opciones estarán visibles. para cambiar el valor, los usuarios abren la lista y hacen clic en otro valor.<br/> ![captura de pantalla de la lista desplegable, opciones ocultas ](images/ctrl-drop-image6.png)<br/> en este ejemplo, la lista está en su estado normal.<br/> ![captura de pantalla de la lista desplegable, opciones mostradas ](images/ctrl-drop-image7.png)<br/> En este ejemplo, la lista se ha desplegado.<br/> |
| **Vista previa** muestra una lista desplegable que muestra una vista previa de los resultados de la selección para ayudar a los usuarios a elegir.<br/>             | ![captura de pantalla de las opciones de color y texto ](images/ctrl-drop-image8.png)<br/> En estos ejemplos, las listas desplegables muestran una vista previa de los resultados de la selección.<br/>                                                                                                                                                                                                                                                                                                                                           |
| **Lista desplegable editable** cuadro combinado desplegable, que permite a los usuarios escribir un valor que no está en la lista desplegable.<br/> | ![aa511458. dropdownlists27 (en-US, msdn. 10). png](images/ctrl-drop-image9.png)![captura de pantalla del cuadro combinado de tamaño de fuente editable ](images/ctrl-drop-image10.png)<br/> Ejemplos de una lista desplegable editable en los modos de edición y desplegable.<br/> Use este control cuando desee proporcionar la flexibilidad de un cuadro de texto, pero desea ayudar a los usuarios a proporcionar una lista adecuada de opciones probables.<br/>                                                                                                   |
| **Cuadros de lista editables** un cuadro combinado normal, que permite a los usuarios escribir un valor que no está en la lista siempre visible. <br/> | ![captura de pantalla de la lista desplegable de opciones de fuente ](images/ctrl-drop-image11.png)<br/> En estos ejemplos, siempre se muestran los cuadros de lista modificables.<br/> Este control es una opción mejor que la lista desplegable editable cuando es importante animar a los usuarios a revisar las opciones alternativas o invitar a cambiar.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No use el cambio de una lista desplegable o un cuadro combinado para**:
    -   Ejecutar comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar de forma dinámica otros controles relacionados con el control seleccionado (los[lectores de pantalla](inter-accessibility.md) no pueden detectar dichos eventos).

### <a name="presentation"></a>Presentación

-   **Ordene los elementos de la lista en un orden lógico**, como agrupar las opciones de alta relación, colocando las opciones más comunes primero o usando el orden alfabético. Ordenar nombres en orden alfabético, números en orden numérico y fechas en orden cronológico. Las listas con 12 o más elementos se deben ordenar alfabéticamente para facilitar la búsqueda de elementos.

    **Correcto:** ![ captura de pantalla de la lista desplegable lógica ](images/ctrl-drop-image12.png)

    En este ejemplo, los elementos de la lista se ordenan por su relación espacial.

    **Incorrecto:** ![ captura de pantalla de la lista desplegable desorganizada ](images/ctrl-drop-image13.png)

    En este ejemplo, hay muchos elementos de lista que deben ordenarse en orden alfabético.

    **Correcto:** ![ captura de pantalla de la lista desplegable en orden alfabético ](images/ctrl-drop-image14.png)

    En este ejemplo, los elementos de la lista se ordenan alfabéticamente, a excepción de la opción que representa todos los elementos.

-   **Coloque las opciones que representan todos o ninguno al principio de la lista, independientemente del criterio de ordenación de los elementos restantes.**
-   **Incluya las opciones de meta entre paréntesis.**

    ![Captura de pantalla que muestra una lista desplegable con la opción "(ninguno)" seleccionada.](images/ctrl-drop-image15.png)

    En este ejemplo, "(None)" es una metaopción porque no es un valor válido para la opción, sino que describe que no se usa la opción en sí.

-   **Al deshabilitar una lista desplegable o un cuadro combinado, deshabilite también las etiquetas y los botones de comando asociados.**

### <a name="drop-down-lists"></a>Listas desplegables

-   Cuando se usa una sola lista desplegable para cambiar la vista de un control asociado, **cambie la vista inmediatamente en la selección en lugar de requerir un botón de comando independiente.** Use un botón de comando independiente solo si la lista tarda bastante tiempo en representarse. Sin embargo, los encabezados de lista y los [botones de menú](ctrl-command-buttons.md) son los controles preferidos para este propósito.
-   **No tener elementos de lista en blanco** **use las opciones meta-Options**. Los usuarios no saben cómo interpretar los elementos en blanco, mientras que el significado de las metaopciones es explícito.

    **Correcto:** ![ captura de pantalla de la lista desplegable con ninguno seleccionado ](images/ctrl-drop-image16.png)

    **Incorrecto:** ![ captura de pantalla de la lista desplegable con la opción en blanco seleccionada ](images/ctrl-drop-image17.png)

    En el ejemplo incorrecto, el significado de la opción blank no es claro.

### <a name="preview-drop-down-lists"></a>Listas desplegables de vista previa

-   **Use las vistas previas en los elementos de la lista cuando sea mejor mostrar con imágenes que describir solo con texto.**

    ![captura de pantalla de la lista desplegable de fuentes vista previa ](images/ctrl-drop-image18.png)

    En este ejemplo, la vista previa explica las opciones mucho mejor que el texto por sí solo.

-   **No use iconos innecesarios e inservibles en las versiones preliminares**.

    **Incorrecto:** ![ captura de pantalla de la lista desplegable de etiquetas con iconos ](images/ctrl-drop-image19.png)

    En este ejemplo, los iconos de vista previa no son necesarios porque no comunican ninguna información.

### <a name="combo-boxes"></a>Cuadros combinados

-   **Limite la longitud del texto de entrada cuando sea posible.** Por ejemplo, si la entrada válida es un número comprendido entre 0 y 999, use un cuadro combinado que tenga un límite de tres caracteres.
-   **Si hay muchas opciones posibles, Centre el contenido de la lista en las opciones más probables**. Dado que los usuarios pueden especificar valores que no están en la lista, los cuadros combinados no tienen que mostrar todas las opciones, solo las opciones más probables o una muestra representativa.

    ![captura de pantalla de la lista desplegable de tamaños de fuente ](images/ctrl-drop-image10.png)

    En este ejemplo, no se muestran muchas opciones válidas, como 15, o bien fuentes de medio tamaño como 9,5.

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione la opción más segura (para evitar la pérdida de datos o el acceso al sistema) y la opción más segura de forma predeterminada.** Si seguridad y seguridad no son factores, seleccione la opción más probable o cómoda.
    -   **Excepción:** Muestra un valor predeterminado en blanco si el control representa una propiedad en un [Estado mixto](glossary.md), lo que sucede cuando se muestra una propiedad para varios objetos que no tienen la misma configuración.

## <a name="prompts"></a>Mensajes

Un mensaje es una etiqueta o una instrucción corta colocada dentro de una lista desplegable editable como su valor predeterminado. A diferencia del texto estático, los mensajes desaparecen de la pantalla una vez que los usuarios escriben algo en el cuadro combinado o obtienen el foco de entrada.

![captura de pantalla de un cuadro de búsqueda ](images/ctrl-drop-image20.png)

Un mensaje típico.

Use un símbolo del sistema cuando:

-   El espacio de la pantalla es tan importante que no se desea usar una etiqueta o instrucción, como en una barra de herramientas.
-   El mensaje es principalmente para identificar el propósito de la lista de manera compacta. No debe ser información fundamental que los usuarios deban ver mientras usan el cuadro combinado.

No use mensajes solo para indicar a los usuarios que seleccionen algo de la lista o haga clic en los botones. Por ejemplo, preguntar como Seleccione una opción o escribir un nombre de archivo y hacer clic en enviar no es necesario.

Cuando se utilizan mensajes:

-   Dibuje el texto del mensaje en cursiva cursiva y el texto real en negro normal. El texto del mensaje no se debe confundir con el texto real.
-   Mantenga el texto del mensaje conciso. Puede usar fragmentos en lugar de oraciones completas.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   No use signos de puntuación o puntos suspensivos de finalización.
-   El texto del mensaje no se debe editar y debe desaparecer una vez que los usuarios hacen clic en o en la pestaña en el cuadro de texto.
    -   **Excepción:** El mensaje se muestra si el cuadro de texto tiene el foco de entrada predeterminado y solo desaparece una vez que el usuario comienza a escribir.
-   El texto del mensaje se restaura si el cuadro de texto todavía está vacío cuando pierde el foco de entrada.

**Incorrecto:** ![ captura de pantalla de seis listas desplegables modificables](images/ctrl-drop-image21.png)

En este ejemplo, el espacio de la pantalla no es Premium; una vez que se rellena una lista desplegable editable, es difícil para los usuarios recordar para qué sirve; y el texto del mensaje es editable y dibujado de la misma manera que el texto real.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de la lista desplegable y especificaciones ](images/ctrl-drop-image22.png)

Ajuste de tamaño y espaciado recomendados para las listas desplegables y los cuadros combinados.

-   **Elija un ancho adecuado para los datos válidos más largos.** Las listas desplegables no se pueden desplazar horizontalmente, de modo que los usuarios solo pueden ver lo que está visible en el control. (Sin embargo, tenga en cuenta que los cuadros combinados pueden tener habilitada la funcionalidad de desplazamiento automático).
-   **Incluya un 30% adicional** (hasta el 200 por ciento para el texto más corto) para cualquier texto (pero no para los números) que se traducirá.
-   **Elija una longitud de lista que elimine el desplazamiento vertical innecesario.** Dado que las listas desplegables se muestran a petición, sus listas deben mostrar hasta 30 elementos. Los cuadros de lista modificables (los que no tienen un botón desplegable) deben mostrarse entre 3 y 12 elementos.

## <a name="labels"></a>Etiquetas

**Etiquetas de control**

-   Escriba la etiqueta como una palabra o frase, no como una frase, y termine con un signo de dos puntos. **Excepciones:**
    -   Listas desplegables editables con mensajes ubicados en los que el espacio es Premium.
    -   Si una lista desplegable o un cuadro combinado está subordinado a un botón de radio o una casilla y se introduce por la etiqueta que termina con un signo de dos puntos, no incluya una etiqueta adicional en el control.
-   Asigne una [clave de acceso](glossary.md) única para cada etiqueta. Para obtener instrucciones, consulte [teclado](inter-keyboard.md).
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Coloque la etiqueta a la izquierda o encima del control y alinee la etiqueta con el borde izquierdo del control. Si la etiqueta está a la izquierda, alinee verticalmente el texto de la etiqueta con el texto del control.

    **Correcto:** ![ captura de pantalla de la alineación de la etiqueta de la lista desplegable ](images/ctrl-drop-image23.png)

    En este ejemplo, la etiqueta se alinea correctamente con el texto del control.

    **Incorrecto:** ![ captura de pantalla de la lista desplegable alineada incorrectamente ](images/ctrl-drop-image24.png)

    En este ejemplo, la etiqueta está alineada incorrectamente con el texto del control.

-   Puede especificar unidades (segundos, conexiones, etc.) entre paréntesis después de la etiqueta.
-   No haga que el contenido de la lista desplegable o el cuadro combinado (o su etiqueta de unidades) forme parte de una frase, ya que no es localizable.

**Texto de la opción**

-   Asigne un nombre único a cada opción.
-   Use [mayúsculas y minúsculas](glossary.md), a menos que un elemento sea un nombre adecuado.
-   Escriba la etiqueta como una palabra o frase, no como una frase, y no use ningún signo de puntuación final.
-   Use frases paralelas e intente mantener la longitud sobre el mismo para todas las opciones.

**Texto informativo**

-   Si necesita agregar texto informativo sobre una lista desplegable o un cuadro combinado, agréguelo encima de la etiqueta. Use frases completas con una puntuación final.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   La información adicional que sea útil pero no necesaria debe mantenerse en breve. Coloque esta información entre paréntesis entre la etiqueta y el signo de dos puntos, o sin paréntesis debajo del control.

    ![captura de pantalla de la lista desplegable con datos agregados ](images/ctrl-drop-image25.png)

    En este ejemplo se muestra información adicional situada debajo del control.

## <a name="documentation"></a>Documentación

Al hacer referencia a las listas desplegables:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso o el signo de dos puntos. incluya una lista o un cuadro, lo que sea más claro.
-   Para las opciones de lista, use el texto de la opción exacto, incluido el uso de mayúsculas.
-   En programación y otra documentación técnica, consulte las listas desplegables como listas desplegables. En cualquier otro lugar, use List o Box, lo que sea más claro.
-   Para describir la interacción del usuario, use haga clic en.
-   Siempre que sea posible, dé formato a la etiqueta y a las opciones de lista usando texto en negrita. De lo contrario, coloque la etiqueta y las opciones entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la lista **tamaño de fuente** , haga clic en **fuentes grandes**.

Al hacer referencia a los cuadros combinados:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso o el signo de dos puntos. incluya el cuadro palabra.
-   Para las opciones de lista, use el texto exacto de la opción, incluido el uso de mayúsculas.
-   En programación y otra documentación técnica, consulte cuadros combinados como cuadros combinados. En cualquier otro lugar, use Box.
-   Para describir la interacción del usuario, use entrar.
-   Siempre que sea posible, dé formato a la etiqueta y a las opciones de lista usando texto en negrita. De lo contrario, coloque la etiqueta y las opciones entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en el cuadro **fuente** , escriba la fuente que desea utilizar.

 

