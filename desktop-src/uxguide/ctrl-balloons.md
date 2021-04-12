---
title: Globos
description: Un globo es una pequeña ventana emergente que informa a los usuarios de un problema no crítico o una condición especial en un control.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 348167594db2f7895e185d8d7761832ec5c0c1cb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361811"
---
# <a name="balloons"></a>Globos

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Un globo es una pequeña ventana emergente que informa a los usuarios de un problema no crítico o una condición especial en un control.

![Captura de pantalla que muestra un globo que indica que Bloq Mayús está activado.](images/ctrl-balloons-image1.png)

Globo típico.

Los globos tienen un icono, un título y el texto del cuerpo, todos ellos opcionales. A diferencia de la información sobre herramientas y recuadros informativos, los globos también tienen una cola que identifica su origen. Normalmente, el origen es un control si es así, se conoce como [control propietario](glossary.md).

Aunque los globos informan a los usuarios de problemas no críticos, no impiden problemas, aunque es posible que el control propietario. Los problemas no controlados deben controlarse mediante la interfaz de usuario (UI) del propietario cuando los usuarios intentan confirmar la acción.

Los globos se suelen usar con cuadros de texto o controles que usan cuadros de texto para cambiar valores, como cuadros combinados, vistas de lista y vistas de árbol. Otros tipos de controles están suficientemente restringidos y no necesitan recibir más globos de comentarios. Además, si hay un problema con otros tipos de controles, a menudo implica una incoherencia entre varios controles una situación en la que los globos no son adecuados. Solo los controles de entrada de texto no están restringidos y son un origen común de los errores de un [solo punto](glossary.md).

Una notificación es un tipo específico de globo mostrado por un icono de [área de notificación](winenv-notification.md) .

**Nota:** Las instrucciones relacionadas con las [notificaciones](mess-notif.md), la [información sobre herramientas y recuadros informativos](ctrl-tooltips-and-infotips.md), y [los mensajes de error](mess-error.md) se presentan en artículos independientes.

**¿Es este el control adecuado?**

Para decidirte, intenta responder a estas preguntas:

-   **¿La información describe un problema o una condición especial?** Si no es así, usa otro control. No utilice globos para mostrar información complementaria de un control. considere la posibilidad de usar [texto estático](glossary.md),[recuadros informativos](glossary.md), [divulgación progresiva](glossary.md)o mensajes en su lugar.
-   **¿Se puede detectar el problema o la condición especial inmediatamente** en la entrada o cuando el control propietario pierde el foco de entrada? Si no es así, use un mensaje de error que se muestra en un cuadro de [diálogo de tarea](glossary.md) o de [mensaje](glossary.md).
-   **En el caso de problemas, ¿es crítico el problema?** Si es así, use un mensaje de error que se muestra en un cuadro de diálogo de tarea o de mensaje. Estos mensajes de error requieren interacción (que es adecuado para errores críticos), mientras que los globos no.
-   **En el caso de las condiciones especiales, ¿es válida la condición pero probablemente no esté pensada?** Si es así, los globos son adecuados. En el caso de las condiciones no válidas, es mejor evitarlos en primer lugar. En el caso de las condiciones previstas, no es necesario hacer nada.
-   **¿El problema o la condición especial se pueden expresar de forma concisa?** Si no es así, usa otro control. Los globos no pueden tener explicaciones detalladas ni proporcionar información complementaria.
-   **¿La información describe el control en el que se mantiene el puntero actualmente?** Si es así, use una sugerencia en su lugar, a menos que los usuarios tengan que interactuar con el mensaje.
-   **¿La información está relacionada con la actividad actual del usuario?** Si no es así, considere la posibilidad de usar en su lugar una [notificación](mess-notif.md) o un [cuadro de diálogo](win-dialog-box.md) . Es probable que los usuarios pasen por alto los globos fuera de la actividad actual y, de forma predeterminada, se agote el tiempo de espera de los globos después de 10 segundos.
-   **¿La información procede de un solo origen específico?** Si un problema o una condición tienen varios orígenes o ningún origen específico, use en su lugar un [mensaje en contexto](glossary.md) o un cuadro de diálogo.

**Incorrecto:** ![ captura de pantalla de un globo: Inicio de sesión incorrecto](images/ctrl-balloons-image2.png)

En este ejemplo, el problema podría ser con el nombre de usuario o la contraseña, pero la notificación del problema con un globo sugiere visualmente que solo la contraseña es el problema. Por lo tanto, los comentarios de escribir un nombre de usuario incorrecto son engañosos.

Los globos son una alternativa a recuadros informativos, cuadros de diálogo y mensajes en contexto. A diferencia de la información sobre herramientas y recuadros informativos:

-   Los globos se pueden mostrar independientemente de la ubicación actual del puntero, por lo que tienen un final que indica su origen.
-   Los globos tienen un título, texto de cuerpo y un icono.
-   Los globos pueden ser interactivos, pero es imposible hacer clic en una sugerencia.

A diferencia de los cuadros de diálogo modales:

-   Los globos no roban el foco de entrada ni requieren interacción.
-   Los globos identifican un único origen específico. Los cuadros de diálogo modales pueden tener varios orígenes o no tener ningún origen específico.

A diferencia de los mensajes en contexto:

-   Los globos son más evidentes.
-   Los globos no requieren espacio de pantalla disponible ni el diseño dinámico necesario para mostrar los mensajes en contexto.
-   Los globos se eliminan automáticamente después de un tiempo de espera.

**Patrones de uso**

Los globos tienen estos patrones de uso:



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problema de entrada** Un problema de entrada de usuario no crítico procedente de un solo control propietario, normalmente un cuadro de texto. <br/>                                               | el uso de globos para mensajes de error no roba el foco de entrada, pero todavía es muy apreciable si el control propietario tiene el foco de entrada. para corregir el problema, es posible que el usuario tenga que cambiar o volver a escribir la entrada. pero si el control propietario omite la entrada incorrecta, es posible que el usuario no tenga que realizar ningún cambio. Dado que el problema no es crítico, no es necesario ningún [icono de error](vis-std-icons.md) . <br/> ![Captura de pantalla que muestra un globo que indica un carácter incorrecto.](images/ctrl-balloons-image3.png)<br/> Globo que se usa para notificar un problema de entrada de usuario no crítico.<br/>                                                                                                  |
| **Condición especial** El control propietario está en un estado que afecta a la entrada. Es probable que este estado no sea el deseado y que el usuario no se vea afectado. <br/> | Use globos para evitar la frustración al avisar a los usuarios de condiciones especiales tan pronto como se produzcan (por ejemplo, superando el tamaño máximo de entrada o estableciendo Bloq Mayús en por error). es importante dar tales comentarios sin robar el foco de entrada ni forzar la interacción, ya que estas condiciones podrían ser intencionadas. Estos globos son especialmente importantes para las casillas de contraseña y PIN, donde los usuarios trabajan con los comentarios mínimos. Estos globos tienen un [icono de advertencia](vis-std-icons.md). <br/> ![Captura de pantalla que muestra globos que indican que Bloq Mayús está activado y se escribe un carácter incorrecto.](images/ctrl-balloons-image4.png)<br/> Globo que se usa para notificar una condición especial.<br/> |



 

**Directrices**

**Cuándo se debe mostrar**

-   **Muestre el globo en cuanto se detecte el problema o la condición especial, incluso si es repetidamente, sin ningún retraso perceptible.**
    -   En el caso de problemas relacionados con caracteres individuales o el tamaño de entrada máximo, muestre el globo inmediatamente en la entrada.
    -   En el caso de problemas relacionados con el valor de entrada (incluida la exigencia de un valor que no está en blanco), muestre el globo cuando el control propietario pierda el foco de entrada. De lo contrario, Mostrar globos mientras los usuarios escriben datos potencialmente válidos pueden distraerse y molestos.
-   **Muestra un solo globo a la vez.** Mostrar varios globos puede ser abrumador. Si un solo evento produce varios problemas, presente todos los problemas a la vez o informe solo del problema más importante.

**Incorrecto:** ![ captura de pantalla de dos globos que señalan a un cuadro](images/ctrl-balloons-image5.png)

En este ejemplo, se presentan incorrectamente dos problemas al mismo tiempo.

**Cuánto tiempo se va a mostrar**

-   **Quitar un globo cuando:**
    -   El problema se resuelve o se quita una condición especial.
    -   El usuario especifica datos válidos (para problemas de entrada).
    -   Se agota el tiempo de espera del globo. De forma predeterminada, los globos se eliminan después de 10 segundos, aunque los usuarios pueden cambiar esto modificando el \_ parámetro del sistema SPI MESSAGEDURATION.
-   **Quite el tiempo de espera si los usuarios no pueden continuar hasta que se resuelva el problema. Desarrolladores:** en Win32, puede establecer la hora de visualización con el \_ mensaje TTM SETDELAYTIME.

**Cómo mostrar**

-   **Mostrar globos debajo de su control propietario.** Esto permite a los usuarios ver el contexto, incluido el control propietario y su etiqueta. Microsoft Windows ajusta automáticamente las posiciones de los globos para que estén completamente en pantalla. El comportamiento predeterminado es mostrar un globo encima de su control propietario, como se hace con las notificaciones.

**Correcto:** ![ captura de pantalla de un globo que se muestra debajo de su control](images/ctrl-balloons-image6.png)

**Incorrecto:** ![ captura de pantalla de un globo mostrado encima de su control](images/ctrl-balloons-image7.png)

En el ejemplo incorrecto, el globo se muestra de forma complicada sobre su control propietario.

**Cuadros de texto contraseña y PIN**

-   **Use un globo para indicar que Bloq Mayús está activado** y use el texto del ejemplo siguiente:

![captura de pantalla de un globo que indica que el Bloq Mayús está activado](images/ctrl-balloons-image8.png)

En este ejemplo, un globo indica que Bloq Mayús está activado en un cuadro de texto de PIN.

-   **Use un globo para indicar cuándo un usuario intenta superar el tamaño de entrada máximo.** Alcanzar el tamaño máximo de entrada es mucho menos obvio en los cuadros de texto contraseña y PIN que los cuadros de texto ordinarios.

![captura de pantalla de un globo que indica los límites del código PIN](images/ctrl-balloons-image9.png)

En este ejemplo, un globo indica que el usuario está intentando superar el tamaño de entrada máximo.

-   **Use un globo para indicar si los usuarios escriben caracteres incorrectos.** Sin embargo, es mejor no tener estas restricciones, ya que reducen la seguridad de la contraseña o el PIN. Para evitar la divulgación de información, el globo solo debe mencionar hechos documentados sobre contraseñas o PIN válidos.

![captura de pantalla de un globo que indica una entrada incorrecta](images/ctrl-balloons-image10.png)

En este ejemplo, un globo indica que el PIN requiere números.

**Otros cuadros de texto**

-   **Considere la posibilidad de usar un globo para indicar si los usuarios intentan superar el tamaño de entrada máximo para los cuadros de texto graves y críticos destinados a usuarios inexpertos.** Entre los ejemplos se incluyen nombres de usuario y nombres de cuenta. Los cuadros de texto emiten un pitido cuando los usuarios intentan superar la entrada máxima, pero es posible que los usuarios inexpertos no sepan el significado del pitido.

![captura de pantalla de un globo que indica los límites de caracteres](images/ctrl-balloons-image11.png)

En este ejemplo, un globo indica que el usuario intentó superar el tamaño de entrada máximo.

**Interacción**

-   **Cuando los usuarios hacen clic en un globo, solo tiene que descartar el globo sin mostrar ninguna otra interfaz de usuario ni tener ningún otro efecto secundario.** A diferencia de las notificaciones, los globos no deben tener botones de cierre.

**Iconos**

-   Elija el icono en función del patrón de uso:



    |  Patrón |  Icono                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Problema de entrada | Sin icono. No usar un [icono de error](vis-std-icons.md) aquí es coherente con las directrices de [tono de Windows](text-style-tone.md) . |
    | Condición especial | [Icono de advertencia](vis-std-icons.md)estándar de 16x16 píxeles.                                                                                  |

**Accesibilidad**

Cuando se usa correctamente, los globos mejoran la accesibilidad. Para que se pueda obtener acceso a los globos:

-   Solo muestra los globos relacionados con la actividad actual del usuario.
-   Mantenga el texto del globo conciso. Esto hace que el texto del globo sea más fácil de leer para los usuarios con deficiencias visuales y minimiza la interrupción cuando lo leen los lectores de pantalla.
-   Vuelva a mostrar el globo cada vez que se repite el problema o la condición.

**Texto**

**Texto del título**

-   **Use el texto del título que resume brevemente el problema de entrada o la condición especial en lenguajes claros, sencillos y concisos.** Los usuarios deben poder comprender el propósito del globo rápidamente y con el mínimo esfuerzo.
-   **Utilice fragmentos de texto o frases completas sin puntuación final.**
-   **Use mayúsculas de estilo de frase.** Para obtener más información, consulte el [Glosario](./glossary.md).
-   **No use más de 48 caracteres (en inglés) para dar cabida a la localización.** El título tiene una longitud máxima de 63 caracteres y debe poder expandirse al menos en un 30 por ciento para adaptarse a la localización.

**Texto del cuerpo**

-   **Use la primera oración del texto del cuerpo para indicar el problema o la condición de una manera claramente relevante para el usuario.** No repita la información en el título. Omita este valor si no hay nada más que agregar.
-   **Use la segunda oración para indicar lo que el usuario puede hacer para resolver el problema o revertir el estado.** De acuerdo con las directrices de [estilo y tono](./text-style-tone.md) , no es necesario usar la palabra en esta instrucción. Coloque dos saltos de línea entre la primera y la segunda oración.

![captura de pantalla de un globo con el título y el texto del cuerpo](images/ctrl-balloons-image12.png)

En este ejemplo se muestra el diseño de texto de globo estándar.

-   **Explique cómo resolver el problema o revertir el estado aunque la explicación sea obvia,** pero omita la redundancia entre la declaración del problema y su resolución. **Excepciones:**
    -   Omita la resolución si no se puede expresar de manera concisa o sin redundancia significativa.
    -   Omita la resolución si no hay nada que pueda hacer el usuario, por ejemplo, cuando se omiten los caracteres incorrectos.
-   **Use frases completas con una puntuación final.**
-   **Use mayúsculas de estilo de frase.**
-   **No use más de 200 caracteres (en inglés) para dar cabida a la localización.** El texto del cuerpo tiene una longitud máxima de 255 caracteres y debe ser capaz de expandirse al menos en un 30 por ciento para adaptarse a la localización.

**Documentación**

Al hacer referencia a los globos:

-   Use el texto de título exacto, incluido el uso de mayúsculas.
-   Haga referencia al componente como un globo, no como una notificación o una alerta.
-   Siempre que sea posible, dé formato al texto del título usando texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

