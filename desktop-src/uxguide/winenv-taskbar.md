---
title: Barra de tareas
description: La barra de tareas es el punto de acceso para los programas que se muestran en el escritorio. Con la nueva Windows 7 características de la barra de tareas, los usuarios pueden proporcionar comandos, acceder a recursos y ver el estado del programa directamente desde la barra de tareas.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 86b63e5f3b3dc1e8cecba78cbb1599c305d738250d92f76055596226c9028727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117854347"
---
# <a name="taskbar"></a>Barra de tareas

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

La barra de tareas es el punto de acceso para los programas que se muestran en el escritorio. Con la nueva Windows 7 características de la barra de tareas, los usuarios pueden proporcionar comandos, acceder a recursos y ver el estado del programa directamente desde la barra de tareas.

La barra de tareas es el punto de acceso para los programas que se muestran en el escritorio, incluso si el programa está minimizado. Se dice que estos programas tienen presencia en el escritorio. Con la barra de tareas, los usuarios pueden ver las ventanas principales abiertas y determinadas ventanas secundarias en el escritorio, y pueden cambiar rápidamente entre ellas.

![captura de pantalla de la barra de tareas con características llamadas ](images/winenv-taskbar-image1.png)

Barra de tareas Windows Microsoft.

Los controles de la barra de tareas se conocen como botones de la barra de tareas. Cuando un programa crea una ventana principal (o una ventana secundaria con ciertas características), Windows un botón de la barra de tareas para esa ventana y la quita cuando se cierra esa ventana.

Los programas diseñados para Windows 7 pueden aprovechar estas nuevas características del botón de la barra de tareas:

-   Las listas de accesos directos proporcionan acceso rápido a destinos usados con frecuencia (como archivos, carpetas y vínculos) y comandos a través de un menú contextual al que se puede acceder desde el botón de la barra de tareas del programa y el elemento menú Inicio incluso si el programa no se está ejecutando actualmente.
-   Las barras de herramientas en miniatura proporcionan acceso rápido a los comandos usados con frecuencia para una ventana determinada. Las barras de herramientas en miniatura aparecen en la miniatura del botón de la barra de tareas.
-   Los iconos de superposición muestran el cambio de estado en el icono de botón de la barra de tareas del programa.
-   Las barras de progreso muestran el progreso de las tareas de ejecución larga en el botón de la barra de tareas del programa.
-   Los botones de la barra de tareas de sub window permiten a los usuarios usar miniaturas de botón de la barra de tareas para cambiar directamente a pestañas de ventana, ventanas de proyecto, ventanas secundarias de interfaz de múltiples documentos (MDI) y ventanas secundarias.
-   Los botones de la barra de tareas anclados permiten a los usuarios anclar botones de programa a la barra de tareas para proporcionar acceso rápido a los programas incluso cuando no se están ejecutando.

Técnicamente, la barra de tareas abarca toda la barra desde la botón Inicio al área de notificación; Sin embargo, más comúnmente, la barra de tareas solo hace referencia al área que contiene los botones de la barra de tareas. Para varias configuraciones de monitor, solo un monitor tiene una barra de tareas y ese monitor es el predeterminado.

**Nota:** Las directrices relacionadas [con el escritorio,](winenv-desktop.md) [el área de notificación](winenv-notification.md)y la administración de ventanas se presentan en artículos independientes. [](win-window-mgt.md)

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Los programas diseñados para Windows 7 pueden aprovechar estas características del botón de la barra de tareas. Pregúntese las siguientes preguntas clave para determinar si desea usarlas o no:

**Listas de saltos**

-   **¿A menudo los usuarios necesitan iniciar nuevas tareas mediante el programa?** Si es así, considere la posibilidad de proporcionar Lista de accesos directos. Aunque las listas de saltos se pueden usar para otros fines, la mayoría de los escenarios implican iniciar una nueva tarea.
-   **¿A menudo los usuarios necesitan acceder a archivos, carpetas, vínculos u otros recursos usados recientemente o con frecuencia?** Si es así, considere la posibilidad de proporcionar Lista de accesos directos acceso a estos recursos útiles.

    ![captura de pantalla de la barra de tareas con la lista de saltos de Internet Explorer ](images/winenv-taskbar-image2.png)

    En este ejemplo, Windows Internet Explorer un Lista de accesos directos para presentar páginas visitadas con frecuencia.

-   **¿A menudo los usuarios necesitan acceso rápido a un pequeño número de comandos del programa mientras usan otros programas, incluso si el programa no se está ejecutando?** Si es así, considere la posibilidad de proporcionar Lista de accesos directos con estos comandos usados con frecuencia. Estos comandos deben funcionar incluso si el programa no se está ejecutando y deben aplicarse a todo el programa, no a una ventana específica. Como alternativa, considere la posibilidad de proporcionar una barra de herramientas en miniatura para los comandos que se aplican a una ventana específica.

    ![captura de pantalla de la barra de tareas con la lista de accesos de notas rápidas ](images/winenv-taskbar-image3.png)

    En este ejemplo, el Notas rápidas complemento permite a los usuarios crear una nueva nota rápidamente mientras usan otros programas.

-   **¿Está promocionando características nuevas, de uso único o difíciles de encontrar?** Si es así, no use jump lists porque no están diseñados para este propósito. En su lugar, mejore la detectabilidad de estos comandos directamente en el programa.

**Barras de herramientas de miniaturas**

¿Se aplican todas las condiciones siguientes?

-   **¿Los comandos se aplican a una ventana específica?** Las barras de herramientas en miniatura son para los comandos que se aplican a las tareas existentes, Lista de accesos directos comandos son para iniciar nuevas tareas.
-   **¿Es necesario que los usuarios interactúen rápidamente con una tarea en ejecución mientras usan otros programas?** Si es así, las barras de herramientas en miniatura son una buena opción. Las barras de herramientas en miniatura pueden presentar un máximo de siete comandos, pero generalmente se prefiere un máximo de cinco comandos.
-   **¿Los comandos son inmediatos?** Es decir, ¿no requieren entradas adicionales? Las barras de herramientas en miniatura deben tener comandos inmediatos para ser eficaces, mientras que las listas de accesos directos funcionan mejor con comandos que requieren entrada adicional.

    **Incorrecto:**

    ![captura de pantalla de la barra de tareas con ventanas superpuestas ](images/winenv-taskbar-image4.png)

    Los comandos que requieren entrada adicional no funcionan bien en las barras de herramientas en miniatura.

-   **¿Los comandos son directos?** Es decir, ¿los usuarios pueden interactuar con ellos con un solo clic? Las barras de herramientas deben tener comandos directos para ser eficaces.
-   **¿Los comandos están bien representados por iconos?** Los comandos de la barra de herramientas de miniaturas se presentan mediante iconos no etiquetas de texto, Lista de accesos directos los comandos se representan mediante etiquetas de texto.

    **Incorrecto:**

    ![captura de pantalla del comando thumbnail con icono ](images/winenv-taskbar-image5.png)

    En este ejemplo, el comando no está bien representado por iconos.

**Iconos de superposición**

-   **¿El programa tiene "presencia de escritorio"?** Si no es así, use un icono de área de notificación en su lugar. Si es así, considere la posibilidad de usar un icono de superposición en lugar de colocar el estado en el icono del área de notificación para los programas diseñados para Windows 7. Esto garantiza que el icono siempre estará visible (cuando se usan iconos grandes) y consolida el programa con su estado en un solo lugar.
-   **¿Se muestra temporalmente el icono de superposición para mostrar un cambio de estado?** Si es así, un icono de superposición puede ser adecuado, en función de los siguientes factores:
    -   **¿Es útil y pertinente el estado al usar otros programas?** Si no es así, muestre la información en las barras de estado [del](ctrl-status-bars.md) programa u otro área de estado del programa.

        ![captura de pantalla de la barra de estado de la ventana de Internet Explorer ](images/winenv-taskbar-image7.png)

        En este ejemplo, se usa la barra de estado porque el estado no es útil cuando se usan otros programas.

    -   **¿El estado muestra el progreso?** Si es así, use en su lugar una barra de progreso del botón de la barra de tareas.
    -   **¿Es crítico el estado? ¿Se requiere una acción inmediata?** Si es así, muestre la información de forma que exija atención y no se pueda omitir fácilmente, como un cuadro [de diálogo](win-dialog-box.md).

**Barras de progreso**

-   **¿Los comentarios sobre el progreso son útiles y pertinentes mientras se usan otros programas?** Es decir, ¿es probable que los usuarios supervisen el progreso mientras usan otros programas y cambien su comportamiento como resultado? Este estado útil y pertinente normalmente se muestra mediante un cuadro de diálogo de progreso de modeless o una página de progreso dedicada, pero no con un puntero ocupado, un indicador de actividad o una barra de progreso en una barra de estado. Si el estado no es útil al usar otros programas, solo tiene que mostrar los comentarios de progreso directamente en el propio programa.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo copiar con barra de progreso ](images/winenv-taskbar-image8.png)

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso en el botón de la barra de tareas ](images/winenv-taskbar-image9.png)

    En el ejemplo incorrecto, la barra de tareas de progreso del botón no es muy útil.

-   **¿La tarea es continua?** Si la tarea nunca se completa, no es necesario mostrar su progreso. Algunos ejemplos de tareas continuas son los exámenes antivirus que los usuarios no inician y la indexación de archivos.

    **Incorrecto:**

    ![captura de pantalla del icono de progreso de una tarea continua ](images/winenv-taskbar-image10.png)

    En este ejemplo, no es necesario que una tarea continua muestre el progreso.

**Barras de tareas de sub window**

-   **¿El programa contiene pestañas, ventanas de proyecto, ventanas secundarias MDI o ventanas secundarias a las que los usuarios suelen querer cambiar directamente?** Si es así, es posible que sea adecuado dar a estas ventanas sus propias miniaturas de botón de la barra de tareas.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Uso eficaz de listas de saltos y barras de herramientas de miniaturas

Las listas de accesos directos y las barras de herramientas en miniatura ayudan a los usuarios a acceder a los recursos y a realizar comandos de forma más eficaz. Sin embargo, al diseñar cómo el programa admite estas características, no se da por hecho una mayor eficacia. Si los usuarios no pueden predecir con precisión qué característica tiene el comando que necesitan, o si tienen que comprobar varios lugares, finalmente los usuarios se frustrarán y dejarán de usar estas características.

Las listas de saltos y las barras de herramientas en miniatura funcionan de forma más eficaz cuando:

-   **Claramente diferenciado.** Los usuarios saben cuándo buscar un destino o un comando en un Lista de accesos directos y cuándo buscar en una barra de herramientas en miniatura. Hay un propósito claro para cada uno, por lo que los usuarios rara vez confunden el contenido de los dos. Por lo general, las listas de accesos rápidos se usan para iniciar nuevas tareas, mientras que las barras de herramientas en miniatura se usan para interactuar con tareas en ejecución mientras se usan otros programas.
-   **Útil.** Los destinos y comandos ofrecidos son los que necesitan los usuarios. Si es probable que los usuarios no necesiten algo, no se incluye. No use el número máximo de elementos si no son necesarios.
-   **Predecible.** Los destinos y comandos ofrecidos son los que los usuarios esperan encontrar. Los usuarios rara vez tienen que buscar en más de un lugar.
-   **Bien organizado.** Los usuarios pueden encontrar lo que buscan rápidamente. Usan etiquetas descriptivas pero concisas e iconos adecuados para ayudar al reconocimiento.

Asegúrese de realizar investigaciones de usuario para asegurarse de que tiene la razón. Si, en última instancia, descubre que no puede diseñar listas de saltos y barras de herramientas en miniatura juntas que logren estos objetivos, considere la posibilidad de proporcionar solo una de ellas. Es mejor tener una manera predecible de proporcionar comandos que dos confusos.

## <a name="guidelines"></a>Directrices

### <a name="taskbar-buttons"></a>Botones de la barra de tareas

-   **Haga que los siguientes tipos de ventana aparezcan en la barra de tareas (para Windows 7, mediante una miniatura de botón de la barra de tareas):**
    -   Ventanas principales (que incluye cuadros de diálogo sin propietarios)
    -   Hojas de propiedades
    -   Cuadros de diálogo de progreso de modeless
    -   Asistentes
-   **Para Windows 7, use miniaturas de botón de la barra de tareas para agrupar los siguientes tipos de ventana con el botón de la barra de tareas de la ventana principal desde el que se inició.** Cada programa (en concreto, cada programa que se percibe como un programa independiente) debe tener un solo botón de barra de tareas.

    -   Ventanas secundarias
    -   Pestañas del área de trabajo
    -   Project windows
    -   ventanas secundarias MDI

    **Correcto:**

    ![captura de pantalla del Explorador de Windows y la barra de progreso ](images/winenv-taskbar-image11.png)

    En este ejemplo, una ventana secundaria se agrupa con el botón de la barra de tareas de la ventana principal.

    **Incorrecto:**

    ![captura de pantalla del explorador de Windows y el panel de control ](images/winenv-taskbar-image12.png)

    En este ejemplo, Panel de control se agrupa incorrectamente con Windows Explorer. Los usuarios los perciben como programas independientes.

    **Incorrecto:**

    ![captura de pantalla del programa, la barra de progreso y una barra de tareas ](images/winenv-taskbar-image13.png)

    En este ejemplo, Copias de seguridad de Windows usa incorrectamente dos botones de la barra de tareas para un solo programa.

-   **La restauración de una ventana principal también debe restaurar** todas sus ventanas secundarias, incluso si esas ventanas secundarias tienen sus propios botones de barra de tareas. Al restaurar, coloque las ventanas secundarias encima de la ventana principal.
-   **En Windows 7, los programas que normalmente tienen presencia de escritorio pueden mostrar temporalmente un botón de la barra de tareas para mostrar el estado.** Solo lo hace si el programa se muestra normalmente en el escritorio y los usuarios interactúan con él con frecuencia. Un programa que normalmente se ejecuta sin presencia de escritorio debe usar su icono de área de notificación en su lugar, aunque es posible que no siempre esté visible.

    **Incorrecto:**

    ![captura de pantalla del botón de la barra de tareas del centro de sincronización de Windows ](images/winenv-taskbar-image14.png)

    En este ejemplo, Windows Centro de sincronización usa incorrectamente un botón de barra de tareas temporal para mostrar el estado. En su lugar, debe usar su icono de área de notificación.

### <a name="icons"></a>Iconos

-   **Diseñe el icono del programa para que se vea bien en la barra de tareas.** Asegúrese de que sea significativo y refleje su función y su marca. Haz que sea distinto, haz que sea especial y asegúrate de que se representa bien en todos los tamaños de icono. Dedime el tiempo necesario para hacerlo bien. Siga las [directrices del icono de estilo de Avión.](vis-icons.md)
-   **Si el programa usa iconos de superposición, diseñe el icono base del programa para controlar bien las superposiciones.** Los iconos superpuestos se muestran en la esquina inferior derecha, por lo que debe diseñar el icono para que esa área se pueda ocultar.

    ![captura de pantalla de iconos y con superposición inferior derecha ](images/winenv-taskbar-image15.png)

    En este ejemplo, el icono de botón de la barra de tareas del programa no tiene información importante en el área inferior derecha.

-   **No use superposiciones en el icono base** del programa, independientemente de si el programa usa iconos de superposición o no. El uso de una superposición en el icono base será confuso porque los usuarios tendrán que averiguar que no se está comunicando el estado.

    **Incorrecto:**

    ![captura de pantalla del icono base con superposición ](images/winenv-taskbar-image16.png)

    En este ejemplo, el icono base del programa parece que muestra el estado.

Para obtener instrucciones y ejemplos de iconos generales, vea [Iconos](vis-icons.md).

### <a name="overlay-icons"></a>Iconos de superposición

-   **Use iconos de superposición para indicar solo el estado útil y pertinente.** Considere la presentación de un icono de superposición como una posible interrupción del trabajo del usuario, por lo que el cambio de estado debe ser lo suficientemente importante como para merecer una posible interrupción.

    **Incorrecto:**

    ![captura de pantalla de tres iconos superpuestos ](images/winenv-taskbar-image17.png)

    En estos ejemplos, el icono de superposición no es lo suficientemente importante como para merecer una posible interrupción.

-   **Use iconos de superposición para el estado temporal.** Los iconos de superposición pierden su valor si se muestran constantemente, por lo que el estado normal del programa no debe mostrar un icono. Quite el icono de superposición cuando el icono:

    -   **Es para un problema:** Quite el icono una vez que se haya resuelto el problema.
    -   **Alerta de que algo es nuevo:** Quite el icono una vez que el usuario haya activado el programa.

    **Excepción:** El programa puede mostrar constantemente un icono de superposición si los usuarios siempre necesitan conocer su estado.

    ![captura de pantalla de Live Messenger con icono de superposición ](images/winenv-taskbar-image18.png)

    En este ejemplo, Windows Live Messenger muestra siempre un icono de superposición para que los usuarios siempre puedan comprobar su presencia notificada.

-   **No muestre un icono para indicar que se ha resuelto un problema.** En su lugar, simplemente quite cualquier icono anterior que indique un problema. Suponga que los usuarios normalmente esperan que el programa se ejecute sin problemas.
-   **Muestra iconos superpuestos o iconos de área de notificación, pero nunca ambos.** El programa puede admitir ambos mecanismos para la compatibilidad con versiones anteriores, pero si el programa muestra el estado mediante iconos superpuestos, no debe usar también iconos de área de notificación para el estado.

    **Incorrecto:**

    ![captura de pantalla de la barra de tareas con el icono mostrado dos veces ](images/winenv-taskbar-image19.png)

    En este ejemplo, el nuevo icono de correo se muestra de forma redundante.

-   **No flashee el botón de la barra de tareas para llamar la atención sobre un cambio de estado.** Hacerlo sería demasiado distraer. Permitir que los usuarios detecten iconos superpuestos por sí mismos.
-   **Se prefieren iconos de superposición estándar para indicar los cambios de estado o de estado.** Use estos iconos de superposición estándar: 

    | Overlay | Status |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | ![captura de pantalla del icono de advertencia pequeño ](images/winenv-taskbar-image20.png)<br/>               | Advertencia<br/>               |
    | ![captura de pantalla del icono de error pequeño ](images/winenv-taskbar-image21.png)<br/>                 | Error<br/>                 |
    | ![captura de pantalla del icono pequeño deshabilitado o desconectado ](images/winenv-taskbar-image22.png)<br/> | Deshabilitado o desconectado<br/> |
    | ![captura de pantalla del icono pequeño bloqueado o sin conexión ](images/winenv-taskbar-image23.png)<br/>       | Bloqueado/sin conexión<br/>       |

    

     

-   **Para los iconos de superposición personalizados, elija un diseño fácilmente reconocible.** Use iconos de color completo de 16 x 16 píxeles de alta calidad. Prefiere iconos con contornos distintivos sobre iconos con forma cuadrada o rectangular. Aplique también las [otras directrices de icono](vis-icons.md) de estilo Avión.
-   **Mantenga sencillo el diseño de iconos de superposición personalizados.** No intente comunicar ideas complejas, desconocidas o abstractas. Si no puede pensar en un icono personalizado adecuado, use un icono estándar de error o icono de advertencia en su lugar cuando corresponda. Estos iconos se pueden usar eficazmente para comunicar muchos tipos de estado.
-   **No cambie el estado con demasiada frecuencia.** Los iconos superpuestos no deben parecer ruidosos, inestables ni exigir atención. El ojo es sensible a los cambios en el campo periférico de la visión, por lo que los cambios de estado deben ser sutiles.
    -   **No cambie el icono rápidamente.** Si el estado subyacente cambia rápidamente, haga que el icono refleje el estado general.

        **Incorrecto:**

        ![captura de pantalla del icono de superposición en dos estados ](images/winenv-taskbar-image24.png)

        En este ejemplo, el icono de superposición que cambia rápidamente requiere atención.

    -   **No use animaciones.** Hacerlo es demasiado distraer.
    -   **No flashee el icono.** Hacerlo es demasiado distraer. Si un evento requiere atención inmediata, use un cuadro de diálogo en su lugar. Si el evento necesita atención, use una notificación.

### <a name="taskbar-button-flashing"></a>Parpadear el botón de la barra de tareas

-   **Use el parpadeo de botones de la barra de tareas con moderación para exigir la atención inmediata del usuario para mantener una tarea en curso en ejecución.** Es difícil que los usuarios se concentren mientras parpadea un botón de la barra de tareas, así que suponga que interrumpirán lo que hacen para que se detenga. Aunque parpadear un botón de la barra de tareas es mejor que robar el foco de entrada, los botones de la barra de tareas parpadeantes siguen siendo muy intrusivos. Asegúrese de que la interrupción está justificada, por ejemplo, para indicar que el usuario debe guardar los datos antes de cerrar una ventana. Los programas inactivos rara vez deben requerir una acción inmediata. No flashee el botón de la barra de tareas si lo único que tiene que hacer el usuario es activar el programa, leer un mensaje o ver un cambio de estado.
-   **Si no se requiere una acción inmediata, tenga en cuenta estas alternativas:**
    -   Use una [notificación de acción correcta](mess-notif.md) para indicar que se ha completado una tarea.
    -   No haga nada. Espere a que los usuarios atendan el problema la próxima vez que activen el programa. Esta suele ser la mejor opción.
-   **Si un programa inactivo requiere atención inmediata, flashee el botón de la barra de tareas para llamar la atención y déjelo resaltado.** No haga nada más: no restaure ni active la ventana y no reprodgue ningún efecto de sonido. En su lugar, respete la selección del estado de la ventana del usuario y deje que el usuario active la ventana cuando esté listo.
-   **Para las ventanas secundarias que tienen un botón de la barra de tareas, flash su botón en lugar del botón de la barra de tareas de la ventana principal.** Esto permite que los usuarios asistan directamente a la ventana.
-   **En el caso de las ventanas secundarias que no tienen un botón de barra de tareas, flashee el botón de la barra de tareas de la ventana principal y lleve la ventana secundaria encima de todas las demás ventanas de ese programa.** Las ventanas secundarias que requieren atención deben ser las más destacadas para asegurarse de que los usuarios las ven.
-   **Flash solo un botón de la barra de tareas para una ventana a la vez.** No es necesario parpadear más de un botón y distraer demasiado.
-   **Quite el resaltado del botón de la barra de tareas una vez que el programa se active.**
-   **Cuando el programa se active, asegúrese de que hay algo obvio que hacer.** Normalmente, este objetivo se logra mediante la visualización de un cuadro de diálogo que realiza una pregunta o inicia una acción.

### <a name="quick-launch-shortcuts"></a>inicio rápido accesos directos

-   **Coloque los métodos abreviados de programa en inicio rápido solo si los usuarios optan por participar.** Dado inicio rápido se quitó de Windows 7, los programas diseñados para Windows 7 no deben agregar accesos directos de programa al área inicio rápido ni proporcionar opciones para ello.

### <a name="jump-lists"></a>Listas de saltos

**Diseño**

-   **Diseñar listas de saltos para satisfacer los objetivos de los usuarios para sus tareas diarias.** Tenga en cuenta lo siguiente:
    -   **El propósito del programa.** Piense en lo que es más probable que hagan los usuarios a continuación. En el caso de los programas de creación de documentos, es probable que los usuarios vuelvan a los documentos usados recientemente. En el caso de los programas que muestran contenido existente, es posible que los usuarios quieran acceder a los recursos que usan con frecuencia. En el caso de otros programas, es posible que los usuarios puedan realizar tareas que no hayan hecho antes, como leer mensajes nuevos, ver vídeos nuevos o comprobar su próxima reunión.
    -   **Lo que más interesa a los usuarios.** Piense por qué los usuarios usarían el Lista de accesos directos en lugar de otros medios. Por ejemplo, es más probable que a los usuarios les importan los destinos que han identificado explícitamente como importantes (por ejemplo, las direcciones web que los usuarios colocan en la barra de vínculos o en Favoritos o escriben). Es menos probable que se preocupa por las obtenidas indirectamente o con poco esfuerzo (por ejemplo, las direcciones web visitadas a través del redireccionamiento o haciendo clic en vínculos).

        **Correcto:**

        ![captura de pantalla de la lista de saltos con un vínculo a un destino ](images/winenv-taskbar-image25.png)

        **Incorrecto:**

        ![captura de pantalla de la lista de saltos con cinco vínculos al destino ](images/winenv-taskbar-image26.png)

        En el ejemplo incorrecto, el Lista de accesos directos contiene muchos destinos que es probable que a los usuarios no les preocupen.

-   **No haga destinos demasiado pormenorizados.** Hacer que los destinos sea demasiado estrechos y específicos puede dar lugar a redundancia, con varias maneras de ir al mismo lugar. Por ejemplo, en lugar de enumerar páginas web individuales, en su lugar se enumeran las páginas principales de nivel superior. en lugar de enumerar canciones, enumera los álbumes.

    **Correcto:**

    ![captura de pantalla de la lista de saltos organizada por grupos ](images/winenv-taskbar-image27.png)

    **Incorrecto:**

    ![captura de pantalla de la lista de saltos organizada por canciones ](images/winenv-taskbar-image28.png)

    En el ejemplo incorrecto, la enumeración de canciones en un Lista de accesos directos la rellenará con un solo álbum.

-   **No rellene todas las ranuras Lista de accesos directos disponibles si no es necesario.** Cént Lista de accesos directos contenido en los elementos más útiles si el programa tiene solo tres elementos útiles, proporcione solo tres. A más elementos de un Lista de accesos directos, más esfuerzo se necesita para encontrar un elemento específico.

    ![captura de pantalla de jump list con un comando ](images/winenv-taskbar-image29.png)

    En este ejemplo, el Notas rápidas proporciona un único Lista de accesos directos, ya que es todo lo que se necesita.

-   **Proporcione información sobre herramientas solo cuando sea necesario para ayudar a los usuarios a comprender Lista de accesos directos elementos.** Evite la información sobre herramientas redundante porque es una distracción innecesaria. Para obtener más instrucciones sobre herramientas, vea [Información sobre herramientas e información sobre herramientas.](ctrl-tooltips-and-infotips.md)

    **Incorrecto:**

    ![captura de pantalla de jump list con información sobre herramientas redundante ](images/winenv-taskbar-image30.png)

    En este ejemplo, la información Lista de accesos directos información sobre herramientas es redundante.

**Lista de accesos directos frente a las características del programa**

-   **No haga que los destinos y comandos estén disponibles solo a través de listas de saltos.** Los mismos destinos y comandos deben estar disponibles directamente desde el propio programa.
-   **Use nombres coherentes para destinos y etiquetas para los comandos.** Lista de accesos directos los elementos deben etiquetarse igual que los elementos equivalentes a los que se accede directamente desde el programa.
-   **Habilite el programa para controlar destinos y comandos incluso cuando el programa no se esté ejecutando.** Esto es necesario para una experiencia coherente, confiable y cómoda.

**Agrupación**

-   **Proporcione al menos uno y, como máximo, tres grupos.** Lista de accesos directos siempre se agrupan para etiquetar su propósito. Tener más de tres grupos hace que los elementos sea más difícil de encontrar.
-   **Use nombres de grupo estándar cuando sea necesario.** Los nombres de grupo estándar son familiares y fáciles de entender para los usuarios.

    A los comandos se les asigna el nombre del grupo Tareas, que Windows y, por lo tanto, no se pueden cambiar.

    **Correcto:**

    ![captura de pantalla de la lista de saltos con el nombre del grupo reciente ](images/winenv-taskbar-image31.png)

    **Incorrecto:**

    ![captura de pantalla de la lista de saltos con el nombre del grupo de historial ](images/winenv-taskbar-image32.png)

    Recientes es el mejor nombre de grupo porque es familiar y no merece la pena distinguir sutilmente entre el historial y el reciente.

**Comandos**

-   **Proporcione un conjunto fijo de comandos independientemente del estado de ejecución del programa, el documento actual o el usuario actual.** Los comandos deben aplicarse a todo el programa, no a una ventana o documento específicos. Esto es necesario para una experiencia coherente, confiable y cómoda. Los comandos no deben quitarse ni deshabilitarse.

    **Excepciones:** Puede sustituir o quitar comandos cuando:

    -   Un conjunto de comandos mutuamente excluyentes comparte una sola ranura de comandos, siempre y cuando siempre se aplique un comando.
    -   Los comandos no se aplican hasta que se han usado características específicas, siempre y cuando siempre se apliquen los comandos.

    **Incorrecto:**

    ![captura de pantalla de la lista de saltos con la tarea de impresión ](images/winenv-taskbar-image33.png)

    En este ejemplo, Imprimir no es un buen Lista de accesos directos comando porque depende del documento actual.

    **Correcto:**

    ![captura de pantalla de jump list con inicio y cerrar sesión ](images/winenv-taskbar-image34.png)

    En este ejemplo, Iniciar sesión y Cerrar sesión son comandos mutuamente excluyentes. Además, los separadores se usan para agrupar comandos relacionados.

-   **Use las siguientes etiquetas de comando estándar cuando sea necesario.** Las etiquetas de comandos estándar son más fáciles de entender para los usuarios.
-   **Presente los comandos en un orden lógico.** Los pedidos comunes incluyen por frecuencia de uso o orden de uso. Coloque comandos muy relacionados entre sí. En el grupo Tareas, coloque los separadores entre grupos de comandos relacionados según sea necesario.
-   **No proporcione comandos para abrir o cerrar el programa.** Estos comandos están integrados en todas las listas de accesos.

**Iconos de comando**

-   **Dentro del grupo Tareas,** proporcione un icono de comando solo cuando ayude a los usuarios a comprender, reconocer o diferenciar comandos, especialmente cuando hay un icono establecido para el comando que se usa dentro del programa.

    -   **Excepción:** Si el programa usa ambos destinos (que siempre tienen iconos) y comandos, considere la posibilidad de proporcionar iconos para todos los comandos si no lo hace sería complicado.

    **Incorrecto:**

    ![captura de pantalla de la lista de saltos uso incoherente de iconos ](images/winenv-taskbar-image35.png)

    En este ejemplo, Internet Explorer proporcionar iconos para todos los comandos a fin de evitar una apariencia difícil.

**Destinations**

-   **Proporcione un conjunto dinámico de destinos específicos del usuario actual, pero independientes del programa que ejecuta el estado o el documento actual.** Como se mencionó anteriormente, asegúrese de que se ajusten al propósito del programa, de que son los que más les importan a los usuarios y de que tienen el nivel adecuado de especificidad.
-   **Cuando sea adecuado, use una lista de destino "automática".** Los destinos automáticos se administran Windows, pero el programa controla los destinos específicos que se pasan.
    -   Considere la posibilidad de usar Recientes para los programas de creación de documentos en los que es probable que los usuarios vuelvan a destinos usados recientemente.

        ![captura de pantalla de la lista de saltos con el nombre del grupo "reciente" ](images/winenv-taskbar-image36.png)

        En este ejemplo, Windows Bloc de notas destinos recientes.

    -   Considere la posibilidad de usar Frecuente para programas que muestran contenido existente, donde es probable que los usuarios vuelvan a los elementos que usan con frecuencia. Los destinos frecuentes se ordenan por orden de frecuencia, primero con más frecuencia.

        ![captura de pantalla de la lista de saltos con el nombre frecuente del grupo ](images/winenv-taskbar-image37.png)

        En este ejemplo, Windows Explorer usa destinos frecuentes.

    -   Usar Frecuente si es reciente daría lugar a muchos destinos inutilizados. Las listas frecuentes son más estables y la mejor opción cuando los usuarios van a muchos destinos diferentes, pero no es probable que vuelvan a los usados con muy poco frecuencia.

        **Incorrecto:**

        ![captura de pantalla de la lista de saltos con varios elementos recientes ](images/winenv-taskbar-image38.png)

        El uso de Recientes en Windows Internet Explorer provocaría muchos destinos inutilizados.

    -   Si las opciones Recientes o Frecuentes son igualmente adecuadas, use Recientes porque ese enfoque es más fácil de entender para los usuarios y es más predecible.
    -   Si usa Recientes y el programa tiene un equivalente en el menú Archivo, haga que las listas tengan el mismo contenido en el mismo orden. Para los usuarios, deben parecerse a las mismas listas.

-   **Cuando sea necesario, use una lista de destino personalizada.** El programa tiene control total sobre el contenido y el criterio de ordenación de una lista de destino personalizada y, por tanto, puede basar la lista en cualquier factor.
    -   Cree versiones personalizadas de Recientes o Frecuentes si son adecuadas, pero la administración automática no funciona bien para el programa. Por ejemplo, es posible que el programa tenga que realizar un seguimiento de diversos factores más allá de los comandos de archivo abierto. En este caso, use el mismo nombre (Reciente o Frecuente) y el mismo criterio de ordenación porque los usuarios no serán conscientes de la diferencia.
    -   De lo contrario, use otro tipo de destino para satisfacer mejor los objetivos del usuario. A menudo, estas listas ayudan a los usuarios a realizar tareas que no han hecho antes, como leer mensajes nuevos, ver vídeos nuevos o comprobar su próxima reunión.

        ![captura de pantalla de la lista de saltos con el nombre del grupo "nuevo" ](images/winenv-taskbar-image39.png)

        En este ejemplo, Windows Media Center muestra que el usuario aún no ha visto el registro reciente.

    -   Elija un criterio de ordenación que se corresponda con el modelo mental del usuario de la lista. Por ejemplo, una lista de tareas de estilo tendría lo siguiente que hacer en primer lugar. Si no hay ningún modelo mental claro, ordene la lista de destino en orden alfabético.

-   **No use varias listas de destino que ofrecen vistas diferentes de los mismos datos.** En su lugar, varias listas de destino deben tener principalmente datos diferentes para admitir escenarios de diferencia. Por ejemplo, puede proporcionar una lista Reciente o una Lista frecuente, pero no ambas. Esto es un desperdicio si hay elementos superpuestos, pero confuso si se quitan los elementos superpuestos.

    **Incorrecto:**

    ![captura de pantalla de la lista de saltos con elementos de grupo repetidos ](images/winenv-taskbar-image40.png)

    En este ejemplo, proporcionar vistas diferentes de los mismos destinos es un desperdicio.

    **Correcto:**

    ![captura de pantalla de jump list con tareas bien organizadas ](images/winenv-taskbar-image41.png)

    En este ejemplo, las listas de destino tienen datos diferentes para diferentes tareas.

-   **Si el programa tiene un comando para borrar los datos de privacidad, borre también las listas de destinos.** Las listas de destino pueden contener datos confidenciales.

### <a name="thumbnail-toolbars"></a>Barras de herramientas de miniaturas

**Interacción**

-   **Proporcione hasta siete de los comandos más importantes y usados con frecuencia que se aplican a la ventana que se muestra en la miniatura.** No se sienta obligado a proporcionar tantos comandos como pueda si el programa solo tiene tres comandos importantes que se usan con frecuencia y solo proporciona tres.

    **Incorrecto:**

    ![captura de pantalla de la barra de herramientas con demasiados comandos ](images/winenv-taskbar-image42.png)

    En este ejemplo, la barra de herramientas de miniaturas tiene comandos que no son importantes.

-   **Use comandos directos e inmediatos.** Estos comandos deben tener un efecto inmediato al hacer clic en el comando no debería mostrar un menú desplegable ni un cuadro de diálogo para obtener más entradas.

    **Incorrecto:**

    ![captura de pantalla de miniatura con menú desplegable ](images/winenv-taskbar-image43.png)

    Los comandos de la barra de herramientas de miniaturas deben tener un efecto inmediato.

-   **Deshabilite los comandos que no se aplican al contexto actual o que generarían directamente un error.** No oculte estos comandos porque hacer esto hace que la presentación de la barra de herramientas sea inestable.
-   **No descarte la miniatura cuando los usuarios hacen clic en un comando si es probable que revisen los resultados o haga clic inmediatamente en otro comando.** Quite la miniatura de los comandos que indican que el usuario ha terminado por ahora, por ejemplo, con comandos que muestran otras ventanas.

    ![captura de pantalla de la miniatura del reproductor multimedia con el comando ](images/winenv-taskbar-image44.png)

    En este ejemplo, al hacer clic en Siguiente Reproductor de Windows Media muestra la miniatura porque es posible que los usuarios quieran proporcionar otros comandos.

    ![captura de pantalla de miniatura con icono de chat ](images/winenv-taskbar-image45.png)

    En este ejemplo, al hacer clic en Chat en Windows Live Messenger descarta la miniatura porque es más probable que los usuarios envíen un mensaje.

**Presentación**

-   **Asegúrese de que los iconos de la barra de herramientas de miniaturas se ajustan a las directrices de icono de estilo Avión.** Para cada comando, proporcione iconos de color completo de alta calidad de 16x16, 20x20 y 24 x 24 píxeles. Las versiones más grandes se usan en los modos de presentación de valores altos de ppp.
-   **Asegúrese de que los iconos estén claramente visibles en el color de fondo de la barra de herramientas en los estados normales y de mantener el puntero.** Evalúe siempre los iconos en contexto y en los modos de contraste alto.
-   **Elija diseños de icono de comando que comuniquen claramente su efecto.** Los iconos de comandos bien diseñados se explican por sí solos para ayudar a los usuarios a encontrar y comprender los comandos de forma eficaz.
-   **Elija iconos que sean reconocibles y distintivos.** Asegúrese de que los iconos tienen formas y colores distintivos. Esto ayuda a los usuarios a encontrar los comandos rápidamente, aunque no recuerden el símbolo del icono. Después del uso inicial, los usuarios no deben tener que confiar en la información sobre herramientas para distinguir entre los comandos.
-   **Proporcione información sobre herramientas para etiquetar cada comando.** Una buena información sobre herramientas etiqueta el control sin etiquetar al que se apunta. Para obtener instrucciones y ejemplos, vea [Información sobre herramientas e información sobre herramientas.](ctrl-tooltips-and-infotips.md)

### <a name="progress-bars"></a>Barras de progreso

-   **Siga las instrucciones generales de la barra** de progreso, lo que incluye no reiniciar ni hacer una copia de seguridad del progreso y usar una barra de progreso roja para indicar un problema.
-   **Evite usar barras de progreso indeterminados.** Las barras de progreso indeterminado muestran la actividad, no el progreso. Reserve barras de progreso indeterminadas para aquellas situaciones poco frecuentes en las que los usuarios no toman actividad para concederse.

Para obtener más instrucciones, vea [Barras de progreso](progress-bars.md).

## <a name="text"></a>Texto

### <a name="window-titles"></a>Títulos de ventana

Al elegir títulos de ventana, tenga en cuenta la apariencia del título en la barra de tareas:

-   Optimice los títulos para mostrarlos en la barra de tareas colocando primero la información distintiva de forma concisa.
-   En el caso de los cuadros de diálogo de progreso del modelo, primero resuma el progreso. Ejemplo: "66 % completado".
-   Evite los títulos de ventana que tengan truncamientos difíciles.

    **Incorrecto:**

    ![captura de pantalla del título que corta el nombre del programa ](images/winenv-taskbar-image48.png)

    En este ejemplo, el título de la ventana truncada tiene resultados desafortunados.

### <a name="jump-list-commands"></a>Lista de accesos directos comandos

-   **Comandos de inicio con un verbo.**
-   **Use mayúsculas de estilo de frase.**

Para obtener más instrucciones de etiquetas de comandos, vea [Menús](cmd-menus.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a la barra de tareas:

-   Consulte toda la barra como barra de tareas (una sola palabra compuesta en minúsculas).
-   Consulte los elementos de la barra de tareas específicamente por su etiqueta o, por lo general, como botones de la barra de tareas.
-   Cuando sea posible, formatee las etiquetas de la barra de tareas con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.
-   Consulte iconos superpuestos como iconos de botón de la barra de tareas. No haga referencia a ellas como notificaciones, aunque su propósito sea notificar a los usuarios. Sin embargo, puede decir que estos iconos notifican a los usuarios eventos específicos.

Ejemplo: el icono del botón De la barra de tareas Nuevo correo le notifica que ha llegado un nuevo mensaje de correo electrónico.

 

