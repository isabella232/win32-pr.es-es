---
title: Limitaciones
description: Limitaciones
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL on Windows,limitations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171369"
---
# <a name="limitations"></a>Limitaciones

La implementación genérica tiene las siguientes limitaciones:

-   Impresión.

    Puede imprimir una imagen openGL directamente en una impresora solo mediante metarchivos. Para obtener más información, vea [Printing an OpenGL Image](printing-an-opengl-image.md).

-   Los gráficos OpenGL y GDI no se pueden mezclar en una ventana de doble búfer.

    Una aplicación puede dibujar directamente gráficos OpenGL y gráficos GDI en una ventana de un solo búfer, pero no en una ventana de doble búfer.

-   No hay paletas de colores de hardware por ventana.

    Windows una paleta de colores de hardware del sistema única, que se aplica a toda la pantalla. Una ventana OpenGL no puede tener su propia paleta de hardware, pero puede tener su propia paleta lógica. Para ello, debe convertirse en una aplicación que tenga en cuenta la paleta. Para obtener más información, vea [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).

-   No hay compatibilidad directa con el Portapapeles, el intercambio dinámico de datos (DDE) ni OLE.

    Una ventana con gráficos OpenGL no admite directamente estas Windows funcionalidades. Sin embargo, hay soluciones alternativas para usar el Portapapeles. Para obtener más información, [vea Copiar una imagen OpenGL en el Portapapeles.](copying-an-opengl-image-to-the-clipboard.md)

-   No se incluye la biblioteca de clases de C++ de Inventor 2.0.

    La biblioteca de clases de Inventor, creada sobre OpenGL, proporciona construcciones de nivel superior para programar gráficos 3D. No se incluye en la versión actual de la implementación de OpenGL de Microsoft para Windows.

-   No se admiten las siguientes características de formato de píxel: imágenes estereoplano, planos de bits alfa y búferes auxiliares.

    Sin embargo, hay compatibilidad con varios búferes auxiliares, incluidos: búfer de galería de símbolos, búfer de acumulación, búfer de reserva (almacenamiento en búfer doble), búfer de plano subyacente y superposición y búfer de profundidad (eje z).

 

 




