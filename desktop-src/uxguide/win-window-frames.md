---
title: Marcos de ventana
description: La mayoría de los programas deben usar marcos de ventana estándar. Las aplicaciones inmersivas pueden tener un modo de pantalla completa que oculta el marco de la ventana. Considere la posibilidad de usar el cristal estratégicamente para una apariencia más sencilla, más ligera y más cohesiva.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dee701f7aad12e348a89034010de1f44134e9d3e
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812252"
---
# <a name="window-frames"></a>Marcos de ventana

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

La mayoría de los programas deben usar marcos de ventana estándar. Las aplicaciones inmersivas pueden tener un modo de pantalla completa que oculta el marco de la ventana. Considere la posibilidad de usar el cristal estratégicamente para una apariencia más sencilla, más ligera y más cohesiva.

Con un marco de ventana, los usuarios pueden manipular una ventana y ver el título y el icono para identificar su contenido.

![captura de pantalla del marco de ventana alrededor de la ventana del Bloc de notas ](images/win-window-frames-image1.png)

Marco de ventana típico.

**Nota:** Las directrices relacionadas [con la administración de](win-window-mgt.md) ventanas y la personal [de](exper-branding.md) marca se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="glass-window-frames"></a>Marcos de ventana de glass

Los marcos de ventanas de cristal son un nuevo aspecto sorprendente de microsoft Windows, con el objetivo de ser atractivos y ligeros. Estos fotogramas translúcidos dan a las ventanas una apariencia abierta y menos intrusiva, lo que ayuda a los usuarios a centrarse en el contenido y la funcionalidad en lugar de en la interfaz que lo rodea.

![captura de pantalla de marco de cristal alrededor de la calculadora ](images/win-window-frames-image2.png)

Marcos de ventana de glass.

Puede usar glass estratégicamente en regiones pequeñas dentro de una ventana que toque el marco de la ventana. Estas regiones parecen formar parte del marco de ventana, aunque técnicamente forman parte del área de cliente de la ventana.

![captura de pantalla de la ventana con borde translúcido ](images/win-window-frames-image3.png)

En este ejemplo, se usa glass en el área de cliente para que parezca parte del marco.

### <a name="hidden-frames"></a>Marcos ocultos

A veces, el mejor marco de ventana no es ningún marco. Este suele ser el [](glossary.md) caso de [](glossary.md) la ventana principal de aplicaciones de pantalla completa inmersivas que no se usan junto con otros programas, como reproductores multimedia, juegos y aplicaciones de pantalla completa.

Los visores de contenido suelen beneficiarse de tener la opción de mostrar el contenido a pantalla completa. Algunos ejemplos son Windows Internet Explorer , Galería fotográfica de Windows Live, Windows Movie Maker HD, Microsoft PowerPoint y Microsoft Word.

![captura de pantalla del reproductor multimedia en la vista de pantalla completa ](images/win-window-frames-image4.png)

En este ejemplo, Reproductor de Windows Media mostrar su contenido en pantalla completa.

### <a name="custom-frames"></a>Marcos personalizados

La mayoría Windows aplicaciones deben usar los marcos de ventana estándar. Sin embargo, para aplicaciones envolventes, de pantalla completa y independientes, como juegos y aplicaciones de quiosco, puede ser adecuado usar marcos personalizados para las ventanas que no se muestran a pantalla completa. La motivación para usar marcos personalizados debe ser proporcionar a la experiencia general una sensación única, no solo para la [personalización de marca.](exper-branding.md)

![ilustración del juego de juegos de imágenes y el marco ](images/win-window-frames-image5.png)

Los fotogramas personalizados son adecuados para aplicaciones envolventes, de pantalla completa y independientes, como juegos.

## <a name="guidelines"></a>Directrices

### <a name="window-frames"></a>Marcos de ventana

-   Use marcos de ventana estándar.
    -   **Excepción:** Para proporcionar una sensación única a las aplicaciones independientes de pantalla completa inmersiva:
        -   Considere la posibilidad de ocultar el marco de ventana [de la ventana principal.](glossary.md)
        -   Considere la posibilidad de usar marcos personalizados [para la ventana secundaria](glossary.md).
        -   Si un marco personalizado es adecuado, elija un diseño ligero y no preste demasiada atención a sí mismo.

            **Incorrecto:**

            ![captura de pantalla del marco de distraer ](images/win-window-frames-image6.png)

            En este ejemplo, el marco personalizado llama demasiada atención a sí mismo.
-   No agregue controles a un marco de ventana. Coloque los controles dentro de la ventana en su lugar.

    **Incorrecto:**

    ![captura de pantalla del control en el marco de la ventana ](images/win-window-frames-image7.png)

    **Correcto:**

    ![captura de pantalla del control en el área de cliente ](images/win-window-frames-image8.png)

    En el ejemplo correcto, el control está dentro del área de cliente en lugar del marco de ventana.

### <a name="full-screen-mode"></a>Modo de pantalla completa

-   Para los programas que tienen un modo de pantalla completa opcional, para habilitar el modo de pantalla completa:
    -   Tenga un comando de pantalla completa modal en la barra de menús o la barra de herramientas. Cuando el usuario haga clic en el comando, muestre el comando en su estado seleccionado.

        ![captura de pantalla de la ventana con el elemento de menú de pantalla completa ](images/win-window-frames-image9.png)

        En este ejemplo se muestra el comando de pantalla completa junto con su tecla de método abreviado estándar.

-   Use F11 para la tecla de método abreviado de pantalla completa.
-   Si hay una barra de herramientas y se usa normalmente el modo de pantalla completa, también tiene un botón de barra de herramientas gráfico con información sobre herramientas de pantalla completa.

    ![captura de pantalla de pantalla completa y botones de reversión ](images/win-window-frames-image10.png)

    Ejemplos de botones de la barra de herramientas de pantalla completa.

-   Para revertir desde el modo de pantalla completa:
    -   Tenga un comando de pantalla completa modal en la barra de menús o la barra de herramientas. Cuando el usuario haga clic en el comando, muestre el comando en su estado borrado.
    -   Use F11 para la tecla de método abreviado de pantalla completa. Si aún no está asignado, Esc también se puede usar para este propósito.

### <a name="glass"></a>Vidrio

Los marcos de ventana estándar usan glass automáticamente Windows, pero también puede usar el cristal en regiones que tocan el marco de la ventana.

-   **Considere la posibilidad de usar el cristal estratégicamente en regiones pequeñas que toquen el marco de ventana sin texto.** Esto puede dar a un programa una apariencia más sencilla, más ligera y más cohesiva haciendo que la región parezca formar parte del marco.
-   ![captura de pantalla de la ventana con borde translúcido ](images/win-window-frames-image3.png)
-   En este ejemplo, Glass centra la atención del usuario en el contenido en lugar de en los controles.
-   **No use glass en situaciones en las que un fondo de ventana sin formato sea más atractivo o más fácil de usar.**

**Correcto:**

![captura de pantalla de la ventana con cuatro gráficos y etiqueta ](images/win-window-frames-image11.png)

En este ejemplo, se usa glass para dar a la ventana Alt+Tab un aspecto ligero. Glass funciona para esta ventana porque consta de gráficos y una única etiqueta de texto fuerte.

**Incorrecto:**

![captura de pantalla de la ventana con doce gráficos ](images/win-window-frames-image12.png)

En este ejemplo incorrecto, el uso de gafas es distraer. Un fondo de ventana sin formato sería una mejor opción.

 

 
