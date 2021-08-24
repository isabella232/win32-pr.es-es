---
title: Barras de estado (conceptos básicos de diseño)
description: Una barra de estado es un área en la parte inferior de una ventana principal que muestra información sobre el estado de la ventana actual (por ejemplo, qué se está visualizando y cómo), tareas en segundo plano (como impresión, examen y formato) u otra información contextual (como selección y estado del teclado).
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: fa76563adbd3810b48339cc49014441512e3d76a0ac7484ff632f64f635b4cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934231"
---
# <a name="status-bars-design-basics"></a>Barras de estado (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Una barra de estado es un área en la parte inferior de una ventana principal que muestra información sobre el estado de la ventana actual (por ejemplo, qué se está visualizando y cómo), tareas en segundo plano (como impresión, examen y formato) u otra información contextual (como selección y estado del teclado).

Las barras de estado suelen indicar el estado a través de texto e iconos, pero también pueden tener indicadores de progreso, así como menús para comandos y opciones relacionadas con el estado.

![captura de pantalla de la barra de estado típica ](images/ctrl-status-bars-image1.png)

Una barra de estado típica.

> [!Note]  
> Las instrucciones relacionadas con [el área de notificación](winenv-notification.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿Es relevante el estado cuando los usuarios usan activamente otros programas?** Si es así, use un [icono de área de notificación](winenv-notification.md).
-   **¿Es necesario que el elemento de estado muestre notificaciones?** Si es así, debe usar un icono de área de notificación.
-   **¿La ventana es una ventana principal?** Si no es así, no use una barra de estado. Los cuadros de diálogo, los asistentes, los paneles de control y las hojas de propiedades no deben tener barras de estado.
-   **¿La información es principalmente el estado?** Si no es así, no use una barra de estado. Las barras de estado no deben usarse como barra de [menús secundaria o barra de](cmd-menus.md) [herramientas](cmd-toolbars.md).
-   **¿Explica la información cómo usar el control seleccionado?** Si es así, muestre la información junto al control asociado mediante una explicación complementaria o una etiqueta de instrucción en su lugar.
-   **¿El estado es útil y pertinente? Es decir, ¿es probable que los usuarios cambien su comportamiento como resultado de esta información?** Si no es así, no muestra el estado o lo coloca en un archivo de registro.
-   **¿El estado es crítico? ¿Se requiere una acción inmediata?** Si es así, muestre la información en un formulario que exija [](win-dialog-box.md) atención y no se pueda omitir fácilmente, como un cuadro de diálogo o dentro de la propia ventana principal.

    ![captura de pantalla de la barra de estado "error de certificado" roja ](images/ctrl-status-bars-image2.png)

    Una barra de direcciones roja en Windows Internet Explorer.

-   **¿El programa está pensado principalmente para usuarios principiantes?** Por lo general, los usuarios sin experiencia no son conscientes de las barras de estado, por lo que se replanteará el uso de barras de estado en este caso.

## <a name="design-concepts"></a>Conceptos de diseño

Las barras de estado son una excelente manera de proporcionar información de estado sin interrumpir a los usuarios ni interrumpir su flujo. Sin embargo, las barras de estado son fáciles de pasar por alto. De hecho, es tan fácil que muchos usuarios no se fijan en las barras de estado.

La solución a este problema no es exigir la atención del usuario mediante iconos de colores, animaciones o flashing, sino diseñar para esta limitación. Puede hacerlo de la siguiente forma:

-   **Asegúrese de que la información de estado es útil y pertinente.** Si no es así, no proporcione ninguna barra de estado.
-   **No usar barras de estado para obtener información fundamental.** Los usuarios nunca deben saber qué hay en la barra de estado. Si los usuarios deben verlo, no lo coloque en una barra de estado.

**Si solo hace una cosa...**

Asegúrese de que la información de la barra de estado es útil y pertinente, pero no fundamental.

## <a name="usage-patterns"></a>Patrones de uso

Las barras de estado tienen varios patrones de uso:



|   Uso                                                                                                                                 |    Ejemplo                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Estado de la ventana actual**<br/> Mostrar el origen de lo que se muestra junto con los modos de vista <br/>              | ![captura de pantalla de una barra de estado de "ubicación" ](images/ctrl-status-bars-image3.png)<br/> En este ejemplo, la barra de estado muestra la ruta de acceso al documento.<br/>                                                         |
| **Progress**<br/> Mostrar el progreso de las tareas en segundo plano, ya sea con una barra de progreso determinada o una animación. <br/> | ![captura de pantalla de la barra de estado con la barra de progreso ](images/ctrl-status-bars-image4.png)<br/> En este ejemplo, la barra de estado incluye una barra de progreso para mostrar la página web que se carga en Internet Explorer ventana.<br/> |
| **Información contextual**<br/> Mostrar información contextual sobre lo que el usuario está haciendo actualmente. <br/>              | ![captura de pantalla de la barra de estado que muestra el número de píxeles ](images/ctrl-status-bars-image5.png)<br/> En este ejemplo, Microsoft Paint muestra el tamaño de selección en píxeles.<br/>                                           |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   Considere la posibilidad de proporcionar un comando Ver barra de estado si solo algunos usuarios necesitarán la información de la barra de estado. Oculte la barra de estado de forma predeterminada si la mayoría de los usuarios no la necesitarán.
-   No use la barra de estado para explicar los elementos de la barra de menús. Este patrón de ayuda no es reconocible.

### <a name="presentation"></a>Presentación

-   Deshabilite el estado modal que no se aplica. El estado modal incluye los estados de teclado y documento.
-   Quite el estado no modal que no se aplica.
-   Presente la información de estado en el orden siguiente: estado de la ventana actual; progress; e información contextual.

### <a name="icons"></a>Iconos

-   Elija diseños de iconos de estado fácilmente reconocibles. Prefiere iconos con contornos únicos sobre iconos en forma cuadrada o rectangular.
-   Use franjas de rojo puro, amarillo y verde solo para comunicar la información de estado. De lo contrario, estos iconos son confusos.

    **Correcto:**

    ![captura de pantalla de la barra de estado con iconos azules ](images/ctrl-status-bars-image6.png)

    **Incorrecto:**

    ![captura de pantalla de la barra de estado con un icono rojo ](images/ctrl-status-bars-image7.png)

    En el ejemplo incorrecto, el icono rojo sugiere involuntarlamente un error, lo que crea confusión.

-   Use variaciones de icono o superposiciones para indicar los cambios de estado o de estado. Use variaciones de icono para mostrar cambios en cantidades o puntos fuertes. Para otros tipos de estado, use estas superposiciones estándar: 

    | Overlay                 | Estado            |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | ![captura de pantalla del icono de advertencia ](images/ctrl-status-bars-image8.png)<br/>                | Advertencia<br/>               |
    | ![captura de pantalla del icono de error ](images/ctrl-status-bars-image9.png)<br/>                  | Error<br/>                 |
    | ![captura de pantalla del icono deshabilitado o desconectado ](images/ctrl-status-bars-image10.png)<br/> | Deshabilitado o desconectado<br/> |
    | ![captura de pantalla del icono bloqueado o sin conexión ](images/ctrl-status-bars-image11.png)<br/>       | Bloqueado o sin conexión<br/>       |

    

     

-   No cambie el estado con demasiada frecuencia. Los iconos de la barra de estado no deben parecer ruidosos, inestables ni exigir atención. El ojo es sensible a los cambios en el campo periférico de la visión, por lo que los cambios de estado deben ser sutiles.
-   En el caso de los iconos que proporcionan información de estado importante, se prefieren etiquetas en su lugar.
-   Los iconos de la barra de estado sin etiquetar deben tener información sobre herramientas.

Para obtener más información, vea [Iconos](vis-icons.md).

### <a name="interaction"></a>Interacción

-   Haga que un área de barra de estado sea interactiva para permitir que los usuarios accedan directamente a los comandos y opciones relacionados.
    -   Use un control que parezca y se comporte como un [botón de menú](ctrl-command-buttons.md) o un botón de división. Estas áreas de la barra de estado deben tener una flecha desplegable para indicar que se puede hacer clic en ellas.
    -   Muestra el menú al hacer clic con el botón izquierdo en el mouse hacia abajo, no hacia arriba.
    -   No admite hacer clic con el botón derecho o hacer doble clic. Los usuarios no esperan estas interacciones en una barra de estado, por lo que es probable que no las intenten.
-   Mostrar información sobre herramientas al mantener el puntero.

## <a name="text"></a>Texto

-   Por lo general, use etiquetas concisas. Corte cualquier texto que se pueda eliminar.
-   Prefiere fragmentos de oración, sin terminar de puntuar. Use oraciones completa (con puntuación final) solo cuando los fragmentos de oración no sean significativamente más cortos.
-   En el caso de las etiquetas de progreso opcionales, indique lo que está haciendo la operación con una etiqueta que comienza con un verbo (forma de error) y termina con un botón de puntos suspensivos. Por ejemplo: "Copiar...". Esta etiqueta puede cambiar dinámicamente si la operación tiene varios pasos o está procesando varios objetos.
-   No use color, negrita o cursiva para resaltar el texto de la barra de estado.
-   Para obtener instrucciones de expresiones sobre herramientas, vea [Información sobre herramientas e información sobre herramientas.](ctrl-tooltips-and-infotips.md)

## <a name="documentation"></a>Documentación

Consulte las barras de estado como barras de estado, no como líneas de estado u otras variaciones. Ejemplo: "El número de página actual se muestra en la barra de estado".

 

