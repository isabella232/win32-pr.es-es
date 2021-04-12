---
title: Barras de estado (conceptos básicos del diseño)
description: Una barra de estado es un área en la parte inferior de una ventana principal que muestra información sobre el estado de la ventana actual (por ejemplo, lo que se está viendo y cómo), tareas en segundo plano (como la impresión, el análisis y el formato) u otra información contextual (como la selección y el estado del teclado).
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8f65d104f59cd0aec0c242d623f83c410c22f48d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279741"
---
# <a name="status-bars-design-basics"></a>Barras de estado (conceptos básicos del diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Una barra de estado es un área en la parte inferior de una ventana principal que muestra información sobre el estado de la ventana actual (por ejemplo, lo que se está viendo y cómo), tareas en segundo plano (como la impresión, el análisis y el formato) u otra información contextual (como la selección y el estado del teclado).

Las barras de Estado suelen indicar el estado a través de texto e iconos, pero también pueden tener indicadores de progreso, así como menús para comandos y opciones relacionados con el estado.

![captura de pantalla de la barra de estado típica ](images/ctrl-status-bars-image1.png)

Barra de estado típica.

> [!Note]  
> Las instrucciones relacionadas con el [área de notificación](winenv-notification.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿El estado es importante cuando los usuarios usan activamente otros programas?** Si es así, use un [icono de área de notificación](winenv-notification.md).
-   **¿Es necesario que el elemento de estado muestre notificaciones?** En ese caso, debe usar un icono de área de notificación.
-   **¿La ventana es una ventana principal?** Si no es así, no use una barra de estado. Los cuadros de diálogo, los asistentes, los paneles de control y las hojas de propiedades no deben tener barras de estado.
-   **¿La información es principalmente el estado?** Si no es así, no use una barra de estado. Las barras de estado no se deben usar como [barra de menús](cmd-menus.md) o [barra de herramientas](cmd-toolbars.md)secundaria.
-   **¿La información explica cómo usar el control seleccionado?** En ese caso, muestre la información situada junto al control asociado mediante una explicación complementaria o una etiqueta de instrucción.
-   **¿El estado es útil y relevante? Es decir, ¿es probable que los usuarios cambien su comportamiento como resultado de esta información?** En caso contrario, no muestre el estado o colóquelo en un archivo de registro.
-   **¿El estado es crítico? ¿Es necesaria una acción inmediata?** Si es así, muestre la información en un formulario que requiera atención y no se pueda omitir fácilmente, como un [cuadro de diálogo](win-dialog-box.md) o dentro de la propia ventana principal.

    ![captura de pantalla de la barra de estado "error de certificado" rojo ](images/ctrl-status-bars-image2.png)

    Barra de direcciones roja en Windows Internet Explorer.

-   **¿El programa está pensado principalmente para usuarios inexpertos?** Los usuarios inscritos generalmente no reconocen las barras de estado, por lo que reconsidere el uso de barras de estado en este caso.

## <a name="design-concepts"></a>Conceptos de diseño

Las barras de estado son una excelente manera de proporcionar información de estado sin interrumpir a los usuarios ni romper su flujo. Sin embargo, las barras de estado son fáciles de pasar por alto. De hecho, es muy fácil que muchos usuarios no perciban barras de estado.

La solución a este problema no exige la atención del usuario mediante el uso de iconos de llamativa, animación o intermitencia, sino también para diseñar esta limitación. Puede hacerlo de la siguiente forma:

-   **Asegurarse de que la información de estado es útil y relevante.** Si no es así, no proporcione ninguna barra de estado.
-   **No usar barras de estado para obtener información crucial.** Los usuarios nunca deben tener que saber lo que hay en la barra de estado. Si los usuarios deben verlo, no los coloque en una barra de estado.

**Si solo hace algo...**

Asegúrese de que la información de la barra de estado sea útil y relevante, pero no fundamental.

## <a name="usage-patterns"></a>Patrones de uso

Las barras de estado tienen varios patrones de uso:



|                                                                                                                                    |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Estado de la ventana actual**<br/> Mostrar el origen de lo que se muestra junto con los modos de vista <br/>              | ![captura de pantalla de una barra de estado de "ubicación" ](images/ctrl-status-bars-image3.png)<br/> En este ejemplo, la barra de estado muestra la ruta de acceso al documento.<br/>                                                         |
| **Progress**<br/> Muestra el progreso de las tareas en segundo plano, ya sea con una barra de progreso o una animación de finalización. <br/> | ![captura de pantalla de la barra de estado con barra de progreso ](images/ctrl-status-bars-image4.png)<br/> En este ejemplo, la barra de estado incluye una barra de progreso para mostrar la carga de la página web en una ventana de Internet Explorer.<br/> |
| **Información contextual**<br/> Mostrar información contextual sobre lo que está haciendo actualmente el usuario. <br/>              | ![captura de pantalla de la barra de estado que muestra el número de píxeles ](images/ctrl-status-bars-image5.png)<br/> En este ejemplo, Microsoft Paint muestra el tamaño de la selección en píxeles.<br/>                                           |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   Considere la posibilidad de proporcionar un comando View Status Bar si solo algunos usuarios necesitarán la información de la barra de estado. Oculte la barra de estado de forma predeterminada si la mayoría de los usuarios no la necesitará.
-   No use la barra de estado para explicar los elementos de la barra de menús. Este patrón de ayuda no es reconocible.

### <a name="presentation"></a>Presentación

-   Deshabilite el estado modal que no se aplique. El estado modal incluye los Estados de teclado y de documento.
-   Quitar el estado no modal que no se aplica.
-   Presente la información de estado en el siguiente orden: estado de la ventana actual; progreso y la información contextual.

### <a name="icons"></a>Iconos

-   Elija diseños de iconos de estado fácilmente reconocibles. Prefiere iconos con contornos únicos en los iconos con forma de cuadrado o rectangular.
-   Use swaths de rojo puro, amarillo y verde solo para comunicar información de estado. De lo contrario, estos iconos son confusos.

    **Correcto:**

    ![captura de pantalla de la barra de estado con iconos azules ](images/ctrl-status-bars-image6.png)

    **Incorrecto:**

    ![captura de pantalla de la barra de estado con un icono rojo ](images/ctrl-status-bars-image7.png)

    En el ejemplo incorrecto, el icono rojo sugiere involuntariamente un error, con lo que se crea confusión.

-   Use variaciones o superposiciones de iconos para indicar el estado o los cambios de estado. Use variaciones de los iconos para mostrar los cambios en las cantidades o los puntos fuertes. Para otros tipos de estado, use estas superposiciones estándar: 

    |                                                                                               |                                  |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | **Overlay**<br/>                                                                        | **Estado**<br/>            |
    | ![captura de pantalla del icono de advertencia ](images/ctrl-status-bars-image8.png)<br/>                | Advertencia<br/>               |
    | ![captura de pantalla del icono de error ](images/ctrl-status-bars-image9.png)<br/>                  | Error<br/>                 |
    | ![captura de pantalla del icono deshabilitado o desconectado ](images/ctrl-status-bars-image10.png)<br/> | Deshabilitado o desconectado<br/> |
    | ![captura de pantalla del icono de bloqueado/sin conexión ](images/ctrl-status-bars-image11.png)<br/>       | Bloqueado/sin conexión<br/>       |

    

     

-   No cambie el estado con demasiada frecuencia. Los iconos de la barra de estado no deben parecer ruidos, inestables o de petición. El ojo es sensible a los cambios en el campo de visión de periféricos, por lo que los cambios de estado deben ser sutiles.
-   En el caso de los iconos que proporcionan información importante sobre el estado, prefieran etiquetas en contexto.
-   Los iconos de la barra de estado sin etiqueta deben tener información sobre herramientas.

Para obtener más información, vea [iconos](vis-icons.md).

### <a name="interaction"></a>Interacción

-   Haga que el área de la barra de estado sea interactiva para permitir el acceso directo a los usuarios a comandos y opciones relacionados.
    -   Use un control que tenga el aspecto y el comportamiento como un [botón de menú](ctrl-command-buttons.md) o un botón de expansión. Estas áreas de la barra de estado deben tener una flecha desplegable para indicar que se pueden hacer clic en ellas.
    -   Mostrar el menú a la izquierda: haga clic en el mouse hacia abajo, no en subir.
    -   No se admite hacer clic con el botón derecho o hacer doble clic. Los usuarios no esperan estas interacciones en una barra de estado, por lo que no es probable que las intenten.
-   Mostrar información sobre herramientas al mantener el mouse.

## <a name="text"></a>Texto

-   Por lo general, use etiquetas concisas. Cortar cualquier texto que se pueda eliminar.
-   Prefiere los fragmentos de oraciones, sin puntuación final. Use oraciones completas (con puntuación final) solo cuando los fragmentos de oraciones no sean mucho más cortos.
-   En el caso de las etiquetas de progreso opcionales, indique cuál es la operación con una etiqueta que comienza con un verbo (formulario gerundio) y termina con puntos suspensivos. Por ejemplo: "copiando...". Esta etiqueta puede cambiar dinámicamente si la operación tiene varios pasos o si está procesando varios objetos.
-   No utilice color, Bold o cursiva para resaltar el texto de la barra de estado.
-   Para obtener instrucciones sobre las frases de la información sobre herramientas, consulte [información sobre herramientas y recuadros informativos](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentación

Haga referencia a las barras de estado como barras de estado, no líneas de estado u otras variaciones. Ejemplo: "el número de página actual se muestra en la barra de estado".

 

