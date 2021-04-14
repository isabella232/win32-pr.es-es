---
title: Superposición, proporcionaban y planos principales
description: Puede usar planos de capa de hardware (planos superpuestos y proporcionaban) en sus aplicaciones.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL en Windows, planos de capas de hardware
- planos de capa de hardware OpenGL
- planos superpuesto OpenGL
- proporcionaban de los aviones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665650"
---
# <a name="overlay-underlay-and-main-planes"></a>Superposición, proporcionaban y planos principales

Puede usar planos de capa de hardware (planos superpuestos y proporcionaban) en sus aplicaciones. Con Windows, los formatos de píxel describen las configuraciones de píxeles de un dispositivo de gráficos. Cada formato de píxel describe la profundidad y otras características de los búferes de color principales y describe los búferes adicionales (como profundidad, acumulación, estarcido y auxiliar) que usa el plano principal. Los formatos de píxel ahora se han ampliado para incluir búferes de superposición y proporcionaban.

Los planos de capa siempre tienen un búfer de color Front-Left y también pueden incluir búferes de color frontal y derecho. Cada plano de capa tiene un contexto de representación específico para representar en los búferes de capas. No se pueden usar las funciones de dibujo de GDI en los planos de capas.

Una ventana administra los búferes de color de los planos de capa de forma similar al modo en que administra los búferes de color del plano principal. Puede mostrar varias ventanas con planos superpuestos y/o proporcionaban al mismo tiempo. No puede tener ventanas de superposición de libre flotante que puedan moverse sobre cualquier ventana del plano de dibujo principal. Además, dado que ocultaría los planos subyacentes en una ventana en todo momento, no puede usar planos emergentes de hardware que no tengan ningún color transparente.

Cada plano de capa de una ventana tiene una paleta asociada. Puede establecer la paleta de un plano de capas de índice de color, pero la paleta de un plano de color RGBA es fija. Debe obtener la paleta adecuada cuando una ventana está en primer plano. Los planos de capa tienen un color o índice de píxeles transparente que permite que se muestren los planos de capas subyacentes.

Puede copiar el estado de un contexto de representación en otro contexto de representación en un plano de capas independiente. También puede compartir listas de visualización entre los contextos de representación en diferentes planos de capas.

Las siguientes funciones se usan con planos de capas:

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




