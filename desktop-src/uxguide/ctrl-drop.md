---
title: Cuadros combinados de listas desplegables
description: Con una lista desplegable o un cuadro combinado, los usuarios pueden elegir entre una lista de valores mutuamente excluyentes.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 79a50f4033223030fd135bb0fcfa247e07f0693d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267527"
---
# <a name="drop-down-lists--combo-boxes"></a>Listas desplegables de & combinados

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con una lista desplegable o un cuadro combinado, los usuarios pueden elegir entre una lista de valores mutuamente excluyentes. Los usuarios pueden elegir una sola opción. Con una lista desplegable estándar, los usuarios se limitan a las opciones de la lista, pero con un cuadro combinado pueden especificar una opción que no esté en la lista.

![captura de pantalla del cuadro combinado de tiempo de recordatorio ](images/ctrl-drop-image1.png)

Un cuadro combinado típico.

A medida que lea este artículo, es importante comprender los siguientes términos:

-   Un cuadro de lista estándar es un cuadro que contiene una lista de varios elementos, con varios elementos visibles.
-   Una lista desplegable es una lista en la que el elemento seleccionado siempre está visible y los demás están visibles a petición haciendo clic en un botón desplegable.
-   Un cuadro combinado es una combinación de un cuadro de lista estándar o una lista desplegable y un cuadro de texto [editable,](ctrl-text-boxes.md)lo que permite a los usuarios escribir un valor que no está en la lista.
    -   Una lista desplegable editable es una combinación de una lista desplegable y un cuadro de texto editable.
    -   Un cuadro de lista editable es una combinación de un cuadro de lista estándar y un cuadro de texto editable.

> [!Note]  
> Las directrices relacionadas [con el](vis-layout.md) diseño se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa el control para elegir una opción de una lista de valores mutuamente excluyentes?** Si no es así, usa otro control. Para elegir varias opciones, use en su lugar una lista estándar de selección [múltiple,](ctrl-list-boxes.md)una lista de casillas, un generador de listas o agregar o quitar lista.
-   **¿Son los comandos de opciones?** Si es así, use un [botón de menú o](ctrl-command-buttons.md) un botón de división en su lugar. Use listas desplegables y cuadros combinados para objetos (nombres) o atributos (adjetivos), pero no comandos (verbos).
-   **¿La lista presenta datos, en lugar de opciones de programa?** En cualquier caso, una lista desplegable o un cuadro combinado es una opción adecuada. Por el contrario, [los botones de](ctrl-radio-buttons.md) radio solo son adecuados para un número reducido de opciones de programa.

**Listas desplegables**

-   **¿Hay una opción predeterminada que se recomienda para la mayoría de los usuarios en la mayoría de las situaciones?** ¿Es mucho más importante ver la opción seleccionada que ver las alternativas? Considere la posibilidad de usar una lista desplegable si no desea animar a los usuarios a realizar cambios ocultando las alternativas. Si no es así, considere los botones de radio, una lista de selección única o un cuadro de lista editable, que dan más énfasis a las opciones alternativas.

    ![captura de pantalla de la máxima calidad como botón predeterminado ](images/ctrl-drop-image2.png)

    En este ejemplo, la calidad de color más alta es la mejor opción para la mayoría de los usuarios, por lo que una lista desplegable es una buena opción para bajar las alternativas.

-   **¿Desea llamar la atención sobre la opción?** Si es así, considere los botones de radio, una lista de selección única o un cuadro de lista editable, que tienden a llamar más la atención al tomar más espacio en la pantalla. Dado que las listas desplegables son compactas, son buenas opciones para las opciones que desea reducir el tamaño.
-   **¿El espacio de pantalla es premium?** Si es así, use una lista desplegable porque el espacio de pantalla utilizado es fijo e independiente del número de opciones.
-   **¿Hay otras listas desplegables en la ventana?** Si es así, considere la posibilidad de usar una lista desplegable para mantener la coherencia.

**Listas desplegables editables**

Además de los principios que se proporcionan para las listas desplegables, también se aplican los siguientes:

-   **¿Están restringidas las posibles opciones?** Si es así, use una lista desplegable normal en su lugar. Los cuadros combinados son para la entrada sin restricciones, en la que es posible que los usuarios deban escribir un valor que no esté actualmente en la lista. Dado que la entrada no está entrenada, si los usuarios escriben texto que no es válido, debe controlar el error con un mensaje de error.
-   **¿Puede enumerar las opciones más probables de antemano?** Si no es así, use un cuadro de texto en su lugar.
-   **¿Se usa la lista desplegable para enumerar la entrada del usuario anterior?** A menos que los usuarios necesiten revisar la lista completa de la entrada anterior, use un cuadro de texto con la opción autocompletar en su lugar.

    ![captura de pantalla del cuadro de diálogo ejecutar con la lista desplegable ](images/ctrl-drop-image3.png)

    En este ejemplo, es posible que los usuarios deban revisar su entrada anterior, por lo que una lista desplegable editable es una buena opción.

    ![captura de pantalla de Outlook para línea y autocompletar ](images/ctrl-drop-image4.png)

    En este ejemplo, un cuadro de texto con autocompletar es una buena opción.

-   **¿Necesitarán los usuarios ayuda para seleccionar valores válidos?** Si es así, use un cuadro de texto con [un botón Examinar](ctrl-command-buttons.md) en su lugar.

    ![captura de pantalla del botón De Outlook a línea y examinar ](images/ctrl-drop-image5.png)

    En este ejemplo, los usuarios pueden hacer clic en "Para" para ayudarles a seleccionar valores válidos.

-   **¿Es importante animar a los usuarios a revisar las opciones alternativas o invitar a cambios?** Si es así, considere la posibilidad de usar un cuadro de lista editable en su lugar. Con una lista desplegable editable, los usuarios no conocerán las alternativas hasta que se coloque la lista.
-   **¿Es necesario que los usuarios busquen rápidamente un elemento en una lista grande?** (Solo Win32) Si es así, use un cuadro combinado porque los usuarios pueden seleccionar un elemento escribiendo su nombre completo. Por el contrario, la lista desplegable Win32 selecciona elementos basados solo en el último carácter escrito (por lo que escribir "Jun" en una lista de meses coincidiría con noviembre, no con junio). En este caso, use un cuadro combinado incluso si las opciones posibles están restringidas.

**Cuadros de lista editables**

-   **¿Están restringidas las posibles opciones?** Si es así, use una lista de selección única o una lista desplegable normal en su lugar. Los cuadros combinados son para la entrada sin restricciones, donde es posible que los usuarios necesiten escribir un valor que no esté actualmente en la lista. Dado que la entrada no está entrenada, si los usuarios escriben texto que no es válido, debe controlar el error con un mensaje de error.
-   **¿Puede enumerar las opciones más probables de antemano?** Si no es así, use un cuadro de texto en su lugar.
-   **¿Es importante animar a los usuarios a revisar las opciones alternativas o invitar a cambios?** Si no es así, considere una lista desplegable modificable en su lugar.
-   **¿Desea llamar la atención sobre la opción?** Si no es así, considere una lista desplegable modificable en su lugar. Dado que las listas desplegables son compactas, son buenas opciones para las opciones que desea reducir el tamaño.
-   **¿El espacio de pantalla es premium?** Si es así, use una lista desplegable editable porque el espacio de pantalla utilizado es fijo e independiente del número de opciones.

Para las listas desplegables, el número de elementos de la lista no es un **factor a** la hora de elegir el control porque escalan desde miles de elementos hasta llegar a uno. Las listas desplegables editables se escalan de miles de elementos a ninguno, ya que los usuarios pueden escribir un valor que no esté en la lista. Dado que las listas desplegables se pueden usar para los datos, es posible que el número de elementos no se conozca de antemano y quizás no se pueda garantizar. **Incluya siempre al menos tres elementos en cuadros de lista editables para justificar el espacio de pantalla adicional.**

## <a name="usage-patterns"></a>Patrones de uso

Las listas desplegables y los cuadros combinados tienen varios patrones de uso:



|   Uso     |    Ejemplo   |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lista desplegable una** lista desplegable estándar, con un conjunto fijo de valores predeterminados. <br/>                                 | Cuando se cierra, solo está visible el elemento seleccionado. Cuando los usuarios hacen clic en el botón desplegable, todas las opciones se vuelven visibles. Para cambiar el valor, los usuarios pueden abrir la lista y hacer clic en otro valor.<br/> ![captura de pantalla de la lista desplegable, opciones ocultas ](images/ctrl-drop-image6.png)<br/> En este ejemplo, la lista está en su estado normal.<br/> ![captura de pantalla de la lista desplegable, se muestran las opciones ](images/ctrl-drop-image7.png)<br/> En este ejemplo, se ha descartado la lista.<br/> |
| **Lista desplegable vista previa:** lista desplegable que muestra una vista previa de los resultados de la selección para ayudar a los usuarios a elegir.<br/>             | ![captura de pantalla de opciones de color y texto ](images/ctrl-drop-image8.png)<br/> En estos ejemplos, la lista desplegable muestra una vista previa de los resultados de la selección.<br/>                                                                                                                                                                                                                                                                                                                                           |
| **Lista desplegable editable:** un cuadro combinado desplegable, que permite a los usuarios escribir un valor que no está en la lista desplegable.<br/> | ![aa511458.dropdownlists27(en-us,msdn.10).png](images/ctrl-drop-image9.png)![captura de pantalla del cuadro combinado de tamaño de fuente editable ](images/ctrl-drop-image10.png)<br/> Ejemplos de una lista desplegable editable en los modos de edición y lista desplegable.<br/> Use este control cuando quiera proporcionar la flexibilidad de un cuadro de texto, pero quiera ayudar a los usuarios proporcionando una lista práctica de opciones probables.<br/>                                                                                                   |
| **La lista editable incluye** un cuadro combinado normal, que permite a los usuarios escribir un valor que no está en la lista siempre visible. <br/> | ![captura de pantalla de la lista desplegable de opciones de fuente ](images/ctrl-drop-image11.png)<br/> En estos ejemplos, siempre se muestran los cuadros de lista editables.<br/> Este control es una mejor opción que la lista desplegable editable cuando es importante animar a los usuarios a revisar las opciones alternativas o invitar a cambios.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No use el cambio de una lista desplegable** o un cuadro combinado a :
    -   Realice comandos.
    -   Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.
    -   Mostrar dinámicamente otros controles relacionados con el control seleccionado[(los](inter-accessibility.md) lectores de pantalla no pueden detectar tales eventos).

### <a name="presentation"></a>Presentación

-   **Ordenar elementos de lista en un orden lógico,** como agrupar opciones muy relacionadas, colocar primero las opciones más comunes o usar el orden alfabético. Ordene los nombres en orden alfabético, los números en orden numérico y las fechas en orden cronológico. Las listas con 12 o más elementos deben ordenarse alfabéticamente para facilitar la búsqueda de elementos.

    **Correcto:** ![ captura de pantalla de la lista desplegable lógica ](images/ctrl-drop-image12.png)

    En este ejemplo, los elementos de lista se ordenan por su relación espacial.

    **Incorrecto:** ![ captura de pantalla de la lista desplegable desorganizada ](images/ctrl-drop-image13.png)

    En este ejemplo, hay tantos elementos de lista que deben ordenarse en orden alfabético.

    **Correcto:** ![ captura de pantalla de la lista desplegable alfabética ](images/ctrl-drop-image14.png)

    En este ejemplo, los elementos de lista se ordenan en orden alfabético, excepto la opción que representa todos los elementos.

-   **Coloque las opciones que representan All o None al principio de la lista, independientemente del criterio de ordenación de los elementos restantes.**
-   **Incluya las meta-opciones entre paréntesis.**

    ![Captura de pantalla que muestra una lista desplegable con la opción "(None)" seleccionada.](images/ctrl-drop-image15.png)

    En este ejemplo, "(None)" es una meta-opción porque no es un valor válido para la opción, sino que describe que la propia opción no se está utilizando.

-   **Al deshabilitar una lista desplegable o un cuadro combinado, deshabilite también las etiquetas asociadas y los botones de comando.**

### <a name="drop-down-lists"></a>Listas desplegables

-   Cuando se usa una sola lista desplegable para cambiar la vista de un control asociado, cambie la vista inmediatamente después de la selección en lugar de requerir un **botón de comando independiente.** Use un botón de comando independiente solo si la lista tarda una cantidad significativa de tiempo en representarse. Sin embargo, los encabezados de lista [y los botones de](ctrl-command-buttons.md) menú son los controles preferidos para este propósito.
-   **No tiene elementos de lista en blanco que** usen **metapádes en su lugar.** Los usuarios no saben cómo interpretar elementos en blanco, mientras que el significado de las meta-opciones es explícito.

    **Correcto:** ![ captura de pantalla de la lista desplegable con ninguna seleccionada ](images/ctrl-drop-image16.png)

    **Incorrecto:** ![ captura de pantalla de la lista desplegable con el espacio en blanco seleccionado ](images/ctrl-drop-image17.png)

    En el ejemplo incorrecto, el significado de la opción en blanco no es claro.

### <a name="preview-drop-down-lists"></a>Listas desplegables de vista previa

-   **Use vistas previas en los elementos de lista cuando sea mejor mostrar con imágenes que describir el uso de texto solo.**

    ![captura de pantalla de la lista desplegable de fuentes vista previa ](images/ctrl-drop-image18.png)

    En este ejemplo, la versión preliminar explica las opciones mucho mejor que el texto por sí solo.

-   **No use iconos innecesarios y poco útiles en las versiones preliminares.**

    **Incorrecto:** ![ captura de pantalla de la lista desplegable de etiquetas con iconos ](images/ctrl-drop-image19.png)

    En este ejemplo, los iconos de vista previa no son necesarios porque no comunican ninguna información.

### <a name="combo-boxes"></a>Cuadros combinados

-   **Limite la longitud del texto de entrada cuando pueda.** Por ejemplo, si la entrada válida es un número entre 0 y 999, use un cuadro combinado que esté limitado a tres caracteres.
-   **Si hay muchas opciones posibles, centre el contenido de la lista en las opciones más probables.** Dado que los usuarios pueden escribir valores que no están en la lista, los cuadros combinados no tienen que enumerar todas las opciones, solo las opciones probables o un ejemplo representativo.

    ![captura de pantalla de la lista desplegable de tamaños de fuente ](images/ctrl-drop-image10.png)

    En este ejemplo, no se muestran muchas opciones válidas, como 15 o fuentes de tamaño medio, como 9,5.

### <a name="default-values"></a>Valores predeterminados

-   **Seleccione la opción más segura (para evitar la pérdida de datos o el acceso del sistema) y la opción más segura de forma predeterminada.** Si la seguridad y la seguridad no son factores, seleccione la opción más probable o conveniente.
    -   **Excepción:** Muestra un valor predeterminado en blanco si el control representa una propiedad en un estado mixto [,](glossary.md)lo que sucede cuando se muestra una propiedad para varios objetos que no tienen la misma configuración.

## <a name="prompts"></a>Mensajes

Un aviso es una etiqueta o una instrucción corta colocada dentro de una lista desplegable editable como su valor predeterminado. A diferencia del texto estático, los mensajes desaparecen de la pantalla una vez que los usuarios escriben algo en el cuadro combinado o obtienen el foco de entrada.

![captura de pantalla de un cuadro de búsqueda ](images/ctrl-drop-image20.png)

Un aviso típico.

Use un símbolo del sistema cuando:

-   El espacio de pantalla es tan premium que no se desea usar una etiqueta o una instrucción, como en una barra de herramientas.
-   El aviso es principalmente para identificar el propósito de la lista de una manera compacta. No debe ser información fundamental que los usuarios necesiten ver mientras usan el cuadro combinado.

No use mensajes solo para dirigir a los usuarios a seleccionar algo de la lista o para hacer clic en los botones. Por ejemplo, no es necesario seleccionar una opción o escribir un nombre de archivo y, a continuación, hacer clic en Enviar.

Al usar avisos:

-   Dibuje el texto del aviso en gris cursiva y texto real en negro normal. El texto del aviso no debe confundirse con el texto real.
-   Mantenga el texto del aviso conciso. Puede usar fragmentos en lugar de oraciones completa.
-   Use [mayúsculas de estilo oración.](glossary.md)
-   No use signos de puntuación finales ni puntos suspensivos.
-   El texto del mensaje no debe ser editable y debe desaparecer una vez que los usuarios hacen clic en el cuadro de texto o se tabulan en él.
    -   **Excepción:** El mensaje se muestra si el cuadro de texto tiene el foco de entrada predeterminado y solo desaparece una vez que el usuario empieza a escribir.
-   El texto del mensaje se restaura si el cuadro de texto sigue vacío cuando pierde el foco de entrada.

**Incorrecto:** ![ captura de pantalla de seis listas desplegables editables](images/ctrl-drop-image21.png)

En este ejemplo, el espacio de la pantalla no es premium; Una vez que se rellena una lista desplegable editable, es difícil que los usuarios recuerden para qué es. y el texto del símbolo del sistema se puede editar y dibujar de la misma manera que el texto real.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla de la lista desplegable y las especificaciones ](images/ctrl-drop-image22.png)

Tamaño y espaciado recomendados para listas desplegables y cuadros combinados.

-   **Elija un ancho adecuado para los datos válidos más largos.** Las listas desplegables no se pueden desplazar horizontalmente, por lo que los usuarios solo pueden ver lo que está visible en el control. (Tenga en cuenta, sin embargo, que los cuadros combinados pueden tener habilitada la funcionalidad AutoScroll).
-   **Incluya un 30 %** adicional (hasta un 200 % para texto más corto) para cualquier texto (pero no números) que se localizará.
-   **Elija una longitud de lista que elimine el desplazamiento vertical innecesario.** Dado que las listas desplegables se muestran a petición, sus listas deben mostrar hasta 30 elementos. Los cuadros de lista editables (aquellos que no tienen un botón desplegable) deben mostrar entre 3 y 12 elementos.

## <a name="labels"></a>Etiquetas

**Etiquetas de control**

-   Escriba la etiqueta como una palabra o frase, no como una frase, y termine con dos puntos. **Excepciones:**
    -   Listas desplegables editables con avisos ubicados donde el espacio es premium.
    -   Si una lista desplegable o un cuadro combinado están subordinados a un botón de radio o a una casilla y su etiqueta termina con dos puntos, no coloque ninguna etiqueta adicional en el control.
-   Asigne una clave [de acceso única](glossary.md) para cada etiqueta. Para obtener instrucciones, vea [Teclado.](inter-keyboard.md)
-   Use [mayúsculas de estilo oración.](glossary.md)
-   Coloque la etiqueta a la izquierda del control o encima del control y alinee la etiqueta con el borde izquierdo del control. Si label está a la izquierda, alinee verticalmente el texto de la etiqueta con el texto del control.

    **Correcto:** ![ captura de pantalla de la alineación de la etiqueta de lista desplegable ](images/ctrl-drop-image23.png)

    En este ejemplo, la etiqueta se alinea correctamente con el texto del control.

    **Incorrecto:** ![ captura de pantalla de la lista desplegable alineada incorrectamente ](images/ctrl-drop-image24.png)

    En este ejemplo, la etiqueta está alineada incorrectamente con el texto del control.

-   Puede especificar unidades (segundos, conexiones, entre paréntesis) después de la etiqueta.
-   No haga que el contenido de la lista desplegable o el cuadro combinado (o su etiqueta de unidades) forma parte de una oración, porque esto no es localizable.

**Texto de la opción**

-   Asigne un nombre único a cada opción.
-   Use [mayúsculas y mayúsculas de estilo](glossary.md)oración, a menos que un elemento sea un nombre adecuado.
-   Escriba la etiqueta como una palabra o frase, no como una frase, y no use ningún signo de puntuación final.
-   Use expresiones paralelas e intente mantener la longitud aproximadamente igual para todas las opciones.

**Texto informativo**

-   Si necesita agregar texto informativo sobre una lista desplegable o un cuadro combinado, agrégrelo encima de la etiqueta. Use oraciones completas con signos de puntuación finales.
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   La información adicional que es útil, pero no necesaria, debe mantenerse corta. Coloque esta información entre paréntesis entre la etiqueta y los dos puntos, o sin paréntesis debajo del control .

    ![captura de pantalla de la lista desplegable con datos agregados ](images/ctrl-drop-image25.png)

    En este ejemplo se muestra información adicional situada debajo del control .

## <a name="documentation"></a>Documentación

Al hacer referencia a listas desplegables:

-   Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya el carácter de subrayado ni los dos puntos de la clave de acceso. incluir lista o cuadro, lo que sea más claro.
-   Para las opciones de lista, use el texto exacto de la opción, incluida su inclusión en mayúsculas.
-   En programación y otra documentación técnica, consulte listas desplegables como listas desplegables. En cualquier otro lugar, use list o box, lo que sea más claro.
-   Para describir la interacción del usuario, use click.
-   Cuando sea posible, formatee las opciones de etiqueta y lista mediante texto en negrita. De lo contrario, coloque la etiqueta y las opciones entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en la **lista Tamaño de** fuente , haga clic en Fuentes **grandes**.

Al hacer referencia a cuadros combinados:

-   Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya el carácter de subrayado ni los dos puntos de la clave de acceso. incluya el cuadro de palabras.
-   Para las opciones de lista, use el texto exacto de la opción, incluido su uso de mayúsculas y mayúsculas.
-   En programación y otra documentación técnica, consulte cuadros combinados como cuadros combinados. En cualquier otro lugar, use box.
-   Para describir la interacción del usuario, use Entrar.
-   Cuando sea posible, formatee las opciones de etiqueta y lista mediante texto en negrita. De lo contrario, coloque la etiqueta y las opciones entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en el **cuadro Fuente** , escriba la fuente que desea usar.

 

