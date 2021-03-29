---
title: Limitaciones
description: Limitaciones
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL en Windows, limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775259"
---
# <a name="limitations"></a>Limitaciones

La implementación genérica tiene las siguientes limitaciones:

-   Impresión.

    Puede imprimir una imagen de OpenGL directamente en una impresora solo con metaarchivos. Para obtener más información, consulte [Imprimir una imagen de OpenGL](printing-an-opengl-image.md).

-   Los gráficos de OpenGL y GDI no se pueden mezclar en una ventana de búfer doble.

    Una aplicación puede dibujar directamente gráficos OpenGL y gráficos GDI en una ventana de un solo búfer, pero no en una ventana de búfer doble.

-   No hay paletas de colores de hardware por ventana.

    Windows tiene una sola paleta de colores de hardware del sistema, que se aplica a toda la pantalla. Una ventana de OpenGL no puede tener su propia paleta de hardware, pero puede tener su propia paleta lógica. Para ello, debe convertirse en una aplicación que tenga en cuenta la paleta. Para obtener más información, vea [modos de color OpenGL y administración de la paleta de Windows](opengl-color-modes-and-windows-palette-management.md).

-   No hay compatibilidad directa con el portapapeles, el intercambio dinámico de datos (DDE) o OLE.

    Una ventana con gráficos OpenGL no es compatible directamente con estas funciones de Windows. Sin embargo, hay soluciones alternativas para usar el portapapeles. Para obtener más información, vea [copiar una imagen de OpenGL en el portapapeles](copying-an-opengl-image-to-the-clipboard.md).

-   No se incluye la biblioteca de clases de C++ de inventor 2,0.

    La biblioteca de clases Inventory, que se basa en OpenGL, proporciona construcciones de nivel superior para programar gráficos 3D. No se incluye en la versión actual de la implementación de OpenGL para Windows de Microsoft.

-   No se admiten las siguientes características de formato de píxel: imágenes Stereoscopic, bitplanes alfa y búferes auxiliares.

    Sin embargo, hay compatibilidad con varios búferes auxiliares, entre los que se incluyen: búfer de estarcido, búfer de acumulación, búfer de reserva (doble búfer), superposición y búfer de plano de proporcionaban y búfer de profundidad (eje z).

 

 




