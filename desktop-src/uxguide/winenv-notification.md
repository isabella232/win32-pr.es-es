---
title: Área de notificación
description: El área de notificación proporciona notificaciones y estado. Los programas bien diseñados usan el área de notificación adecuadamente, sin ser molestos ni distraer.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 48550b37068b44c83254f09983b68f9881845c6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471701"
---
# <a name="notification-area"></a>Área de notificación

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El área de notificación proporciona notificaciones y estado. Los programas bien diseñados usan el área de notificación adecuadamente, sin ser molestos ni distraer.

El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado. También se puede usar para mostrar iconos para las características del sistema y del programa que no tienen presencia en el escritorio.

Los elementos del área de notificación se conocen como iconos de área de notificación o simplemente iconos si el contexto del área de notificación ya está claramente establecido.

![captura de pantalla del área de notificación, la hora y la fecha ](images/winenv-notification-image1.png)

Área de notificación.

Para proporcionar a los usuarios el control de su escritorio Windows 7, no todos los iconos del área de notificación se muestran de forma predeterminada. En su lugar, los iconos se muestran en el desbordamiento del área de notificación a menos que el usuario la promueve al área de notificación.

![Captura de pantalla que muestra un área de notificación y un desbordamiento.](images/winenv-notification-image2.png)

Desbordamiento del área de notificación.

**Nota:** Las directrices relacionadas con [la barra de](winenv-taskbar.md)tareas, las [notificaciones](mess-notif.md) y los globos se presentan en [artículos](ctrl-balloons.md) independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿El programa necesita mostrar una notificación?** Si es así, debe usar un icono de área de notificación.
-   **¿Se muestra temporalmente el icono para mostrar un cambio de estado?** Si es así, un icono de área de notificación puede ser adecuado, en función de los siguientes factores:

    -   **¿El estado es útil y pertinente?** Es decir, ¿es probable que los usuarios supervisen el icono y cambien su comportamiento como resultado de esta información? Si no es así, no muestra el estado o lo coloca en un archivo de registro.

        **Incorrecto:**

        ![captura de pantalla del área de notificación con el icono de unidad ](images/winenv-notification-image3.png)

        En este ejemplo, el icono de actividad de unidad de disco es inadecuado porque es poco probable que los usuarios cambien su comportamiento en función de él.

    -   **¿Es crítico el estado? ¿Se requiere una acción inmediata?** Si es así, muestre la información de forma que exija atención y no se pueda omitir fácilmente, como un cuadro [de diálogo](win-dialog-box.md).

    Los programas diseñados para Windows 7 pueden usar iconos superpuestos en el botón de la barra de tareas del programa para mostrar el cambio de estado, así como barras de progreso del botón de la barra de tareas para mostrar el progreso de las tareas de ejecución larga.

-   **¿La característica ya tiene "presencia de escritorio"?** Es decir, cuando se ejecuta, ¿aparece la característica en una ventana del escritorio (posiblemente minimizada)? Si es así, muestre el estado en la barra de estado del [programa,](ctrl-status-bars.md)en otro área de estado o, para Windows 7, directamente en el botón de la barra de tareas. Si la característica no tiene presencia en el escritorio, puede usar un icono para el acceso al programa y para mostrar el estado.
-   **¿Es el icono principalmente para iniciar un programa o acceder rápidamente a sus características o configuraciones?** Si es así, use la menú Inicio para iniciar programas en su lugar. El área de notificación no está pensada para el acceso rápido a programas o comandos.

    ![captura de pantalla de la barra de herramientas de inicio rápido ](images/winenv-notification-image4.png)

    En este ejemplo de Windows Vista, inicio rápido se usa para iniciar Windows Explorer y Windows Internet Explorer rápidamente.

    Para los programas diseñados para Windows 7, los usuarios pueden anclar botones de la barra de tareas para un acceso rápido al programa. Los programas pueden usar una barra Lista de accesos directos o miniatura para acceder a los comandos usados con frecuencia directamente desde el botón de la barra de herramientas de un programa. El inicio rápido no se muestra de forma predeterminada en Windows 7.

    ![captura de pantalla de la barra de tareas y la lista de saltos con iconos ](images/winenv-notification-image5.png)

    En este ejemplo, se usa Lista de accesos directos para el acceso rápido a comandos.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="the-windows-desktop"></a>El Windows escritorio

El Windows escritorio tiene los siguientes puntos de acceso del programa:

-   **Área de trabajo.** Área en pantalla donde los usuarios pueden realizar su trabajo, así como almacenar programas, documentos y sus accesos directos. Aunque técnicamente el escritorio incluye la barra de tareas, en la mayoría de los contextos hace referencia solo al área de trabajo.
-   **botón Inicio.** Punto de acceso para todos los programas y lugares Windows especiales (Documentos, Imágenes, Música, Juegos, Equipo, Panel de control), con listas "usadas más recientemente" para acceder rápidamente a los documentos y programas usados recientemente.
-   **inicio rápido.** Un punto de acceso directo para los programas seleccionados por el usuario. inicio rápido se quitó de Windows 7.
-   **Barra.** Punto de acceso para ejecutar programas que tienen presencia en el escritorio. Aunque técnicamente la barra de tareas abarca toda la barra desde el botón Inicio hasta el área de notificación, en la mayoría de los contextos, la barra de tareas hace referencia al área entre, que contiene los botones de la barra de tareas. Esta área se conoce a veces como la banda de tareas.
-   **Deskbands. No se recomienda.**
-   **Área de notificación.** Un origen a corto plazo para las notificaciones y el estado, así como un punto de acceso para las características relacionadas con el sistema y el programa que no tienen presencia en el escritorio.

![captura de pantalla que identifica los puntos de acceso de escritorio ](images/winenv-notification-image6.png)

Los Windows de acceso de escritorio incluyen el botón Inicio, la barra de tareas y el área de notificación. Observe la característica de miniatura del botón de la barra de tareas.

**El escritorio es un recurso compartido limitado que es el punto de entrada del usuario para Windows.** Deje el control de los usuarios. Debe usar las áreas de escritorio según lo previsto, cualquier otro uso debe considerarse un abuso. Por ejemplo, nunca vea las áreas de escritorio como maneras de promocionar el programa o su [marca](exper-branding.md).

### <a name="using-the-notification-area-appropriately"></a>Uso adecuado del área de notificación

El área de notificación estaba pensada originalmente como un origen temporal para las notificaciones y el estado. Su eficacia y comodidad ha animado a los desarrolladores a darle otros propósitos, como iniciar programas y ejecutar comandos. Desafortunadamente, con el tiempo, estas adiciones hacían que el área de notificación sea demasiado grande y ruidoso, y confundía su propósito con los otros puntos de acceso de escritorio.

Windows XP solucionó el problema de escala haciendo que el área se contrayese y ocultando los iconos no usados. Windows Vista solucionó el ruido mediante la eliminación de notificaciones innecesarias e innecesarias. Windows 7 ha ido un paso más allá al centrar la notificación en su propósito original de ser un origen de notificación. **La mayoría de los iconos están ocultos de forma predeterminada Windows 7, pero el usuario puede promover manualmente al área de notificación. Para mantener a los usuarios en el control de sus escritorios, no hay ninguna manera de que el programa realice esta promoción automáticamente.** Windows muestra notificaciones de iconos ocultos al promocionarlos temporalmente.

![captura de pantalla del área de notificación y el desbordamiento ](images/winenv-notification-image7.png)

En Windows 7, la mayoría de los iconos del área de notificación están ocultos de forma predeterminada.

Además, Windows 7 admite muchas características directamente en los botones de la barra de tareas. En concreto, puede usar:

-   Listas de accesos directos y barras de herramientas en miniatura para acceder rápidamente a los comandos usados con frecuencia.
-   Iconos de superposición para mostrar el estado de los programas en ejecución.
-   Barras de progreso del botón de la barra de tareas para mostrar el progreso de las tareas de ejecución larga.

En resumen, si el programa tiene presencia de escritorio, aproveche al máximo las Windows del botón 7 de la barra de tareas para estos fines. **Mantenga los iconos del área de notificación centrados en mostrar las notificaciones y el estado.**

### <a name="keeping-users-in-control"></a>Mantener el control de los usuarios

Mantener a los usuarios en control se extiende más allá de usar correctamente el área de notificación. Dependiendo de la naturaleza del icono, es posible que quiera permitir que los usuarios hagan lo siguiente:

-   **Quite el icono.** El icono puede proporcionar un estado pertinente y útil, pero incluso así, es posible que los usuarios no quieran verlo. Windows permite a los usuarios ocultar iconos, pero esta característica no es fácil de detectar. Para mantener el control de los usuarios, proporcione la **opción Mostrar icono en** el área de notificación en el menú contextual del icono. Tenga en cuenta que quitar un icono no tiene que afectar al programa, la característica o el proceso subyacentes.
-   **Seleccione los tipos de notificaciones que se mostrarán.** La notificación debe ser útil y pertinente, pero puede haber notificaciones que los usuarios no quieran ver. Esto es especialmente cierto para las notificaciones [FYI](mess-notif.md). Permitir que los usuarios elijan habilitar las menos importantes.
-   **Suspender características opcionales.** Los iconos se usan para mostrar el estado de las características sin presencia del escritorio. Estas características tienden a ser tareas en segundo plano opcionales de ejecución larga, como impresión, indexación, examen o sincronización. Es posible que los usuarios quieran suspender estas características para aumentar el rendimiento del sistema, reducir el consumo de energía o porque están sin conexión.
-   **Salga del programa.** Proporcione la más adecuada de estas opciones:
    -   **Salir temporalmente del programa.** El programa se detiene y reinicia cuando Windows se reinicia. Este enfoque es adecuado para utilidades importantes del sistema, como los programas de seguridad.
    -   **Salir del programa de forma permanente.** El programa se detiene y no se reinicia Windows se reinicia (a menos que el usuario decida reiniciarlo más adelante). El usuario ya no quiere ejecutar el programa o quiere ejecutarlo a petición quizás para mejorar el rendimiento del sistema.

Aunque es una buena idea proporcionar la mayoría de estas opciones en el menú contextual del icono, la experiencia predeterminada del programa debe ser adecuada para la mayoría de los usuarios. No active todo de forma predeterminada y espere que los usuarios desactiven las características. En su lugar, active las características importantes de forma predeterminada y permita que los usuarios habiliten características adicionales según sea necesario.

**Si solo hace cuatro cosas...**

1.  No abuse del área de notificación. Úselo solo como origen para las notificaciones y el estado, y para las características sin presencia del escritorio.
2.  Mantenga el control de los usuarios. Proporcione las opciones adecuadas para controlar el icono, sus notificaciones y las características subyacentes.
3.  Presente una experiencia predeterminada que sea adecuada para la mayoría de los usuarios. Permita a los usuarios habilitar las características deseadas en lugar de esperar que deshabilite las no deseadas.
4.  Aproveche al máximo las características del Windows de la barra de tareas 7 para mostrar el estado y hacer que las tareas que se realizan con más frecuencia del programa son eficaces.

## <a name="usage-patterns"></a>Patrones de uso

Los iconos del área de notificación tienen varios patrones de uso:




| | | <strong>Acceso y estado del sistema</strong><br /> Se muestra continuamente para mostrar el estado del sistema importante, pero no crítico, y para proporcionar acceso a las características y configuraciones pertinentes. <br /> | Las características del sistema que necesitan iconos de área de notificación no tienen presencia de escritorio persistente. También se puede usar como origen de la notificación. <br /><img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br /> En este ejemplo, los iconos de batería, red y volumen se muestran continuamente cuando procede.<br /> | | <strong>Acceso y estado de la tarea en segundo plano</strong><br /> Se muestra mientras se ejecuta una tarea en segundo plano para mostrar el estado y proporcionar acceso a las características y la configuración. <br /> | Los procesos en segundo plano necesitan iconos de área de notificación cuando no tienen presencia en el escritorio. También se puede usar como origen de la notificación. <br /><img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br /> En este ejemplo, el icono del Centro de acciones permite a los usuarios comprobar su estado incluso cuando no tiene presencia en el escritorio.<br /> | | <strong>Estado del evento temporal</strong><br /> Los programas con presencia de escritorio pueden mostrar iconos temporalmente para mostrar eventos importantes o cambios en el estado. <br /> | <img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br /> En este ejemplo, los iconos para imprimir e instalar actualizaciones se muestran temporalmente para mostrar eventos importantes o cambios en el estado.<br /> | | <strong>Origen de notificación temporal</strong><br /> Se muestra temporalmente para mostrar una notificación. Se quita después de un tiempo de espera, o cuando se aborda el problema subyacente o se realiza una tarea. <br /> | Los iconos temporales son los preferidos para los orígenes de notificaciones puros. No muestre un icono que no proporcione un estado dinámico útil, relevante solo porque una característica podría necesitar mostrar una notificación en el futuro. <br /><img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br /> En este ejemplo, se muestra el icono de plug-and-play mientras se muestra una nueva notificación detectada por hardware.<br /> | | <strong>Aplicación de instancia única minimizada</strong><br /> Para reducir el desorden de la barra de tareas, una aplicación de ejecución larga de instancia única se puede minimizar en un icono de área de notificación en su lugar. <br /> | <img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br /> En este ejemplo de Windows Vista, Outlook y Windows Live Messenger son aplicaciones de instancia única que minimizan los iconos del área de notificación.<br /> Considere la posibilidad de usar este patrón solo si se aplican todos los siguientes elementos: <br /><ul><li>La aplicación solo puede tener una sola instancia.</li><li>La aplicación se ejecuta durante un largo período de tiempo.</li><li>El icono muestra el estado.</li><li>El icono puede ser un origen de notificación.</li><li>Esto es opcional y los usuarios deben <a href="glossary.md">participar en</a>.</li></ul>Si se aplican todas estas condiciones, minimizar un icono elimina tener dos puntos de acceso cuando solo se necesita uno. <br /><strong>Nota:</strong> Este patrón de icono ya no se recomienda para Windows 7. Use botones de la barra de tareas normales en su lugar si el programa tiene presencia en el escritorio.<br /><img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br /> En este ejemplo de Windows 7, un botón de la barra de tareas normal ocupa poco espacio, pero se beneficia de las características del botón de la barra de tareas de Windows 7, incluidas las listas de saltos, los iconos de superposición y las miniaturas enriquecciones.<br /> | 




 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Proporcione solo un icono de área de notificación por componente.**
-   **Use un icono con versiones de 16x16, 20x20 y 24 x 24 píxeles.** Las versiones más grandes se usan en modos de presentación de valores altos de ppp.

### <a name="when-to-show"></a>Cuándo mostrar

-   Para el patrón de origen de notificación temporal:
    -   Windows muestra el icono cuando se muestra la notificación.
    -   Quite el icono en función de su [patrón de diseño de](mess-notif.md) notificación:



    | Patrón                                     | Cuándo quitar                                         |
    |--------------------------------------|------------------------------------------|
    | Acción correcta<br/>            | Cuando se quita la notificación.<br/> |
    | Error de acción<br/>            | Cuando se resuelve el problema.<br/>     |
    | Evento del sistema no crítico<br/> | Cuando se resuelve el problema.<br/>     |
    | Tarea de usuario opcional<br/>        | Cuando se realiza la tarea.<br/>            |
    | FYI<br/>                       | Cuando se quita la notificación.<br/> |



 

-   **Para el patrón de estado del evento temporal, muestre el icono mientras se produce el evento.**
-   Para todos los demás patrones, muestre el icono cuando se esté ejecutando el **programa,**  la característica o el proceso y el icono sea relevante a menos que el usuario haya borrado su opción Mostrar icono en el área de notificación (para obtener más información, vea [Menús contextuales).](#context-menus) La mayoría de los iconos están ocultos de forma predeterminada Windows 7, pero el usuario puede promover al área de notificación.
-   **No muestre iconos diseñados para administradores para usuarios estándar.** Registre la información en el registro Windows eventos.

### <a name="where-to-show"></a>Dónde mostrar

-   **Mostrar ventanas iniciadas desde iconos de área de notificación cerca del área de notificación.**

![figura de una ventana cerca del área de notificación ](images/winenv-notification-image14.png)

Windows desde los iconos del área de notificación se muestran cerca del área de notificación.

### <a name="icons"></a>Iconos

-   **Elija el icono en función de su patrón de diseño:**

    | Patrón                                                 | Tipo de icono                                   |
    |--------------------------------------------------|------------------------------------|
    | Acceso y estado del sistema<br/>              | Icono de características del sistema<br/>     |
    | Acceso y estado de la tarea en segundo plano<br/>     | Icono de programa o característica<br/> |
    | Origen de notificación temporal<br/>         | Icono de programa o característica<br/> |
    | Estado del evento temporal<br/>                | Icono de programa o característica<br/> |
    | Aplicación de instancia única minimizada<br/> | Icono del programa<br/>            |

    

     

    ![captura de pantalla del área de notificación y los iconos de Outlook ](images/winenv-notification-image15.png)

    En este ejemplo, Outlook un icono de característica de correo electrónico para un origen de notificación temporal y su icono de aplicación para la aplicación minimizada.

-   **Elija un diseño de icono fácilmente reconocible.** Prefiere iconos con contornos únicos sobre iconos en forma cuadrada o rectangular. Mantener los diseños simples prefiere símbolos en lugar de imágenes realistas. Aplique también las [otras directrices de icono de estilo](vis-icons.md) acrob.
-   **Use variaciones de icono o superposiciones para indicar los cambios de estado o de estado.** Use variaciones de icono para mostrar los cambios en cantidades o puntos fuertes. Para otros tipos de estado, use las siguientes superposiciones estándar. Use solo una sola superposición y localíquela en la parte inferior derecha para mantener la coherencia. 

    | Overlay                                                                                                       | Estado                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![captura de pantalla del icono de advertencia pequeño ](images/winenv-notification-image16.png)<br/>               | Advertencia<br/>               |
    | ![captura de pantalla del icono de error pequeño ](images/winenv-notification-image17.png)<br/>                 | Error<br/>                 |
    | ![captura de pantalla del icono pequeño deshabilitado o desconectado ](images/winenv-notification-image18.png)<br/> | Deshabilitado o desconectado<br/> |
    | ![captura de pantalla del icono pequeño bloqueado o sin conexión ](images/winenv-notification-image19.png)<br/>       | Bloqueado o sin conexión<br/>       |

    

     

    ![captura de pantalla del área de notificación y dos iconos ](images/winenv-notification-image20.png)

    En este ejemplo, los iconos inalámbricos y de batería muestran cambios en cantidades o puntos fuertes.

    ![captura de pantalla del área de notificación y dos superposiciones ](images/winenv-notification-image21.png)

    En este ejemplo, las superposiciones se usan para mostrar los estados de error y advertencia.

-   **Evite franjas de rojo puro, amarillo y verde en los iconos base.** Para evitar confusiones, reserve estos colores para comunicar el estado. Si la [personalidad de](exper-branding.md) marca usa estos colores, considere la posibilidad de usar tono muted para los iconos del área de notificación base.
-   Para [la extensión progresiva,](mess-notif.md)use iconos con una apariencia progresivamente más enfática a medida **que la situación sea más urgente.**

    ![captura de pantalla del área de notificación y cinco iconos ](images/winenv-notification-image22.png)

    En estos ejemplos, la apariencia del icono de batería se vuelve más enfática a medida que aumenta la urgencia.

-   **No cambie el estado con demasiada frecuencia.** Los iconos del área de notificación no deben aparecer ruidosos, inestables ni exigir atención. El ojo es sensible a los cambios en el campo periférico de la visión, por lo que los cambios de estado deben ser sutiles.
    -   **No cambie el icono rápidamente.** Si el estado subyacente cambia rápidamente, haga que el icono refleje el estado de alto nivel.

        **Incorrecto:**

        ![captura de pantalla del área de notificación y el icono del módem ](images/winenv-notification-image23.png)

        En este ejemplo, el icono de módem muestra luces parpadeantes (como hace un módem de hardware), pero esos cambios de estado no son significativos para los usuarios.

    -   **No use animaciones de ejecución larga para mostrar actividades continuas.** Estas animaciones son una distracción. La presencia de un icono en el área de notificación indica suficientemente la actividad continua.
    -   **Las animaciones breves y sutiles son aceptables para mostrar el progreso durante cambios de estado temporales y transitivos importantes.**

        ![captura de pantalla del área de notificación y el icono inalámbrico ](images/winenv-notification-image24.png)

        En este ejemplo, el icono Inalámbrico muestra un indicador de actividad para mostrar que el trabajo está en curso.

    -   **No flashee el icono.** Hacerlo es demasiado distraer. Si un evento requiere atención inmediata, use un cuadro de diálogo en su lugar. Si el evento necesita atención, use una notificación.

-   **No deshabilite los iconos del área de notificación.** Si el icono no se aplica actualmente, quítelo. Sin embargo, puede mostrar un icono habilitado con una superposición de estado deshabilitada si los usuarios pueden habilitar desde el icono.

    ![captura de pantalla del área de notificación y el control deslizante del volumen ](images/winenv-notification-image25.png)

    En este ejemplo, los usuarios pueden habilitar la salida de sonido desde el icono.

Para obtener instrucciones y ejemplos de iconos generales, vea [Iconos.](vis-icons.md)

### <a name="interaction"></a>Interacción

**Nota:** Los siguientes eventos de clic deben producirse al pasar el mouse hacia arriba, no al bajar el mouse.

**Al mantener el puntero**

-   **Muestra una información sobre herramientas o información que indica lo que representa el icono.**

    ![captura de pantalla del área de notificación y la información sobre herramientas ](images/winenv-notification-image26.png)

    En este ejemplo, se usa una información sobre herramientas para describir el icono al mantener el puntero.

Para obtener instrucciones de texto de información, consulte [la sección Texto](#context-menus) de este artículo.

**Clic con un solo clic a la izquierda**

-   **Muestre lo que los usuarios más probables quieran ver,** que puede ser:

    -   Ventana de control desplegable, cuadro de diálogo o ventana de programa con la configuración más útil y tareas que se realizan habitualmente. Para obtener instrucciones de presentación, consulte [Los flyouts del área de notificación.](#notification-area-flyouts)

        ![captura de pantalla del área de notificación y los flyouts ](images/winenv-notification-image27.png)

        En estos ejemplos, al hacer clic a la izquierda se muestran ventanas emergentes con la configuración más útil.

    -   Un flyout de estado.

        ![captura de pantalla del área de notificación y el flyout de estado ](images/winenv-notification-image28.png)

        En este ejemplo, al hacer clic en la izquierda se muestra el menú desplegable de estado.

        -   Elemento del panel de control relacionado.
        -   Menú contextual.

    Los usuarios esperan que los clics izquierdos muestren algo, por lo que no mostrar nada hace que un icono de área de notificación parezca no responder.

-   **Muestre un menú contextual solo si las demás** opciones no se aplican, con el comando predeterminado en negrita. En este caso, muestre el mismo menú contextual que se muestra al hacer clic con el botón derecho para evitar confusiones.
-   **Prefiere usar una ventana emergente en lugar de un cuadro de diálogo** para una sensación más ligera. Muestre solo la configuración más común y haga que su efecto sea inmediato para una interacción más sencilla. Descarte la ventana emergente si el usuario hace clic en cualquier parte fuera de la ventana.
-   **Mostrar ventanas pequeñas cerca del icono asociado.** Sin embargo, las ventanas grandes, como los elementos del panel de control, se pueden mostrar en el centro del monitor predeterminado.

**Hacer doble clic a la izquierda**

-   **Realice el comando predeterminado en el menú contextual.** Normalmente, esto muestra la interfaz de usuario principal asociada al icono, como el elemento del panel de control asociado, la hoja de propiedades o la ventana del programa.
-   **Si no hay ningún comando predeterminado, realice la misma acción que un solo clic izquierdo.**

**Haga clic con el botón secundario en**

-   **Muestra el menú contextual**, con el comando predeterminado en negrita.

### <a name="context-menus"></a>Menús contextuales

-   **Muestra el menú contextual cerca de su icono asociado,** pero lejos de la barra de tareas.
-   **El menú contextual puede incluir los siguientes elementos,** según corresponda, en el orden indicado (el texto exacto está entre comillas):

Comandos principales

Abrir (valor predeterminado, enumerar primero, en negrita)

Ejecutar

Comandos secundarios

< separador>

Comando Suspend/resume enable/disable (marca de verificación)

"Minimizado en el área de notificación" (marca de verificación)

Participar en notificaciones (marca de verificación)

"Icono mostrar en el área de notificación" (marca de verificación)

< separador>

"Opciones"

"Salida"

-   **Quite en lugar de deshabilitar los elementos del menú contextual que no se apliquen.**
-   En el caso de los comandos Open, Run y Suspend/Resume, sea específico sobre lo que se **abre, ejecuta,** suspende y reanuda.

![Captura de pantalla que muestra un área de notificación y comandos.](images/winenv-notification-image29.png)

En este ejemplo, Windows Defender comandos open y run específicos.

-   **Use Suspender o reanudar la ejecución de tareas en segundo plano, Habilitar o deshabilitar para todo lo demás.**
-   **Use marcas de verificación para indicar el estado.** Enumerar y habilitar todos los estados y colocar la marca de verificación junto al estado actual. No deshabilite las opciones ni cambie las etiquetas de las opciones para indicar el estado actual.

**Correcto:**

![captura de pantalla de un comando con marca de verificación ](images/winenv-notification-image29.png)

**Incorrecto:**

![captura de pantalla de un comando sin marca de verificación ](images/winenv-notification-image30.png)

En el ejemplo incorrecto, Windows Defender debe usar una marca de verificación para indicar el estado actual.

-   **Todas las tareas en segundo plano deben tener un comando Suspender/Reanudar.** La elección del comando debe suspender temporalmente la tarea. Es posible que los usuarios quieran suspender temporalmente las tareas en segundo plano para aumentar el rendimiento del sistema o reducir el consumo de energía. Las tareas en segundo plano suspendidas se reinician cuando el usuario las reanuda o Windows se reinicia.
-   **Permitir a los usuarios participar o no en** distintos tipos de notificación si el programa tiene notificaciones que es posible que algunos usuarios no quieran ver. El [patrón de notificación FYI](mess-notif.md) requiere que los usuarios opten por participar, por lo que estas notificaciones deben deshabilitarse de forma predeterminada.

![captura de pantalla del área de notificación y los comandos ](images/winenv-notification-image31.png)

En este ejemplo, Outlook permite a los usuarios elegir las notificaciones que reciben del icono.

-   **Al desactivar la opción "Mostrar** icono en el área de notificación", se quita el icono del área de notificación, pero no se afecta al programa, la característica o el proceso subyacentes. Los usuarios pueden volver a mostrar el icono desde el cuadro de diálogo Opciones del programa. No vuelva a mostrar automáticamente el icono cuando Windows se reinicie.
-   **El comando Exit sale del programa para la sesión Windows actual y quita el icono.** No tenga un comando Exit si el programa no se puede apagar. El programa se reinicia cuando Windows se reinicia. Los usuarios pueden salir permanentemente del programa desde el cuadro de diálogo Opciones .
-   **No tiene un comando Acerca de.** El icono, su información y el menú contextual deben comunicar dicha información. Si los usuarios desean más información, pueden ver la interfaz de usuario principal.
    -   **Excepción:** Puede proporcionar un comando Acerca de si el icono es para un programa que no tiene presencia en el escritorio.

Para obtener instrucciones y ejemplos generales del menú contextual, vea [Menús](cmd-menus.md).

### <a name="rich-tooltips"></a>Información sobre herramientas enriquecida

-   **Use información sobre herramientas enriquecciones solo para que la información sea más fácil de entender.** No use información sobre herramientas enriquecciones solo para decorar la característica. Si no puede usar la enriquecimiento para facilitar la descripción de la información, use en su lugar una información sobre herramientas sin formato.

    **Incorrecto:**

    ![captura de pantalla del área de notificación y la información sobre herramientas enriquección ](images/winenv-notification-image32.png)

    **Correcto:**

    ![captura de pantalla del área de notificación y la información sobre herramientas sin formato ](images/winenv-notification-image33.png)

    En el ejemplo incorrecto, el icono de calendario no facilita la lectura de la fecha.

-   **Use una presentación concisa.** Use texto conciso y un diseño conciso con un icono de 32 x 32 píxeles. La información sobre herramientas cómoda corre el riesgo de distraerse, especialmente cuando se muestra de forma involuntarla.
-   **No coloque controles ni elementos que parezcan interactivos en una información sobre herramientas enriquezca.** La información sobre herramientas no es interactiva y, por tanto, no debería aparecer interactiva. No use texto azul o subrayado.

    **Correcto:**

    ![captura de pantalla de información sobre herramientas enriquez con texto negro ](images/winenv-notification-image34.png)

    **Incorrecto:**

    ![captura de pantalla de información sobre herramientas enriquecte con texto azul ](images/winenv-notification-image35.png)

    En el ejemplo incorrecto, el plan de energía actual parece ser un vínculo, pero es imposible hacer clic en él.

### <a name="notification-area-flyouts"></a>Flyouts del área de notificación

-   Cuando sea necesario, presente los flyouts del área de notificación con tres secciones:
    -   **Resumen.** Muestre la misma información que se muestra en la información sobre herramientas o información sobre herramientas del icono, posiblemente con más detalle. Para mantener la coherencia, use el mismo texto e iconos y, por lo general, el mismo diseño (si se usa una información sobre herramientas enriquecencia). A diferencia de las sugerencias de información, esta información es accesible cuando se usa la función táctil.
    -   **Tareas comunes.** Presente las tareas que se realizan más comúnmente directamente en el menú desplegable.
    -   **Vínculos relacionados.** Proporcione como máximo uno de cada tipo de los siguientes vínculos opcionales:
        -   Vínculo a la tarea que se realiza con más frecuencia en Panel de control. Proporcione si hay una tarea realizada con frecuencia que no se puede presentar en la sección tareas comunes.
        -   Vínculo al elemento Panel de control relacionado. Este Panel de control elemento debe permitir a los usuarios realizar cualquier tarea que no se pueda realizar en la sección tareas comunes.
        -   Vínculo a un tema de Ayuda específico y relevante. Siga las instrucciones [estándar del vínculo de Ayuda](winenv-help.md).

![captura de pantalla del área de notificación y el flyout ](images/winenv-notification-image36.png)

En este ejemplo se muestra un flyout de área de notificación mediante la presentación recomendada.

### <a name="options-dialog-box"></a>Opciones (cuadro de diálogo)

-   Las opciones no accesibles directamente desde el menú contextual deben estar en el cuadro de diálogo Opciones . Este cuadro de diálogo podría ser el panel de control de la característica.
-   **El cuadro de diálogo Opciones puede incluir los siguientes elementos según** corresponda (el texto exacto está entre comillas):
    -   Habilitar \[ nombre de característica \] (casilla)
        -   Al desactivar esta opción se cierra permanentemente el programa. El programa se puede reiniciar desde su elemento del panel de control. El comando Salir del menú contextual cierra el programa solo para la sesión Windows actual.
    -   "Mostrar icono en el área de notificación" (casilla)
        -   Quitar el icono del área de notificación no afecta a la característica subyacente.
        -   Al seleccionar esta opción, el usuario puede restaurar el icono, lo que, por supuesto, no se puede hacer desde el propio icono.
-   Deshabilite las características que rara vez se usan, o que pueden ser molestos o distraídas. Permitir que [los usuarios opten por](glossary.md) estas características.

Para obtener instrucciones y ejemplos generales del cuadro de diálogo Opciones, vea [Propiedades Windows](win-property-win.md).

### <a name="minimizing-programs-to-the-notification-area"></a>Minimizar los programas en el área de notificación

**Nota: Ya no se recomienda minimizar las ventanas de programa en el área de notificación para Windows 7.** En su lugar, use [botones de la barra](winenv-taskbar.md) de tareas normales. El programa puede admitir ambos mecanismos para la compatibilidad con versiones anteriores.

-   Para reducir el desorden de la barra de tareas, considere la posibilidad de minimizar los programas en el área de notificación solo si se aplican todos los siguientes elementos:
    -   El programa solo puede tener una sola instancia.
    -   El programa se ejecuta durante un período de tiempo prolongado.
    -   El icono muestra el estado.
    -   El icono puede ser un origen de notificación.
    -   Esto es opcional y los usuarios deben [participar en](glossary.md).
-   Use el botón Minimizar en la barra de título de la aplicación, no el botón Cerrar.

## <a name="text"></a>Texto

### <a name="infotips"></a>Información sobre

-   La información sobre iconos debe tener uno de los siguientes formatos (donde el nombre de la empresa es opcional):
    -   (Nombre de la compañía) Nombre de característica, programa o dispositivo
    -   ![captura de pantalla de información sobre información con el nombre de la empresa ](images/winenv-notification-image37.png)
    -   (Nombre de la compañía) Nombre de característica, programa o dispositivo: resumen de estado
    -   ![captura de pantalla de información de información que muestra el resumen de estado ](images/winenv-notification-image38.png)
    -   (Nombre de la compañía) Instrucción de estado de nombre de dispositivo, programa o característica.
    -   ![captura de pantalla de infotip que muestra la instrucción de estado ](images/winenv-notification-image39.png)
    -   (Nombre de la compañía) Nombre de característica, programa o dispositivo
    -   Lista de estado con cada elemento en una línea independiente
    -   ![captura de pantalla de información que muestra la lista de estado ](images/winenv-notification-image40.png)

Expresiones de información:

-   Céntrate en la información más útil. Muestra otra información a la izquierda con un solo clic.
-   Sea conciso. Use fragmentos de oración o instrucciones simples.
-   No use signos de puntuación finales a menos que la sugerencia se indique como una frase completa.
-   Omita palabras innecesarias. No incluya la versión de software ni otra información extraneosa.

    **Incorrecto:**

    ![captura de pantalla de información con información innecesaria ](images/winenv-notification-image41.png)

    En este ejemplo, la información sobre información tiene información adicional.

-   No explique cómo interactuar con el icono.

    **Incorrecto:**

    ![captura de pantalla de información con instrucciones de clic con el botón derecho ](images/winenv-notification-image42.png)

    En este ejemplo, el icono Conexión de red inalámbrica proporciona instrucciones para hacer clic con el botón derecho.

## <a name="documentation"></a>Documentación

Al hacer referencia al área de notificación:

-   Consulte el área de notificación como el área de notificación, no la bandeja del sistema.

Al hacer referencia a un icono de área de notificación:

-   Consulte el icono con el nombre exacto especificado en la información, incluida su mayúscula y después el icono.
-   Para obtener la primera referencia, consulte también el área de notificación.
-   Cuando sea posible, formatee el texto del encabezado con negrita. De lo contrario, coloque el encabezado entre comillas solo si es necesario para evitar confusiones.

**Ejemplo:** Para comprobar rápidamente el estado de la red, haga clic en el **icono Red** en el área de notificación.

 

