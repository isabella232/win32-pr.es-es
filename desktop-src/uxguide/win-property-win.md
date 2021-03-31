---
title: Ventanas de propiedades
description: La ventana de propiedades es el nombre colectivo de la hoja de propiedades de los siguientes tipos de interfaces de usuario (UI) que se usa para ver y cambiar las propiedades de un objeto o una colección de objetos en un cuadro de diálogo. Inspector de propiedad que se usa para ver y cambiar las propiedades de un objeto o colección de objetos en un panel. Cuadro de diálogo Opciones que se usa para ver y cambiar las opciones de una aplicación.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c255d638f236b4bc4a4f1a6c923eac24421cfe9d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103819975"
---
# <a name="property-windows"></a>Ventanas de propiedades

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

La ventana de propiedades es el nombre colectivo para los siguientes tipos de interfaces de usuario (IU):

-   Hoja de propiedades: se usa para **ver y cambiar las propiedades de un objeto o una colección de objetos en un cuadro de diálogo**.
-   Inspector de propiedad: se usa para **ver y cambiar las propiedades de un objeto o una colección de objetos en un panel**.
-   Cuadro de diálogo Opciones: se usa para **ver y cambiar las opciones de una aplicación**.

Una propiedad de un objeto es una de las siguientes:

-   Un valor de configuración que los usuarios pueden cambiar (como el nombre de un archivo y el atributo de solo lectura).
-   Atributo de un objeto que los usuarios no pueden cambiar directamente (como el tamaño de un archivo y la fecha de creación).

A diferencia de los cuadros de diálogo (distintos de los cuadros de diálogo de opciones) y los asistentes, las ventanas de propiedades normalmente admiten varias tareas en lugar de una sola tarea.

Las ventanas de propiedades suelen estar organizadas en páginas, a las que se tiene acceso a través de pestañas. Las ventanas de propiedades suelen estar asociadas a las pestañas (y viceversa), pero las **pestañas no son esenciales para las ventanas de propiedades**.

![captura de pantalla de la hoja de propiedades de propiedades del documento ](images/win-property-win-image1.png)

Hoja de propiedades típica.

**Nota:** Las instrucciones relacionadas con el [diseño](vis-layout.md) y las [pestañas](ctrl-tabs.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿La configuración de las propiedades requiere que los usuarios realicen una secuencia de pasos fija y no trivial?** Si es así, use un [Asistente](win-wizards.md) o un [flujo de tareas](glossary.md) en su lugar.
-   **¿Es el contenido únicamente las opciones de una aplicación?** Si es así, use un cuadro de diálogo Opciones.
-   **¿Es el contenido únicamente los atributos de una aplicación?** Si es así, use un [cuadro acerca de](glossary.md).
-   **¿Es el contenido principalmente las propiedades de un objeto (su configuración o sus atributos)?** Si no es así, use un cuadro de diálogo [cuadro](win-dialog-box.md) o un [cuadro de diálogo con pestañas](glossary.md)estándar.
-   ¿ **Es probable que los usuarios vean o cambien las propiedades con frecuencia o durante un período de tiempo prolongado?** Si es así, use un inspector de propiedad. de lo contrario, use una hoja de propiedades.
-   ¿ **Es probable que los usuarios vean o cambien las propiedades de varios objetos a la vez?** Si es así, use un inspector de propiedad. de lo contrario, use una hoja de propiedades.

**Las hojas de propiedades y los inspectores de propiedad no son exclusivos.** Puede mostrar las propiedades a las que se accede con mayor frecuencia en un inspector de propiedad y en el conjunto completo de la hoja de propiedades.

## <a name="design-concepts"></a>Conceptos de diseño

**A menudo, las ventanas de propiedades se convierten en una base de dumping para una variedad impar de valores de bajo nivel basados en la tecnología.** Con demasiada frecuencia, estas propiedades se organizan en pestañas, pero más allá de las que no están diseñadas para tareas o usuarios concretos. Como resultado, cuando los usuarios se enfrentan a una tarea en una ventana de propiedades, a menudo no saben qué hacer.

Para asegurarse de que las ventanas de propiedades son útiles y se pueden usar, siga estos pasos:

-   Asegúrese de que las propiedades son necesarias.
-   Presente propiedades en términos de los objetivos del usuario, no de la tecnología.
-   Presentar propiedades en el nivel de la derecha.
-   Diseñe páginas para tareas específicas.
-   Diseñe páginas para usuarios específicos, especialmente usuarios limitados (no administradores).
-   Organice las páginas de propiedades de forma eficaz.

**Si solo hace algo...**

Presente propiedades en términos de los objetivos del usuario, no de la tecnología. Imagine que está explicando la propiedad y por qué es útil para un amigo. ¿Cómo lo explicaría? ¿Qué lenguaje usaría? Este es el lenguaje que se va a usar en las páginas de propiedades.

## <a name="usage-patterns"></a>Patrones de uso

Las ventanas de propiedades tienen varios patrones de uso.

-   Hojas de propiedades. Las propiedades de un solo objeto se muestran en un cuadro de diálogo no modal.
-   Hojas de propiedades de varios objetos. Las propiedades de varios objetos se muestran en un cuadro de diálogo no modal.
-   Hojas de propiedades de configuración vigente. Las propiedades efectivas de un único objeto se muestran en un cuadro de diálogo no modal.
-   Cuadros de diálogo de opciones. Las propiedades de una aplicación se muestran en un cuadro de diálogo modal.
-   Inspectores de propiedad. Las propiedades de la selección actual (un solo objeto o grupo de objetos) se muestran en un panel de ventana no modal o en una ventana desacoplada.

Todos los patrones de ventana de propiedades excepto los inspectores de propiedad usan una confirmación diferida, lo que significa que los cambios surten efecto solo cuando los usuarios hacen clic en aceptar o aplicar. Los inspectores de propiedad usan una confirmación inmediata (las propiedades se cambian en cuanto los usuarios realizan cambios), por lo que no hay necesidad de los botones aceptar, cancelar y aplicar.

## <a name="guidelines"></a>Directrices

### <a name="property-sheets"></a>Hojas de propiedades

-   **Mostrar una hoja de propiedades cuando los usuarios:**
    -   Seleccione el comando propiedades para un objeto.
    -   Establezca el foco de entrada en un objeto y presione Alt + Entrar.

**Hojas de propiedades de varios objetos**

-   **Muestra las propiedades comunes de todos los objetos seleccionados.** Si los valores de propiedad difieren, muestre los controles asociados a esos valores utilizando un estado mixto. (Vea las directrices de control respectivas para usar valores de estado mixto).
-   Si el objeto seleccionado es una colección de varios objetos discretos (como una carpeta de archivos), se **muestran las propiedades del único objeto agrupado en lugar de una hoja de propiedades de varios objetos para los objetos discretos.**

### <a name="options-dialog-boxes"></a>Cuadro de diálogo Opciones

-   **No separe las opciones de la personalización.** Es decir, no tiene un comando opciones y un comando personalizar. A menudo, los usuarios están confundidos por esta separación. En su lugar, obtenga acceso a la personalización a través de las opciones.

### <a name="property-pages"></a>páginas de propiedades

-   **Siga estas instrucciones para el orden de las páginas:**
    -   Haga que la página general o su equivalente sea la primera página.
    -   Haga que la página avanzadas o su equivalente sea la última página.
    -   Para las páginas restantes:
        -   Organícelas en grupos de páginas relacionadas.
        -   Ordene los grupos por la probabilidad de su uso.
        -   Dentro de cada grupo, ordene las páginas por sus relaciones o por la probabilidad de su uso.
        -   No debe tener tantas páginas que necesiten mostrarse en orden alfabético.
-   **Haga que las páginas sean coherentes relacionando todas las propiedades de cada página con un único propósito basado en tareas específico.**
-   **Si el espacio lo permite, explique el propósito de la ventana de propiedades en la parte superior de la página si no es obvio para los usuarios de destino.** Si la página se utiliza para realizar una sola tarea, **formule el texto como una instrucción clara acerca de cómo realizar esa tarea**. Use oraciones completas, terminando con un punto.

    ![captura de pantalla de la hoja de propiedades propiedades del firewall ](images/win-property-win-image2.png)

    En este ejemplo, el propósito del firewall de Microsoft Windows se explica en la parte superior de la página general.

-   **Haga que el contenido similar sea coherente entre las páginas usando nombres y ubicaciones de control coherentes.** Por ejemplo, si varias páginas tienen cuadros de nombre, intente colocarlas en la misma ubicación de la página y usar etiquetas coherentes. El contenido similar no debe rebotar en torno a la página.
-   **Coloque la misma propiedad en la misma página en toda la aplicación.** Por ejemplo, no coloque una propiedad de expiración en la pestaña General para un tipo de objeto y en la pestaña avanzadas para otro tipo.
-   **Si es probable que los usuarios empiecen con la última página que se muestra, haga que la pestaña de la página sea persistente y selecciónela de forma predeterminada.** Haga que la configuración se mantenga en una ventana por propiedad y por usuario. De lo contrario, seleccione la primera página de forma predeterminada.
-   **No haga que la configuración de una página dependa de la configuración de otras páginas.** En su lugar, coloque la configuración dependiente en una sola página. Cambiar una configuración en una página nunca cambiará automáticamente la configuración de otras páginas.
    -   **Excepción:** Si los valores dependientes se encuentran en dos ventanas de propiedades diferentes, use etiquetas de texto estático para explicar esta relación en ambas ubicaciones.
-   **No desplace las páginas de propiedades.** Las pestañas y las barras de desplazamiento se usan para aumentar el área efectiva de una ventana, pero un mecanismo debe ser suficiente. En lugar de usar barras de desplazamiento, haga que las páginas de propiedades sean más grandes y diseñe las páginas de forma eficaz.

**Primeras páginas**

-   En el caso de las propiedades del objeto, **Coloque el nombre del objeto en la primera página.**
-   Si va a asociar [iconos](vis-icons.md) (opcionales) con los objetos, **muestre el icono correspondiente en la esquina superior izquierda** de la primera página.

**Páginas generales**

-   **Evite las páginas generales.** No es necesario tener una página general. Use una página general solo si:
    -   Las propiedades se aplican a varias tareas y son significativas para la mayoría de los usuarios. No ponga propiedades especializadas o avanzadas en una página general, pero puede hacer que sean accesibles a través de un botón de comando en la página general.
    -   Las propiedades no se ajustan a una categoría más específica. En su lugar, use ese nombre para la página.

**Páginas avanzadas**

-   **Evite las páginas avanzadas.** Use una página avanzada solo si:
    -   Las propiedades se aplican a tareas poco frecuentes y son significativas principalmente para los usuarios avanzados.
    -   Las propiedades no se ajustan a una categoría más específica. En su lugar, use ese nombre para la página.
-   **No llame a propiedades avanzadas basadas únicamente en medidas tecnológicas.** Por ejemplo, una opción de grapado de impresora puede ser una característica de impresora avanzada, pero es significativa para todos los usuarios, por lo que no debe estar en una página avanzada.

### <a name="owned-property-windows"></a>Ventanas de propiedades de propiedad

-   **No mostrar más de una ventana de propiedades propiedad de una ventana de propiedades.** Al mostrar más de una, el significado de los botones aceptar y cancelar es difícil de entender. Puede mostrar otros tipos de cuadros de diálogo auxiliares (como selector de objetos) según sea necesario.

    **Incorrecto:**

    ![captura de pantalla de tres ventanas de propiedades de propiedad ](images/win-property-win-image3.png)

    En este ejemplo, el cuadro de diálogo Opciones de propietario tiene tres niveles de ventanas de propiedades de propiedad. Como resultado, los significados de aceptar y cancelar son confusos.

-   En el caso de las ventanas de propiedades que usan un modelo de confirmación diferida, asegúrese de que **los usuarios pueden cancelar los cambios realizados en una ventana de propiedades de propiedad haciendo clic en Cancelar en la ventana propietaria.**
-   Si una ventana de propiedades con propietario requiere una confirmación inmediata, **indique que los cambios se confirmaron cambiando el nombre del botón Cancelar en la ventana propietaria a cerrar.** Revierta el botón a cancelar si el usuario hace clic en aplicar.

    ![captura de pantalla de la ventana de propiedades con aceptar y cerrar ](images/win-property-win-image4.png)

    En este ejemplo, no se pueden cancelar los cambios en los diccionarios personalizados y la configuración de gramática. Puede proporcionar a los usuarios estos comentarios cambiando Cancelar para cerrar.

**Otras ventanas de propiedad**

-   Si se usa una ventana propiedad para realizar una tarea auxiliar, **no cambie el nombre del botón Cancelar.** Las instrucciones anteriores solo se aplican a las ventanas de propiedades de propiedad, no a los cuadros de diálogo que se usan para realizar tareas auxiliares.

    ![captura de pantalla de la ventana propietaria y el liberador de espacio en disco ](images/win-property-win-image5.png)

    En este ejemplo, el liberador de espacio en disco es una tarea auxiliar, por lo que no se aplican las directrices anteriores. Por ejemplo, el botón Cancelar de la ventana propietaria no debe cambiarse a cerrar.

-   Si la ventana de propiedad se utiliza para realizar una tarea auxiliar, **no cierre la ventana de propiedades de propietario cuando se haga clic en el botón de comando.** Lo que hace es desorientar y presupone que el único motivo por el que el usuario mostró la ventana de propiedades era realizar ese comando.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo Opciones ](images/win-property-win-image6.png)

    En este ejemplo, al hacer clic en **proteger documento** , se cierra incorrectamente el cuadro de diálogo Opciones.

### <a name="tabs"></a>Tabulaciones

-   **Use etiquetas de pestaña concisas.** Use una o dos palabras que describan claramente el contenido de la página. Las etiquetas más largas producen un uso ineficaz del espacio de la pantalla, especialmente cuando se localizan las etiquetas.
-   **Usar etiquetas de pestaña específicas y significativas.** Evite etiquetas de pestañas genéricas que se puedan aplicar a cualquier pestaña, como general, avanzada o configuración.
-   **Use las pestañas horizontales si:**
    -   La ventana de propiedades tiene siete o menos pestañas (incluidas las extensiones de terceros).
    -   **Todas las pestañas se ajustan a una fila, incluso cuando se localiza la interfaz de usuario.**
    -   Las pestañas horizontales se usan en las demás ventanas de propiedades de la aplicación.
-   **Use las pestañas verticales si:**

    -   La ventana de propiedades tiene ocho o más pestañas (incluidas las extensiones de terceros).
    -   **El uso de pestañas horizontales requeriría más de una fila.**
    -   Use pestañas verticales en las otras ventanas de propiedades de la aplicación.

    ![captura de pantalla de la ventana de propiedades con pestañas verticales ](images/win-property-win-image7.png)

    En este ejemplo, las pestañas verticales se usan para acomodar ocho o más pestañas.

-   En el caso de los **inspectores de propiedad, para ahorrar espacio, considere la posibilidad de usar una lista desplegable en lugar de pestañas**, especialmente si el usuario no suele cambiar la pestaña actual.
-   **Si una pestaña no se aplica al contexto actual y los usuarios no la esperan, quite la pestaña.** De este modo, se simplifica la interfaz de usuario y los usuarios no la recibirán.

    **Incorrecto:**

    ![captura de pantalla de la pestaña ubicaciones de archivos atenuadas ](images/win-property-win-image8.png)

    En este ejemplo, la pestaña ubicaciones de archivo está deshabilitada incorrectamente cuando se usa Microsoft Word 2003 como editor de correo electrónico. La página debe quitarse porque los usuarios no esperan ver o cambiar las ubicaciones de los archivos en este contexto.

-   **Si una pestaña no se aplica al contexto actual y los usuarios podrían esperar que:**

    -   **Mostrar la pestaña.**
    -   **Deshabilite los controles de la página.**
    -   **Incluye texto que explica por qué los controles están deshabilitados.**

    No deshabilite la pestaña porque no se explica por sí misma y prohíbe la exploración. Además, los usuarios que busquen una propiedad específica se verán obligados a buscar en las demás pestañas.

    ![captura de pantalla de los controles de vista atenuados ](images/win-property-win-image9.png)

    En este ejemplo de Word 2003, no se aplica ninguna de las opciones de vista al diseño de lectura. Sin embargo, los usuarios pueden esperar que se apliquen en función de la etiqueta de la pestaña, por lo que se muestra la página, pero las opciones están deshabilitadas.

-   **No asigne efectos a las pestañas de cambio.** Cambiar la pestaña actual nunca debe tener efectos secundarios, aplicar valores de configuración o producir un mensaje de error.
-   **No anide tabulaciones ni combina tabulaciones horizontales con pestañas verticales.** En su lugar, reduzca el número de pestañas, use solo pestañas verticales o use otro control, como una lista desplegable.
-   **No use pestañas si una ventana de propiedades tiene una sola pestaña y no es extensible.** En su lugar, use un cuadro de diálogo normal con aceptar, cancelar y un botón opcional aplicar. Las ventanas de propiedades extensibles (que se pueden extender por terceros) siempre tienen que usar pestañas.
-   **No coloque iconos en las pestañas.** Normalmente, los iconos agregan un desorden visual innecesario, consumen espacio de pantalla y no suelen mejorar la comprensión de los usuarios. Agregue solo iconos que ayuden a la comprensión, como los símbolos estándar.

    **Incorrecto:**

    ![captura de pantalla de etiquetas de pestaña con iconos ](images/win-property-win-image10.png)

    En este ejemplo, los gráficos agregan un desorden visual innecesario y hacen poco para mejorar la comprensión de los usuarios.

-   **No use logotipos de producto para gráficos de pestañas.** Las pestañas no son para la personalización de marca.
-   **No desplace las tabulaciones horizontales.** El desplazamiento horizontal no es fácilmente reconocible. No obstante, puede desplazarse por las pestañas verticales.

    **Incorrecto:**

    ![captura de pantalla de etiqueta de pestaña horizontal truncada ](images/win-property-win-image11.png)

    En este ejemplo, se desplazan las pestañas horizontales.

### <a name="command-buttons"></a>Botones de comando

-   **Coloque los botones de comando que se aplican a todas las páginas de propiedades en la parte inferior de la ventana de propiedades.** Alinee los botones a la derecha y use este orden (de izquierda a derecha): aceptar, cancelar y aplicar.
-   **Coloque los botones de comando que se aplican solo a las páginas de propiedades individuales directamente en la página de propiedades.**

### <a name="commit-buttons"></a>Botones de confirmación

**Botones aceptar**

-   **En el caso de las ventanas de propiedades de propietario, el botón Aceptar significa aplicar los cambios pendientes (realizados desde que se abrió la ventana o la última aplicación) y cerrar la ventana.**
-   **En el caso de las ventanas de propiedades de propiedad, el botón Aceptar significa mantener los cambios, cerrar la ventana y aplicar los cambios cuando se apliquen los cambios de la ventana propietaria.**
-   **No cambie el nombre del botón Aceptar.** A diferencia de otros cuadros de diálogo, las ventanas de propiedades no se usan para realizar una tarea específica. Si tiene sentido cambiar el nombre del botón Aceptar (por ejemplo, imprimir), la ventana no es una ventana de propiedades.
-   **No asigne una clave de acceso.**

**Cancelar botones**

-   **El botón Cancelar significa descartar todos los cambios pendientes (realizados desde que se abrió la ventana o la última vez que se aplicó) y cerrar la ventana.**
-   **Si no se pueden abandonar todos los cambios pendientes, cambie el nombre del botón Cancelar a cerrar.** Al hacer clic en cancelar, se deben abandonar todos los cambios pendientes.
-   **Si la ventana de propiedades de propiedad requiere una confirmación inmediata, cambie el nombre del botón Cancelar en la ventana propietaria a cerrar para mostrar que se confirmaron los cambios.**
-   **No asigne una clave de acceso.**

**Aplicar botones**

-   **En el caso de las hojas de propiedades de propietario, el botón aplicar significa aplicar los cambios pendientes (realizados desde que se abrió la ventana o la última aplicación), pero dejar la ventana abierta.** Esto permite a los usuarios evaluar los cambios antes de cerrar la hoja de propiedades.
-   **En el caso de las hojas de propiedades de propiedad, no use.** El uso de un botón aplicar en una hoja de propiedades de propiedad hace que el significado de los botones de confirmación de la hoja de propiedades del propietario sea difícil de entender.
-   **Proporcione un botón Aplicar solo si la hoja de propiedades tiene valores de configuración (al menos uno) con efectos que los usuarios pueden evaluar de forma significativa.** Normalmente, se usan botones aplicar cuando la configuración realiza cambios visibles. Los usuarios deben poder aplicar un cambio, evaluar el cambio y realizar cambios adicionales en función de esa evaluación. Si no es así, quite el botón aplicar en lugar de deshabilitarlo.

    **Incorrecto:**

    ![captura de pantalla de las propiedades del sistema con el botón aplicar ](images/win-property-win-image12.png)

    En este ejemplo, ninguna de las propiedades del sistema tiene un efecto visual, por lo que el botón aplicar no tiene ningún valor y debe quitarse.

-   **Coloque todas las opciones de configuración que los usuarios pueden querer aplicar en las páginas propietarias.** No utilice los botones aplicar en las hojas de propiedades de propiedad, ya que esto es confuso.
-   **Use aplicar botones solo con las hojas de propiedades, no con los cuadros de diálogo Opciones.**
-   **Habilite el botón Aplicar solo cuando haya cambios pendientes**; de lo contrario, deshabilítelo.
-   **Asigne "A" como tecla de acceso.**

**Botones cerrar**

-   **Si no se pueden abandonar todos los cambios pendientes, cambie el nombre del botón Cancelar a cerrar.** Al hacer clic en cancelar, se deben abandonar todos los cambios pendientes.
-   **No confirme si los usuarios descartan los cambios.**
    -   **Excepción:** Si la ventana de propiedades tiene una configuración que requiere un esfuerzo significativo para establecer y el usuario ha realizado cambios, puede mostrar una [confirmación](mess-confirm.md) si el usuario hace clic en el botón cerrar de la barra de título. La razón es que algunos usuarios suponen equivocadamente que el botón cerrar de la barra de título tiene el mismo efecto que el botón Aceptar.
-   **Con la excepción del mensaje de confirmación, asegúrese de que el botón cerrar de la barra de título tiene el mismo efecto que cancelar o cerrar.**

### <a name="page-contents"></a>Contenido de la página

-   **Asegúrese de que las propiedades son necesarias.** No abarrota las páginas con propiedades innecesarias solo para evitar tomar decisiones de diseño difíciles.
-   **Presente propiedades en términos de los objetivos del usuario, no de la tecnología.** El hecho de que una propiedad configure una tecnología específica no significa que deba presentar la propiedad en términos de esa tecnología.
    -   Si debe presentar la configuración en términos de tecnología (quizás porque los usuarios reconocen el nombre de la tecnología), incluya una breve descripción de cómo se beneficia el usuario de esa configuración.
-   **Presentar propiedades en el nivel de la derecha.** No es necesario presentar valores de bajo nivel individuales en una página de propiedades, por lo que debe presentar las propiedades en un nivel que tenga sentido para los usuarios.
-   **Diseñe páginas de propiedades para tareas específicas.** Determine las tareas que realizarán los usuarios y asegúrese de que hay una ruta de acceso clara para realizar dichas tareas.
-   **Organice las páginas de propiedades** de forma eficaz reduciendo el número de pestañas, decidiendo qué va en una página en función de la Agrupación lógica y la coherencia, y simplificando la presentación de la página.

<!-- -->

-   **Si se recomienda encarecidamente, considere la posibilidad de agregar "(recomendado)" a la etiqueta.**
-   **Proporcione un botón de comando restaurar valores predeterminados para una página de propiedades o toda la ventana de propiedades cuando:**

    -   Es probable que los usuarios tengan en cuenta la configuración compleja y difícil de entender.
    -   Tener una configuración incorrecta puede provocar una interrupción de la funcionalidad, pero los valores predeterminados podrían restaurar la funcionalidad.
    -   Es más fácil que los usuarios vuelvan a empezar cuando el objeto esté mal configurado.

    ![captura de pantalla de la pestaña con el botón Restaurar valores predeterminados ](images/win-property-win-image13.png)

    En este ejemplo, la configuración de Firewall de Windows es compleja y puede dar lugar a una funcionalidad interrumpida. Si hay algún problema, a menudo es más fácil que los usuarios empiecen a hacer clic en restaurar valores predeterminados.

-   Confirme el comando restaurar valores predeterminados si su efecto no es obvio o la configuración es compleja. Indica la confirmación mediante el uso de [puntos suspensivos](ctrl-command-buttons.md).
-   **Cuando sea necesario, mostrar una vista previa de los resultados de una configuración.**

    ![captura de pantalla de ejemplos de puntero de propiedades del mouse ](images/win-property-win-image14.png)

    En este ejemplo, la página muestra una vista previa de los esquemas de puntero. Al hacer clic en aplicar también se muestra una vista previa, tener una vista previa en la página es más eficaz para los usuarios.

    ![captura de pantalla de la vista previa de los resultados de la configuración de fuentes ](images/win-property-win-image15.png)

    En este ejemplo, el cuadro vista previa muestra los resultados de la configuración de la fuente. Este ejemplo muestra que puede obtener una vista previa de la configuración que no es gráfica.

### <a name="help"></a>Ayuda

-   Al proporcionar asistencia al usuario, **considere la posibilidad de usar las siguientes opciones** (en orden de preferencia):
    -   Proporcione a los controles interactivos etiquetas autoexplicativas. Los usuarios tienen más probabilidades de leer las etiquetas en los controles interactivos que cualquier otro texto.
    -   Proporcionar explicaciones en contexto mediante etiquetas de texto estático.
    -   Proporcionar un [vínculo](ctrl-links.md) específico a un tema de ayuda relevante.
-   **Busque vínculos de ayuda en la parte inferior de cada página.** Si una página tiene varios grupos de configuración distintos que tienen un tema de ayuda (quizás dentro de los cuadros de grupo), busque el vínculo de ayuda en la parte inferior del grupo.
-   **No use vínculos a temas de ayuda generales ni imprecisos ni botones de ayuda genérica.** Los usuarios a menudo omiten la ayuda genérica.

Para obtener más información y ejemplos, vea la [ayuda](winenv-help.md)de.

### <a name="standard-users-and-protected-administrators"></a>Usuarios estándar y administradores protegidos

**Muchas opciones requieren privilegios de administrador para cambiar.** Si un proceso requiere privilegios de administrador, Windows y versiones posteriores requieren que [los usuarios estándar](glossary.md) y [los administradores protegidos](glossary.md) eleven sus privilegios explícitamente. Esto ayuda a evitar que se ejecute código malintencionado con privilegios de administrador.

Para obtener más información y ejemplos, vea [control de cuentas de usuario](winenv-uac.md).

### <a name="default-values"></a>Valores predeterminados

-   **La configuración de una ventana de propiedades debe reflejar el estado actual de la aplicación, el objeto o la colección de objetos.** De lo contrario, podría ser engañoso y, posiblemente, provocar resultados no deseados. Por ejemplo, si la configuración refleja las recomendaciones pero no el estado actual, los usuarios pueden hacer clic en Cancelar en lugar de realizar cambios, pensando que no se necesita ningún cambio.
-   **Elija el más seguro (para evitar la pérdida de datos o el acceso al sistema) y el estado inicial más seguro.** Supongamos que la mayoría de los usuarios no cambiarán la configuración.
-   **Si la seguridad y la seguridad no son factores, elija el estado inicial que sea más probable o práctico.**

## <a name="text"></a>Texto

### <a name="commands"></a>Comandos:

-   Para mostrar las opciones del programa, use "opciones".
-   Para mostrar la ventana de propiedades de un objeto, use "propiedades".
-   Para mostrar un resumen de la configuración de personalización de programas utilizada comúnmente, use "[personalizar](glossary.md)".
-   No use "Settings" o "Preferences".
-   No use [puntos suspensivos](ctrl-command-buttons.md) para estos comandos.

### <a name="property-sheet-titles"></a>Títulos de la hoja de propiedades

-   Para un solo objeto, use " \[ propiedades de nombre de objeto \] ".
    -   Si el objeto no tiene nombre, utilice el nombre de tipo del objeto. (Por ejemplo, propiedades de cuenta de usuario).
-   En el caso de varios objetos, use " \[ primer nombre de objeto \] ,... Propiedades ".
    -   Si los objetos no tienen nombres, use el nombre de tipo de los objetos. (Por ejemplo, las propiedades de las cuentas de usuario).
    -   Si los objetos tienen tipos diferentes, use "propiedades de selección".
-   Usar [mayúsculas y minúsculas de estilo de título](glossary.md).
-   No uses puntuación final.
-   No use guiones, como " \[ nombre del objeto \] -propiedades".

### <a name="property-inspector-titles"></a>Títulos del inspector de propiedades

-   Use "propiedades".
-   Usar mayúsculas y minúsculas de estilo de título.
-   No uses puntuación final.

### <a name="options-dialog-box-titles"></a>Cuadro de diálogo Opciones (títulos)

-   Use "opciones".
-   Usar mayúsculas y minúsculas de estilo de título.
-   No uses puntuación final.

### <a name="property-page-tab-names"></a>Nombres de pestañas de página de propiedades

-   **Use etiquetas de pestaña concisas.** Use una o dos palabras que describan claramente el contenido de la página. El uso de nombres de pestañas más largos produce un uso ineficaz del espacio de la pantalla, especialmente cuando los nombres de las pestañas están localizados.
-   **Usar etiquetas de pestaña específicas y significativas.** Evite etiquetas de pestañas genéricas que se puedan aplicar a cualquier pestaña, como general, avanzada o configuración.
-   Escriba la etiqueta como una frase de una o dos palabras y no use ningún signo de puntuación final.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   No asigne una [clave de acceso](glossary.md)única.

### <a name="property-page-text"></a>Texto de la página de propiedades

-   Evite grandes bloques de texto.
-   Proporcione espacio suficiente para que el texto se expanda el 30 por ciento si se va a localizar.
-   No use texto con frase como comando en las ventanas de propiedades. Dado que es posible que los usuarios deseen simplemente ver la configuración, no desea pedirles que cambien la configuración.
-   Usar mayúsculas y minúsculas de estilo oraciones.

## <a name="documentation"></a>Documentación

Al hacer referencia a las ventanas de propiedades:

-   En programación y otra documentación técnica, consulte los cuadros de diálogo Opciones y hojas de propiedades como hojas de propiedades. En todo el mundo, use el cuadro de diálogo, especialmente en la documentación del usuario.
-   Use el texto de título exacto, incluido el uso de mayúsculas.
-   Para describir la interacción del usuario, use abrir y cerrar.
-   Siempre que sea posible, dé formato al título usando texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

Al hacer referencia a las páginas de propiedades:

-   En programación y otra documentación técnica, consulte las páginas de propiedades como páginas de propiedades. En cualquier otro lugar, use la pestaña, especialmente en la documentación del usuario.
-   Use el texto de título exacto, incluido el uso de mayúsculas.
-   Para describir la interacción del usuario, use hacer clic para hacer referencia a hacer clic en una pestaña.
-   Siempre que sea posible, dé formato al nombre con texto en negrita. De lo contrario, ponga el nombre entre comillas solo si es necesario para evitar confusiones.

 

 