---
title: Marcos de ventana
description: La mayoría de los programas deben usar marcos de ventana estándar. Las aplicaciones envolventes pueden tener un modo de pantalla completa que oculte el marco de la ventana. Considere la posibilidad de usar cristal estratégicamente para obtener un aspecto más sencillo, más claro y más coherente.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558325"
---
# <a name="window-frames"></a>Marcos de ventana

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

La mayoría de los programas deben usar marcos de ventana estándar. Las aplicaciones envolventes pueden tener un modo de pantalla completa que oculte el marco de la ventana. Considere la posibilidad de usar cristal estratégicamente para obtener un aspecto más sencillo, más claro y más coherente.

Con un marco de ventana, los usuarios pueden manipular una ventana y ver el título y el icono para identificar su contenido.

![captura de pantalla del marco de ventana alrededor de la ventana del Bloc de notas ](images/win-window-frames-image1.png)

Marco de ventana típico.

**Nota:** Las instrucciones relacionadas con la [Administración de ventanas](win-window-mgt.md) y la [Personalización de marca](exper-branding.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="glass-window-frames"></a>Cuadros de ventana de cristal

Los marcos de ventana Glass son un nuevo aspecto sorprendente de la estética de Microsoft Windows, con el objetivo de ser atractivos y ligeros. Estos fotogramas translúcidos proporcionan a Windows una apariencia menos intrusiva, que ayuda a los usuarios a centrarse en el contenido y la funcionalidad, en lugar de en la interfaz que lo rodea.

![captura de pantalla del marco Glass alrededor de la calculadora ](images/win-window-frames-image2.png)

Marcos de la ventana de cristal.

Puede usar cristal de manera estratégica en pequeñas regiones dentro de una ventana que toca el marco de la ventana. Estas regiones parecen formar parte del marco de ventana, aunque técnicamente forman parte del área de cliente de la ventana.

![captura de pantalla de la ventana con borde translúcido ](images/win-window-frames-image3.png)

En este ejemplo, se utiliza Glass en el área cliente para que parezca parte del marco.

### <a name="hidden-frames"></a>Fotogramas ocultos

A veces, el marco de ventana mejor no es ningún fotograma. Este suele ser el caso de la [ventana principal](glossary.md) de aplicaciones de [pantalla completa](glossary.md) que no se usan junto con otros programas, como reproductores multimedia, juegos y aplicaciones de quiosco.

Los visores de contenido a menudo se benefician de tener la opción de mostrar el contenido en pantalla completa. Algunos ejemplos son Windows Internet Explorer, Galería fotográfica de Windows Live, Windows Movie Maker HD, Microsoft PowerPoint y Microsoft Word.

![captura de pantalla del reproductor de media en la vista de pantalla completa ](images/win-window-frames-image4.png)

En este ejemplo, Windows Media Player puede mostrar su contenido en pantalla completa.

### <a name="custom-frames"></a>Marcos personalizados

La mayoría de las aplicaciones Windows deben usar los marcos de ventana estándar. Sin embargo, en el caso de las aplicaciones independientes, de pantalla completa e independiente, como los juegos y las aplicaciones de quiosco, puede ser adecuado utilizar fotogramas personalizados para las ventanas que no se muestran en pantalla completa. La motivación para usar fotogramas personalizados debe ser dar a la experiencia global una sensación única, no solo para la [Personalización de marca](exper-branding.md).

![Ilustración del rompecabezas y el fotograma de la imagen codificada ](images/win-window-frames-image5.png)

Los fotogramas personalizados son adecuados para aplicaciones independientes, de pantalla completa e independiente, como los juegos.

## <a name="guidelines"></a>Directrices

### <a name="window-frames"></a>Marcos de ventana

-   Usar marcos de ventana estándar.
    -   **Excepción:** Para proporcionar a las aplicaciones independientes una pantalla completa, una única sensación:
        -   Considere la posibilidad de ocultar el marco de ventana de la [ventana principal](glossary.md).
        -   Considere la posibilidad de usar marcos personalizados para la [ventana secundaria](glossary.md).
        -   Si un fotograma personalizado es adecuado, elija un diseño ligero y no se Centre demasiado en ello.

            **Incorrecto:**

            ![captura de pantalla del marco distracción ](images/win-window-frames-image6.png)

            En este ejemplo, el marco personalizado atrae demasiado atención a sí mismo.
-   No agregue controles a un marco de ventana. Coloque los controles dentro de la ventana en su lugar.

    **Incorrecto:**

    ![captura de pantalla del control en el marco de ventana ](images/win-window-frames-image7.png)

    **Correcto:**

    ![captura de pantalla del control en el área cliente ](images/win-window-frames-image8.png)

    En el ejemplo correcto, el control está dentro del área cliente en lugar del marco de la ventana.

### <a name="full-screen-mode"></a>Modo de pantalla completa

-   Para los programas que tienen un modo de pantalla completa opcional, para habilitar el modo de pantalla completa:
    -   Tener un comando de pantalla completa modal en la barra de menús o la barra de herramientas. Cuando el usuario haga clic en el comando, muestre el comando en su estado seleccionado.

        ![captura de pantalla de la ventana con el elemento de menú de pantalla completa ](images/win-window-frames-image9.png)

        En este ejemplo se muestra el comando pantalla completa junto con su tecla de método abreviado estándar.

-   Utilice F11 para la tecla de método abreviado de pantalla completa.
-   Si se usa normalmente una barra de herramientas y el modo de pantalla completa, también tiene un botón gráfico de la barra de herramientas con una información sobre herramientas de pantalla completa.

    ![captura de pantalla de los botones pantalla completa y revertir ](images/win-window-frames-image10.png)

    Ejemplos de botones de la barra de herramientas de pantalla completa.

-   Para volver al modo de pantalla completa:
    -   Tener un comando de pantalla completa modal en la barra de menús o la barra de herramientas. Cuando el usuario haga clic en el comando, muestre el comando en su estado desactivado.
    -   Utilice F11 para la tecla de método abreviado de pantalla completa. Si aún no se ha asignado, ESC también puede usarse para este fin.

### <a name="glass"></a>Vidrio

Los marcos de ventana estándar usan cristal automáticamente en Windows, pero también puede usar Glass en regiones que tocan el marco de la ventana.

-   **Considere la posibilidad de usar Glass estratégicamente en regiones pequeñas que tocan el marco de la ventana sin texto.** Si lo hace, puede dar un aspecto más sencillo, más ligero y coherente haciendo que la región parezca parte del marco.
-   ![captura de pantalla de la ventana con borde translúcido ](images/win-window-frames-image3.png)
-   En este ejemplo, cristal centra la atención del usuario sobre el contenido en lugar de los controles.
-   **No use cristal en situaciones en las que un fondo de ventana sin formato sea más atractivo o fácil de usar.**

**Correcto:**

![captura de pantalla de la ventana con cuatro gráficos y etiquetas ](images/win-window-frames-image11.png)

En este ejemplo, Glass se usa para dar una apariencia ligera a la ventana Alt + Tab. Glass funciona para esta ventana porque consta de gráficos y una sola etiqueta de texto segura.

**Incorrecto:**

![captura de pantalla de la ventana con doce gráficos ](images/win-window-frames-image12.png)

En este ejemplo incorrecto, el uso de cristal es distracción. Un fondo de ventana simple sería una opción mejor.

 

 