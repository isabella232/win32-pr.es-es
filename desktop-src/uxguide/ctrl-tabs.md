---
title: Tabulaciones
description: Las pestañas proporcionan una manera de presentar información relacionada en páginas etiquetadas independientes.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b2649862885e55bdfe10fdca7f34b7618d976a38
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554873"
---
# <a name="tabs"></a>Tabulaciones

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Las pestañas proporcionan una manera de presentar información relacionada en páginas etiquetadas independientes.

![captura de pantalla de cinco pestañas ](images/ctrl-tabs-image1.png)

Conjunto típico de pestañas.

Las pestañas suelen estar asociadas con ventanas de propiedades (y viceversa), pero las pestañas se pueden usar en cualquier tipo de ventana.

Los controles de ficha representan las carpetas de Manila con pestañas que se usan para organizar información en los contenedores de archivos que se encuentran normalmente en el Estados Unidos. (Las carpetas de Manila no se usan en todo el mundo).

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md), los [menús de ficha](cmd-menus.md), los [cuadros de diálogo](win-dialog-box.md)y las ventanas de [propiedades](win-property-win.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Pueden ajustarse los controles de manera cómoda en una sola página de tamaño razonable?** Si es así, use una sola página.
-   **¿Hay solo una pestaña?** Si es así, use una sola página.
-   **¿Las pestañas se relacionan entre sí de alguna manera obvia?** Si no es así, considere la posibilidad de dividir la información en ventanas independientes de información relacionada.
-   **Si se usa para la configuración, ¿son completamente independientes las configuraciones de páginas diferentes?** ¿Se va a cambiar una configuración en una página que afecta a la configuración de otras páginas? Si no son independientes, utilice en su lugar páginas de tareas o un [Asistente](win-wizards.md) .
-   **¿Son las pestañas principalmente del mismo nivel o hay una relación jerárquica?** Si es jerárquico, considere la posibilidad de usar los [cuadros de diálogo](win-dialog-box.md) secundarios o de divulgación progresiva para mostrar información relacionada.
-   **¿Se usan las pestañas para mostrar los pasos dentro de una tarea?** Puede usar "pestañas" para mostrar los pasos dentro de una tarea solo si se presentan como pasos, y hay una manera obvia y alternativa de llegar al paso de texto, como un botón siguiente. En caso contrario, si se requieren los pasos, utilice las páginas de un flujo de páginas o un [Asistente](win-wizards.md). Si los pasos son opcionales, muestre los pasos opcionales mediante los [cuadros de diálogo](win-dialog-box.md) modales.
-   **¿Las pestañas son vistas diferentes de los mismos datos?** Si es así, considere la posibilidad de usar un [botón de expansión](ctrl-command-buttons.md) o una [lista](/windows/desktop/uxguide/ctrl-drop) desplegable para cambiar las vistas. Aunque las pestañas se pueden usar de forma eficaz para cambiar las vistas, las alternativas son más ligeras.

## <a name="usage-patterns"></a>Patrones de uso

Las pestañas tienen varios patrones de uso:



|                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Superficie de ventana dinámica**<br/> al igual que las barras de desplazamiento, las pestañas se pueden usar para aumentar el área de la superficie de la ventana para mostrar información relacionada.<br/>                                                    | Con este patrón, el uso de pestañas es conceptualmente similar a colocar toda la información en las pestañas linealmente en una sola superficie desplazable, con las etiquetas de pestaña como encabezados. <br/> ![captura de pantalla de cinco pestañas ](images/ctrl-tabs-image1.png)<br/> En este ejemplo, las pestañas aumentan de forma eficaz el área de la superficie de la ventana.<br/>                          |
| **Varias vistas**<br/> al igual que los botones de expansión o las listas desplegables, las pestañas se pueden usar para mostrar vistas diferentes de la misma información o de la misma información relacionada. <br/>                                           | ![captura de pantalla de las pestañas diseño, división y vista previa ](images/ctrl-tabs-image2.png)<br/> En este ejemplo, las pestañas cambian las vistas dentro de un documento.<br/>                                                                                                                                                                                                         |
| **Varios documentos**<br/> al igual que varias ventanas, las pestañas se pueden usar para mostrar distintos documentos en una sola ventana. <br/>                                                                   | ![captura de pantalla de tres pestañas para documentos diferentes ](images/ctrl-tabs-image3.png)<br/> ![figura de pestañas para diferentes meses ](images/ctrl-tabs-image4.png)<br/> En estos ejemplos, las pestañas muestran documentos diferentes en una sola ventana de la aplicación.<br/>                                                                                       |
| **Opciones exclusivas**<br/> al igual que los botones de radio, las pestañas se pueden usar para presentar varias opciones exclusivas. en este patrón, solo se aplica la pestaña seleccionada y se omiten todas las demás pestañas. <br/> | ![captura de pantalla de las pestañas ubicación, datos y mensajes ](images/ctrl-tabs-image5.png)<br/> En este ejemplo, las pestañas se usan (incorrectamente) como sustituto de los botones de radio.<br/> **No se recomienda este patrón** porque utiliza un comportamiento no estándar. Las pestañas se comportan como un valor de configuración en lugar de una manera de navegar dentro de la ventana. <br/> |



 

**Si solo hace algo...**

Asegúrese de que la información de las pestañas esté relacionada y de que la configuración de páginas diferentes sea independiente. La última pestaña seleccionada no debe tener ningún significado especial.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Use las pestañas horizontales si:**
    -   La ventana tiene siete o menos pestañas.
    -   **Todas las pestañas se ajustan a una fila, incluso cuando se localiza la interfaz de usuario (UI).**
-   **Use las pestañas verticales si:**
    -   La ventana de propiedades tiene ocho o más pestañas.
    -   **El uso de pestañas horizontales requeriría más de una fila.**

        ![captura de pantalla de la ventana de propiedades con once opciones ](images/ctrl-tabs-image6.png)

        En este ejemplo, las pestañas verticales admiten ocho o más pestañas.

-   **No anide tabulaciones ni combina tabulaciones horizontales con pestañas verticales.** En su lugar, reduzca el número de pestañas, use solo pestañas verticales o use otro control, como una lista desplegable.
-   **No desplace las tabulaciones horizontales.** El desplazamiento horizontal no es fácilmente reconocible. No obstante, puede desplazarse por las pestañas verticales.

    **Incorrecto:**

    ![captura de pantalla de etiqueta de pestaña horizontal truncada ](images/ctrl-tabs-image7.png)

    En este ejemplo, se desplazan las pestañas horizontales.

-   En el caso de las pestañas de una ventana o un panel de tamaño variable, coloque una barra de desplazamiento, cuando sea necesario, en la página, no en la ventana ni en el panel. Las pestañas siempre deben ser visibles y no desplazarse fuera de la vista.

    ![captura de pantalla de la página de pestañas vertical con barra de desplazamiento ](images/ctrl-tabs-image8.png)

    En este ejemplo, la página de ficha tiene la barra de desplazamiento, no el panel.

-   **Asegúrese de que las pestañas se parezcan a las pestañas y no a otro tipo de control.**

    **Incorrecto:**

    ![captura de pantalla de la ventana con botones para pestañas ](images/ctrl-tabs-image9.png)

    En este ejemplo, estas pestañas son similares a los botones de comando.

### <a name="interaction"></a>Interacción

-   **Cuando los controles se aplican solo a una página, colóquelos en el borde de la página con pestañas.**
-   **Cuando los controles se aplican a toda la ventana, colóquelos fuera de la página con pestañas.**
-   **No asigne efectos a las pestañas de cambio.** Las pestañas deben ser accesibles en cualquier orden. Cambiar la pestaña actual nunca debe tener efectos secundarios, aplicar valores de configuración o producir un mensaje de error.
-   **No asigne un significado especial a la última pestaña seleccionada.** La selección de pestañas está desplazada por la selección de la última pestaña del usuario no es una configuración.
-   **No haga que la configuración de una página dependa de la configuración de otras páginas.** En su lugar, coloque cualquier configuración dependiente en la misma página.
-   **Si es probable que los usuarios empiecen con la última pestaña mostrada, haga que la pestaña continúe y selecciónela de forma predeterminada.** Haga que la configuración se mantenga en cada ventana y por usuario. De lo contrario, seleccione la primera página de forma predeterminada.

### <a name="icons"></a>Iconos

-   **No coloque iconos en las pestañas.** Normalmente, los iconos agregan un desorden visual innecesario, consumen espacio de pantalla y no suelen mejorar la comprensión de los usuarios. Agregue solo iconos que ayuden a la comprensión, como los símbolos estándar.

    **Incorrecto:**

    ![captura de pantalla de la ventana con iconos en pestañas ](images/ctrl-tabs-image10.png)

    En este ejemplo, los iconos agregan desorden visual y hacen poco para mejorar la comprensión de los usuarios.

    **Excepción:** Puede usar iconos claramente reconocibles si es posible que no haya espacio suficiente para mostrar etiquetas significativas:

    **Correcto:**

    ![captura de pantalla de pestañas con iconos y etiquetas resumidas ](images/ctrl-tabs-image11.png)

    En este ejemplo, la ventana es tan estrecha que los iconos comunican mejor las pestañas que las etiquetas.

-   **No use logotipos de producto para gráficos de pestañas.** Las pestañas no son para la [Personalización de marca](exper-branding.md).

### <a name="dynamic-window-surface-pattern"></a>Patrón de superficie de ventana dinámica

-   **No use barras de desplazamiento en las páginas de fichas.** Las pestañas funcionan de forma similar a las barras de desplazamiento para aumentar el área efectiva de una ventana. Un mecanismo debe ser suficiente.
-   **Use etiquetas de pestaña concisas.** Use una o dos palabras que describan claramente el contenido de la página. Las etiquetas más largas consumen espacio de pantalla, especialmente cuando se localizan las etiquetas.
-   **Usar etiquetas de pestaña específicas y significativas.** Evite etiquetas de pestañas genéricas que se puedan aplicar a cualquier pestaña, como general, avanzada o configuración.
-   **Si una pestaña no se aplica al contexto actual y los usuarios no la esperan, quítela.** De este modo, se simplifica la interfaz de usuario y los usuarios no la recibirán.

    **Incorrecto:**

    ![captura de pantalla de la ventana de opciones con el nombre de pestaña atenuado ](images/ctrl-tabs-image12.png)

    En este ejemplo, la pestaña ubicaciones de archivo está deshabilitada incorrectamente cuando se usa Microsoft Word como editor de correo electrónico. En lugar de deshabilitar esta pestaña, debe quitarse porque los usuarios no esperan ver o cambiar las ubicaciones de los archivos en este contexto.

-   **Si una pestaña no se aplica al contexto actual y los usuarios podrían esperar que:**

    -   Mostrar la pestaña.
    -   Deshabilite los controles de la página.
    -   Incluye texto que explica por qué los controles están deshabilitados.

    No deshabilite la pestaña, ya que no se explica por sí misma y prohíbe la exploración. Los usuarios que buscan un valor específico se verán obligados a buscar en las demás pestañas.

    ![captura de pantalla de la ventana con las opciones de la pestaña vista atenuadas ](images/ctrl-tabs-image13.png)

    En este ejemplo, no se aplica ninguna de las opciones de vista al diseño de lectura. Sin embargo, los usuarios pueden esperar que se apliquen en función de la etiqueta de la pestaña, por lo que se muestra la página, pero las opciones están deshabilitadas.

### <a name="multiple-views-and-documents-patterns"></a>Varios patrones de vistas y documentos

-   **Use los nombres de vista o documento en las etiquetas de pestaña.**
-   **Evite nombres de pestañas excesivamente largos.** Si es necesario, puede tener un tamaño máximo de nombre o truncar la etiqueta de pestaña mostrada mediante puntos suspensivos. Las etiquetas más largas consumen espacio de pantalla, especialmente cuando se localizan las etiquetas.
-   **Si una pestaña no se aplica al contexto actual, quite la pestaña.**

### <a name="exclusive-options-pattern"></a>Patrón de opciones exclusivas

-   **No utilice este patrón.** En su lugar, use los botones de radio o una lista desplegable.

    **Incorrecto:**

    ![captura de pantalla de la ventana con dos pestañas ' crear ' ](images/ctrl-tabs-image14.png)

    En este ejemplo, las pestañas se usan incorrectamente como sustituto de los botones de radio.

    **Correcto:**

    ![captura de pantalla de la ventana con dos botones de radio ](images/ctrl-tabs-image15.png)

    En este ejemplo, los botones de radio se usan correctamente en su lugar.

## <a name="labels"></a>Etiquetas

-   Etiquete las pestañas según su patrón. Use nombres en lugar de verbos, sin puntuación final. Vea las directrices de patrón anteriores para obtener más información.
-   Use mayúsculas de estilo de frase.
-   No asigne una clave de acceso. Se puede tener acceso a las pestañas a través de sus teclas de método abreviado (Ctrl + Tab, Ctrl + Mayús + Tab, Ctrl + Re Pág, Ctrl + Av Pág). Hay una escasez de opciones de clave de acceso adecuadas, por lo que no asignar teclas de acceso a pestañas facilita su asignación a otros controles.

## <a name="documentation"></a>Documentación

Al hacer referencia a las pestañas:

-   Use el texto de etiqueta exacto, incluido el uso de mayúsculas, e incluya la pestaña palabra.
-   Para describir la interacción del usuario, use haga clic en.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.
-   Dado que varios usos pueden ser ambiguos, especialmente para un público internacional, use la pestaña Sustantivo solo para hacer referencia a un control de ficha. Para otros usos, aclare el significado con un descriptor: la tecla Tab, una tabulación o una marca de tabulación en la regla.

Ejemplo: en el menú **herramientas** , haga clic en **Opciones** y, a continuación, haga clic en la pestaña **Ver** .

