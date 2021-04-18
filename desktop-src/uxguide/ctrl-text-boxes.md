---
title: Cuadros de texto
description: Con un cuadro de texto, los usuarios pueden mostrar, escribir o modificar un texto o un valor numérico.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547270"
---
# <a name="text-boxes"></a>Cuadros de texto

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con un cuadro de texto, los usuarios pueden mostrar, escribir o modificar un texto o un valor numérico.

![captura de pantalla de un cuadro de texto y una etiqueta típicos ](images/ctrl-text-boxes-image1.png)

Cuadro de texto típico.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md), las [fuentes](vis-fonts.md)y los [globos](ctrl-balloons.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Es práctico enumerar todos los valores válidos de forma eficaz?** En caso afirmativo, considere la posibilidad de usar una lista de [selección única](ctrl-list-boxes.md), una [vista de lista](ctrl-list-views.md), una [lista](/windows/desktop/uxguide/ctrl-drop)desplegable, una lista desplegable editable o un [control deslizante](ctrl-sliders.md) .
-   **¿Los datos válidos no están restringidos completamente? O son los datos válidos restringidos solo por formato (tipos de caracteres o longitud restringida)?** Si es así, use un cuadro de texto.
-   **¿Representa el valor un tipo de datos que tiene un control común especializado?** Entre los ejemplos se incluyen la fecha, la hora o la dirección IPv4 o IPv6. Si es así, utilice el control adecuado, como un control de fecha en lugar de un cuadro de texto.
-   Si los datos son numéricos:
    -   **¿Los usuarios perciben la configuración como una cantidad relativa?** Si es así, usa un control deslizante.
    -   **¿Sería bueno que el usuario recibiera una respuesta instantánea del efecto de los cambios en la configuración?** Si es así, use un control deslizante, posiblemente junto con un cuadro de texto. Por ejemplo, los usuarios pueden elegir fácilmente un color con un control deslizante, ya que pueden ver de inmediato el efecto de los cambios en los valores de matiz, saturación o luminosidad.

## <a name="design-concepts"></a>Conceptos de diseño

Aunque los cuadros de texto tienen la ventaja de ser muy flexibles, tienen el inconveniente de tener restricciones mínimas. Las únicas restricciones en un cuadro de texto editable son:

-   Opcionalmente, puede establecer el número máximo de caracteres.
-   Opcionalmente, puede restringir la entrada solo a caracteres numéricos (0 9).
-   Si usa un [control de número](ctrl-spin-controls.md), puede limitar las opciones de control de número a valores válidos.

Aparte de su longitud y la presencia opcional de un control de número, los cuadros de texto no tienen ninguna pista visual que sugiera los valores válidos o su formato. Esto significa depender de etiquetas para transmitir esta información a los usuarios. Si los usuarios escriben texto que no es válido, debe controlar el error con un mensaje de error.

Como norma general, **debe usar el control más restringido que pueda**. Usar controles sin restricciones como cuadros de texto como último recurso. Dicho esto, al considerar las restricciones, tenga en cuenta las necesidades de los usuarios globales. Por ejemplo, un control que está restringido a Estados Unidos códigos postales no se globaliza, pero un cuadro de texto sin restricciones que acepta cualquier formato de código postal es.

## <a name="usage-patterns"></a>Patrones de uso

Un cuadro de texto es un control flexible con varios usos posibles.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Entrada de datos</strong><br/> Cuadro de texto sin restricciones de una sola línea que se usa para escribir o editar cadenas cortas.<br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> Cuadro de texto sin restricciones de una sola línea.<br/></td>
</tr>
<tr class="even">
<td><strong>Entrada de datos con formato</strong><br/> Un conjunto de cuadros de texto cortos de una sola línea y de tamaño fijo que se usan para escribir datos con un formato específico. <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> Cuadro de texto que se usa para la entrada de datos con formato.<br/>
<blockquote>
[!Note]<br />
La característica <a href="glossary.md">de salida automática</a> desplaza automáticamente el foco de entrada de un cuadro de texto al siguiente. Una desventaja de este enfoque es que los datos no se pueden copiar ni pegar como una sola unidad.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Entrada de datos asistida</strong><br/> Cuadro de texto sin restricciones de una sola línea que se usa para escribir o editar cadenas, junto con un botón de comando que ayuda a los usuarios a seleccionar valores válidos.<br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> En este ejemplo, el comando Browse ayuda a los usuarios a seleccionar valores válidos.<br/></td>
</tr>
<tr class="even">
<td><strong>Entrada de texto</strong><br/> Cuadro de texto sin restricciones y de varias líneas que se usa para escribir o editar cadenas largas. <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> Cuadro de texto sin restricciones de varias líneas.<br/></td>
</tr>
<tr class="odd">
<td><strong>Entradas numéricas</strong><br/> Cuadro de texto de una sola línea y solo numérico que se usa para escribir o editar números, con un <a href="ctrl-spin-controls.md">control de número</a> opcional para facilitar la entrada basada en el mouse. <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> Cuadro de texto que se usa para la entrada numérica.<br/> La combinación de un cuadro de texto y su control de número asociado se denomina <a href="ctrl-spin-controls.md">cuadro de número</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>Entrada de contraseña y PIN</strong><br/> Cuadro de texto sin restricciones de una sola línea que se usa para escribir contraseñas y PIN de forma segura.<br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> Cuadro de texto que se usa para escribir contraseñas.<br/></td>
</tr>
<tr class="odd">
<td><strong>Salida de datos</strong><br/> Cuadro de texto de solo una línea de solo lectura, que siempre se muestra sin borde, que se usa para mostrar cadenas cortas. <br/></td>
<td>A diferencia del texto estático, los datos que se muestran mediante un cuadro de texto se pueden desplazar (útil si los datos son más anchos que el control), se seleccionan y se copian.<br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> Cuadro de texto de solo una línea de solo lectura que se usa para mostrar los datos.<br/></td>
</tr>
<tr class="even">
<td><strong>Salida de texto</strong><br/> Cuadro de texto de solo lectura y de varias líneas que se usa para mostrar cadenas largas. <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> Cuadro de texto de solo lectura que se usa para mostrar los datos.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Al deshabilitar un cuadro de texto, deshabilite también las etiquetas asociadas, las etiquetas de instrucciones, los controles de número y los botones de comando.**
-   **Usar Autocompletar para ayudar a los usuarios a escribir datos que es probable que se usen repetidamente**. Algunos ejemplos son los nombres de usuario, las direcciones y los nombres de archivo. Sin embargo, no use la función autocompletar para cuadros de texto que pueden contener información confidencial, como contraseñas, PIN, números de tarjetas de crédito o información médica.
-   **No haga que los usuarios se desplacen innecesariamente.** Si espera que los datos sean más grandes que el cuadro de texto y puede hacer que el cuadro de texto sea más grande sin dañar el diseño, ajuste el tamaño del cuadro para eliminar la necesidad de desplazarse.

    **Incorrecto:**

    ![captura de pantalla de un cuadro de texto de nombre de equipo ](images/ctrl-text-boxes-image10.png)

    En este ejemplo, el cuadro de texto debe realizarse mucho más para controlar sus datos.

-   Barras de desplazamiento:
    -   **No coloque barras de desplazamiento horizontal en cuadros de texto de varias líneas.** En su lugar, use el desplazamiento vertical y el ajuste de línea.
    -   **No coloque ninguna barra de desplazamiento en los cuadros de texto de una sola línea.**
-   **En el caso de entradas numéricas, puede utilizar un control de número.** En entrada de texto, use una lista desplegable o una lista desplegable editable.
-   **No use la característica de salida automática excepto para la entrada de datos con formato.** El cambio de foco automático puede sorprender a los usuarios.

### <a name="editable-text-boxes"></a>Cuadros de texto modificables

-   **Limite la longitud del texto de entrada cuando sea posible.** Por ejemplo, si la entrada válida es un número comprendido entre 0 y 999, use un cuadro de texto numérico que tenga un límite de tres caracteres. Todas las partes de los cuadros de texto que usan la entrada de datos con formato deben tener una longitud fija corta.
-   **Ser flexible con formatos de datos.** Si es probable que los usuarios escriban texto con una amplia variedad de formatos, intente administrar todos los más comunes. Por ejemplo, se pueden especificar muchos nombres, números e identificadores con espacios opcionales y signos de puntuación, y las mayúsculas y minúsculas no importan a menudo.
-   Si no puede controlar los formatos más probables, solicite un formato específico mediante la entrada de datos con formato o indique los formatos válidos en la etiqueta.

    **Aceptable:**

    ![captura de pantalla de un cuadro de texto para entrada numérica ](images/ctrl-text-boxes-image11.png)

    En este ejemplo, un cuadro de texto requiere una entrada en un formato específico.

    **Manera**

    ![captura de pantalla del cuadro de texto de entrada de datos con formato ](images/ctrl-text-boxes-image12.png)

    En este ejemplo, el modelo de entrada de datos con formato se usa para requerir un formato específico.

    **Rendimiento**

    ![captura de pantalla de un cuadro de texto sin restricciones ](images/ctrl-text-boxes-image13.png)

    En este ejemplo, un cuadro de texto controla todos los formatos más probables.

-   Considere la flexibilidad de formato al elegir la longitud máxima de entrada. Por ejemplo, un número de tarjeta de crédito válido puede usar hasta 19 caracteres, por lo que limitar la longitud a cualquier valor más corto dificultaría la entrada de números con formatos más largos.
-   **No use el patrón de entrada de datos con formato si es más probable que los usuarios peguen datos largos y complejos.** En su lugar, Reserve el modelo de entrada de datos con formato para situaciones en las que es más probable que los usuarios escriban los datos.

    ![captura de pantalla de un cuadro de texto con la etiqueta: dirección IPv6 ](images/ctrl-text-boxes-image14.png)

    En este ejemplo, no se usa el modelo de entrada de datos con formato, por lo que los usuarios pueden pegar direcciones IPv6.

-   **Si es más probable que los usuarios vuelvan a escribir todo el valor, seleccione todo el texto en el foco de entrada.** Si es más probable que los usuarios editen, coloque el símbolo de intercalación al final del texto.

    ![captura de pantalla de un cuadro de texto de contraseña ](images/ctrl-text-boxes-image15.png)

    En este ejemplo, es más probable que los usuarios reemplacen a Edit, por lo que el valor completo se selecciona en el foco de entrada.

    ![captura de pantalla de un cuadro de texto para escribir palabras clave ](images/ctrl-text-boxes-image16.png)

    En este ejemplo, es más probable que los usuarios agreguen palabras clave que reemplacen el texto, por lo que el símbolo de intercalación se coloca al final del texto.

-   **Use siempre un cuadro de texto de varias líneas si los caracteres de nueva línea son entradas válidas.**
-   **Cuando el cuadro de texto es para un archivo o una ruta de acceso, proporcione siempre un botón examinar.**

### <a name="numeric-text-boxes"></a>Cuadros de texto numéricos

-   **Elija la unidad más cómoda y etiquete las unidades.** Por ejemplo, considere la posibilidad de usar milliliters en lugar de los litros (o viceversa), los porcentajes en lugar de los valores directos (o viceversa), etc.

    **Correcto:**

    ![captura de pantalla de un cuadro de texto con un litro como unidad ](images/ctrl-text-boxes-image17.png)

    En este ejemplo, la unidad tiene la etiqueta, pero requiere que los usuarios escriban números decimales.

    **Manera**

    ![captura de pantalla de un cuadro de texto con milliliters como unidad ](images/ctrl-text-boxes-image18.png)

    En este ejemplo, el cuadro de texto utiliza una unidad más cómoda.

-   **Use un control de número siempre que resulte útil.** Sin embargo, a veces los controles de giro no son prácticos, como cuando los usuarios necesitan escribir muchos números grandes. Use los controles de número cuando:
    -   Es probable que la entrada sea un número pequeño, normalmente inferior a 100.
    -   Es probable que los usuarios realicen un pequeño cambio en un número existente.
    -   Es más probable que los usuarios utilicen el mouse que el teclado.
-   **Alinear a la derecha el texto numérico siempre que:**

    -   Hay más de un cuadro de texto numérico.
    -   Los cuadros de texto están alineados verticalmente.
    -   Es probable que los usuarios agreguen o comparen los valores.

    **Correcto:**

    ![captura de pantalla de los cuadros de texto de gastos (Hotel, etc.) ](images/ctrl-text-boxes-image19.png)

    En este ejemplo, el texto numérico está alineado a la derecha para facilitar la comparación de los valores.

    **Incorrecto:**

    ![captura de pantalla de cuadros de texto para valores RGB ](images/ctrl-text-boxes-image20.png)

    En este ejemplo, el texto numérico se alinea incorrectamente a la izquierda.

-   **Alinea siempre a la derecha los valores monetarios.**
-   **No asigne ningún significado especial a valores numéricos específicos**, incluso si la aplicación usa internamente esos significados especiales. En su lugar, use las casillas o los botones de radio para una selección de usuario explícita.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta: Use-1 para deshabilitar el almacenamiento en caché ](images/ctrl-text-boxes-image21.png)

    En este ejemplo, el valor-1 tiene un significado especial.

    **Correcto:**

    ![captura de pantalla de la etiqueta de la casilla: Caching ](images/ctrl-text-boxes-image22.png)

    En este ejemplo, una casilla hace que la opción sea explícita.

### <a name="password-and-pin-input"></a>Entrada de contraseña y PIN

-   **Use siempre el control común de contraseña en lugar de crear el suyo propio.** Las contraseñas y los pin requieren un tratamiento especial para que se controle de forma segura.

Para obtener más instrucciones y ejemplos, vea [globos](ctrl-balloons.md).

### <a name="textual-output"></a>Salida de texto

-   **Considere la posibilidad de usar el color de fondo blanco del sistema para texto de solo lectura de varias líneas.** Un fondo blanco facilita la lectura del texto. Una gran cantidad de texto sobre un fondo gris desaconseja la lectura.

Para obtener más información sobre los colores de fondo, vea [fuentes](vis-fonts.md).

### <a name="data-output"></a>Salida de datos

-   **No use un borde para cuadros de texto de solo una línea de solo lectura.** El borde es una pista visual de que el texto es editable.
-   **No deshabilite cuadros de texto de una sola línea y de solo lectura.** Esto impide que los usuarios seleccionen y copien el texto en el portapapeles. También impide que los usuarios desplacen los datos si superan el tamaño de sus límites.
-   **No establezca una detención de tabulación en el cuadro de texto de solo una línea de solo lectura a menos que el usuario tenga que desplazarse o copiar el texto.**

## <a name="input-validation-and-error-handling"></a>Validación de entrada y control de errores

Dado que los cuadros de texto normalmente no están restringidos para aceptar solo entradas válidas, es posible que tenga que validar la entrada y controlar los problemas. Valide los distintos tipos de problemas de entrada de la siguiente manera:

-   Si el usuario escribe un carácter que no es válido, ignore el carácter y muestre un [globo de problema de entrada](ctrl-balloons.md) que explique los caracteres válidos.

    ![captura de pantalla del cuadro de texto clave de producto](images/ctrl-text-boxes-image23.png)

    En este ejemplo, un globo informa de un carácter de entrada incorrecto.

-   Si los datos de entrada tienen un valor o un formato que no es válido, muestre un globo de problema de entrada cuando el cuadro de texto pierda el foco de entrada.
-   Si los datos de entrada son incoherentes con otros controles de la ventana, proporcione un mensaje de error cuando se complete toda la entrada, por ejemplo, cuando los usuarios hacen clic en Aceptar para un cuadro de diálogo modal.

**No borre los datos de entrada no válidos a menos que los usuarios no puedan corregir los errores fácilmente.** Esto permite a los usuarios corregir errores sin necesidad de iniciarse. Por ejemplo, debe borrar las contraseñas y los pin incorrectos, ya que los usuarios no pueden corregirlos fácilmente.

Para obtener más instrucciones y ejemplos, consulte [mensajes de error](mess-error.md) y [globos](ctrl-balloons.md).

## <a name="prompts"></a>Mensajes

Un mensaje es una etiqueta o una instrucción corta colocada dentro de un cuadro de texto como su valor predeterminado. A diferencia del texto estático, los mensajes desaparecen de la pantalla una vez que los usuarios escriben algo en el cuadro de texto o obtienen el foco de entrada.

![captura de pantalla del cuadro de texto prompt con la etiqueta: Search ](images/ctrl-text-boxes-image24.png)

Un mensaje típico.

Use un símbolo del sistema cuando:

-   El espacio de la pantalla es tan importante que no se desea usar una etiqueta o instrucción, como en una barra de herramientas.
-   El mensaje es principalmente para identificar el propósito del cuadro de texto de una manera compacta. No debe ser información fundamental que el usuario necesite ver mientras usa el cuadro de texto.

No use mensajes solo para indicar a los usuarios que escriban algo o haga clic en los botones. Por ejemplo, no escriba el texto del mensaje que dice escriba un nombre de archivo y haga clic en enviar.

Cuando se utilizan mensajes:

-   Dibuje el texto del mensaje en gris en cursiva y el texto de entrada real en negro normal. El texto del mensaje no se debe confundir con el texto real.
-   Mantenga el texto del mensaje conciso. Puede usar fragmentos en lugar de oraciones completas.
-   Use mayúsculas de estilo de frase.
-   No use signos de puntuación o puntos suspensivos de finalización.
-   El texto del mensaje no se debe editar y debe desaparecer una vez que los usuarios hacen clic en o en la pestaña en el cuadro de texto.
    -   **Excepción:** Si el cuadro de texto tiene el foco de entrada predeterminado, se muestra el mensaje y desaparece cuando el usuario comienza a escribir.
-   El texto del mensaje se restaura si el cuadro de texto todavía está vacío cuando pierde el foco de entrada.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![figura de cuadros de texto de una línea y dos líneas ](images/ctrl-text-boxes-image25.png)

Ajuste de tamaño y espaciado recomendados para los cuadros de texto.

El ancho de un cuadro de texto es una pista visual del tamaño de entrada esperado. Al ajustar el tamaño de los cuadros de texto:

-   **Elija un ancho adecuado para los datos válidos más largos.** En la mayoría de los casos, los usuarios no deberían tener que desplazarse por la cadena más larga probable que escriban o vean.
-   **Incluya un 30% adicional** (hasta el 200 por ciento para el texto más corto) para cualquier texto (pero no para los números) que se traducirá.
-   **Si la entrada esperada no tiene un tamaño determinado, elija un ancho que sea coherente con los demás cuadros de texto o controles de la ventana.**
-   **Cambiar el tamaño de los cuadros de texto multilínea para mostrar un número entero de líneas de texto.**

## <a name="labels"></a>Etiquetas

### <a name="text-box-labels"></a>Etiquetas de cuadro de texto

-   Todos los cuadros de texto necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, terminando con dos puntos y usando [texto estático](glossary.md).

    **Excepciones:**

    -   Cuadros de texto con mensajes donde el espacio es Premium.
    -   Para el etiquetado, un grupo de cuadros de texto utilizados para la **entrada de datos con formato** se debe tratar como un solo cuadro de texto.
    -   Si un cuadro de texto está subordinado a un botón de radio o casilla, y se introduce por la etiqueta que termina con un signo de dos puntos, no incluya una etiqueta adicional en el cuadro de texto.
    -   **Omita las etiquetas de control que representen la instrucción principal.** En este caso, la instrucción principal toma el signo de dos puntos (a menos que sea una pregunta) y una clave de acceso.

        **Aceptable:**

        ![captura de pantalla de un cuadro de texto con la etiqueta redundante resulta](images/ctrl-text-boxes-image26.png)

        En este ejemplo, la etiqueta del cuadro de texto es simplemente una resituación de la instrucción principal.

        **Manera**

        ![captura de pantalla del cuadro de texto con la instrucción principal únicamente ](images/ctrl-text-boxes-image27.png)

        En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma el signo de dos puntos y la tecla de acceso.

-   Asigne una clave de acceso única. Para obtener instrucciones de asignación de claves de acceso, consulte [teclado](inter-keyboard.md).
-   Use mayúsculas de estilo de frase.
-   Coloque la etiqueta a la izquierda o encima del cuadro de texto y alinee la etiqueta con el borde izquierdo del cuadro de texto. Si la etiqueta está a la izquierda, alinee verticalmente el texto de la etiqueta con el texto del cuadro de texto.

    **Correcto:**

    ![captura de pantalla de la etiqueta alineada a la izquierda sobre el cuadro de texto ](images/ctrl-text-boxes-image28.png)

    ![captura de pantalla de la etiqueta alineada de texto a la izquierda del cuadro de texto ](images/ctrl-text-boxes-image29.png)

    En estos ejemplos, la etiqueta en la parte superior se alinea con el borde izquierdo del cuadro de texto y la etiqueta de la izquierda se alinea con el texto del cuadro de texto.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta alineada de texto sobre el cuadro de texto ](images/ctrl-text-boxes-image30.png)

    ![captura de pantalla de la etiqueta alineada en la parte izquierda del cuadro de texto ](images/ctrl-text-boxes-image31.png)

    En estos ejemplos incorrectos, la etiqueta en la parte superior se alinea con el texto del cuadro de texto y la etiqueta de la izquierda se alinea con la parte superior del cuadro de texto.

-   Puede especificar unidades (por ejemplo, segundos o conexiones) entre paréntesis después de la etiqueta.
-   Si un cuadro de texto acepta un número máximo de caracteres arbitrariamente pequeño, puede indicar la entrada máxima en la etiqueta. El ancho del cuadro de texto también debe sugerir el tamaño máximo.

    ![captura de pantalla del cuadro de texto de contraseña ](images/ctrl-text-boxes-image32.png)

    En este ejemplo, la etiqueta proporciona el número máximo de caracteres.

-   No haga que el contenido del cuadro de texto (o su etiqueta de unidades) forme parte de una frase, ya que no es localizable.
-   Si el cuadro de texto se puede usar para escribir varios elementos, deje claro cómo debe separar los elementos de la etiqueta.

    ![captura de pantalla de nombres independientes de etiqueta con punto y coma ](images/ctrl-text-boxes-image33.png)

    En este ejemplo, el separador de elementos se proporciona en la etiqueta.

-   Para obtener instrucciones sobre cómo indicar la entrada necesaria, consulte la entrada necesaria en los [cuadros de diálogo](win-dialog-box.md).

### <a name="instruction-labels"></a>Etiquetas de instrucción

-   Si necesita agregar texto informativo sobre un cuadro de texto, agréguelo encima de la etiqueta. Use frases completas con una puntuación final.
-   Use mayúsculas de estilo de frase.
-   La información adicional que sea útil pero no necesaria debe mantenerse en breve. Coloque esta información entre paréntesis entre la etiqueta y el signo de dos puntos, o sin paréntesis debajo del cuadro de texto.

    ![captura de pantalla de la información agregada debajo del cuadro de texto ](images/ctrl-text-boxes-image34.png)

    En este ejemplo, se coloca información adicional debajo del cuadro de texto.

### <a name="prompt-labels"></a>Etiquetas de mensajes

-   Mantenga el texto del mensaje conciso. Puede usar fragmentos en lugar de oraciones completas.
-   Use mayúsculas de estilo de frase.
-   No use signos de puntuación o puntos suspensivos de finalización.
-   Si el símbolo del sistema indica a los usuarios que escriban información sobre la que se actuará con un botón situado junto al cuadro de texto, simplemente coloque el botón junto al cuadro de texto. No utilice el símbolo del sistema para indicar a los usuarios que haga clic en el botón (por ejemplo, no escriba el texto del mensaje que dice, arrastre un archivo y, a continuación, haga clic en enviar).

## <a name="documentation"></a>Documentación

Al hacer referencia a los cuadros de texto:

-   Use Type para hacer referencia a interacciones de usuario que requieren escribir o pegar; de lo contrario, use entrar si los usuarios pueden colocar información en el cuadro de texto mediante otros medios, como seleccionar el valor de una lista o utilizar un botón examinar.
-   Use SELECT para hacer referencia a una entrada en un cuadro de texto de solo lectura.
-   Use el texto exacto de la etiqueta, incluido el uso de mayúsculas, e incluya el cuadro palabra. No incluya el carácter de subrayado o el signo de dos puntos. No haga referencia a un cuadro de texto como un cuadro de texto o un campo.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

    Ejemplo: escriba la contraseña en el cuadro **contraseña** y haga clic en **Aceptar**.

-   Si el cuadro de texto requiere un formato específico, documente solo el formato aceptable que se usa con más frecuencia. Permita a los usuarios detectar otros formatos por su cuenta. Quiere ser flexible con formatos de datos, pero si lo hace, no debería producirse una documentación compleja.

    **Correcto:**

    Escriba el número de serie del elemento con el formato 1234-56-7890.

    **Incorrecto:**

    Escriba el número de serie del elemento con cualquiera de los siguientes formatos:

    1234567890

    1234-56-7890

    1234 56 7890

