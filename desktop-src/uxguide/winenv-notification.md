---
title: Área de notificación
description: El área de notificación proporciona notificaciones y estado. Los programas bien diseñados usan el área de notificación de manera adecuada, sin ser molestas ni distraer.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0293038dd155f12b96b22dd1c273a50f1c030ffa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003296"
---
# <a name="notification-area"></a>Área de notificación

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El área de notificación proporciona notificaciones y estado. Los programas bien diseñados usan el área de notificación de manera adecuada, sin ser molestas ni distraer.

El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado. También se puede usar para mostrar iconos de características del sistema y de programas que no tienen presencia en el escritorio.

Los elementos del área de notificación se conocen como iconos del área de notificación o simplemente iconos si el contexto del área de notificación ya está claramente establecido.

![captura de pantalla del área de notificación, la hora y la fecha ](images/winenv-notification-image1.png)

El área de notificación.

Para proporcionar a los usuarios el control de su escritorio en Windows 7, no se muestran todos los iconos del área de notificación de forma predeterminada. En su lugar, los iconos se muestran en el desbordamiento del área de notificación, a menos que el usuario los promocione al área de notificación.

![Captura de pantalla que muestra el área de notificación y el desbordamiento.](images/winenv-notification-image2.png)

Desbordamiento del área de notificación.

**Nota:** Las instrucciones relacionadas con la [barra de tareas](winenv-taskbar.md), las [notificaciones](mess-notif.md) y los [globos](ctrl-balloons.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿El programa necesita mostrar una notificación?** En ese caso, debe usar un icono de área de notificación.
-   **¿Se muestra el icono temporalmente para mostrar un cambio de estado?** En ese caso, puede que el icono del área de notificación sea adecuado, en función de los siguientes factores:

    -   **¿El estado es útil y relevante?** Es decir, ¿es probable que los usuarios supervisen el icono y cambien su comportamiento como resultado de esta información? En caso contrario, no muestre el estado o colóquelo en un archivo de registro.

        **Incorrecto:**

        ![captura de pantalla del área de notificación con el icono de la unidad ](images/winenv-notification-image3.png)

        En este ejemplo, el icono de actividad de la unidad de disco no es adecuado porque es poco probable que los usuarios cambien su comportamiento en función de ello.

    -   **¿El estado es crítico? ¿Es necesaria una acción inmediata?** Si es así, muestre la información de una manera que requiera atención y no se pueda omitir fácilmente, como un [cuadro de diálogo](win-dialog-box.md).

    Los programas diseñados para Windows 7 pueden usar iconos superpuestos en el botón de la barra de tareas del programa para mostrar el cambio de estado, así como las barras de progreso del botón de la barra de tareas para mostrar el progreso de las tareas de ejecución prolongada.

-   **¿La característica ya tiene "presencia de escritorio"?** Es decir, cuando se ejecuta, ¿la característica aparece en una ventana en el escritorio (posiblemente minimizada)? Si es así, muestre el estado en la [barra de estado](ctrl-status-bars.md)del programa, en otro área de estado o, para Windows 7, directamente en el botón de la barra de tareas. Si la característica no tiene presencia de escritorio, puede usar un icono para el acceso a programas y para mostrar el estado.
-   **¿Es el icono principalmente iniciar un programa o acceder rápidamente a sus características o configuraciones?** Si es así, use el menú Inicio para iniciar programas en su lugar. El área de notificación no está pensada para el acceso rápido a programas o comandos.

    ![captura de pantalla de la barra de herramientas Inicio rápido ](images/winenv-notification-image4.png)

    En este ejemplo de Windows Vista, el inicio rápido se usa para iniciar rápidamente el explorador de Windows y Windows Internet Explorer.

    En el caso de los programas diseñados para Windows 7, los usuarios pueden anclar botones de la barra de tareas para el acceso rápido a programas. Los programas pueden usar una barra de herramientas de miniaturas o de Jump List para tener acceso a los comandos usados con frecuencia directamente desde el botón de la barra de herramientas de un programa El área Inicio rápido no se muestra de forma predeterminada en Windows 7.

    ![captura de pantalla de la barra de tareas y Jump List con iconos ](images/winenv-notification-image5.png)

    En este ejemplo, se usa una Jump List para obtener acceso rápido a los comandos.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="the-windows-desktop"></a>Escritorio de Windows

El escritorio de Windows tiene los siguientes puntos de acceso de programa:

-   **Área de trabajo.** Área en pantalla en la que los usuarios pueden realizar su trabajo, así como almacenar programas, documentos y sus métodos abreviados. Aunque técnicamente el escritorio incluye la barra de tareas, en la mayoría de los contextos, hace referencia solo al área de trabajo.
-   **Botón iniciar.** El punto de acceso para todos los programas y lugares especiales de Windows (documentos, imágenes, música, juegos, equipo, panel de control), con las listas de "usados más recientemente" para obtener acceso rápidamente a los programas y documentos usados recientemente.
-   **Inicio rápido.** Punto de acceso directo para los programas seleccionados por el usuario. El inicio rápido se ha quitado de Windows 7.
-   **Situada.** Punto de acceso para ejecutar programas que tienen presencia de escritorio. Aunque técnicamente la barra de tareas abarca toda la barra desde el botón Inicio hasta el área de notificación, en la mayoría de los contextos barra de tareas hace referencia al área de entre, que contiene los botones de la barra de tareas. A veces, esta área se denomina taskband.
-   **Deskbands. No se recomienda.**
-   **Área de notificación.** Un origen a corto plazo para las notificaciones y el estado, así como un punto de acceso para las características relacionadas con el sistema y los programas que no tienen presencia en el escritorio.

![captura de pantalla que identifica puntos de acceso de escritorio ](images/winenv-notification-image6.png)

Los puntos de acceso del escritorio de Windows incluyen el botón Inicio, la barra de tareas y el área de notificación. Observe la característica de miniaturas del botón de la barra de tareas.

**El escritorio es un recurso compartido limitado que es el punto de entrada del usuario a Windows.** Dejar a los usuarios en el control. Debe usar las áreas de escritorio tal y como se pretende que cualquier otro uso se debe considerar un abuso. Por ejemplo, no vea nunca áreas de escritorio como formas de promover el programa o su [marca](exper-branding.md).

### <a name="using-the-notification-area-appropriately"></a>Usar el área de notificación correctamente

El área de notificación se diseñó originalmente como un origen temporal para las notificaciones y el estado. Su eficacia y comodidad le animamos a los desarrolladores a darle otros propósitos, como el inicio de programas y la ejecución de comandos. Desafortunadamente con el tiempo, estas adiciones hicieron que el área de notificación sea demasiado grande y ruidoso, y confundieron su finalidad con los otros puntos de acceso de escritorio.

Windows XP solucionó el problema de escala haciendo que el área sea contraíble y ocultando los iconos sin usar. Windows Vista dirigió el ruido quitando notificaciones innecesarias y molestas. Windows 7 ha ido un paso más allá centrándose en la notificación con el fin original de ser un origen de notificación. **La mayoría de los iconos están ocultos de forma predeterminada en Windows 7, pero el usuario puede promoverlos manualmente al área de notificación. Para evitar que los usuarios controlen sus escritorios, no hay forma de que el programa realice esta promoción automáticamente.** Windows sigue mostrando notificaciones de iconos ocultos mediante la promoción temporal.

![captura de pantalla del área de notificación y el desbordamiento ](images/winenv-notification-image7.png)

En Windows 7, la mayoría de los iconos del área de notificación están ocultos de forma predeterminada.

Además, Windows 7 admite muchas características directamente en los botones de la barra de tareas. En concreto, puede usar:

-   Jump List y barras de herramientas en miniatura para acceder rápidamente a los comandos usados con frecuencia.
-   Iconos superpuesto para mostrar el estado de los programas en ejecución.
-   Barras de progreso del botón de la barra de tareas para mostrar el progreso de las tareas de ejecución prolongada.

En Resumen, si el programa tiene presencia de escritorio, saque el máximo partido de las características del botón de la barra de tareas de Windows 7 para estos fines. **Mantenga los iconos del área de notificación centrados en Mostrar notificaciones y estado.**

### <a name="keeping-users-in-control"></a>Mantener el control de los usuarios

Mantener los usuarios en el control se extiende más allá del área de notificación correctamente. En función de la naturaleza del icono, puede que desee permitir que los usuarios hagan lo siguiente:

-   **Quitar el icono.** Es posible que el icono proporcione un estado relevante y útil, pero, aunque es posible que los usuarios no quieran verlo. Windows permite a los usuarios Ocultar iconos, pero esta característica no se puede detectar fácilmente. Para mantener el control de los usuarios, proporcione un **icono de pantalla en** la opción área de notificación en el menú contextual del icono. Tenga en cuenta que la eliminación de un icono no tiene que afectar al programa, la característica o el proceso subyacentes.
-   **Seleccione los tipos de notificaciones que se van a mostrar.** La notificación debe ser útil y pertinente, pero puede haber notificaciones que los usuarios no quieren ver. Esto es especialmente cierto para las [notificaciones](mess-notif.md)de la FYI. Permita que los usuarios elijan habilitar las menos importantes.
-   **Suspender características opcionales.** Los iconos se usan para mostrar el estado de las características sin presencia de escritorio. Estas características tienden a ser tareas en segundo plano opcionales de larga duración, como la impresión, la indexación, la exploración o la sincronización. Es posible que los usuarios deseen suspender estas características para aumentar el rendimiento del sistema, reducir el consumo de energía o porque están sin conexión.
-   **Salga del programa.** Proporcione las opciones más adecuadas:
    -   **Cierre temporalmente el programa.** El programa se detiene y se reinicia cuando se reinicia Windows. Este enfoque es adecuado para utilidades importantes del sistema, como los programas de seguridad.
    -   **Salga del programa de forma permanente.** El programa se detiene y no se reinicia cuando se reinicia Windows (a menos que el usuario decida reiniciarse más tarde). El usuario ya no desea ejecutar el programa, o bien desea ejecutar el programa a petición, quizás para mejorar el rendimiento del sistema.

Aunque es una buena idea proporcionar la mayoría de estas opciones en el menú contextual del icono, la experiencia predeterminada del programa debe ser adecuada para la mayoría de los usuarios. No active el todo de forma predeterminada y espere que los usuarios desactiven las características. En su lugar, active las características importantes en de forma predeterminada y permita que los usuarios habiliten características adicionales según sea necesario.

**Si solo hace cuatro cosas...**

1.  No abuse del área de notificación. Úselo solo como origen para las notificaciones y el estado, así como para las características sin presencia de escritorio.
2.  Mantenga a los usuarios en el control. Proporcione las opciones adecuadas para controlar el icono, sus notificaciones y las características subyacentes.
3.  Presente una experiencia predeterminada que sea adecuada para la mayoría de los usuarios. Permita a los usuarios habilitar las características deseadas en lugar de esperar que deshabiliten las no deseadas.
4.  Saque el máximo partido de las características del botón de la barra de tareas de Windows 7 para mostrar el estado y hacer que las tareas realizadas con mayor frecuencia del programa sean eficientes.

## <a name="usage-patterns"></a>Patrones de uso

Los iconos del área de notificación tienen varios patrones de uso:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Estado del sistema y acceso</strong><br/> Se muestra continuamente para mostrar el estado del sistema importante, pero no crítico, y para proporcionar acceso a las características y configuraciones pertinentes. <br/></td>
<td>Las características del sistema que necesitan iconos del área de notificación no tienen ninguna presencia persistente en el escritorio. También se puede usar como origen de la notificación. <br/> <img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br/> En este ejemplo, los iconos de batería, red y volumen se muestran continuamente cuando proceda.<br/></td>
</tr>
<tr class="even">
<td><strong>Estado y acceso de la tarea en segundo plano</strong><br/> Se muestra mientras se ejecuta una tarea en segundo plano para mostrar el estado y proporcionar acceso a las características y la configuración. <br/></td>
<td>Los procesos en segundo plano necesitan iconos del área de notificación cuando no tienen presencia de escritorio. También se puede usar como origen de la notificación. <br/> <img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br/> En este ejemplo, el icono del centro de actividades permite a los usuarios comprobar su estado aunque no tenga presencia de escritorio.<br/></td>
</tr>
<tr class="odd">
<td><strong>Estado de evento temporal</strong><br/> Los programas con presencia de escritorio pueden mostrar temporalmente los iconos para Mostrar eventos importantes o cambios en el estado. <br/></td>
<td><img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br/> En este ejemplo, los iconos para imprimir e instalar actualizaciones se muestran temporalmente para Mostrar eventos importantes o cambios de estado.<br/></td>
</tr>
<tr class="even">
<td><strong>Origen de notificación temporal</strong><br/> Se muestra temporalmente para mostrar una notificación. Se quita después de un tiempo de espera, o cuando se soluciona el problema subyacente o se realiza la tarea. <br/></td>
<td>Se prefieren iconos temporales para orígenes de notificación puros. No mostrar un icono que no proporcione un estado útil, relevante y dinámico, solo porque una característica puede necesitar mostrar una notificación en el futuro. <br/> <img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br/> En este ejemplo, se muestra el icono de plug and Play mientras se muestra una nueva notificación de hardware detectado.<br/></td>
</tr>
<tr class="odd">
<td><strong>Aplicación de instancia única minimizada</strong><br/> Para reducir la aglomeración en la barra de tareas, una aplicación de una sola instancia y de larga ejecución se puede minimizar en un icono de área de notificación. <br/></td>
<td><img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br/> En este ejemplo de Windows Vista, Outlook y Windows Live Messenger son aplicaciones de instancia única que minimizan los iconos del área de notificación.<br/> Considere la posibilidad de usar este patrón solo si se aplica lo siguiente: <br/>
<ul>
<li>La aplicación solo puede tener una única instancia.</li>
<li>La aplicación se ejecuta durante un período de tiempo prolongado.</li>
<li>El icono muestra el estado.</li>
<li>El icono puede ser un origen de notificación.</li>
<li>Esto es opcional y los usuarios deben <a href="glossary.md">participar</a>.</li>
</ul>
Si se aplican todas estas condiciones, la reducción de un icono elimina dos puntos de acceso cuando solo se necesita uno. <br/> <strong>Nota:</strong> Este patrón de icono ya no se recomienda para Windows 7. En su lugar, use los botones de la barra de tareas normales si el programa tiene presencia de escritorio.<br/> <img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br/> En este ejemplo de Windows 7, un botón de la barra de tareas normal ocupa poco espacio, pero las ventajas de las características de los botones de la barra de tareas de Windows 7, como Jump Lists, iconos de superposición y miniaturas enriquecidas.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Proporcione solo un icono de área de notificación por componente.**
-   **Use un icono con versiones de píxel de 16x16, 20x20 y 24x24.** Las versiones mayores se usan en los modos de presentación de alta ppp.

### <a name="when-to-show"></a>Cuándo Mostrar

-   Para el patrón de origen de la notificación temporal:
    -   Windows muestra el icono cuando se muestra la notificación.
    -   Quite el icono en función de su modelo de [diseño de notificación](mess-notif.md) :



    | Patrón                                     | Cuándo quitar                                         |
    |--------------------------------------|------------------------------------------|
    | Acción correcta<br/>            | Cuando se quita la notificación.<br/> |
    | Error de acción<br/>            | Cuando se resuelve el problema.<br/>     |
    | Evento no crítico del sistema<br/> | Cuando se resuelve el problema.<br/>     |
    | Tarea de usuario opcional<br/>        | Cuando se realiza la tarea.<br/>            |
    | Asesor<br/>                       | Cuando se quita la notificación.<br/> |



 

-   **Para el patrón de estado de evento temporal, muestre el icono mientras se está produciendo el evento.**
-   En el caso de todos los demás patrones, **muestre el icono cuando se esté ejecutando el programa, la característica o el proceso y el icono sea relevante** a menos que el usuario haya desactivado el **icono Mostrar en** la opción del área de notificación (para obtener más información, vea [menús contextuales](#context-menus)). La mayoría de los iconos están ocultos de forma predeterminada en Windows 7, pero el usuario puede promoverlos al área de notificación.
-   **No muestre iconos destinados a los administradores a los usuarios estándar.** Grabe la información en el registro de eventos de Windows.

### <a name="where-to-show"></a>Dónde Mostrar

-   **Mostrar ventanas iniciadas desde los iconos del área de notificación cerca del área de notificación.**

![figura de una ventana cerca del área de notificación ](images/winenv-notification-image14.png)

Las ventanas iniciadas desde los iconos del área de notificación se muestran cerca del área de notificación.

### <a name="icons"></a>Iconos

-   **Elija el icono en función de su modelo de diseño:**

    | Patrón                                                 | Tipo de icono                                   |
    |--------------------------------------------------|------------------------------------|
    | Estado del sistema y acceso<br/>              | Icono de característica del sistema<br/>     |
    | Estado y acceso de la tarea en segundo plano<br/>     | Icono de programa o característica<br/> |
    | Origen de notificación temporal<br/>         | Icono de programa o característica<br/> |
    | Estado de evento temporal<br/>                | Icono de programa o característica<br/> |
    | Aplicación de instancia única minimizada<br/> | Icono de programa<br/>            |

    

     

    ![captura de pantalla del área de notificación y los iconos de Outlook ](images/winenv-notification-image15.png)

    En este ejemplo, Outlook usa un icono de característica de correo electrónico para un origen de notificación temporal y su icono de aplicación para la aplicación minimizada.

-   **Elija un diseño de icono fácilmente reconocible.** Prefiere iconos con contornos únicos en los iconos con forma de cuadrado o rectangular. Mantenga los diseños de preferencia simples en imágenes realistas. Aplique también las otras [instrucciones de iconos de estilo Aero](vis-icons.md) .
-   **Use variaciones o superposiciones de iconos para indicar el estado o los cambios de estado.** Use variaciones de los iconos para mostrar los cambios en las cantidades o los puntos fuertes. Para otros tipos de estado, utilice las siguientes superposiciones estándar. Use solo una superposición y búsquela en la parte inferior derecha para mantener la coherencia. 

    | Overlay                                                                                                       | Status                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![captura de pantalla de un icono pequeño de advertencia ](images/winenv-notification-image16.png)<br/>               | Advertencia<br/>               |
    | ![captura de pantalla de un icono de error pequeño ](images/winenv-notification-image17.png)<br/>                 | Error<br/>                 |
    | ![captura de pantalla de un icono pequeño desconectado o desconectado ](images/winenv-notification-image18.png)<br/> | Deshabilitado o desconectado<br/> |
    | ![captura de pantalla del icono pequeño de bloqueado/sin conexión ](images/winenv-notification-image19.png)<br/>       | Bloqueado/sin conexión<br/>       |

    

     

    ![captura de pantalla del área de notificación y dos iconos ](images/winenv-notification-image20.png)

    En este ejemplo, los iconos de batería y de red muestran los cambios en cantidades o fuertes.

    ![captura de pantalla del área de notificación y dos superposiciones ](images/winenv-notification-image21.png)

    En este ejemplo, se usan superposiciones para mostrar los Estados de error y ADVERTENCIA.

-   **Evite swaths de color rojo, amarillo y verde puro en los iconos base.** Para evitar confusiones, Reserve estos colores para comunicar el estado. Si su [Personalización de marca](exper-branding.md) usa estos colores, considere la posibilidad de usar tonos silenciados para los iconos base del área de notificación.
-   Para una [escalación progresiva](mess-notif.md), **utilice iconos con una apariencia progresivamente más Emphatic a medida que la situación sea más urgente.**

    ![captura de pantalla del área de notificación y cinco iconos ](images/winenv-notification-image22.png)

    En estos ejemplos, la apariencia del icono de la batería se vuelve más Emphatic a medida que aumenta la urgencia.

-   **No cambie el estado con demasiada frecuencia.** Los iconos del área de notificación no deben parecer ruidos, inestables o de petición. El ojo es sensible a los cambios en el campo de visión de periféricos, por lo que los cambios de estado deben ser sutiles.
    -   **No cambie el icono rápidamente.** Si el estado subyacente cambia rápidamente, haga que el icono refleje el estado de alto nivel.

        **Incorrecto:**

        ![captura de pantalla del área de notificación y el icono del módem ](images/winenv-notification-image23.png)

        En este ejemplo, el icono de módem muestra luces intermitentes (como un módem de hardware), pero esos cambios de estado no son significativos para los usuarios.

    -   **No use animaciones de ejecución prolongada para mostrar actividades continuas.** Estas animaciones son una distracción. La presencia de un icono en el área de notificación indica suficiente actividad continua.
    -   **Breves, se aceptan animaciones sutiles para mostrar el progreso durante los cambios de estado transitivos y temporales importantes.**

        ![captura de pantalla del área de notificación y el icono inalámbrico ](images/winenv-notification-image24.png)

        En este ejemplo, el icono inalámbrico muestra un indicador de actividad para mostrar que el trabajo está en curso.

    -   **No parpadee el icono.** Si lo hace, se destraerá. Si un evento requiere atención inmediata, utilice en su lugar un cuadro de diálogo. Si, de lo contrario, el evento necesita atención, use una notificación.

-   **No deshabilite los iconos del área de notificación.** Si el icono no se aplica actualmente, quítelo. Sin embargo, puede mostrar un icono habilitado con una superposición de estado deshabilitada si los usuarios pueden habilitar desde el icono.

    ![captura de pantalla del área de notificación y el control deslizante de volumen ](images/winenv-notification-image25.png)

    En este ejemplo, los usuarios pueden habilitar la salida de sonido desde el icono.

Para obtener instrucciones y ejemplos de iconos generales, vea [iconos](vis-icons.md).

### <a name="interaction"></a>Interacción

**Nota:** Los siguientes eventos Click deben aparecer al presionar el mouse, no hacia abajo.

**Al mantener el puntero**

-   **Muestra una información sobre herramientas o un recuadro informativo que indica lo que representa el icono.**

    ![captura de pantalla del área de notificación e información sobre herramientas ](images/winenv-notification-image26.png)

    En este ejemplo, se usa una información sobre herramientas para describir el icono al mantener el mouse.

Para obtener instrucciones de texto retextual, consulte la sección de [texto](#context-menus) de este artículo.

**Clic con el botón primario**

-   **Muestre los usuarios que sea más probable que desee ver**, que puede ser:

    -   Ventana flotante, cuadro de diálogo o ventana de programa con la configuración más útil y las tareas que se realizan habitualmente. Para obtener instrucciones de presentación, vea [controles flotantes del área de notificación](#notification-area-flyouts).

        ![captura de pantalla del área de notificación y los controles flotantes ](images/winenv-notification-image27.png)

        En estos ejemplos, al hacer clic con el botón primario se muestran ventanas emergentes con la configuración más útil.

    -   Un control flotante de estado.

        ![captura de pantalla del área de notificación y el control flotante de estado ](images/winenv-notification-image28.png)

        En este ejemplo, al hacer clic a la izquierda se muestra el control flotante de estado.

        -   Elemento relacionado del panel de control.
        -   Menú contextual.

    Los usuarios esperan un solo clic a la izquierda para mostrar algo, por lo que no mostrar nada hace que un icono del área de notificación parezca que no responde.

-   **Mostrar un menú contextual solo si las otras opciones no se aplican**, con el comando predeterminado en negrita. En este caso, se muestra el mismo menú contextual que se muestra al hacer clic con el botón secundario para evitar confusiones.
-   **Prefiera usar una ventana emergente en un cuadro de diálogo** para obtener una sensación más ligera. Mostrar solo la configuración más común y hacer que tengan efecto inmediato para una interacción más sencilla. Descartar la ventana emergente si el usuario hace clic en cualquier parte fuera de la ventana.
-   **Mostrar pequeñas ventanas cerca del icono asociado.** Sin embargo, las ventanas grandes, como los elementos del panel de control, se pueden mostrar en el centro del monitor predeterminado.

**Doble clic con el botón primario**

-   **Ejecute el comando predeterminado en el menú contextual.** Normalmente, se muestra la interfaz de usuario principal asociada al icono, como el elemento del panel de control, la hoja de propiedades o la ventana de programa asociados.
-   **Si no hay ningún comando predeterminado, realice la misma acción que un solo clic a la izquierda.**

**Haga clic con el botón secundario en**

-   **Mostrar el menú contextual** con el comando predeterminado en negrita.

### <a name="context-menus"></a>Menús contextuales

-   **Mostrar el menú contextual cerca de su icono asociado**, pero fuera de la barra de tareas.
-   **El menú contextual puede incluir los siguientes elementos**, según corresponda, en el orden indicado (el texto exacto está entre comillas):

Comandos principales

Abrir (valor predeterminado, mostrar primero, en negrita)

Ejecutar

Comandos secundarios

< separador>

Comando suspender/reanudar habilitar/deshabilitar (marca de verificación)

"Minimizado a área de notificación" (marca de verificación)

Participación en las notificaciones (marca de verificación)

"Icono Mostrar en el área de notificación" (marca de verificación)

< separador>

Las

"Salida"

-   **Quite en lugar de deshabilitar los elementos de menú contextual que no se aplican.**
-   Para los comandos abrir, ejecutar y suspender/reanudar, **sea específico de lo que se abre, se ejecuta, se suspende y se reanuda.**

![Captura de pantalla que muestra un área de notificación y comandos.](images/winenv-notification-image29.png)

En este ejemplo, Windows Defender tiene comandos de apertura y ejecución específicos.

-   **Use suspender o reanudar tareas en segundo plano, habilitar o deshabilitar para todo lo demás.**
-   **Use las marcas de verificación para indicar el estado.** Enumerar y habilitar todos los Estados y colocar la marca de verificación junto al estado actual. No deshabilite las opciones o cambie las etiquetas de opción para indicar el estado actual.

**Correcto:**

![captura de pantalla de un comando con marca de verificación ](images/winenv-notification-image29.png)

**Incorrecto:**

![captura de pantalla de un comando sin marca de verificación ](images/winenv-notification-image30.png)

En el ejemplo incorrecto, Windows Defender debe usar una marca de verificación para indicar el estado actual.

-   **Todas las tareas en segundo plano deben tener un comando Suspend/Resume.** La elección del comando debe suspender temporalmente la tarea. Es posible que los usuarios deseen suspender temporalmente las tareas en segundo plano para aumentar el rendimiento del sistema o reducir el consumo de energía. Las tareas en segundo plano suspendidas se reinician cuando se reanuda el usuario o cuando se reinicia Windows.
-   **Permitir a los usuarios participar o no en diferentes tipos de notificación** si el programa tiene notificaciones que algunos usuarios podrían no querer ver. El patrón de notificación [FYI](mess-notif.md) requiere que los usuarios participen, por lo que estas notificaciones deben estar deshabilitadas de forma predeterminada.

![captura de pantalla del área de notificación y los comandos ](images/winenv-notification-image31.png)

En este ejemplo, Outlook permite a los usuarios elegir las notificaciones que reciben desde el icono.

-   Al **desactivar la opción "Mostrar icono en el área de notificación", se quita el icono del área de notificación**, pero no se afecta al programa, la característica o el proceso subyacentes. Los usuarios pueden volver a mostrar el icono en el cuadro de diálogo Opciones del programa. No vuelva a mostrar automáticamente el icono cuando se reinicie Windows.
-   **El comando Exit sale del programa para la sesión actual de Windows y quita el icono.** No tiene un comando salir si el programa no se puede cerrar. El programa se reinicia cuando se reinicia Windows. Los usuarios pueden salir permanentemente del programa desde el cuadro de diálogo Opciones.
-   **No tiene un comando about.** Esta información debe comunicarse con el icono, su recuadro informativo y el menú contextual. Si los usuarios desean más información, pueden ver la interfaz de usuario principal.
    -   **Excepción:** Puede proporcionar un comando about si el icono es para un programa que no tiene presencia de escritorio.

Para obtener instrucciones y ejemplos generales del menú contextual, vea [menús](cmd-menus.md).

### <a name="rich-tooltips"></a>Información sobre herramientas enriquecida

-   **Use información sobre herramientas enriquecida solo para facilitar la comprensión de la información.** No use información sobre herramientas enriquecida solo para decorar la característica. Si no puede usar la riqueza para facilitar la comprensión de la información, utilice en su lugar una información sobre herramientas sin formato.

    **Incorrecto:**

    ![captura de pantalla del área de notificación y la información sobre herramientas enriquecida ](images/winenv-notification-image32.png)

    **Correcto:**

    ![captura de pantalla del área de notificación y la información sobre herramientas sin formato ](images/winenv-notification-image33.png)

    En el ejemplo incorrecto, el icono de calendario no facilita la comprensión de la fecha.

-   **Use una presentación concisa.** Use texto conciso y un diseño conciso con un icono de 32 píxeles. La información sobre herramientas de "espacioso" se arriesga a distraer, especialmente cuando se muestra involuntariamente.
-   **No coloque controles o elementos que parezcan interactivos en una información sobre herramientas enriquecida.** La información sobre herramientas no es interactiva y, por tanto, no debe aparecer interactiva. No use texto azul o subrayado.

    **Correcto:**

    ![captura de pantalla de la información sobre herramientas enriquecida con texto en negro ](images/winenv-notification-image34.png)

    **Incorrecto:**

    ![captura de pantalla de la información sobre herramientas enriquecida con texto azul ](images/winenv-notification-image35.png)

    En el ejemplo incorrecto, el plan de energía actual parece ser un vínculo, pero es imposible hacer clic en él.

### <a name="notification-area-flyouts"></a>Controles flotantes del área de notificación

-   Cuando sea adecuado, presente controles flotantes del área de notificación con tres secciones:
    -   **Resumen.** Mostrar la misma información que se muestra en la información sobre herramientas o el recuadro informativo del icono, posiblemente con más detalles. Para mantener la coherencia, use el mismo texto e iconos y, por lo general, el mismo diseño (si usa una información sobre herramientas enriquecida). A diferencia de recuadros informativos, esta información es accesible al usar Touch.
    -   **Tareas comunes.** Presente las tareas que se realizan con mayor frecuencia directamente en el control flotante.
    -   **Vínculos relacionados.** Proporcione como máximo uno de cada tipo de los siguientes vínculos opcionales:
        -   Vínculo a la tarea que se realiza con mayor frecuencia en el panel de control. Proporcione si hay una tarea que se realiza con frecuencia y que no se puede presentar en la sección tareas comunes.
        -   Un vínculo al elemento relacionado del panel de control. Este elemento del panel de control debe permitir a los usuarios realizar las tareas que no se pueden realizar en la sección tareas comunes.
        -   Un vínculo a un tema de ayuda específico y relevante. Siga las [instrucciones de vínculo](winenv-help.md)de la ayuda estándar.

![captura de pantalla del área de notificación y el control flotante ](images/winenv-notification-image36.png)

En este ejemplo se muestra un control flotante del área de notificación mediante la presentación recomendada.

### <a name="options-dialog-box"></a>Opciones (cuadro de diálogo)

-   Las opciones que no son accesibles directamente desde el menú contextual deben estar en el cuadro de diálogo Opciones. Este cuadro de diálogo puede ser el panel de control de la característica.
-   **El cuadro de diálogo Opciones puede incluir los siguientes elementos** según corresponda (el texto exacto está entre comillas):
    -   Habilitar \[ nombre de característica \] (casilla)
        -   Al desactivar esta opción, se cierra el programa de forma permanente. El programa se puede reiniciar desde el elemento del panel de control. El comando exit en el menú contextual sale del programa solo para la sesión actual de Windows.
    -   "Icono Mostrar en el área de notificación" (casilla)
        -   Quitar el icono del área de notificación no afecta a la característica subyacente.
        -   La selección de esta opción permite al usuario restaurar el icono, que no se puede hacer desde el propio icono.
-   Deshabilite las características que rara vez se usan o que pueden resultar molestas o distraer. Permita a los usuarios [participar](glossary.md) en estas características.

Para obtener instrucciones y ejemplos del cuadro de diálogo Opciones generales, consulte [ventanas de propiedades](win-property-win.md).

### <a name="minimizing-programs-to-the-notification-area"></a>Minimizar programas en el área de notificación

**Nota: ya no se recomienda minimizar las ventanas de programa en el área de notificación para Windows 7.** En su lugar, use los botones normales de la [barra de tareas](winenv-taskbar.md) . El programa puede admitir ambos mecanismos para la compatibilidad con versiones anteriores.

-   Para reducir la aglomeración en la barra de tareas, considere la posibilidad de permitir minimizar los programas en el área de notificación solo si se aplica lo siguiente:
    -   El programa solo puede tener una única instancia.
    -   El programa se ejecuta durante un período de tiempo prolongado.
    -   El icono muestra el estado.
    -   El icono puede ser un origen de notificación.
    -   Esto es opcional y los usuarios deben [participar](glossary.md).
-   Use el botón minimizar en la barra de título de la aplicación, no el botón Cerrar.

## <a name="text"></a>Texto

### <a name="infotips"></a>Recuadros informativos

-   El recuadro informativo del icono debe tener uno de los siguientes formatos (donde el nombre de la compañía es opcional):
    -   (Nombre de la compañía) Nombre de la característica, el programa o el dispositivo
    -   ![captura de pantalla de recuadro informativo con el nombre de la empresa ](images/winenv-notification-image37.png)
    -   (Nombre de la compañía) Nombre de la característica, el programa o el dispositivo: Resumen de estado
    -   ![captura de pantalla de recuadro informativo que muestra el Resumen de estado ](images/winenv-notification-image38.png)
    -   (Nombre de la compañía) Instrucción de estado de nombre de dispositivo, programa o característica.
    -   ![captura de pantalla de la instrucción de estado que muestra la sugerencia ](images/winenv-notification-image39.png)
    -   (Nombre de la compañía) Nombre de la característica, el programa o el dispositivo
    -   Lista de Estados con cada elemento en una línea independiente
    -   ![captura de pantalla de recuadro informativo que muestra la lista de estado ](images/winenv-notification-image40.png)

Formulación de recuadro informativo:

-   Céntrese en la información más útil. Mostrar otra información en un solo clic a la izquierda.
-   Sea conciso. Utilice fragmentos de oraciones o instrucciones sencillas.
-   No use signos de puntuación finales a menos que Tip esté frase como una oración completa.
-   Omitir palabras innecesarias. No incluya la versión de software ni otra información extraña.

    **Incorrecto:**

    ![captura de pantalla de recuadro informativo con información innecesaria ](images/winenv-notification-image41.png)

    En este ejemplo, el recuadro informativo tiene información extraña.

-   No explique cómo interactuar con el icono.

    **Incorrecto:**

    ![captura de pantalla de recuadro informativo con instrucciones de clic con el botón secundario ](images/winenv-notification-image42.png)

    En este ejemplo, el icono de conexión de red inalámbrica proporciona instrucciones para hacer clic con el botón secundario.

## <a name="documentation"></a>Documentación

Al hacer referencia al área de notificación:

-   Consulte el área de notificación en el área de notificación, no en la bandeja del sistema.

Al hacer referencia a un icono del área de notificación:

-   Consulte el icono con el nombre exacto proporcionado en su recuadro informativo, incluido el uso de mayúsculas, seguido de un icono.
-   Para la primera referencia, consulte también el área de notificación.
-   Siempre que sea posible, dé formato al texto del encabezado con negrita. De lo contrario, coloque el encabezado entre comillas solo si es necesario para evitar confusiones.

**Ejemplo:** Para comprobar el estado de la red rápidamente, haga clic en el icono de **red** en el área de notificación.

 

