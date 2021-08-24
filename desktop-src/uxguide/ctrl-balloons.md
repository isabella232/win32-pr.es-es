---
title: Globos
description: Un globo es una pequeña ventana emergente que informa a los usuarios de un problema no crítico o una condición especial en un control.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ea95eee6e745dc85dbe7cd354df0906b5df4a7870198fc662effd326c6fbaae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818693"
---
# <a name="balloons"></a>Globos

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Un globo es una pequeña ventana emergente que informa a los usuarios de un problema no crítico o una condición especial en un control.

![Captura de pantalla que muestra un globo que indica que El bloqueo de límites está en.](images/ctrl-balloons-image1.png)

Un globo típico.

Los globos tienen un icono, un título y texto del cuerpo, todos ellos opcionales. A diferencia de la información sobre herramientas y la información sobre herramientas, los globos también tienen una cola que identifica su origen. Normalmente, el origen es un control, si es así, se conoce como control [de propietario](glossary.md).

Aunque los globos informan a los usuarios de problemas no críticos, no evitan problemas, aunque el control de propietario podría. La interfaz de usuario (UI) propietaria debe controlar los problemas no controladas cuando los usuarios intenten confirmar la acción.

Los globos se usan normalmente con cuadros de texto o controles que usan cuadros de texto para cambiar valores, como cuadros combinados, vistas de lista y vistas de árbol. Otros tipos de controles están suficientemente restringidos y no necesitan los globos de comentarios adicionales que se ofrecen. Además, si hay un problema con otros tipos de controles, a menudo implica incoherencia entre varios controles, situación para la que los globos no son adecuados. Solo los controles de entrada de texto están sin restricciones y son un origen común de [errores de punto único.](glossary.md)

Una notificación es un tipo específico de globo mostrado por un icono [de área de](winenv-notification.md) notificación.

**Nota:** Las directrices relacionadas [con las notificaciones,](mess-notif.md)la información sobre herramientas y la información sobre [herramientas,](ctrl-tooltips-and-infotips.md)y los mensajes de [error](mess-error.md) se presentan en artículos independientes.

**¿Es este el control adecuado?**

Para decidirte, intenta responder a estas preguntas:

-   **¿Describe la información un problema o una condición especial?** Si no es así, usa otro control. No use globos para mostrar información complementaria para un control. considere la posibilidad [de usar texto estático,](glossary.md)[información sobre información,](glossary.md) [divulgación progresiva](glossary.md)o avisos en su lugar.
-   **¿Se puede detectar el problema o la condición especial inmediatamente** en la entrada o cuando el control de propietario pierde el foco de entrada? Si no es así, use un mensaje de error que se muestra en un cuadro [de diálogo o](glossary.md) mensaje de [tarea](glossary.md).
-   **En el caso de los problemas, ¿el problema es crítico?** Si es así, use un mensaje de error que se muestra en un cuadro de diálogo o mensaje de tarea. Estos mensajes de error requieren interacción (que es adecuada para errores críticos), mientras que los globos no.
-   **En el caso de las condiciones especiales, ¿la condición es válida pero es probable que no sea intencionado?** Si es así, los globos son adecuados. En el caso de las condiciones no válidas, es mejor evitarlas en primer lugar. En el caso de las condiciones previstas probablemente, no es necesario hacer nada.
-   **¿Se puede expresar el problema o la condición especial de forma concisa?** Si no es así, usa otro control. Los globos no pueden tener explicaciones detalladas ni proporcionar información complementaria.
-   **¿Describe la información el control sobre el que se mantiene el puntero?** Si es así, use una sugerencia en su lugar, a menos que los usuarios necesiten interactuar con el mensaje.
-   **¿La información está relacionada con la actividad actual del usuario?** Si no es así, considere la posibilidad de [usar una notificación](mess-notif.md) o un cuadro de diálogo en [su](win-dialog-box.md) lugar. Es probable que los usuarios pasen por alto los globos fuera de la actividad actual y, de forma predeterminada, los globos tienen un tiempo de espera de 10 segundos.
-   **¿La información procede de un origen único y específico?** Si un problema o condición tiene varios orígenes o ningún origen específico, use un mensaje local [o](glossary.md) un cuadro de diálogo en su lugar.

**Incorrecto:** ![ captura de pantalla de un globo: inicio de sesión no correcto](images/ctrl-balloons-image2.png)

En este ejemplo, el problema podría ser con el nombre de usuario o la contraseña, pero notificar el problema con un globo sugiere visualmente que solo la contraseña es el problema. Por lo tanto, los comentarios de escribir un nombre de usuario incorrecto son confusos.

Los globos son una alternativa a información sobre información, cuadros de diálogo y mensajes en su lugar. A diferencia de la información sobre herramientas y la información sobre herramientas:

-   Los globos se pueden mostrar independientemente de la ubicación actual del puntero, por lo que tienen un final que indica su origen.
-   Los globos tienen un título, texto del cuerpo y un icono.
-   Los globos pueden ser interactivos, mientras que es imposible hacer clic en una sugerencia.

A diferencia de los cuadros de diálogo modales:

-   Los globos no roban el foco de entrada ni requieren interacción.
-   Los globos identifican un origen único y específico. Los diálogos modales pueden tener varios orígenes o ningún origen específico.

A diferencia de los mensajes en su lugar:

-   Los globos son más evidentes.
-   Los globos no requieren espacio de pantalla disponible ni el diseño dinámico necesario para mostrar los mensajes en su lugar.
-   Los globos se quitan automáticamente después de un tiempo de espera.

**Patrones de uso**

Los globos tienen estos patrones de uso:



|   Uso                                                                                                                                                            |    Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problema de entrada** Un problema de entrada de usuario no crítico procedente de un control de propietario único, normalmente un cuadro de texto. <br/>                                               | El uso de globos para mensajes de error no roba el foco de entrada, pero sigue siendo muy perceptible si el control de propietario tiene el foco de entrada. Para corregir el problema, es posible que el usuario tenga que cambiar o volver a escribir la entrada; pero si el control de propietario omite la entrada incorrecta, es posible que el usuario no tenga que realizar ningún cambio. dado que el problema no es crítico, no [es necesario ningún icono](vis-std-icons.md) de error. <br/> ![Captura de pantalla que muestra un globo que indica un carácter incorrecto.](images/ctrl-balloons-image3.png)<br/> Globo que se usa para notificar un problema de entrada de usuario no crítico.<br/>                                                                                                  |
| **Condición especial** El control de propietario está en un estado que afecta a la entrada. Es probable que este estado no sea intencionado y el usuario no se dé cuenta de que la entrada se ve afectada. <br/> | use globos para evitar frustraciones mediante la alerta a los usuarios de condiciones especiales en cuanto se cumplen (por ejemplo, superando el tamaño máximo de entrada o estableciendo límites de bloqueo por error). es importante proporcionar estos comentarios sin robar el foco de entrada ni forzar la interacción porque estas condiciones pueden ser intencionadas. estos globos son especialmente importantes para los cuadros de contraseña y anclado, donde los usuarios trabajan con comentarios mínimos. estos globos tienen un [icono de advertencia](vis-std-icons.md). <br/> ![Captura de pantalla que muestra globos que indican que El bloqueo de límites está en y se introduce un carácter incorrecto.](images/ctrl-balloons-image4.png)<br/> Globo que se usa para notificar una condición especial.<br/> |



 

**Directrices**

**Cuándo se debe mostrar**

-   **Muestre el globo en cuanto se detecte el problema o la condición especial, aunque se repita, sin ningún retraso apreciable.**
    -   Para problemas relacionados con caracteres individuales o el tamaño máximo de entrada, muestre el globo inmediatamente en la entrada.
    -   En el caso de problemas relacionados con el valor de entrada (incluida la necesidad de un valor no en blanco), muestre el globo cuando el control de propietario pierda el foco de entrada. De lo contrario, mostrar globos mientras los usuarios escriben entradas potencialmente válidas puede distraer y ser molesto.
-   **Mostrar solo un globo a la vez.** Mostrar varios globos puede ser abrumador. Si un solo evento produce varios problemas, presente todos los problemas a la vez o informe solo del problema más importante.

**Incorrecto:** ![ captura de pantalla de dos globos que apuntan a un cuadro](images/ctrl-balloons-image5.png)

En este ejemplo, dos problemas se presentan incorrectamente al mismo tiempo.

**Cuánto tiempo se debe mostrar**

-   **Quite un globo cuando:**
    -   El problema se resuelve o se quita una condición especial.
    -   El usuario escribe datos válidos (para problemas de entrada).
    -   Se ha pasado el tiempo de espera del globo. De forma predeterminada, los globos se quitan después de 10 segundos, aunque los usuarios pueden cambiarlo modificando el parámetro del sistema SPI \_ MESSAGEDURATION.
-   **Quite el tiempo de espera si los usuarios no pueden continuar hasta que se resuelva el problema. Desarrolladores:** en Win32, puede establecer la hora de presentación con el mensaje \_ SETDELAYTIME de TTM.

**Cómo mostrar**

-   **Mostrar globos debajo de su control de propietario.** Esto permite a los usuarios ver el contexto, incluidos el control de propietario y su etiqueta. Microsoft Windows ajusta automáticamente las posiciones del globo para que estén completamente en pantalla. El comportamiento predeterminado es mostrar un globo encima de su control de propietario, como se hace con las notificaciones.

**Correcto:** ![ captura de pantalla de un globo que se muestra debajo de su control](images/ctrl-balloons-image6.png)

**Incorrecto:** ![ captura de pantalla de un globo que se muestra encima de su control](images/ctrl-balloons-image7.png)

En el ejemplo incorrecto, el globo se muestra incorrectamente encima de su control de propietario.

**Cuadros de texto de contraseña y PIN**

-   **Use un globo para indicar que El bloqueo de límites está en**, utilizando el texto del ejemplo siguiente:

![captura de pantalla de un globo que indica que el bloqueo de límites está en](images/ctrl-balloons-image8.png)

En este ejemplo, un globo indica que El bloqueo de límites está en un cuadro de texto de PIN.

-   **Use un globo para indicar cuándo los usuarios intentan superar el tamaño máximo de entrada.** Alcanzar el tamaño máximo de entrada es mucho menos obvio en los cuadros de texto de contraseña y PIN que en los cuadros de texto normales.

![captura de pantalla de un globo que indica los límites de código pin](images/ctrl-balloons-image9.png)

En este ejemplo, un globo indica que el usuario está intentando superar el tamaño máximo de entrada.

-   **Use un globo para indicar cuándo los usuarios introducen caracteres incorrectos.** Sin embargo, es mejor no tener estas restricciones porque reducen la seguridad de la contraseña o el PIN. Para evitar la divulgación de información, el globo solo debe mencionar hechos documentados sobre contraseñas válidas o PIN.

![captura de pantalla de un globo que indica una entrada incorrecta](images/ctrl-balloons-image10.png)

En este ejemplo, un globo indica que el PIN requiere números.

**Otros cuadros de texto**

-   **Considere la posibilidad de usar un globo para indicar cuándo los usuarios intentan superar el tamaño máximo de entrada para los cuadros de texto críticos y cortos dirigidos a usuarios principiantes.** Algunos ejemplos son los nombres de usuario y los nombres de cuenta. Los cuadros de texto suenan cuando los usuarios intentan superar la entrada máxima, pero es posible que los usuarios principiantes no comprendan el significado del pitido.

![captura de pantalla de un globo que indica los límites de caracteres](images/ctrl-balloons-image11.png)

En este ejemplo, un globo indica que el usuario intentó superar el tamaño máximo de entrada.

**Interacción**

-   **Cuando los usuarios hacen clic en un globo, simplemente descartan el globo sin mostrar ninguna otra interfaz de usuario ni tener ningún otro efecto secundario.** A diferencia de las notificaciones, los globos no deben tener botones de cierre.

**Iconos**

-   Elija el icono en función del patrón de uso:



    |  Patrón |  Icono                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Problema de entrada | Sin icono. No usar un [icono de error](vis-std-icons.md) aquí es coherente con las Windows de [tono.](text-style-tone.md) |
    | Condición especial | Icono de advertencia estándar de 16 x 16 [píxeles.](vis-std-icons.md)                                                                                  |

**Accesibilidad**

Cuando se usan correctamente, los globos mejoran la accesibilidad. Para que los globos sean accesibles:

-   Mostrar solo globos relacionados con la actividad actual del usuario.
-   Mantenga el texto del globo conciso. Esto facilita la lectura del texto del globo para los usuarios con visión baja y minimiza la interrupción cuando los lectores de pantalla leen.
-   Vuelva a mostrar el globo cada vez que se repita el problema o la condición.

**Texto**

**Texto del título**

-   **Use texto de título que resuma brevemente el problema de entrada o la condición especial en un lenguaje claro, sin formato, conciso y específico.** Los usuarios deben ser capaces de comprender el propósito del globo rápidamente y con el mínimo esfuerzo.
-   **Use fragmentos de texto o oraciones completas sin finalizar los signos de puntuación.**
-   **Use mayúsculas de estilo de frase.** Para más información, consulte el [glosario](./glossary.md).
-   **No use más de 48 caracteres (en inglés) para adaptarse a la localización.** El título tiene una longitud máxima de 63 caracteres y debe poder expandirse al menos un 30 por ciento para dar cabida a la localización.

**Texto del cuerpo**

-   **Use la primera oración del texto del cuerpo para decir el problema o la condición de una manera claramente relevante para el usuario.** No repita la información del título. Omita esto si no hay nada más que agregar.
-   **Use la segunda frase para decir lo que el usuario puede hacer para resolver el problema o revertir el estado.** De acuerdo con las [directrices de estilo](./text-style-tone.md) y tono, no es necesario usar la palabra Please en esta instrucción. Coloque dos saltos de línea entre la primera y la segunda frase.

![captura de pantalla de un globo con texto de título y cuerpo](images/ctrl-balloons-image12.png)

En este ejemplo se muestra el diseño de texto de globo estándar.

-   **Explicar cómo resolver el problema o revertir** el estado incluso si esa explicación es obvia, pero omitir la redundancia entre la instrucción del problema y su resolución. **Excepciones:**
    -   Omita la resolución si no se puede expresar de forma concisa o sin redundancia significativa.
    -   Omita la resolución si el usuario no tiene nada que hacer, por ejemplo, cuando se omiten los caracteres incorrectos.
-   **Use oraciones completas con puntuación final.**
-   **Use mayúsculas de estilo de frase.**
-   **No use más de 200 caracteres (en inglés) para adaptarse a la localización.** El texto del cuerpo tiene una longitud máxima de 255 caracteres y debe poder expandirse al menos un 30 por ciento para dar cabida a la localización.

**Documentación**

Al hacer referencia a globos:

-   Use el texto del título exacto, incluida su mayúscula.
-   Consulte el componente como un globo, no como una notificación o una alerta.
-   Cuando sea posible, formatee el texto del título con texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

