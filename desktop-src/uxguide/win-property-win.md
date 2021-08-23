---
title: Propiedades Windows
description: Ventana de propiedades es el nombre colectivo de los siguientes tipos de interfaces de usuario (URI) Hoja de propiedades que se usa para ver y cambiar las propiedades de un objeto o colección de objetos en un cuadro de diálogo. Inspector de propiedades que se usa para ver y cambiar las propiedades de un objeto o colección de objetos en un panel. Cuadro de diálogo Opciones que se usa para ver y cambiar las opciones de una aplicación.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73260459c1dc22ee488233f3c7edebe25203a811a430870fdd4e68e1c2e153ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594425"
---
# <a name="property-windows"></a>Propiedades Windows

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

La ventana de propiedades es el nombre colectivo de los siguientes tipos de interfaces de usuario (URI):

-   Hoja de propiedades: se usa **para ver y cambiar las propiedades de un objeto** o colección de objetos en un cuadro de diálogo .
-   Inspector de propiedad: se usa **para ver y cambiar las propiedades de un objeto** o colección de objetos en un panel .
-   Cuadro de diálogo Opciones: se usa **para ver y cambiar las opciones de una aplicación.**

Una propiedad para un objeto es una de las siguientes:

-   Una configuración que los usuarios pueden cambiar (por ejemplo, el nombre de un archivo y el atributo de solo lectura).
-   Atributo de un objeto que los usuarios no pueden cambiar directamente (como el tamaño de un archivo y la fecha de creación).

A diferencia de los cuadros de diálogo (distintos de los diálogos de opciones) y los asistentes, las ventanas de propiedades normalmente admiten varias tareas en lugar de una sola tarea.

Las ventanas de propiedades normalmente se organizan en páginas, a las que se accede a través de pestañas. Las ventanas de propiedades suelen estar asociadas a pestañas (y viceversa), pero **las pestañas** no son esenciales para las ventanas de propiedades .

![captura de pantalla de la hoja de propiedades de propiedades del documento ](images/win-property-win-image1.png)

Hoja de propiedades típica.

**Nota:** Las directrices relacionadas [con el](vis-layout.md) diseño [y las pestañas](ctrl-tabs.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿El establecimiento de las propiedades requiere que los usuarios realicen una secuencia de pasos fija y no trivial?** Si es así, use un [asistente o](win-wizards.md) un flujo [de tareas en](glossary.md) su lugar.
-   **¿El contenido es solo las opciones de una aplicación?** Si es así, use un cuadro de diálogo de opciones.
-   **¿El contenido es únicamente los atributos de una aplicación?** Si es así, use un [cuadro Acerca de](glossary.md).
-   **¿El contenido es principalmente las propiedades de un objeto (su configuración o atributos)?** Si no es así, use un cuadro [de diálogo estándar o](win-dialog-box.md) un cuadro de diálogo con [pestañas](glossary.md).
-   ¿Es **probable que los usuarios puedan ver o cambiar las propiedades con frecuencia o durante un largo período de tiempo?** Si es así, use un inspector de propiedades; De lo contrario, use una hoja de propiedades.
-   ¿Es **probable que los usuarios puedan ver o cambiar las propiedades de varios objetos diferentes a la vez?** Si es así, use un inspector de propiedades; De lo contrario, use una hoja de propiedades.

**Las hojas de propiedades y los inspectores de propiedades no son exclusivos.** Puede mostrar las propiedades a las que se accede con más frecuencia en un inspector de propiedades y el conjunto completo en la hoja de propiedades.

## <a name="design-concepts"></a>Conceptos de diseño

**Las ventanas de propiedades a menudo se convierten en un terreno de volcado para una variedad impar de configuraciones basadas en tecnología de bajo nivel.** Con demasiada frecuencia, estas propiedades se organizan en pestañas, pero más allá de eso no están diseñadas para tareas o usuarios concretos. Como resultado, cuando los usuarios se enfrentan a una tarea en una ventana de propiedades, a menudo no saben qué hacer.

Para asegurarse de que las ventanas de propiedades son útiles y utilizables, siga estos pasos:

-   Asegúrese de que las propiedades son necesarias.
-   Presentar propiedades en términos de objetivos de usuario, no de tecnología.
-   Presentar propiedades en el nivel correcto.
-   Páginas de diseño para tareas específicas.
-   Diseñar páginas para usuarios específicos, especialmente usuarios limitados (no administradores).
-   Organice las páginas de propiedades de forma eficaz.

**Si solo hace una cosa...**

Presentar propiedades en términos de objetivos de usuario, no de tecnología. Finge que estás explicando la propiedad y por qué es útil para un amigo. ¿Cómo lo explicaría? ¿Qué lenguaje usaría? Este es el lenguaje que se va a usar en las páginas de propiedades.

## <a name="usage-patterns"></a>Patrones de uso

Las ventanas de propiedades tienen varios patrones de uso.

-   Hojas de propiedades. Las propiedades de un solo objeto se muestran en un cuadro de diálogo modeless.
-   Hojas de propiedades de varios objetos. Las propiedades de varios objetos se muestran en un cuadro de diálogo no modelo.
-   Hojas de propiedades de configuración efectivas. Las propiedades efectivas de un único objeto se muestran en un cuadro de diálogo modeless.
-   Cuadros de diálogo Opciones. Las propiedades de una aplicación se muestran en un cuadro de diálogo modal.
-   Inspectores de propiedad. Las propiedades de la selección actual (un único objeto o grupo de objetos) se muestran en un panel de ventana modelada o una ventana desacoplada.

Todos los patrones de ventana de propiedades, excepto los inspectores de propiedad, usan una confirmación retrasada, lo que significa que los cambios solo tienen efecto cuando los usuarios hacen clic en Aceptar o Aplicar. Los inspectores de propiedades usan una confirmación inmediata (las propiedades se cambian en cuanto los usuarios hacen cambios), por lo que no es necesario usar los botones Aceptar, Cancelar y Aplicar.

## <a name="guidelines"></a>Directrices

### <a name="property-sheets"></a>Hojas de propiedades

-   **Mostrar una hoja de propiedades cuando los usuarios:**
    -   Seleccione el comando Propiedades de un objeto.
    -   Establezca el foco de entrada en un objeto y presione Alt+Entrar.

**Hojas de propiedades de varios objetos**

-   **Muestra las propiedades comunes de todos los objetos seleccionados.** Donde los valores de propiedad difieren, muestre los controles asociados a esos valores mediante un estado mixto. (Consulte las directrices de control correspondientes para usar valores de estado mixto).
-   Si el objeto seleccionado es una colección de varios objetos discretos (como una carpeta de archivos), muestre las propiedades del objeto agrupado único en lugar de una hoja de propiedades de varios objetos para los objetos **discretos.**

### <a name="options-dialog-boxes"></a>Cuadros de diálogo Opciones

-   **No separe las opciones de la personalización.** Es decir, no tiene un comando Opciones y un comando Personalizar. Esta separación suele confundir a los usuarios. En su lugar, acceda a la personalización a través de opciones.

### <a name="property-pages"></a>páginas de propiedades

-   **Siga estas directrices para el orden de página:**
    -   Haga que la página General o su equivalente sea la primera página.
    -   Haga que la página Avanzadas o su equivalente sea la última página.
    -   Para las páginas restantes:
        -   Organizarlos en grupos de páginas relacionadas.
        -   Ordenar los grupos según la probabilidad de su uso.
        -   Dentro de cada grupo, ordene las páginas por sus relaciones o por la probabilidad de su uso.
        -   No debería tener tantas páginas que sea necesario mostrarlas en orden alfabético.
-   **Haga que las páginas sea coherentes al relacionar todas las propiedades de cada página con un propósito único, específico y basado en tareas.**
-   **Si el espacio lo permite, explique el propósito de la ventana de propiedades en la parte superior de la página si no es obvio para los usuarios de destino.** Si la página se usa para realizar solo una tarea, frasee el texto como una **instrucción clara sobre cómo realizar esa tarea**. Use oraciones completas que terminen con un punto.

    ![captura de pantalla de la hoja de propiedades de propiedades del firewall ](images/win-property-win-image2.png)

    En este ejemplo, el propósito de Microsoft Windows Firewall se explica en la parte superior de la página General.

-   **Hacer que el contenido similar sea coherente entre páginas mediante ubicaciones y nombres de control coherentes.** Por ejemplo, si varias páginas tienen cuadros Nombre, intente colocarlas en la misma ubicación de la página y use etiquetas coherentes. El contenido similar no debe saltar de una página a otra.
-   **Coloque la misma propiedad en la misma página en toda la aplicación.** Por ejemplo, no coloque una propiedad Expiration en la pestaña General para un tipo de objeto y en la pestaña Avanzadas para otro tipo.
-   **Si es probable que los usuarios comiencen con la última página mostrada, haga que la pestaña de la página se conserve y selecciónelo de forma predeterminada.** Haga que la configuración se conserve en una ventana por propiedad y por usuario. De lo contrario, seleccione la primera página de forma predeterminada.
-   **No haga que la configuración de una página dependa de la configuración de otras páginas.** En su lugar, coloque la configuración dependiente en una sola página. El cambio de una configuración en una página nunca debe cambiar automáticamente la configuración en otras páginas.
    -   **Excepción:** Si la configuración dependiente se encuentra en dos ventanas de propiedades diferentes, use etiquetas de texto estático para explicar esta relación en ambas ubicaciones.
-   **No desplácese por las páginas de propiedades.** Tanto las pestañas como las barras de desplazamiento se usan para aumentar el área efectiva de una ventana, pero un mecanismo debe ser suficiente. En lugar de usar barras de desplazamiento, haga que las páginas de propiedades sea más grande y desplace las páginas de forma eficaz.

**Primeras páginas**

-   Para las propiedades del **objeto, coloque el nombre del objeto en la primera página.**
-   Si va a asociar [](vis-icons.md) iconos (opcionales) a los objetos, muestre el icono adecuado en la esquina superior **izquierda** de la primera página.

**Páginas generales**

-   **Evite las páginas generales.** No es necesario tener una página General. Use una página General solo si:
    -   Las propiedades se aplican a varias tareas y son significativas para la mayoría de los usuarios. No coloque propiedades especializadas o avanzadas en una página General, pero puede hacer que se pueda acceder a ellas a través de un botón de comando de la página General.
    -   Las propiedades no se ajustan a una categoría más específica. Si lo hacen, use ese nombre para la página en su lugar.

**Páginas avanzadas**

-   **Evite las páginas avanzadas.** Use una página Avanzada solo si:
    -   Las propiedades se aplican a tareas poco frecuentes y son significativas principalmente para los usuarios avanzados.
    -   Las propiedades no se ajustan a una categoría más específica. Si lo hacen, use ese nombre para la página en su lugar.
-   **No llame a propiedades avanzadas basadas únicamente en medidas tecnológicas.** Por ejemplo, una opción de estapling de impresora puede ser una característica de impresora avanzada, pero es significativa para todos los usuarios, por lo que no debe estar en una página Avanzada.

### <a name="owned-property-windows"></a>Ventanas de propiedades de propiedad

-   **No muestre más de una ventana de propiedades de propiedad desde una ventana de propiedades.** Mostrar más de uno hace que el significado de los botones Aceptar y Cancelar sea difícil de entender. Puede mostrar otros tipos de cuadros de diálogo auxiliares (como selectores de objetos) según sea necesario.

    **Incorrecto:**

    ![captura de pantalla de tres ventanas de propiedad ](images/win-property-win-image3.png)

    En este ejemplo, el cuadro de diálogo opciones de propietario tiene tres niveles de ventanas de propiedades de propiedad. Como resultado, los significados de Ok y Cancel son confusos.

-   Para las ventanas de propiedades que usan un modelo de confirmación retrasada, asegúrese de que los usuarios pueden cancelar los cambios realizados en una ventana de propiedades de propiedad haciendo clic en Cancelar en **la ventana del propietario.**
-   Si una ventana de propiedades de propiedad requiere una confirmación inmediata, indique que los cambios se confirmaron al cambiar el nombre del botón Cancelar de la **ventana de propietario a Cerrar.** Revierta el botón a Cancelar si el usuario hace clic en Aplicar.

    ![captura de pantalla de la ventana de propiedades con ok y close ](images/win-property-win-image4.png)

    En este ejemplo, los cambios en los diccionarios personalizados y la configuración de gramática no se pueden cancelar. Puede proporcionar a los usuarios estos comentarios cambiando Cancelar a Cerrar.

**Otras ventanas de propiedad**

-   Si se usa una ventana de propiedad para realizar una tarea auxiliar, **no cambie el nombre del botón Cancelar.** Las instrucciones anteriores solo se aplican a las ventanas de propiedades de propiedad, no a los cuadros de diálogo usados para realizar tareas auxiliares.

    ![captura de pantalla de la ventana de propietario y limpieza del disco ](images/win-property-win-image5.png)

    En este ejemplo, Limpieza de disco es una tarea auxiliar, por lo que no se aplican las directrices anteriores. Por ejemplo, el botón Cancelar de la ventana del propietario no debe cambiarse a Cerrar.

-   Si la ventana de propiedad se usa para realizar una tarea auxiliar, no cierre la ventana de propiedades del propietario cuando se haga clic en **el botón de comando.** Si lo hace, se desorienta y se supone que la única razón por la que el usuario ha mostrado la ventana de propiedades era para realizar ese comando.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo opciones ](images/win-property-win-image6.png)

    En este ejemplo, al hacer clic **en Proteger documento** se cierra incorrectamente el cuadro de diálogo Opciones.

### <a name="tabs"></a>Pestañas

-   **Use etiquetas de tabulación concisas.** Use una o dos palabras que describan claramente el contenido de la página. Las etiquetas más largas resultan en un uso ineficaz del espacio de pantalla, especialmente cuando se localizan las etiquetas.
-   **Use etiquetas de tabulación específicas y significativas.** Evite etiquetas de pestaña genéricas que se puedan aplicar a cualquier pestaña, como General, Avanzado o Configuración.
-   **Use pestañas horizontales si:**
    -   La ventana de propiedades tiene siete o menos pestañas (incluidas las extensiones de terceros).
    -   **Todas las pestañas caben en una fila, incluso cuando la interfaz de usuario está localizada.**
    -   Las pestañas horizontales se usan en las demás ventanas de propiedades de la aplicación.
-   **Use pestañas verticales si:**

    -   La ventana de propiedades tiene ocho o más pestañas (incluidas las extensiones de terceros).
    -   **El uso de pestañas horizontales requeriría más de una fila.**
    -   Las pestañas verticales se usan en las demás ventanas de propiedades de la aplicación.

    ![captura de pantalla de la ventana de propiedades con pestañas verticales ](images/win-property-win-image7.png)

    En este ejemplo, las pestañas verticales se usan para dar cabida a ocho o más pestañas.

-   **Para los inspectores** de propiedades, para ahorrar espacio, considere la posibilidad de usar una lista desplegable en lugar de pestañas, especialmente si el usuario rara vez cambia la pestaña actual.
-   Si una pestaña no se aplica al contexto actual y los usuarios no lo **esperan, quite la pestaña.** Esto simplifica la interfaz de usuario y los usuarios no la perderán.

    **Incorrecto:**

    ![captura de pantalla de la pestaña ubicaciones de archivos atenuadas ](images/win-property-win-image8.png)

    En este ejemplo, la pestaña Ubicaciones de archivo está deshabilitada incorrectamente cuando Microsoft Word 2003 se usa como editor de correo electrónico. La página debe quitarse porque los usuarios no esperarán ver ni cambiar las ubicaciones de los archivos en este contexto.

-   **Si una pestaña no se aplica al contexto actual y es posible que los usuarios lo esperen:**

    -   **Muestra la pestaña .**
    -   **Deshabilite los controles de la página.**
    -   **Incluya texto que explique por qué se deshabilitan los controles.**

    No deshabilite la pestaña porque no se explica por sí mismo y prohíbe la exploración. Además, los usuarios que buscan una propiedad específica se verían obligados a buscar en todas las demás pestañas.

    ![captura de pantalla de los controles de vista atenuada ](images/win-property-win-image9.png)

    En este ejemplo de Word 2003, ninguna de las opciones De vista se aplica en Diseño de lectura. Sin embargo, es posible que los usuarios esperen que se apliquen en función de la etiqueta de pestaña, por lo que se muestra la página pero las opciones están deshabilitadas.

-   **No asigne efectos a las pestañas cambiantes.** Cambiar la pestaña actual nunca debe tener efectos secundarios, aplicar la configuración o generar un mensaje de error.
-   **No anidar pestañas ni combinar pestañas horizontales con pestañas verticales.** En su lugar, reduzca el número de pestañas, use solo pestañas verticales o use otro control, como una lista desplegable.
-   **No use pestañas si una ventana de propiedades solo tiene una sola pestaña y no es extensible.** Use un cuadro de diálogo normal con Aceptar, Cancelar y un botón Aplicar opcional en su lugar. Las ventanas de propiedades extensibles (que pueden ser extendidas por terceros) siempre deben usar pestañas.
-   **No coloque iconos en las pestañas.** Normalmente, los iconos agregan desorden visual innecesario, consumen espacio en la pantalla y, a menudo, no mejoran la comprensión del usuario. Agregue solo iconos que ayudan en la comprensión, como los símbolos estándar.

    **Incorrecto:**

    ![captura de pantalla de etiquetas de tabulación con iconos ](images/win-property-win-image10.png)

    En este ejemplo, los gráficos agregan desorden visual innecesario y hacen poco para mejorar la comprensión del usuario.

-   **No use logotipos de producto para gráficos de tabulación.** Las pestañas no son para personal de marca.
-   **No desplácese por pestañas horizontales.** El desplazamiento horizontal no se puede detectar fácilmente. Sin embargo, puede desplazarse por las pestañas verticales.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta de pestaña horizontal truncada ](images/win-property-win-image11.png)

    En este ejemplo, se desplazan las pestañas horizontales.

### <a name="command-buttons"></a>Botones de comando

-   **Coloque los botones de comando que se aplican a todas las páginas de propiedades en la parte inferior de la ventana de propiedades.** Alinee a la derecha los botones y use este orden (de izquierda a derecha): Aceptar, Cancelar y Aplicar.
-   **Coloque los botones de comando que solo se aplican a páginas de propiedades individuales directamente en la página de propiedades.**

### <a name="commit-buttons"></a>Botones de confirmación

**Botones aceptar**

-   **Para las ventanas de propiedades de propietario, el botón Aceptar significa aplicar los cambios pendientes (realizados desde que se abrió la ventana o la última aplicación) y cerrar la ventana.**
-   **Para las ventanas de propiedades de propiedad, el botón Aceptar significa mantener los cambios, cerrar la ventana y aplicar los cambios cuando se aplican los cambios de la ventana de propietario.**
-   **No cambie el nombre del botón Aceptar.** A diferencia de otros cuadros de diálogo, las ventanas de propiedades no se usan para realizar ninguna tarea específica. Si tiene sentido cambiar el nombre del botón Aceptar (por ejemplo, a Imprimir), la ventana no es una ventana de propiedades.
-   **No asigne una clave de acceso.**

**Botones cancelar**

-   **El botón Cancelar significa descartar todos los cambios pendientes (realizados desde que se abrió la ventana o la última vez que se apliquen) y cerrar la ventana.**
-   **Si no se pueden abandonar todos los cambios pendientes, cambie el nombre del botón Cancelar a Cerrar.** Al hacer clic en Cancelar, debe abandonar todos los cambios pendientes.
-   **Si la ventana de propiedades de propiedad requiere una confirmación inmediata, cambie el nombre del botón Cancelar de la ventana de propietario a Cerrar para mostrar que se confirmaron los cambios.**
-   **No asigne una clave de acceso.**

**Aplicar botones**

-   **Para las hojas de propiedades de propietario, el botón Aplicar significa aplicar los cambios pendientes (realizados desde que se abrió la ventana o la última aplicación), pero dejar la ventana abierta.** Esto permite a los usuarios evaluar los cambios antes de cerrar la hoja de propiedades.
-   **En el caso de las hojas de propiedades de propiedad, no use .** El uso de un botón Aplicar en una hoja de propiedades de propiedad hace que el significado de los botones de confirmación en la hoja de propiedades del propietario sea difícil de entender.
-   **Proporcione un botón Aplicar solo si la hoja de propiedades tiene valores (al menos uno) con efectos que los usuarios pueden evaluar de forma significativa.** Normalmente, los botones Aplicar se usan cuando la configuración realiza cambios visibles. Los usuarios deben poder aplicar un cambio, evaluarlo y realizar más cambios en función de esa evaluación. Si no es así, quite el botón Aplicar en lugar de deshabilitarlo.

    **Incorrecto:**

    ![captura de pantalla de las propiedades del sistema con el botón Aplicar ](images/win-property-win-image12.png)

    En este ejemplo, ninguna de las propiedades del sistema tiene un efecto visual, por lo que el botón Aplicar no tiene ningún valor y debe quitarse.

-   **Coloque toda la configuración que los usuarios puedan querer aplicar en las páginas de propietario.** No use los botones Aplicar en hojas de propiedades propias, ya que hacerlo es confuso.
-   **Use Aplicar botones solo con hojas de propiedades, no con cuadros de diálogo de opciones.**
-   **Habilite el botón Aplicar solo cuando haya cambios pendientes**; de lo contrario, deshabilite .
-   **Asigne "A" como clave de acceso.**

**Botones cerrar**

-   **Si no se pueden abandonar todos los cambios pendientes, cambie el nombre del botón Cancelar a Cerrar.** Al hacer clic en Cancelar, debe abandonar todos los cambios pendientes.
-   **No confirme si los usuarios descartan sus cambios.**
    -   **Excepción:** Si la ventana de propiedades tiene una configuración que requiere un esfuerzo [](mess-confirm.md) considerable para establecer y el usuario ha realizado cambios, puede mostrar una confirmación si el usuario hace clic en el botón Cerrar de la barra de título. El motivo es que algunos usuarios asumen erróneamente que el botón Cerrar de la barra de título tiene el mismo efecto que el botón Aceptar.
-   **A excepción del mensaje de confirmación, asegúrese de que el botón Cerrar de la barra de título tiene el mismo efecto que Cancelar o Cerrar.**

### <a name="page-contents"></a>Contenido de la página

-   **Asegúrese de que las propiedades son necesarias.** No abarrote las páginas con propiedades innecesarias solo para evitar tomar decisiones de diseño duro.
-   **Presentar propiedades en términos de objetivos de usuario, no de tecnología.** El hecho de que una propiedad configure una tecnología específica no significa que deba presentar la propiedad en términos de esa tecnología.
    -   Si debe presentar la configuración en términos de tecnología (quizás porque los usuarios reconocen el nombre de la tecnología), incluya una breve descripción de cómo se beneficia el usuario de esa configuración.
-   **Presentar propiedades en el nivel correcto.** No es necesario presentar valores individuales de bajo nivel en una página de propiedades, por lo que debe presentar las propiedades en un nivel que tenga sentido para los usuarios.
-   **Diseñar páginas de propiedades para tareas específicas.** Determine las tareas que realizarán los usuarios y asegúrese de que hay una ruta de acceso clara para realizar esas tareas.
-   **Organice las** páginas de propiedades de forma eficaz mediante la reducción del número de pestañas, la decisión de lo que sucede en una página en función de la agrupación lógica y la coherencia, y la simplificación de la presentación de la página.

<!-- -->

-   **Si se recomienda encarecidamente una opción, considere la posibilidad de agregar "(recommended)" a la etiqueta.**
-   **Proporcione un botón de comando Restaurar valores predeterminados para una página de propiedades o toda la ventana de propiedades cuando:**

    -   Es probable que los usuarios consideren la configuración compleja y difícil de entender.
    -   Tener una configuración incorrecta puede dar lugar a una funcionalidad de última hora, pero los valores predeterminados pueden restaurar la funcionalidad.
    -   Es más fácil que los usuarios empiecen de nuevo cuando el objeto está mal configurado.

    ![captura de pantalla de la pestaña con el botón restaurar valores predeterminados ](images/win-property-win-image13.png)

    En este ejemplo, la configuración Windows firewall es compleja y puede dar lugar a una funcionalidad rota. Si hay un problema, a menudo es más fácil que los usuarios empiecen de nuevo haciendo clic en Restaurar valores predeterminados.

-   Confirme el comando Restaurar valores predeterminados si su efecto no es obvio o la configuración es compleja. Indique la confirmación mediante el uso de [puntos suspensivos](ctrl-command-buttons.md).
-   **Cuando corresponda, muestre una vista previa de los resultados de una configuración.**

    ![captura de pantalla de ejemplos de puntero de propiedades del mouse ](images/win-property-win-image14.png)

    En este ejemplo, la página muestra una vista previa de los esquemas de puntero. Al hacer clic en Aplicar también se muestra una vista previa, tener una vista previa en la página es más eficaz para los usuarios.

    ![captura de pantalla de la vista previa de los resultados de la configuración de fuente ](images/win-property-win-image15.png)

    En este ejemplo, el cuadro Vista previa muestra los resultados de la configuración de fuente. En este ejemplo se muestra que puede obtener una vista previa de la configuración que no es gráfica.

### <a name="help"></a>Ayuda

-   Al proporcionar asistencia al usuario, **considere la posibilidad de usar las siguientes opciones** (enumeradas en su orden de preferencia):
    -   Dé etiquetas autoexplicativas a los controles interactivos. Es más probable que los usuarios lean las etiquetas en controles interactivos que cualquier otro texto.
    -   Proporcione explicaciones en contexto mediante etiquetas de texto estático.
    -   Proporcione un vínculo [específico a](ctrl-links.md) un tema de Ayuda pertinente.
-   **Busque vínculos de Ayuda en la parte inferior de cada página.** Si una página tiene varios grupos distintos de configuraciones que tienen un tema de Ayuda (quizás dentro de cuadros de grupo), busque el vínculo Ayuda en la parte inferior del grupo.
-   **No use vínculos generales o imprecisos de temas de Ayuda ni botones genéricos de Ayuda.** A menudo, los usuarios omiten la Ayuda genérica.

Para obtener más información y ejemplos, vea [Ayuda](winenv-help.md).

### <a name="standard-users-and-protected-administrators"></a>Usuarios estándar y administradores protegidos

**Muchas configuraciones requieren privilegios de administrador para cambiar.** Si un proceso requiere privilegios de administrador, Windows [](glossary.md) y versiones posteriores requieren que los usuarios estándar y los administradores protegidos eleve sus privilegios explícitamente. [](glossary.md) Esto ayuda a evitar que el código malintencionado se ejecute con privilegios de administrador.

Para obtener más información y ejemplos, vea [Control de cuentas de usuario](winenv-uac.md).

### <a name="default-values"></a>Valores predeterminados

-   **La configuración dentro de una ventana de propiedades debe reflejar el estado actual de la aplicación, el objeto o la colección de objetos.** De lo contrario, sería engañoso y posiblemente provocaría resultados no deseados. Por ejemplo, si la configuración refleja las recomendaciones, pero no el estado actual, los usuarios pueden hacer clic en Cancelar en lugar de realizar cambios, pensando que no se necesitan cambios.
-   **Elija el estado inicial más seguro (para evitar la pérdida de datos o el acceso al sistema) y el estado inicial más seguro.** Suponga que la mayoría de los usuarios no cambiarán la configuración.
-   **Si la seguridad y la seguridad no son factores, elija el estado inicial más probable o conveniente.**

## <a name="text"></a>Texto

### <a name="commands"></a>Comandos

-   Para mostrar las opciones del programa, use "Opciones".
-   Para mostrar la ventana de propiedades de un objeto, use "Propiedades".
-   Para mostrar un resumen de la configuración de personalización del programa que se usa habitualmente, use["Personalizar".](glossary.md)
-   No use "Configuración" ni "Preferencias".
-   No use [puntos suspensivos](ctrl-command-buttons.md) para estos comandos.

### <a name="property-sheet-titles"></a>Títulos de la hoja de propiedades

-   Para un solo objeto, use \[ "Propiedades de nombre \] de objeto".
    -   Si el objeto no tiene ningún nombre, use el nombre de tipo del objeto. (Por ejemplo, Propiedades de la cuenta de usuario).
-   Para varios objetos, use " \[ first object name , \] ... Propiedades".
    -   Si los objetos no tienen nombres, use el nombre de tipo de los objetos. (Por ejemplo, Propiedades de cuentas de usuario).
    -   Si los objetos tienen tipos diferentes, use "Propiedades de selección".
-   Use [el uso de mayúsculas de estilo de título.](glossary.md)
-   No uses puntuación final.
-   No use guiones, como \[ "nombre de \] objeto- Propiedades".

### <a name="property-inspector-titles"></a>Títulos del inspector de propiedad

-   Use "Propiedades".
-   Use mayúsculas de estilo de título.
-   No uses puntuación final.

### <a name="options-dialog-box-titles"></a>Títulos del cuadro de diálogo Opciones

-   Use "Opciones".
-   Use mayúsculas de estilo de título.
-   No uses puntuación final.

### <a name="property-page-tab-names"></a>Nombres de pestañas de página de propiedades

-   **Use etiquetas de tabulación concisas.** Use una o dos palabras que describan claramente el contenido de la página. El uso de nombres de tabulación más largos da como resultado un uso ineficaz del espacio de pantalla, especialmente cuando se localizan los nombres de las pestañas.
-   **Use etiquetas de tabulación específicas y significativas.** Evite etiquetas de pestaña genéricas que se puedan aplicar a cualquier pestaña, como General, Avanzado o Configuración.
-   Escriba la etiqueta como una frase de una o dos palabras y no use ningún signo de puntuación final.
-   Use [mayúsculas de estilo oración.](glossary.md)
-   No asigne una clave de [acceso única.](glossary.md)

### <a name="property-page-text"></a>Texto de la página de propiedades

-   Evite grandes bloques de texto.
-   Proporcione espacio suficiente para que el texto se expanda un 30 por ciento si se localizará.
-   No use texto con frases como comando en las ventanas de propiedades. Dado que es posible que los usuarios simplemente quieran ver la configuración, no desea solicitarles que cambien la configuración.
-   Use mayúsculas de estilo oración y signos de puntuación finales.

## <a name="documentation"></a>Documentación

Al hacer referencia a las ventanas de propiedades:

-   En programación y otra documentación técnica, consulte hojas de propiedades y cuadros de diálogo de opciones como hojas de propiedades. En cualquier otro lugar, use el cuadro de diálogo, especialmente en la documentación del usuario.
-   Use el texto del título exacto, incluida su mayúscula.
-   Para describir la interacción del usuario, use Abrir y cerrar.
-   Cuando sea posible, formatee el título con texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

Al hacer referencia a páginas de propiedades:

-   En programación y otra documentación técnica, consulte las páginas de propiedades como páginas de propiedades. En cualquier otro lugar, use la pestaña, especialmente en la documentación del usuario.
-   Use el texto del título exacto, incluida su mayúscula.
-   Para describir la interacción del usuario, use haga clic para hacer referencia a hacer clic en una pestaña.
-   Cuando sea posible, formatee el nombre con texto en negrita. De lo contrario, coloque el nombre entre comillas solo si es necesario para evitar confusiones.

 

 