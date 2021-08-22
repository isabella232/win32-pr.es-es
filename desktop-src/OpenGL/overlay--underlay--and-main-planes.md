---
title: Superposición, subyacente y planos principales
description: Puede usar planos de capa de hardware (superposición y planos subyacentes) en las aplicaciones.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL en Windows, planos de capa de hardware
- planos de capa de hardware OpenGL
- overlay planes OpenGL
- Planos subyacentes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b968a0ab028fd0a699e31ad3a3601d7140435e2b36d0188bef46c5dca7cbad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936494"
---
# <a name="overlay-underlay-and-main-planes"></a>Superposición, subyacente y planos principales

Puede usar planos de capa de hardware (superposición y planos subyacentes) en las aplicaciones. Con Windows, los formatos de píxel describen las configuraciones de píxeles de un dispositivo gráfico. Cada formato de píxel describe la profundidad y otras características de los búferes de color principales y describe los búferes adicionales (como profundidad, acumulación, galería de símbolos y auxiliares) que usa el plano principal. Los formatos de píxel ahora se amplían para incluir búferes superpuestos y subyacentes.

Los planos de capa siempre tienen un búfer de color de la parte delantera izquierda y también pueden incluir búferes de color de la parte delantera derecha y posterior. Cada plano de capa tiene un contexto de representación específico para representar en los búferes de capa. No se pueden usar funciones de dibujo GDI en planos de capas.

Una ventana administra los búferes de color de los planos de capa de forma similar a la forma en que administra los búferes de color del plano principal. Puede mostrar varias ventanas con planos superpuestos o subyacentes al mismo tiempo. No puede tener ventanas superpuestas flotantes libres que puedan moverse sobre cualquier ventana del plano de dibujo principal. Además, dado que ocultaría los planos subyacentes en una ventana en todo momento, no se pueden usar planos emergentes de hardware que no tengan color transparente.

Cada plano de capa de una ventana tiene una paleta asociada. Puede establecer la paleta de un plano de capa de índice de color, pero la paleta de un plano de color RGBA es fija. Debe tener en cuenta la paleta adecuada cuando una ventana está en primer plano. Los planos de capa tienen un color de píxel transparente o un índice que permite mostrar los planos de capas subyacentes.

Puede copiar el estado de un contexto de representación en otro contexto de representación en un plano de capa independiente. También puede compartir listas de presentación entre contextos de representación en distintos planos de capas.

Las siguientes funciones se usan con planos de capa:

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




