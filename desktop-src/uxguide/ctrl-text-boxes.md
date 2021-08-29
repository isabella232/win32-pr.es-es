---
title: Cuadros de texto
description: Con un cuadro de texto, los usuarios pueden mostrar, escribir o editar un valor numérico o de texto.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ca062bbc4adb3b20272684edb62a982e1dd8ebdc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473251"
---
# <a name="text-boxes"></a>Cuadros de texto

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un cuadro de texto, los usuarios pueden mostrar, escribir o editar un valor numérico o de texto.

![captura de pantalla de un cuadro de texto y una etiqueta típicos ](images/ctrl-text-boxes-image1.png)

Cuadro de texto típico.

> [!Note]  
> Las instrucciones relacionadas con [el diseño,](vis-layout.md) [las](vis-fonts.md)fuentes y [los globos](ctrl-balloons.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Es práctico enumerar todos los valores válidos de forma eficaz?** Si es así, considere una [lista](ctrl-list-boxes.md)de selección [única,](ctrl-list-views.md)una vista de [lista,](/windows/desktop/uxguide/ctrl-drop)una lista desplegable, una lista desplegable modificable o un [control deslizante](ctrl-sliders.md) en su lugar.
-   **¿Los datos válidos están completamente sin restricciones? ¿O los datos válidos solo están restringidos por formato (tipos de caracteres o longitud restringida)?** Si es así, use un cuadro de texto.
-   **¿Representa el valor un tipo de datos que tiene un control común especializado?** Algunos ejemplos son la fecha, la hora o la dirección IPv4 o IPv6. Si es así, use el control adecuado, como un control de fecha en lugar de un cuadro de texto.
-   Si los datos son numéricos:
    -   **¿Perciben los usuarios la configuración como una cantidad relativa?** Si es así, usa un control deslizante.
    -   **¿Sería bueno que el usuario recibiera una respuesta instantánea del efecto de los cambios en la configuración?** Si es así, use un control deslizante, posiblemente junto con un cuadro de texto. Por ejemplo, los usuarios pueden elegir fácilmente un color mediante un control deslizante porque pueden ver inmediatamente el efecto de los cambios en los valores de matiz, saturación o luminosidad.

## <a name="design-concepts"></a>Conceptos de diseño

Aunque los cuadros de texto tienen la ventaja de ser muy flexibles, tienen el inconveniente de tener restricciones mínimas. Las únicas restricciones de un cuadro de texto modificable son:

-   Opcionalmente, puede establecer el número máximo de caracteres.
-   Opcionalmente, solo puede restringir la entrada a caracteres numéricos (0 9).
-   Si usa un [control de número](ctrl-spin-controls.md), puede limitar las opciones de control de número a valores válidos.

Aparte de su longitud y la presencia opcional de un control de número, los cuadros de texto no tienen ninguna pista visual que sugiera los valores válidos o su formato. Esto significa confiar en etiquetas para transmitir esta información a los usuarios. Si los usuarios escriben texto que no es válido, debe controlar el error con un mensaje de error.

Como regla general, **debe usar el control más restringido que pueda.** Use controles sin restricciones como cuadros de texto como último recurso. Dicho esto, cuando considere restricciones, tenga en cuenta las necesidades de los usuarios globales. Por ejemplo, un control que está restringido a Estados Unidos códigos postales no está globalizado, pero un cuadro de texto sin restricciones que acepta cualquier formato de código postal es .

## <a name="usage-patterns"></a>Patrones de uso

Un cuadro de texto es un control flexible con varios usos posibles.




| | | <strong>Entrada de datos</strong><br /> Cuadro de texto de una sola línea sin restricciones que se usa para escribir o editar cadenas cortas.<br /> | <img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br /> Cuadro de texto de una sola línea sin restricciones.<br /> | | <strong>Entrada de datos con formato</strong><br /> Conjunto de cuadros de texto cortos, de tamaño fijo y de una sola línea que se usan para escribir datos con un formato específico. <br /> | <img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br /> Cuadro de texto utilizado para la entrada de datos con formato.<br /><blockquote>[!Note]<br />La <a href="glossary.md">característica de salida</a> automática hace avanzar automáticamente el foco de entrada de un cuadro de texto al siguiente. Una desventaja de este enfoque es que los datos no se pueden copiar ni pegar como una sola unidad.</blockquote><br /><br /> | | <strong>Entrada de datos asistida</strong><br /> Cuadro de texto de una sola línea sin restricciones que se usa para escribir o editar cadenas, combinado con un botón de comando que ayuda a los usuarios a seleccionar valores válidos.<br /> | <img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br /> En este ejemplo, el comando Examinar ayuda a los usuarios a seleccionar valores válidos.<br /> | | <strong>Entrada textual</strong><br /> Cuadro de texto de varias líneas sin restricciones que se usa para escribir o editar cadenas largas. <br /> | <img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br /> Cuadro de texto de varias líneas sin restricciones.<br /> | | <strong>Entrada numérica</strong><br /> Cuadro de texto de una sola línea y solo numérico que se usa para escribir o editar números, con un control de número <a href="ctrl-spin-controls.md">opcional</a> para facilitar la entrada basada en el mouse. <br /> | <img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br /> Cuadro de texto utilizado para la entrada numérica.<br /> La combinación de un cuadro de texto y su control de número asociado se denomina cuadro <a href="ctrl-spin-controls.md">de número</a>.<br /> | | <strong>Contraseña y entrada de PIN</strong><br /> Cuadro de texto de una sola línea sin restricciones que se usa para escribir contraseñas y PIN de forma segura.<br /> | <img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br /> Cuadro de texto que se usa para escribir contraseñas.<br /> | | <strong>Salida de datos</strong><br /> Un cuadro de texto de una sola línea y de solo lectura, que siempre se muestra sin un borde, que se usa para mostrar cadenas cortas. <br /> | A diferencia del texto estático, los datos que se muestran mediante un cuadro de texto se pueden desplazar (útil si los datos son más anchos que el control), seleccionar y copiar.<br /><img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br /> Cuadro de texto de una sola línea de solo lectura que se usa para mostrar los datos.<br /> | | <strong>Salida textual</strong><br /> Cuadro de texto de solo lectura de varias líneas que se usa para mostrar cadenas largas. <br /> | <img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br /> Cuadro de texto de solo lectura que se usa para mostrar los datos.<br /> | 




 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Al deshabilitar un cuadro de texto, deshabilite también las etiquetas asociadas, las etiquetas de instrucción, los controles de número y los botones de comando.**
-   **Use autocompletar para ayudar a los usuarios a escribir datos** que es probable que se usen repetidamente. Entre los ejemplos se incluyen nombres de usuario, direcciones y nombres de archivo. Sin embargo, no use autocompletar para cuadros de texto que puedan contener información confidencial, como contraseñas, PIN, números de tarjeta de crédito o información médica.
-   **No haga que los usuarios se desplacen innecesariamente.** Si espera que los datos sean mayores que el cuadro de texto y puede hacer que el cuadro de texto sea más grande sin dañar el diseño, puede cambiar el tamaño del cuadro para eliminar la necesidad de desplazamiento.

    **Incorrecto:**

    ![captura de pantalla de un cuadro de texto de nombre de equipo ](images/ctrl-text-boxes-image10.png)

    En este ejemplo, el cuadro de texto debe ser mucho más largo para controlar sus datos.

-   Barras de desplazamiento:
    -   **No coloque barras de desplazamiento horizontal en cuadros de texto de varias líneas.** En su lugar, use el desplazamiento vertical y el ajuste de línea.
    -   **No coloque ninguna barra de desplazamiento en cuadros de texto de una sola línea.**
-   **Para la entrada numérica, puede usar un control de número.** Para la entrada de texto, use una lista desplegable o una lista desplegable editable en su lugar.
-   **No use la característica de salida automática excepto la entrada de datos con formato.** El cambio automático de foco puede sorpresar a los usuarios.

### <a name="editable-text-boxes"></a>Cuadros de texto editables

-   **Limite la longitud del texto de entrada cuando pueda.** Por ejemplo, si la entrada válida es un número entre 0 y 999, use un cuadro de texto numérico que esté limitado a tres caracteres. Todas las partes de los cuadros de texto que usan entradas de datos con formato deben tener una longitud corta y fija.
-   **Sea flexible con formatos de datos.** Si es probable que los usuarios escriban texto con una amplia variedad de formatos, intente controlar todos los más comunes. Por ejemplo, muchos nombres, números e identificadores se pueden especificar con espacios y signos de puntuación opcionales, y la mayúscula a menudo no importa.
-   Si no puede controlar los formatos probables, requiera un formato específico mediante la entrada de datos con formato o indique los formatos válidos en la etiqueta.

    **Aceptable:**

    ![captura de pantalla de un cuadro de texto para la entrada numérica ](images/ctrl-text-boxes-image11.png)

    En este ejemplo, un cuadro de texto requiere la entrada en un formato específico.

    **Mejor:**

    ![captura de pantalla del cuadro de texto de entrada de datos con formato ](images/ctrl-text-boxes-image12.png)

    En este ejemplo, el patrón de entrada de datos con formato se usa para requerir un formato específico.

    **Mejor:**

    ![captura de pantalla de un cuadro de texto sin restricciones ](images/ctrl-text-boxes-image13.png)

    En este ejemplo, un cuadro de texto controla todos los formatos probables.

-   Tenga en cuenta la flexibilidad de formato al elegir la longitud máxima de entrada. Por ejemplo, un número de tarjeta de crédito válido puede usar hasta 19 caracteres, por lo que limitar la longitud a algo más corto dificultaría la entrada de números con los formatos más largos.
-   **No use el patrón de entrada de datos con formato si es más probable que los usuarios peguen datos largos y complejos.** En su lugar, reserve el patrón de entrada de datos con formato para situaciones en las que los usuarios tienen más probabilidades de escribir los datos.

    ![captura de pantalla de un cuadro de texto con etiqueta: dirección ipv6 ](images/ctrl-text-boxes-image14.png)

    En este ejemplo, no se usa el patrón de entrada de datos con formato, por lo que los usuarios pueden pegar direcciones IPv6.

-   **Si es más probable que los usuarios vuelvan a escribir todo el valor, seleccione todo el texto en el foco de entrada.** Si es más probable que los usuarios editan, coloque el icono de diálogo al final del texto.

    ![captura de pantalla de un cuadro de texto de contraseña ](images/ctrl-text-boxes-image15.png)

    En este ejemplo, es más probable que los usuarios reemplacen que edite, por lo que todo el valor se selecciona en el foco de entrada.

    ![captura de pantalla de un cuadro de texto para escribir palabras clave ](images/ctrl-text-boxes-image16.png)

    En este ejemplo, es más probable que los usuarios agreguen palabras clave que reemplacen el texto, por lo que el elemento de inserción se coloca al final del texto.

-   **Use siempre un cuadro de texto de varias líneas si los caracteres de nueva línea son entradas válidas.**
-   **Cuando el cuadro de texto sea para un archivo o ruta de acceso, proporcione siempre un botón Examinar.**

### <a name="numeric-text-boxes"></a>Cuadros de texto numéricos

-   **Elija la unidad más cómoda y etiquete las unidades.** Por ejemplo, considere la posibilidad de usar mililitros en lugar de peraltes (o viceversa), porcentajes en lugar de valores directos (o viceversa), y así sucesivamente.

    **Correcto:**

    ![captura de pantalla del cuadro de texto con los partidos como unidad ](images/ctrl-text-boxes-image17.png)

    En este ejemplo, la unidad está etiquetada, pero requiere que los usuarios escriban números decimales.

    **Mejor:**

    ![captura de pantalla del cuadro de texto con mililitros como unidad ](images/ctrl-text-boxes-image18.png)

    En este ejemplo, el cuadro de texto usa una unidad más cómoda.

-   **Use un control de giro siempre que sea útil.** Sin embargo, a veces los controles de número no son prácticos, como cuando los usuarios necesitan escribir muchos números grandes. Use controles de giro cuando:
    -   Es probable que la entrada sea un número pequeño, normalmente por debajo de 100.
    -   Es probable que los usuarios realicen un pequeño cambio en un número existente.
    -   Es más probable que los usuarios utilicen el mouse que el teclado.
-   **Alinear a la derecha texto numérico siempre que:**

    -   Hay más de un cuadro de texto numérico.
    -   Los cuadros de texto están alineados verticalmente.
    -   Es probable que los usuarios agreguen o comparen los valores.

    **Correcto:**

    ![captura de pantalla de los cuadros de texto de gastos (hotel, etc.) ](images/ctrl-text-boxes-image19.png)

    En este ejemplo, el texto numérico está alineado a la derecha para facilitar la comparación de valores.

    **Incorrecto:**

    ![captura de pantalla de cuadros de texto para valores rgb ](images/ctrl-text-boxes-image20.png)

    En este ejemplo, el texto numérico se alinea incorrectamente a la izquierda.

-   **Alinear siempre los valores monetarios a la derecha.**
-   **No asigne significados especiales a valores numéricos específicos,** incluso si la aplicación usa internamente esos significados especiales. En su lugar, use casillas o botones de radio para una selección explícita del usuario.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta: use -1 para deshabilitar el almacenamiento en caché ](images/ctrl-text-boxes-image21.png)

    En este ejemplo, el valor -1 tiene un significado especial.

    **Correcto:**

    ![captura de pantalla de la etiqueta de casilla: almacenamiento en caché ](images/ctrl-text-boxes-image22.png)

    En este ejemplo, una casilla hace que la opción sea explícita.

### <a name="password-and-pin-input"></a>Contraseña y entrada de PIN

-   **Use siempre el control común de contraseñas en lugar de crear el suyo propio.** Las contraseñas y los PIN requieren un tratamiento especial para administrarse de forma segura.

Para obtener más instrucciones y ejemplos, vea [Globos](ctrl-balloons.md).

### <a name="textual-output"></a>Salida textual

-   **Considere la posibilidad de usar el color de fondo blanco del sistema para texto grande de solo lectura de varias líneas.** Un fondo blanco facilita la lectura del texto. Una gran cantidad de texto en un fondo gris desaconseja la lectura.

Para obtener más información sobre los colores de fondo, vea [Fuentes](vis-fonts.md).

### <a name="data-output"></a>Salida de datos

-   **No use un borde para cuadros de texto de una sola línea y de solo lectura.** El borde es una pista visual de que el texto es editable.
-   **No deshabilite los cuadros de texto de una sola línea y de solo lectura.** Esto evita que los usuarios seleccionen y copien el texto en el Portapapeles. También impide que los usuarios desplácen los datos si superan el tamaño de sus límites.
-   **No establezca una tabulación en un cuadro de texto de solo lectura de una sola línea, a menos que sea probable que el usuario tenga que desplazarse o copiar el texto.**

## <a name="input-validation-and-error-handling"></a>Validación de entrada y control de errores

Dado que los cuadros de texto no suelen estar restringidos para aceptar solo entradas válidas, es posible que tenga que validar la entrada y controlar los problemas. Valide los distintos tipos de problemas de entrada de la siguiente manera:

-   Si el usuario escribe un carácter que no es válido, ignore el carácter y muestre un globo de problemas de entrada [que](ctrl-balloons.md) explique los caracteres válidos.

    ![captura de pantalla del cuadro de texto clave de producto](images/ctrl-text-boxes-image23.png)

    En este ejemplo, un globo notifica un carácter de entrada incorrecto.

-   Si los datos de entrada tienen un valor o formato que no es válido, muestre un globo de problema de entrada cuando el cuadro de texto pierda el foco de entrada.
-   Si los datos de entrada son incoherentes con otros controles de la ventana, escriba un mensaje de error cuando se complete toda la entrada, por ejemplo, cuando los usuarios hacen clic en Aceptar para un cuadro de diálogo modal.

**No borre los datos de entrada no válidos a menos que los usuarios no puedan corregir los errores fácilmente.** Esto permite a los usuarios corregir errores sin empezar de nuevo. Por ejemplo, debe borrar contraseñas y PIN incorrectas porque los usuarios no pueden corregirlas fácilmente.

Para obtener más instrucciones y ejemplos, vea [Mensajes de error](mess-error.md) y [globos.](ctrl-balloons.md)

## <a name="prompts"></a>Mensajes

Un aviso es una etiqueta o una instrucción corta colocada dentro de un cuadro de texto como su valor predeterminado. A diferencia del texto estático, los mensajes desaparecen de la pantalla una vez que los usuarios escriben algo en el cuadro de texto o obtienen el foco de entrada.

![captura de pantalla del cuadro de texto del símbolo del sistema con etiqueta: buscar ](images/ctrl-text-boxes-image24.png)

Un aviso típico.

Use un símbolo del sistema cuando:

-   El espacio de pantalla es tan premium que no se desea usar una etiqueta o una instrucción, como en una barra de herramientas.
-   El aviso es principalmente para identificar el propósito del cuadro de texto de una manera compacta. No debe ser información fundamental que el usuario necesite ver mientras usa el cuadro de texto.

No use mensajes solo para dirigir a los usuarios para que escriban algo o para hacer clic en los botones. Por ejemplo, no escriba texto del símbolo del sistema que indique Escriba un nombre de archivo y, a continuación, haga clic en Enviar.

Al usar avisos:

-   Dibuje el texto del aviso en gris cursiva y el texto de entrada real en negro normal. El texto del aviso no debe confundirse con el texto real.
-   Mantenga el texto del aviso conciso. Puede usar fragmentos en lugar de oraciones completa.
-   Use mayúsculas de estilo de frase.
-   No use signos de puntuación finales ni puntos suspensivos.
-   El texto del mensaje no debe ser editable y debe desaparecer una vez que los usuarios hacen clic en el cuadro de texto o se tabulan en él.
    -   **Excepción:** Si el cuadro de texto tiene el foco de entrada predeterminado, se muestra el mensaje y desaparece una vez que el usuario empieza a escribir.
-   El texto del mensaje se restaura si el cuadro de texto sigue vacío cuando pierde el foco de entrada.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![figura de cuadros de texto de una y dos líneas ](images/ctrl-text-boxes-image25.png)

Tamaño y espaciado recomendados para los cuadros de texto.

El ancho de un cuadro de texto es una pista visual del tamaño de entrada esperado. Al dimensionar los cuadros de texto:

-   **Elija un ancho adecuado para los datos válidos más largos.** En la mayoría de las situaciones, los usuarios no deben tener que desplazarse por la cadena más probable que escribirán o verán.
-   **Incluya un 30** % adicional (hasta un 200 % para el texto más corto) para cualquier texto (pero no números) que se localizará.
-   **Si la entrada esperada no tiene un tamaño determinado, elija un ancho coherente con los demás cuadros de texto o controles de la ventana.**
-   **Cambiar el tamaño de los cuadros de texto de varias líneas para mostrar un número entero de líneas de texto.**

## <a name="labels"></a>Etiquetas

### <a name="text-box-labels"></a>Etiquetas de cuadro de texto

-   Todos los cuadros de texto necesitan etiquetas. Escriba la etiqueta como una palabra o frase, no como una frase, terminando con dos puntos y usando [texto estático](glossary.md).

    **Excepciones:**

    -   Cuadros de texto con avisos ubicados donde el espacio es premium.
    -   Para el etiquetado, un grupo  de cuadros de texto usados para la entrada de datos con formato debe tratarse como un único cuadro de texto.
    -   Si un cuadro de texto está subordinado a un botón de radio o a una casilla, y se introduce mediante su etiqueta que termina con dos puntos, no coloque una etiqueta adicional en el cuadro de texto.
    -   **Omita las etiquetas de control que restablecen la instrucción principal.** En este caso, la instrucción principal toma los dos puntos (a menos que sea una pregunta) y la clave de acceso.

        **Aceptable:**

        ![captura de pantalla del cuadro de texto con etiqueta repetitiva](images/ctrl-text-boxes-image26.png)

        En este ejemplo, la etiqueta del cuadro de texto es simplemente una nueva instrucción de la instrucción principal.

        **Mejor:**

        ![captura de pantalla del cuadro de texto solo con instrucciones principales ](images/ctrl-text-boxes-image27.png)

        En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma los dos puntos y la clave de acceso.

-   Asigne una clave de acceso única. Para obtener instrucciones de asignación de claves de acceso, vea [Teclado](inter-keyboard.md).
-   Use mayúsculas de estilo de frase.
-   Coloque la etiqueta a la izquierda del cuadro de texto o encima del cuadro de texto y alinee la etiqueta con el borde izquierdo del cuadro de texto. Si la etiqueta está a la izquierda, alinee verticalmente el texto de la etiqueta con el texto del cuadro de texto.

    **Correcto:**

    ![captura de pantalla de la etiqueta alineada a la izquierda encima del cuadro de texto ](images/ctrl-text-boxes-image28.png)

    ![captura de pantalla de la etiqueta alineada con texto a la izquierda del cuadro de texto ](images/ctrl-text-boxes-image29.png)

    En estos ejemplos, la etiqueta de la parte superior se alinea con el borde izquierdo del cuadro de texto y la etiqueta de la izquierda se alinea con el texto del cuadro de texto.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta alineada con texto encima del cuadro de texto ](images/ctrl-text-boxes-image30.png)

    ![captura de pantalla de la etiqueta alineada superior izquierda del cuadro de texto ](images/ctrl-text-boxes-image31.png)

    En estos ejemplos incorrectos, la etiqueta de la parte superior se alinea con el texto del cuadro de texto y la etiqueta de la izquierda se alinea con la parte superior del cuadro de texto.

-   Puede especificar unidades (por ejemplo, segundos o conexiones) entre paréntesis después de la etiqueta.
-   Si un cuadro de texto acepta un número máximo de caracteres arbitrariamente pequeño, puede especificar la entrada máxima en la etiqueta. El ancho del cuadro de texto también debe sugerir el tamaño máximo.

    ![captura de pantalla del cuadro de texto contraseña ](images/ctrl-text-boxes-image32.png)

    En este ejemplo, la etiqueta proporciona el número máximo de caracteres.

-   No haga que el contenido del cuadro de texto (o su etiqueta de unidades) sea parte de una oración, porque esto no es localizable.
-   Si el cuadro de texto se puede usar para escribir varios elementos, asegúrese de que separe los elementos de la etiqueta.

    ![captura de pantalla de los nombres independientes de la etiqueta con punto y coma ](images/ctrl-text-boxes-image33.png)

    En este ejemplo, el separador de elementos se da en la etiqueta .

-   Para obtener instrucciones sobre cómo indicar la entrada necesaria, vea Entrada necesaria en cuadros [de diálogo.](win-dialog-box.md)

### <a name="instruction-labels"></a>Etiquetas de instrucciones

-   Si necesita agregar texto informativo sobre un cuadro de texto, agrégrélo encima de la etiqueta. Use oraciones completas con signos de puntuación finales.
-   Use mayúsculas de estilo de frase.
-   La información adicional que es útil, pero no necesaria, debe mantenerse corta. Coloque esta información entre paréntesis entre la etiqueta y los dos puntos, o sin paréntesis debajo del cuadro de texto.

    ![captura de pantalla de la información agregada debajo del cuadro de texto ](images/ctrl-text-boxes-image34.png)

    En este ejemplo, se coloca información adicional debajo del cuadro de texto.

### <a name="prompt-labels"></a>Etiquetas de aviso

-   Mantenga el texto del aviso conciso. Puede usar fragmentos en lugar de oraciones completa.
-   Use mayúsculas de estilo de frase.
-   No use signos de puntuación finales ni puntos suspensivos.
-   Si el mensaje indica a los usuarios que escriban información sobre la que actuará un botón junto al cuadro de texto, simplemente coloque el botón junto al cuadro de texto. No use el símbolo del sistema para dirigir a los usuarios a hacer clic en el botón (por ejemplo, no escriba el texto del mensaje que dice Arrastrar un archivo y, a continuación, haga clic en Enviar).

## <a name="documentation"></a>Documentación

Al hacer referencia a cuadros de texto:

-   Use el tipo para hacer referencia a las interacciones del usuario que requieren escribir o pegar. De lo contrario, use Entrar si los usuarios pueden colocar información en el cuadro de texto mediante otros medios, como seleccionar el valor de una lista o usar un botón Examinar.
-   Use select para hacer referencia a una entrada en un cuadro de texto de solo lectura.
-   Use el texto exacto de la etiqueta, incluida su mayúscula y la palabra box. No incluya el carácter de subrayado ni los dos puntos de la clave de acceso. No haga referencia a un cuadro de texto como un cuadro de texto o un campo.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

    Ejemplo: escriba la contraseña en el cuadro **Contraseña** y, a continuación, haga clic **en Aceptar.**

-   Si el cuadro de texto requiere un formato específico, documente solo el formato aceptable que se usa con más frecuencia. Permitir que los usuarios detecten cualquier otro formato por su cuenta. Quiere ser flexible con formatos de datos, pero esto no debería dar lugar a documentación compleja.

    **Correcto:**

    Escriba el número de serie de la parte con el formato 1234-56-7890.

    **Incorrecto:**

    Escriba el número de serie del elemento con cualquiera de los formatos siguientes:

    1234567890

    1234-56-7890

    1234 56 7890

