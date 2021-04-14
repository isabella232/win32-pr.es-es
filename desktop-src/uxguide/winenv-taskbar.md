---
title: Barra de tareas
description: La barra de tareas es el punto de acceso para los programas que se muestran en el escritorio. Con las nuevas características de la barra de tareas de Windows 7, los usuarios pueden proporcionar comandos, tener acceso a los recursos y ver el estado del programa directamente desde la barra de tareas.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f8b2bc21a75bc11c43df2cbdd37381165b89a793
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552783"
---
# <a name="taskbar"></a>Barra de tareas

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

La barra de tareas es el punto de acceso para los programas que se muestran en el escritorio. Con las nuevas características de la barra de tareas de Windows 7, los usuarios pueden proporcionar comandos, tener acceso a los recursos y ver el estado del programa directamente desde la barra de tareas.

La barra de tareas es el punto de acceso para los programas que se muestran en el escritorio, incluso si el programa está minimizado. Se dice que estos programas tienen presencia de escritorio. Con la barra de tareas, los usuarios pueden ver las ventanas principales abiertas y ciertas ventanas secundarias en el escritorio, y pueden cambiar rápidamente entre ellas.

![captura de pantalla de la barra de tareas con características llamadas ](images/winenv-taskbar-image1.png)

Barra de tareas de Microsoft Windows.

Los controles de la barra de tareas se conocen como botones de la barra de tareas. Cuando un programa crea una ventana principal (o una ventana secundaria con ciertas características), Windows agrega un botón de la barra de tareas para esa ventana y la quita cuando se cierra la ventana.

Los programas diseñados para Windows 7 pueden aprovechar las ventajas de estas nuevas características del botón de la barra de tareas:

-   Las listas de saltos proporcionan un acceso rápido a los destinos usados con frecuencia (como archivos, carpetas y vínculos) y a los comandos a través de un menú contextual accesible desde el botón de la barra de tareas y el elemento del menú Inicio del programa, incluso si el programa no se está ejecutando actualmente.
-   Las barras de herramientas de miniaturas proporcionan acceso rápido a comandos usados con frecuencia para una ventana determinada. Las barras de herramientas en miniatura aparecen en la miniatura del botón de la barra de tareas.
-   Los iconos de superposición muestran el cambio de estado en el icono de botón de la barra de tareas del programa.
-   Las barras de progreso muestran el progreso de las tareas de ejecución prolongada en el botón de la barra de tareas del programa.
-   Los botones de la barra de tareas de la subventana permiten a los usuarios usar miniaturas de botones de la barra de tareas para cambiar directamente a las ventanas de ventanas, ventanas de proyecto, ventanas secundarias de interfaz de múltiples documentos (MDI) y ventanas secundarias.
-   Los botones anclados de la barra de tareas permiten a los usuarios anclar botones de programa a la barra de tareas para proporcionar acceso rápido a los programas incluso cuando no se están ejecutando.

Técnicamente, la barra de tareas abarca toda la barra desde el botón Inicio hasta el área de notificación. No obstante, lo más habitual es que la barra de tareas solo haga referencia al área que contiene los botones de la barra de tareas. En el caso de las configuraciones de varios monitores, solo un monitor tiene una barra de tareas y dicho monitor es el predeterminado.

**Nota:** Las instrucciones relacionadas con el [escritorio](winenv-desktop.md), el [área de notificación](winenv-notification.md)y la [Administración de ventanas](win-window-mgt.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Los programas diseñados para Windows 7 pueden aprovechar las ventajas de estas características de botón de la barra de tareas. Hágase las siguientes preguntas clave para determinar si se deben usar o no:

**Jump Lists**

-   **¿A menudo los usuarios tienen que iniciar nuevas tareas con el programa?** Si es así, considere la posibilidad de proporcionar una Jump List. Aunque las listas de accesos directos se pueden usar para otros fines, la mayoría de los escenarios implican el inicio de una nueva tarea.
-   **¿A menudo los usuarios necesitan tener acceso a archivos, carpetas, vínculos u otros recursos usados recientemente o con frecuencia?** Si es así, considere la posibilidad de proporcionar una Jump List para tener acceso a estos recursos útiles.

    ![captura de pantalla de la barra de tareas con Internet Explorer Jump List ](images/winenv-taskbar-image2.png)

    En este ejemplo, Windows Internet Explorer usa una Jump List para presentar las páginas que se visitan con frecuencia.

-   **A menudo, los usuarios necesitan un acceso rápido a un pequeño número de comandos del programa mientras usan otros programas, incluso si el programa no se está ejecutando?** Si es así, considere la posibilidad de proporcionar una Jump List con estos comandos usados con frecuencia. Estos comandos deben funcionar incluso si el programa no se está ejecutando y se deben aplicar a todo el programa, no a una ventana específica. Como alternativa, considere la posibilidad de proporcionar una barra de herramientas en miniatura para los comandos que se aplican a una ventana específica.

    ![captura de pantalla de la barra de tareas con lista de saltos de notas rápidas ](images/winenv-taskbar-image3.png)

    En este ejemplo, el accesorio de Notas rápidas permite a los usuarios crear una nueva nota rápidamente mientras usan otros programas.

-   **¿Promueve características nuevas, de uso único o difíciles de encontrar?** Si es así, no utilice Jump Lists porque no están pensadas para este fin. En su lugar, mejore la detectabilidad de estos comandos directamente en el programa.

**Barras de herramientas en miniatura**

¿Se aplican todas las condiciones siguientes?

-   **¿Los comandos se aplican a una ventana específica?** Las barras de herramientas en miniatura son para los comandos que se aplican a las tareas existentes, mientras que los comandos Jump List son para iniciar nuevas tareas.
-   **¿Los usuarios necesitan interactuar con una tarea en ejecución rápidamente mientras usan otros programas?** Si es así, las barras de herramientas de miniaturas son una buena elección. Las barras de herramientas de miniaturas pueden presentar un máximo de siete comandos, pero generalmente se prefiere un máximo de cinco comandos.
-   **¿Los comandos son inmediatos?** Es decir, ¿no requieren ninguna entrada adicional? Las barras de herramientas de miniaturas deben tener comandos inmediatos para ser eficientes, mientras que las listas de accesos directos funcionan mejor con comandos que requieren una entrada adicional.

    **Incorrecto:**

    ![captura de pantalla de la barra de tareas con ventanas superpuestas ](images/winenv-taskbar-image4.png)

    Los comandos que requieren una entrada adicional no funcionan bien en las barras de herramientas en miniatura.

-   **¿Los comandos son directos?** Es decir, ¿pueden los usuarios interactuar con ellos mediante un solo clic? Las barras de herramientas deben tener comandos directos para ser eficientes.
-   **¿Los comandos se representan bien mediante iconos?** Los comandos de la barra de herramientas de miniaturas se presentan mediante iconos que no son etiquetas de texto, mientras que los comandos Jump List se representan mediante etiquetas de texto.

    **Incorrecto:**

    ![captura de pantalla de un comando de miniatura con icono ](images/winenv-taskbar-image5.png)

    En este ejemplo, el comando no está bien representado por iconos.

**Iconos de superposición**

-   **¿El programa tiene "presencia de escritorio"?** En caso contrario, use un icono de área de notificación. Si es así, considere la posibilidad de usar un icono de superposición en lugar de poner el estado en el icono del área de notificación para los programas diseñados para Windows 7. Esto garantiza que el icono siempre estará visible (cuando se usen iconos grandes) y consolide el programa con su estado en un solo lugar.
-   **¿El icono de superposición se muestra temporalmente para mostrar un cambio de estado?** En ese caso, puede que el icono de superposición sea adecuado, en función de los siguientes factores:
    -   **¿Es el estado útil y relevante al usar otros programas?** Si no es así, muestre la información en las [barras de estado](ctrl-status-bars.md) del programa o en el área de estado de otro programa.

        ![captura de pantalla de la barra de estado de la ventana de Internet Explorer ](images/winenv-taskbar-image7.png)

        En este ejemplo, se usa la barra de estado porque el estado no es útil cuando se usan otros programas.

    -   **¿El estado muestra el progreso?** Si es así, utilice en su lugar una barra de progreso del botón de la barra de tareas.
    -   **¿El estado es crítico? ¿Es necesaria una acción inmediata?** Si es así, muestre la información de una manera que requiera atención y no se pueda omitir fácilmente, como un [cuadro de diálogo](win-dialog-box.md).

**Barras de progreso**

-   **¿Los comentarios de progreso son útiles y relevantes al usar otros programas?** Es decir, ¿es probable que los usuarios supervisen el progreso mientras usan otros programas y cambiar su comportamiento como resultado? Este estado útil y relevante se muestra normalmente mediante un cuadro de diálogo de progreso no modal o una página de progreso dedicada, pero no con un puntero ocupado, un indicador de actividad o una barra de progreso en una barra de estado. Si el estado no es útil cuando se utilizan otros programas, solo se muestran los comentarios de progreso directamente en el propio programa.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo copiar con barra de progreso ](images/winenv-taskbar-image8.png)

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso en el botón de la barra de tareas ](images/winenv-taskbar-image9.png)

    En el ejemplo incorrecto, la barra de progreso del botón de la barra de tareas no es muy útil.

-   **¿La tarea es continua?** Si la tarea no se completa nunca, no es necesario mostrar su progreso. Entre los ejemplos de tareas continuas se incluyen los exámenes de antivirus que no inician los usuarios y la indexación de archivos.

    **Incorrecto:**

    ![captura de pantalla del icono de progreso de una tarea continua ](images/winenv-taskbar-image10.png)

    En este ejemplo, no es necesario mostrar el progreso de una tarea continua.

**Barra de tareas de la ventana secundaria**

-   **¿El programa contiene pestañas, ventanas de proyecto, ventanas secundarias MDI o ventanas secundarias a las que los usuarios suelen querer cambiar directamente?** En ese caso, puede ser adecuado asignar miniaturas de botón de la barra de tareas a estas ventanas.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Uso eficaz de listas de accesos directos y barras de herramientas en miniatura

Las listas de accesos directos y las vistas en miniatura ayudan a los usuarios a acceder a los recursos y realizar comandos de forma más eficaz. Sin embargo, al diseñar el modo en que el programa admite estas características, no se ha mejorado la eficacia de los concedidos. Si los usuarios no pueden predecir con precisión qué característica tiene el comando que necesitan o tienen que comprobar varios lugares, los usuarios acabarán frustrados y dejarán de usar estas características.

Las listas de accesos directos y las barras de miniaturas funcionan de forma más eficaz cuando son:

-   **Claramente diferenciados.** Los usuarios saben Cuándo buscar un destino o un comando en una Jump List y cuándo deben buscarse en una barra de herramientas en miniatura. Hay un propósito claro para cada uno, de modo que los usuarios rara vez disfunden el contenido de los dos. Por lo general, las listas de saltos se utilizan para iniciar nuevas tareas, mientras que las barras de herramientas en miniatura se usan para interactuar con las tareas en ejecución mientras se usan otros programas.
-   **Son.** Los destinos y comandos que se ofrecen son los que necesitan los usuarios. Si no es probable que los usuarios necesiten algo, no se incluye. No use el número máximo de elementos si no son necesarios.
-   **Predicción.** Los destinos y comandos que se ofrecen son los que los usuarios esperan encontrar. Los usuarios rara vez tienen que buscar en más de un lugar.
-   **Bien organizado.** Los usuarios pueden encontrar lo que buscan rápidamente. Usan etiquetas descriptivas pero concisas, y iconos adecuados para el reconocimiento de la ayuda.

Asegúrese de realizar una investigación de usuario para asegurarse de que la tiene correcta. Si en última instancia no se puede diseñar listas de saltos y barras de herramientas en miniatura que consigan estos objetivos, considere la posibilidad de proporcionar solo una de ellas. Es mejor tener una manera predecible de proporcionar comandos de los dos confusos.

## <a name="guidelines"></a>Directrices

### <a name="taskbar-buttons"></a>Botones de la barra de tareas

-   **Haga que aparezcan los siguientes tipos de ventana en la barra de tareas (para Windows 7, mediante una miniatura del botón de la barra de tareas):**
    -   Ventanas principales (que incluye cuadros de diálogo sin propietarios)
    -   Hojas de propiedades
    -   Cuadros de diálogo de progreso no modal
    -   Asistentes
-   **En Windows 7, use las miniaturas del botón de la barra de tareas para agrupar los siguientes tipos de ventana con el botón de la barra de tareas de la ventana principal en el que se inició.** Cada programa (específicamente, cada programa percibido como un programa independiente) debe tener un solo botón de la barra de tareas.

    -   Ventanas secundarias
    -   Pestañas del área de trabajo
    -   Ventanas de proyecto
    -   ventanas secundarias MDI

    **Correcto:**

    ![captura de pantalla del explorador de Windows y la barra de progreso ](images/winenv-taskbar-image11.png)

    En este ejemplo, una ventana secundaria se agrupa con el botón de la barra de tareas de la ventana principal.

    **Incorrecto:**

    ![captura de pantalla del explorador de Windows y el panel de control ](images/winenv-taskbar-image12.png)

    En este ejemplo, el panel de control no está correctamente agrupado con el explorador de Windows. Los usuarios los perciben como programas independientes.

    **Incorrecto:**

    ![captura de pantalla del programa, la barra de progreso y una barra de tareas ](images/winenv-taskbar-image13.png)

    En este ejemplo, copia de seguridad de Windows usa incorrectamente dos botones de la barra de tareas para un único programa.

-   La **restauración de una ventana principal también debe restaurar todas las ventanas secundarias,** incluso si esas ventanas secundarias tienen sus propios botones de la barra de tareas. Al restaurar, coloque las ventanas secundarias en la parte superior de la ventana principal.
-   **En Windows 7, los programas que normalmente tienen presencia de escritorio pueden mostrar temporalmente un botón de la barra de tareas para mostrar el estado.** Hágalo solo si el programa se muestra normalmente en el escritorio y los usuarios suelen interactuar con él. Un programa que normalmente se ejecuta sin presencia de escritorio debe usar en su lugar el icono del área de notificación, aunque es posible que no siempre sea visible.

    **Incorrecto:**

    ![captura de pantalla del botón de la barra de tareas del centro de sincronización de Windows ](images/winenv-taskbar-image14.png)

    En este ejemplo, el centro de sincronización de Windows usa incorrectamente un botón de la barra de tareas temporal para mostrar el estado. En su lugar, debe usar su icono de área de notificación.

### <a name="icons"></a>Iconos

-   **Diseñe el icono del programa para que tenga un aspecto excelente en la barra de tareas.** Asegúrese de que sea significativo y refleje su función y su marca. Haga que sea distinto, haga que sea especial y asegúrese de que se representa bien en todos los tamaños de icono. Dedique el tiempo necesario para que sea correcto. Siga las [instrucciones del icono de estilo Aero](vis-icons.md).
-   **Si el programa usa iconos superpuestos, diseñe el icono base del programa para controlar las superposiciones correctamente.** Los iconos de superposición se muestran en la esquina inferior derecha, por lo que debe diseñar el icono para que se oculte el área.

    ![captura de pantalla de iconos y con la superposición inferior derecha ](images/winenv-taskbar-image15.png)

    En este ejemplo, el icono de botón de la barra de tareas del programa no tiene información importante en el área inferior derecha.

-   **No use superposiciones en el icono base del programa,** tanto si el programa usa iconos superpuestos como si no. El uso de una superposición en el icono de base será confuso porque los usuarios tendrán que averiguar que no se está comunicando el estado.

    **Incorrecto:**

    ![captura de pantalla del icono base con la superposición ](images/winenv-taskbar-image16.png)

    En este ejemplo, el icono base del programa tiene el aspecto que muestra el estado.

Para obtener instrucciones y ejemplos de iconos generales, vea [iconos](vis-icons.md).

### <a name="overlay-icons"></a>Iconos de superposición

-   **Use los iconos de superposición para indicar únicamente el estado útil y relevante.** Tenga en cuenta que la presentación de un icono de superposición es una posible interrupción del trabajo del usuario, por lo que el cambio de Estado debe ser lo suficientemente importante como para merecer una posible interrupción.

    **Incorrecto:**

    ![captura de pantalla de tres iconos superpuestos ](images/winenv-taskbar-image17.png)

    En estos ejemplos, el icono de superposición no es lo suficientemente importante como para merecer una posible interrupción.

-   **Usar iconos de superposición para estado temporal.** Los iconos de superposición pierden su valor si se muestran constantemente, por lo que el estado normal del programa no debe mostrar un icono. Quitar el icono de superposición cuando el icono:

    -   **Es un problema:** Quite el icono una vez resuelto el problema.
    -   **Alerta de que algo es nuevo:** Quite el icono una vez que el usuario haya activado el programa.

    **Excepción:** El programa puede mostrar constantemente un icono de superposición si los usuarios siempre necesitan conocer su estado.

    ![captura de pantalla de Live Messenger con el icono de superposición ](images/winenv-taskbar-image18.png)

    En este ejemplo, Windows Live Messenger siempre muestra un icono de superposición para que los usuarios puedan comprobar siempre su presencia detectada.

-   **No mostrar un icono para indicar que se ha resuelto un problema.** En su lugar, simplemente quite cualquier icono anterior que indique un problema. Supongamos que los usuarios esperan normalmente que el programa se ejecute sin problemas.
-   **Mostrar iconos de superposición o iconos del área de notificación, pero nunca ambos.** El programa puede admitir ambos mecanismos para la compatibilidad con versiones anteriores, pero si el programa muestra el estado mediante iconos superpuestos, no debe utilizar también iconos del área de notificación para el estado.

    **Incorrecto:**

    ![captura de pantalla de la barra de tareas con el icono mostrado dos veces ](images/winenv-taskbar-image19.png)

    En este ejemplo, el icono nuevo correo se muestra de forma redundante.

-   **No parpadee el botón de la barra de tareas para llamar la atención sobre un cambio de estado.** Si lo hace, se destraerán. Permita que los usuarios detecten iconos superpuestos por su cuenta.
-   **Prefiere los iconos de superposición estándar para indicar el estado o los cambios de estado.** Use estos iconos de superposición estándar: 

    |                                                                                                   |                                  |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | **Overlay**<br/>                                                                            | **Estado**<br/>            |
    | ![captura de pantalla de un icono pequeño de advertencia ](images/winenv-taskbar-image20.png)<br/>               | Advertencia<br/>               |
    | ![captura de pantalla de un icono de error pequeño ](images/winenv-taskbar-image21.png)<br/>                 | Error<br/>                 |
    | ![captura de pantalla de un icono pequeño desconectado o desconectado ](images/winenv-taskbar-image22.png)<br/> | Deshabilitado o desconectado<br/> |
    | ![captura de pantalla del icono pequeño de bloqueado/sin conexión ](images/winenv-taskbar-image23.png)<br/>       | Bloqueado/sin conexión<br/>       |

    

     

-   **En el caso de los iconos de superposición personalizados, elija un diseño fácilmente reconocible.** Use iconos de color completo de 16x16 de alta calidad. Prefiere iconos con contornos distintivos sobre los iconos con forma de cuadrado o rectangular. Aplique también las otras [instrucciones de iconos de estilo Aero](vis-icons.md) .
-   **Mantenga el diseño de los iconos de superposición personalizados sencillos.** No intente comunicar ideas complejas, desconocidas o abstractas. Si no puede pensar en un icono personalizado adecuado, use un icono de error o un icono de advertencia estándar en su lugar cuando corresponda. Estos iconos se pueden usar de forma eficaz para comunicar muchos tipos de estado.
-   **No cambie el estado con demasiada frecuencia.** Los iconos de superposición no deben parecer ruidos, inestables o de petición. El ojo es sensible a los cambios en el campo de visión de periféricos, por lo que los cambios de estado deben ser sutiles.
    -   **No cambie el icono rápidamente.** Si el estado subyacente cambia rápidamente, haga que el icono refleje el estado de alto nivel.

        **Incorrecto:**

        ![captura de pantalla del icono de superposición en dos Estados ](images/winenv-taskbar-image24.png)

        En este ejemplo, el icono de superposición que cambia rápidamente exige atención.

    -   **No use animaciones.** Si lo hace, se destraerá.
    -   **No parpadee el icono.** Si lo hace, se destraerá. Si un evento requiere atención inmediata, utilice en su lugar un cuadro de diálogo. Si, de lo contrario, el evento necesita atención, use una notificación.

### <a name="taskbar-button-flashing"></a>Botón de la barra de tareas intermitente

-   **Use el botón de la barra de tareas en exceso para solicitar la atención inmediata del usuario para mantener la ejecución de una tarea en curso.** Es difícil para los usuarios concentrar mientras un botón de la barra de tareas parpadea, por lo que se supone que interrumpirán lo que están haciendo para que se detenga. Aunque parpadear un botón de la barra de tareas es mejor que robar el foco de entrada, los botones intermitentes de la barra de tareas siguen siendo muy intrusivos. Asegúrese de que la interrupción esté justificada, como para indicar que el usuario debe guardar los datos antes de cerrar una ventana. Los programas inactivos no suelen requerir una acción inmediata. No parpadee el botón de la barra de tareas si lo único que tiene que hacer el usuario es activar el programa, leer un mensaje o ver un cambio de estado.
-   **Si no se requiere una acción inmediata, tenga en cuenta estas alternativas:**
    -   Use una [notificación de acción correcta](mess-notif.md) para indicar que una tarea se ha completado.
    -   No haga nada. Espere a que los usuarios asistan al problema la próxima vez que activen el programa. Esta suele ser la mejor opción.
-   **Si un programa inactivo requiere atención inmediata, destaque el botón de la barra de tareas para atraer la atención y dejarla resaltada.** No haga nada más: no restaure ni active la ventana y no reproduzca efectos sonoros. En su lugar, respete la selección del estado de la ventana del usuario y deje que el usuario Active la ventana cuando esté listo.
-   **En el caso de las ventanas secundarias que tienen un botón de la barra de tareas, en lugar del botón de la barra de tareas de la ventana principal, Flash.** Si lo hace, los usuarios podrán asistir a la ventana directamente.
-   **En el caso de las ventanas secundarias que no tienen un botón de la barra de tareas, parpadee el botón de la barra de tareas de la ventana principal y coloque la ventana secundaria encima de todas las demás ventanas para ese programa.** Las ventanas secundarias que requieren atención deben ser mayores para asegurarse de que los usuarios las ven.
-   **Solo Flash botón de la barra de tareas de una ventana a la vez.** El parpadeo de más de un botón no es necesario y se distraen.
-   **Quite el resaltado del botón de la barra de tareas cuando el programa se active.**
-   **Cuando el programa se active, asegúrese de que es algo obvio.** Normalmente, este objetivo se consigue mostrando un cuadro de diálogo que formula una pregunta o inicia una acción.

### <a name="quick-launch-shortcuts"></a>Accesos directos de inicio rápido

-   **Coloque los accesos directos de programa en el área de inicio rápido solo si los usuarios optan por.** Dado que el inicio rápido se ha quitado de Windows 7, los programas diseñados para Windows 7 no deben agregar accesos directos de programa al área Inicio rápido ni proporcionar opciones para hacerlo.

### <a name="jump-lists"></a>Jump Lists

**Diseño**

-   **Diseñe listas de saltos para satisfacer los objetivos de sus usuarios para sus tareas cotidianas.** Considere:
    -   **El propósito del programa.** Piense en qué usuarios es más probable que lo hagan a continuación. En el caso de los programas de creación de documentos, es probable que los usuarios vuelvan a documentos usados recientemente. En el caso de los programas que muestran contenido existente, es posible que los usuarios deseen tener acceso a los recursos que usan con frecuencia. En el caso de otros programas, es probable que los usuarios realicen tareas que no hayan realizado antes, como leer nuevos mensajes, ver nuevos vídeos o comprobar la próxima reunión.
    -   **Lo que más le interesan los usuarios.** Piense por qué los usuarios usarían la Jump List en lugar de otros medios. Por ejemplo, los usuarios tienen más probabilidades de preocuparse de los destinos que se identifican explícitamente como importantes (por ejemplo, las direcciones web que se colocan en la barra de vínculos o en los favoritos, o escriben). Es menos probable que se ocupen de las obtenidas indirectamente o con poco esfuerzo (como las direcciones web visitadas a través de la redirección o haciendo clic en los vínculos).

        **Correcto:**

        ![captura de pantalla de Jump List con un vínculo a un destino ](images/winenv-taskbar-image25.png)

        **Incorrecto:**

        ![captura de pantalla de Jump List con cinco vínculos al destino ](images/winenv-taskbar-image26.png)

        En el ejemplo incorrecto, la Jump List contiene muchos destinos que es probable que los usuarios no tengan que preocuparse.

-   **No cree destinos demasiado granulares.** La creación de destinos es demasiado estrecha y específica puede producir redundancia, con varias formas de ir al mismo lugar. Por ejemplo, en lugar de enumerar páginas web individuales, enumere las páginas principales de nivel superior. en lugar de mostrar canciones, enumere álbumes.

    **Correcto:**

    ![captura de pantalla de la Jump List organizada por grupos ](images/winenv-taskbar-image27.png)

    **Incorrecto:**

    ![captura de pantalla de la Jump List organizada por canciones ](images/winenv-taskbar-image28.png)

    En el ejemplo incorrecto, al mostrar las canciones en una Jump List, se rellenará con un solo álbum.

-   **No rellene todas las ranuras de Jump List disponibles si no es necesario.** Centre el contenido de la Jump List en los elementos más útiles si el programa tiene solo tres elementos útiles, proporcione solo tres. Cuanto mayor sea el número de elementos de una Jump List, más esfuerzo se necesita para encontrar cualquier elemento específico.

    ![captura de pantalla de Jump List con un comando ](images/winenv-taskbar-image29.png)

    En este ejemplo, el accesorio Notas rápidas proporciona un comando de Jump List único, ya que es todo lo que se necesita.

-   **Proporcione información sobre herramientas solo cuando sea necesario para ayudar a los usuarios a comprender los elementos de Jump List.** Evite la información sobre herramientas redundante porque son una distracción innecesaria. Para obtener más instrucciones sobre información sobre herramientas, consulte [información sobre herramientas y recuadros informativos](ctrl-tooltips-and-infotips.md).

    **Incorrecto:**

    ![captura de pantalla de Jump List con información sobre herramientas redundante ](images/winenv-taskbar-image30.png)

    En este ejemplo, la información sobre herramientas de Jump List es redundante.

**Características de Jump List frente a características del programa**

-   **No haga que los destinos y comandos estén disponibles solo a través de Jump lists.** Los mismos destinos y comandos deben estar disponibles directamente desde el propio programa.
-   **Use nombres coherentes para los destinos y etiquetas para los comandos.** Los elementos de Jump List deben etiquetarse igual que los elementos equivalentes a los que se tiene acceso directamente desde el programa.
-   **Permite que el programa controle los destinos y comandos incluso cuando el programa no se está ejecutando.** Esto es necesario para una experiencia coherente, confiable y cómoda.

**Agrupación**

-   **Proporcione al menos uno y tres grupos como máximo.** Los elementos de Jump List siempre se agrupan para etiquetar su propósito. Tener más de tres grupos hace que los elementos sean más difíciles de encontrar.
-   **Use los nombres de grupo estándar cuando corresponda.** Los nombres de los grupos estándar son familiares y fáciles de entender para los usuarios.

    A los comandos se les asigna el nombre del grupo de tareas, que es asignado por Windows y, por tanto, no se puede cambiar.

    **Correcto:**

    ![captura de pantalla de Jump List con el nombre de grupo reciente ](images/winenv-taskbar-image31.png)

    **Incorrecto:**

    ![captura de pantalla de Jump List con el nombre del grupo de historial ](images/winenv-taskbar-image32.png)

    Reciente es el mejor nombre de grupo porque es familiar, y la diferencia sutil entre el historial y el reciente no merece la pena hacerlo.

**Comandos**

-   **Proporcionar un conjunto fijo de comandos independientemente del estado de ejecución del programa, el documento actual o el usuario actual.** Los comandos se deben aplicar a todo el programa, no a una ventana o un documento específicos. Esto es necesario para una experiencia coherente, confiable y cómoda. Los comandos no deben quitarse o deshabilitarse.

    **Excepciones:** Puede sustituir o quitar comandos cuando:

    -   Un conjunto de comandos mutuamente exclusivos comparte una sola ranura de comandos, siempre que se aplique un comando.
    -   Los comandos no se aplican hasta que se hayan usado características específicas, siempre y cuando los comandos de lo contrario siempre se apliquen.

    **Incorrecto:**

    ![captura de pantalla de Jump List con la tarea de impresión ](images/winenv-taskbar-image33.png)

    En este ejemplo, Print no es un buen comando Jump List porque depende del documento actual.

    **Correcto:**

    ![captura de pantalla de Jump List con inicio y cierre de sesión ](images/winenv-taskbar-image34.png)

    En este ejemplo, el inicio y cierre de sesión son comandos mutuamente exclusivos. Además, los separadores se usan para agrupar comandos relacionados.

-   **Use las siguientes etiquetas de comando estándar cuando corresponda.** Las etiquetas de comando estándar son más fáciles de entender para los usuarios.
-   **Presente los comandos en un orden lógico.** Los pedidos comunes incluyen la frecuencia de uso o el orden de uso. Coloque comandos muy relacionados entre sí. Dentro del grupo tareas, coloque los separadores entre los grupos de comandos relacionados según sea necesario.
-   **No proporcione comandos para abrir o cerrar el programa.** Estos comandos están integrados en todas las listas de accesos directos.

**Iconos de comando**

-   **En el grupo tareas, proporcione un icono de comando solo cuando Ayude a los usuarios a entender, reconocer o diferenciar comandos,** especialmente cuando hay un icono establecido para el comando que se usa en el programa.

    -   **Excepción:** Si el programa usa ambos destinos (que siempre tienen iconos) y comandos, considere la posibilidad de proporcionar iconos para todos los comandos si, de lo contrario, tendría un aspecto extraño.

    **Incorrecto:**

    ![captura de pantalla del uso incoherente de la Jump List de los iconos ](images/winenv-taskbar-image35.png)

    En este ejemplo, Internet Explorer debe proporcionar iconos para todos los comandos con el fin de evitar un aspecto extraño.

**Destinations**

-   **Proporcionan un conjunto dinámico de destinos que son específicos del usuario actual, pero son independientes del estado de ejecución del programa o del documento actual.** Como se mencionó anteriormente, asegúrese de que se ajustan a la finalidad del programa, que son lo que los usuarios tienen más cuidado y tienen el nivel de especificidad adecuado.
-   **Cuando sea adecuado, use una lista de destino "automática".** Windows administra los destinos automáticos, pero el programa controla los destinos específicos que se pasan.
    -   Considere la posibilidad de usar recientes para programas de creación de documentos en los que es probable que los usuarios vuelvan a destinos usados recientemente.

        ![captura de pantalla de Jump List con el nombre de grupo "reciente" ](images/winenv-taskbar-image36.png)

        En este ejemplo, el Bloc de notas de Windows usa destinos recientes.

    -   Considere la posibilidad de usar con frecuencia para programas que muestran contenido existente, donde es probable que los usuarios vuelvan a los elementos que usan con frecuencia. Los destinos frecuentes se ordenan por orden de frecuencia, lo que suele ser más frecuente.

        ![captura de pantalla de Jump List con un nombre de grupo frecuente ](images/winenv-taskbar-image37.png)

        En este ejemplo, el explorador de Windows usa destinos frecuentes.

    -   Use frecuente si el reciente daría como resultado muchos destinos inútiles. Las listas frecuentes son más estables y la mejor opción cuando los usuarios van a muchos destinos diferentes, pero no es probable que vuelvan a las usadas con poca frecuencia.

        **Incorrecto:**

        ![captura de pantalla de Jump List con varios elementos recientes ](images/winenv-taskbar-image38.png)

        Usar recientes en Windows Internet Explorer daría como resultado muchos destinos inútiles.

    -   Si las opciones recientes o frecuentes son igualmente adecuadas, use reciente porque ese enfoque es más fácil para los usuarios entender y es más predecible.
    -   Si usa reciente y el programa tiene un equivalente en el menú Archivo, haga que las listas tengan el mismo contenido en el mismo orden. Para los usuarios, deben parecerse a las mismas listas.

-   **Cuando sea necesario, use una lista de destino personalizada.** El programa tiene control total sobre el contenido y el criterio de ordenación de la lista de destino personalizada y, por tanto, puede basar la lista en función de los factores.
    -   Cree versiones personalizadas de recientes o frecuentes si son adecuadas, pero la administración automática no funciona bien para el programa. Por ejemplo, es posible que el programa tenga que realizar un seguimiento de diversos factores más allá de los comandos Open File. En este caso, use el mismo nombre (reciente o frecuente) y el criterio de ordenación, ya que los usuarios no tendrán en cuenta la diferencia.
    -   De lo contrario, use un tipo diferente de destino para satisfacer mejor los objetivos del usuario. A menudo, estas listas ayudan a los usuarios a realizar tareas que no han realizado antes, como leer nuevos mensajes, ver nuevos vídeos o comprobar la próxima reunión.

        ![captura de pantalla de Jump List con el nombre de grupo ' New ' ](images/winenv-taskbar-image39.png)

        En este ejemplo, Windows Media Center muestra los programas grabados recientemente que el usuario todavía no ha observado.

    -   Elija un criterio de ordenación que se corresponda con el modelo mental del usuario de la lista. Por ejemplo, una lista de estilos de tareas pendientes tendría lo siguiente que se debe mostrar en primer lugar. Si no hay ningún modelo mental claro, ordene la lista de destino en orden alfabético.

-   **No use varias listas de destino que proporcionen vistas diferentes de los mismos datos.** En su lugar, varias listas de destino deben tener principalmente datos diferentes para admitir escenarios de diferencia. Por ejemplo, puede proporcionar una lista reciente o una lista frecuente, pero no ambos. Si lo hace, es excesivo si los elementos superpuestos están presentes, pero confuso si se quitan los elementos superpuestos.

    **Incorrecto:**

    ![captura de pantalla de Jump List con elementos de grupo repetidos ](images/winenv-taskbar-image40.png)

    En este ejemplo, la entrega de vistas diferentes de los mismos destinos es inestable.

    **Correcto:**

    ![captura de pantalla de Jump List con tareas bien organizadas ](images/winenv-taskbar-image41.png)

    En este ejemplo, las listas de destino tienen datos diferentes para las distintas tareas.

-   **Si el programa tiene un comando para borrar los datos de privacidad, borre también las listas de destinos.** Las listas de destino pueden contener datos confidenciales.

### <a name="thumbnail-toolbars"></a>Barras de herramientas en miniatura

**Interacción**

-   **Proporcione hasta siete de los comandos más importantes que se usan con frecuencia y que se aplican a la ventana que se muestra en la miniatura.** No se sienta obligado a proporcionar tantos comandos como sea posible si el programa solo tiene tres comandos importantes, que se usan con frecuencia, proporcionan solo tres.

    **Incorrecto:**

    ![captura de pantalla de la barra de herramientas con demasiados comandos ](images/winenv-taskbar-image42.png)

    En este ejemplo, la barra de herramientas de miniaturas tiene comandos que no son importantes.

-   **Usar comandos que son directos e inmediatos.** Estos comandos deben tener un efecto inmediato al hacer clic en el comando no debe mostrar un menú desplegable o un cuadro de diálogo para obtener más información.

    **Incorrecto:**

    ![captura de pantalla de la miniatura con el menú desplegable ](images/winenv-taskbar-image43.png)

    Los comandos de la barra de herramientas de miniaturas deben tener un efecto inmediato.

-   **Deshabilitar los comandos que no se aplican al contexto actual o que producirían un error directamente.** No oculte estos comandos, ya que esto hace que la presentación de la barra de herramientas sea inestable.
-   **No descarte la miniatura cuando los usuarios hagan clic en un comando si es probable que revisen los resultados o hagan clic en otro comando inmediatamente.** Quite la miniatura para los comandos que indican que el usuario ha finalizado por ahora, como los comandos que muestran otras ventanas.

    ![captura de pantalla de la miniatura del reproductor de media con el comando ](images/winenv-taskbar-image44.png)

    En este ejemplo, al hacer clic en siguiente en Windows Media Player continúa mostrando la miniatura porque es posible que los usuarios deseen proporcionar otros comandos.

    ![captura de pantalla de la miniatura con el icono de chat ](images/winenv-taskbar-image45.png)

    En este ejemplo, al hacer clic en chat en Windows Live Messenger se descarta la miniatura porque es muy probable que los usuarios envíen un mensaje.

**Presentación**

-   **Asegúrese de que los iconos de la barra de herramientas en miniatura cumplen las directrices de iconos de estilo Aero.** Para cada comando, proporcione iconos de color completo 16x16, 20x20 y 24x24 de alta calidad. Las versiones mayores se usan en los modos de presentación de alta ppp.
-   **Asegúrese de que los iconos están claramente visibles en el color de fondo de la barra de herramientas en los Estados normal y de desplazamiento.** Evalúe siempre los iconos en contexto y en los modos de alto contraste.
-   **Elija los diseños de icono de comando que comuniquen claramente su efecto.** Los iconos de comandos bien diseñados se explican por sí solos para ayudar a los usuarios a encontrar y comprender los comandos de forma eficaz.
-   **Elija los iconos que sean reconocibles y distinguibles.** Asegúrese de que los iconos tienen formas y colores distintivos. Esto ayuda a los usuarios a encontrar los comandos rápidamente, incluso si no recuerdan el símbolo del icono. Después del uso inicial, los usuarios no deben confiar en la información sobre herramientas para distinguir entre los comandos.
-   **Proporcione una información sobre herramientas para etiquetar cada comando.** Una buena información sobre herramientas etiqueta el control sin etiqueta al que apunta. Para obtener instrucciones y ejemplos, consulte la [información sobre herramientas y recuadros informativos](ctrl-tooltips-and-infotips.md).

### <a name="progress-bars"></a>Barras de progreso

-   **Siga las instrucciones generales de la barra de progreso, incluido el** reinicio o la copia de seguridad del progreso, y el uso de una barra de progreso roja para indicar un problema.
-   **Evite el uso de barras de progreso indeterminadas.** Las barras de progreso indeterminadas muestran actividad, no progreso. Reserve barras de progreso indeterminadas para aquellas situaciones excepcionales en las que los usuarios no tienen la actividad concedida.

Para obtener más instrucciones, vea [barras de progreso](progress-bars.md).

## <a name="text"></a>Texto

### <a name="window-titles"></a>Títulos de ventana

Al elegir los títulos de ventana, tenga en cuenta la apariencia del título en la barra de tareas:

-   Optimice los títulos que se muestran en la barra de tareas. para ello, coloque primero la información distintiva en primer lugar.
-   En los cuadros de diálogo de progreso no modal, resuma primero el progreso. Ejemplo: "66% completado".
-   Evite los títulos de ventana que tengan truncamientos extraños.

    **Incorrecto:**

    ![captura de pantalla del título que corta el nombre del programa ](images/winenv-taskbar-image48.png)

    En este ejemplo, el título de la ventana truncado tiene resultados desafortunados.

### <a name="jump-list-commands"></a>Comandos Jump List

-   **Iniciar comandos con un verbo.**
-   **Use mayúsculas de estilo de frase.**

Para obtener más instrucciones sobre las etiquetas de comandos, vea [menús](cmd-menus.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a la barra de tareas:

-   Haga referencia a la barra completa como la barra de tareas (una sola palabra compuesta en minúsculas).
-   Haga referencia a los elementos de la barra de tareas específicamente por su etiqueta o, por lo general, como botones de la barra de tareas.
-   Siempre que sea posible, dé formato a las etiquetas de la barra de tareas con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.
-   Consulte iconos de superposición como iconos de botón de la barra de tareas. No se hace referencia a ellos como notificaciones, incluso si su finalidad es notificar a los usuarios. Sin embargo, puede decir que estos iconos notifican a los usuarios eventos concretos.

Ejemplo: el icono del botón de la barra de tareas nuevo correo informa de que ha llegado un nuevo mensaje de correo electrónico.

 

