---
title: Pestañas
description: Las pestañas proporcionan una manera de presentar información relacionada en páginas etiquetadas independientes.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d6922865abcaa060cc2e4b13e4768d57bcd17aa8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267452"
---
# <a name="tabs"></a>Pestañas

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Las pestañas proporcionan una manera de presentar información relacionada en páginas etiquetadas independientes.

![captura de pantalla de cinco pestañas ](images/ctrl-tabs-image1.png)

Un conjunto típico de pestañas.

Las pestañas suelen asociarse a ventanas de propiedades (y viceversa), pero las pestañas se pueden usar en cualquier tipo de ventana.

Los controles de pestaña representan las carpetas de pestañas que se usan para organizar la información en los archivadores que se encuentran normalmente en el Estados Unidos. (Las carpetas de Yas no se usan en todo el mundo).

> [!Note]  
> Las instrucciones relacionadas con el [](win-dialog-box.md) [diseño,](vis-layout.md) [los menús de pestañas,](cmd-menus.md)los cuadros de diálogo y las [ventanas de propiedades](win-property-win.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Los controles pueden caber cómodamente en una sola página de tamaño razonable?** Si es así, use una sola página.
-   **¿Solo hay una pestaña?** Si es así, use una sola página.
-   **¿Las pestañas están relacionadas entre sí de alguna manera obvia?** Si no es así, considere la posibilidad de dividir la información en ventanas independientes de información relacionada.
-   **Si se usa para la configuración, ¿la configuración de páginas diferentes es completamente independiente?** ¿El cambio de una configuración en una página afectará a la configuración de otras páginas? Si no son independientes, use páginas de tareas o un [asistente en su](win-wizards.md) lugar.
-   **¿Las pestañas son principalmente pares entre sí o hay una relación jerárquica?** Si es jerárquico, considere la posibilidad de usar la divulgación progresiva o cuadros [de diálogo secundarios](win-dialog-box.md) para mostrar información relacionada.
-   **¿Se usan las pestañas para mostrar los pasos dentro de una tarea?** Puede usar "pestañas" para mostrar los pasos dentro de una tarea solo si se presentan para que se parezcan a los pasos y hay una manera obvia y alternativa de llegar al paso de texto, como un botón Siguiente. De lo contrario, si se requieren los pasos, use páginas en un flujo de página o en un [asistente](win-wizards.md). Si los pasos son opcionales, muestre los pasos opcionales mediante cuadros de [diálogo modales](win-dialog-box.md) en su lugar.
-   **¿Las pestañas son vistas diferentes de los mismos datos?** Si es así, considere la posibilidad de [usar un botón de división](ctrl-command-buttons.md) o una lista desplegable [para](/windows/desktop/uxguide/ctrl-drop) cambiar las vistas. Aunque las pestañas se pueden usar eficazmente para cambiar las vistas, las alternativas son más ligeras.

## <a name="usage-patterns"></a>Patrones de uso

Las pestañas tienen varios patrones de uso:



|  Uso                                                                                                                                                                                                 |    Ejemplo                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Superficie de ventana dinámica**<br/> Al igual que las barras de desplazamiento, las pestañas se pueden usar para aumentar el área de superficie de la ventana para mostrar información relacionada.<br/>                                                    | Con este patrón, el uso de pestañas es conceptualmente similar a colocar toda la información en las pestañas linealmente en una sola superficie desplazable, con las etiquetas de tabulación como encabezados. <br/> ![captura de pantalla de cinco pestañas ](images/ctrl-tabs-image1.png)<br/> En este ejemplo, las pestañas aumentan de forma eficaz el área de superficie de la ventana.<br/>                          |
| **Varias vistas**<br/> Al igual que los botones divididos o las listas desplegables, las pestañas se pueden usar para mostrar diferentes vistas de la misma información o información relacionada. <br/>                                           | ![captura de pantalla de las pestañas de diseño, división y vista previa ](images/ctrl-tabs-image2.png)<br/> En este ejemplo, las pestañas cambian las vistas dentro de un documento.<br/>                                                                                                                                                                                                         |
| **Varios documentos**<br/> Al igual que varias ventanas, las pestañas se pueden usar para mostrar documentos diferentes en una sola ventana. <br/>                                                                   | ![captura de pantalla de tres pestañas para distintos documentos ](images/ctrl-tabs-image3.png)<br/> ![figura de pestañas para distintos meses ](images/ctrl-tabs-image4.png)<br/> En estos ejemplos, las pestañas muestran documentos diferentes dentro de una sola ventana de aplicación.<br/>                                                                                       |
| **Opciones exclusivas**<br/> Al igual que los botones de radio, las pestañas se pueden usar para presentar varias opciones exclusivas. en este patrón, solo se aplica la pestaña seleccionada y se omiten todas las demás pestañas. <br/> | ![captura de pantalla de las pestañas de ubicación, datos y mensajes ](images/ctrl-tabs-image5.png)<br/> En este ejemplo, las pestañas se usan (incorrectamente) como sustituto de los botones de radio.<br/> **Este patrón no se recomienda** porque usa un comportamiento no estándar. Las pestañas se comportan como una configuración en lugar de simplemente una manera de navegar dentro de la ventana. <br/> |



 

**Si solo hace una cosa...**

Asegúrese de que la información de las pestañas está relacionada, pero la configuración de las distintas páginas es independiente. La última pestaña seleccionada no debe tener ningún significado especial.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Use pestañas horizontales si:**
    -   La ventana tiene siete o menos pestañas.
    -   **Todas las pestañas caben en una fila, incluso cuando la interfaz de usuario (UI) está localizada.**
-   **Use pestañas verticales si:**
    -   La ventana de propiedades tiene ocho o más pestañas.
    -   **El uso de pestañas horizontales requeriría más de una fila.**

        ![captura de pantalla de la ventana de propiedades con once opciones ](images/ctrl-tabs-image6.png)

        En este ejemplo, las pestañas verticales admiten ocho o más pestañas.

-   **No anidar pestañas ni combinar pestañas horizontales con pestañas verticales.** En su lugar, reduzca el número de pestañas, use solo pestañas verticales o use otro control, como una lista desplegable.
-   **No desplácese por las pestañas horizontales.** El desplazamiento horizontal no se puede detectar fácilmente. Sin embargo, puede desplazarse por las pestañas verticales.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta de pestaña horizontal truncada ](images/ctrl-tabs-image7.png)

    En este ejemplo, las pestañas horizontales se desplazan.

-   En el caso de las pestañas de una ventana o panel de tamaño ajustable, coloque una barra de desplazamiento, cuando sea necesario, en la página, no en la ventana o el panel. Las pestañas siempre deben estar visibles y no desplazarse fuera de la vista.

    ![captura de pantalla de la página de pestaña vertical con barra de desplazamiento ](images/ctrl-tabs-image8.png)

    En este ejemplo, la página de pestañas tiene la barra de desplazamiento, no el panel.

-   **Asegúrese de que las pestañas se parezcan a las pestañas y no a otro tipo de control.**

    **Incorrecto:**

    ![captura de pantalla de la ventana con botones para pestañas ](images/ctrl-tabs-image9.png)

    En este ejemplo, estas pestañas son como botones de comando.

### <a name="interaction"></a>Interacción

-   **Cuando los controles se aplican solo a una página, colócanlos dentro del borde de la página con pestañas.**
-   **Cuando los controles se apliquen a toda la ventana, colócanlos fuera de la página con pestañas.**
-   **No asigne efectos a las pestañas cambiantes.** Las pestañas deben ser accesibles en cualquier orden. Cambiar la pestaña actual nunca debe tener efectos secundarios, aplicar la configuración o generar un mensaje de error.
-   **No asigne un significado especial a la última pestaña seleccionada.** La selección de pestañas es para la navegación la última selección de pestañas del usuario no es una configuración.
-   **No haga que la configuración de una página dependa de la configuración de otras páginas.** En su lugar, coloque cualquier configuración dependiente en la misma página.
-   **Si es probable que los usuarios comiencen con la última pestaña mostrada, haga que la pestaña persista y selecciónelo de forma predeterminada.** Haga que la configuración se conserve por ventana y por usuario. De lo contrario, seleccione la primera página de forma predeterminada.

### <a name="icons"></a>Iconos

-   **No coloque iconos en las pestañas.** Normalmente, los iconos agregan desorden visual innecesario, consumen espacio en la pantalla y, a menudo, no mejoran la comprensión del usuario. Agregue solo iconos que ayudan en la comprensión, como los símbolos estándar.

    **Incorrecto:**

    ![captura de pantalla de la ventana con iconos en las pestañas ](images/ctrl-tabs-image10.png)

    En este ejemplo, los iconos agregan desorden visual y hacen poco para mejorar la comprensión del usuario.

    **Excepción:** Puede usar iconos claramente reconocibles si es posible que no haya espacio suficiente para mostrar etiquetas significativas:

    **Correcto:**

    ![captura de pantalla de pestañas con iconos y etiquetas abreviadas ](images/ctrl-tabs-image11.png)

    En este ejemplo, la ventana es tan estrecha que los iconos comunican mejor las pestañas que las etiquetas.

-   **No use logotipos de producto para gráficos de tabulación.** Las pestañas no son para [personal de marca.](exper-branding.md)

### <a name="dynamic-window-surface-pattern"></a>Patrón de superficie de ventana dinámica

-   **No use barras de desplazamiento en las páginas de pestañas.** Las pestañas funcionan de forma similar a las barras de desplazamiento para aumentar el área efectiva de una ventana. Un mecanismo debe ser suficiente.
-   **Use etiquetas de tabulación concisas.** Use una o dos palabras que describan claramente el contenido de la página. Las etiquetas más largas consumen espacio en la pantalla, especialmente cuando se localizan las etiquetas.
-   **Use etiquetas de tabulación específicas y significativas.** Evite etiquetas de pestaña genéricas que se puedan aplicar a cualquier pestaña, como General, Avanzado o Configuración.
-   **Si una pestaña no se aplica al contexto actual y los usuarios no lo esperan, quítela.** Esto simplifica la interfaz de usuario y los usuarios no la perderán.

    **Incorrecto:**

    ![captura de pantalla de la ventana de opciones con el nombre de la pestaña atenuado ](images/ctrl-tabs-image12.png)

    En este ejemplo, la pestaña Ubicaciones de archivos está deshabilitada incorrectamente cuando Microsoft Word se usa como editor de correo electrónico. En lugar de deshabilitar esta pestaña, debe quitarse porque los usuarios no esperarán ver ni cambiar las ubicaciones de los archivos en este contexto.

-   **Si una pestaña no se aplica al contexto actual y es posible que los usuarios lo esperen:**

    -   Muestra la pestaña .
    -   Deshabilite los controles de la página.
    -   Incluya texto que explique por qué se deshabilitan los controles.

    No deshabilite la pestaña, ya que no se explica por sí mismo y prohíbe la exploración. Los usuarios que buscan un valor específico se verían obligados a buscar en todas las demás pestañas.

    ![captura de pantalla de la ventana con las opciones de la pestaña Ver atenuadas ](images/ctrl-tabs-image13.png)

    En este ejemplo, ninguna de las opciones De vista se aplica en Diseño de lectura. Sin embargo, es posible que los usuarios esperen que se apliquen en función de la etiqueta de pestaña, por lo que se muestra la página pero las opciones están deshabilitadas.

### <a name="multiple-views-and-documents-patterns"></a>Varios patrones de vistas y documentos

-   **Use los nombres de vista o documento en las etiquetas de tabulación.**
-   **Evite nombres de tabulación excesivamente largos.** Si es necesario, tenga un tamaño de nombre máximo o truncúe la etiqueta de pestaña mostrada con puntos suspensivos. Las etiquetas más largas consumen espacio en la pantalla, especialmente cuando se localizan las etiquetas.
-   **Si una pestaña no se aplica al contexto actual, quite la pestaña.**

### <a name="exclusive-options-pattern"></a>Patrón de opciones exclusivas

-   **No use este patrón.** En su lugar, use botones de radio o una lista desplegable.

    **Incorrecto:**

    ![captura de pantalla de la ventana con dos pestañas "crear" ](images/ctrl-tabs-image14.png)

    En este ejemplo, las pestañas se usan incorrectamente como sustituto de los botones de radio.

    **Correcto:**

    ![captura de pantalla de la ventana con dos botones de radio ](images/ctrl-tabs-image15.png)

    En este ejemplo, los botones de radio se usan correctamente en su lugar.

## <a name="labels"></a>Etiquetas

-   Pestañas de etiqueta según su patrón. Use nombres en lugar de verbos, sin terminar los signos de puntuación. Consulte las directrices de patrón anteriores para obtener más información.
-   Use mayúsculas de estilo de frase.
-   No asigne una clave de acceso. Se puede acceder a las pestañas a través de sus teclas de método abreviado (Ctrl+Tab, Ctrl+Mayús+Tab, Ctrl+PgUp, Ctrl+PgDn). Hay escasez de buenas opciones de clave de acceso, por lo que no asignar claves de acceso a pestañas facilita su asignación a otros controles.

## <a name="documentation"></a>Documentación

Al hacer referencia a pestañas:

-   Use el texto exacto de la etiqueta, incluido su uso de mayúsculas, e incluya la pestaña de palabras.
-   Para describir la interacción del usuario, use click.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.
-   Dado que varios usos pueden ser ambiguos, especialmente para una audiencia mundial, use la pestaña de nombres solo para hacer referencia solo a un control de pestaña. Para otros usos, aclare el significado con un descriptor: la tecla Tab, una tabulación o una marca de tabulación en la regla.

Ejemplo: en el **menú Herramientas,** haga clic **en Opciones** y, a continuación, haga clic en **la pestaña** Ver.

