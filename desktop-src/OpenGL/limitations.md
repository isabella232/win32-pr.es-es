---
title: Limitaciones
description: Limitaciones
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL en Windows, limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d058570c049f471dcf6e92c4eb55eb1365948d581127c68a46deb8d863ccc34d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937422"
---
# <a name="limitations"></a>Limitaciones

La implementación genérica tiene las siguientes limitaciones:

-   Impresión.

    Puede imprimir una imagen openGL directamente en una impresora solo mediante metarchivos. Para obtener más información, vea [Impresión de una imagen openGL.](printing-an-opengl-image.md)

-   Los gráficos OpenGL y GDI no se pueden mezclar en una ventana de doble búfer.

    Una aplicación puede dibujar directamente gráficos OpenGL y gráficos GDI en una ventana de un solo búfer, pero no en una ventana de doble búfer.

-   No hay paletas de colores de hardware por ventana.

    Windows una paleta de colores de hardware del sistema única, que se aplica a toda la pantalla. Una ventana OpenGL no puede tener su propia paleta de hardware, pero puede tener su propia paleta lógica. Para ello, debe convertirse en una aplicación que tenga en cuenta la paleta. Para obtener más información, vea [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).

-   No hay compatibilidad directa con el Portapapeles, el intercambio dinámico de datos (DDE) ni OLE.

    Una ventana con gráficos OpenGL no admite directamente estas Windows funcionalidades. Sin embargo, hay soluciones alternativas para usar el Portapapeles. Para obtener más información, [vea Copiar una imagen de OpenGL en el Portapapeles.](copying-an-opengl-image-to-the-clipboard.md)

-   No se incluye la biblioteca de clases de C++ de Inventor 2.0.

    La biblioteca de clases de Inventor, creada sobre OpenGL, proporciona construcciones de nivel superior para programar gráficos 3D. No se incluye en la versión actual de la implementación de OpenGL de Microsoft para Windows.

-   No se admiten las siguientes características de formato de píxel: imágenes estereocopias, planos de bits alfa y búferes auxiliares.

    Sin embargo, hay compatibilidad con varios búferes auxiliares, incluidos: búfer de galería de símbolos, búfer de acumulación, búfer de reserva (almacenamiento en búfer doble), búfer de plano subyacente y superposición, y búfer de profundidad (eje Z).

 

 




