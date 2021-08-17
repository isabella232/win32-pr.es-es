---
description: Las aplicaciones de Direct3D usan el escalado para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación. Las aplicaciones aplican lascales a las imágenes de primitivas para permitir que los polígonos coplanares se represente correctamente.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Escalado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16b07eefcbf43bf2a3c71deb1a1073a656bb8d637696af71484a7a3e478ff8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910221"
---
# <a name="decaling-direct3d-9"></a>Escalado (Direct3D 9)

Las aplicaciones de Direct3D usan el escalado para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación. Las aplicaciones aplican lascales a las imágenes de primitivas para permitir que los polígonos coplanares se represente correctamente.

Por ejemplo, al aplicar marcas de rueda y líneas amarillas a un camino, las marcas deben aparecer directamente encima de la carretera. Sin embargo, los valores z de las marcas y la carretera son los mismos. Por lo tanto, es posible que el búfer de profundidad no produzca una separación limpia entre los dos. Algunos píxeles de la primitiva inversa se pueden representar encima de la primitiva frontal y viceversa. La imagen resultante parece resplandeciente de marco a marco. Este efecto se denomina *z-fighting* o *flimmering.*

Para solucionar este problema, use una galería de símbolos para enmascarar la sección de la primitiva de reserva donde aparecerá la calcomanía. Desactive el almacenamiento en búfer z y represente la imagen de la primitiva frontal en el área enmascarada de la superficie de destino de representación.

Aunque se puede usar la combinación de varias texturas para resolver este problema, al hacerlo se limita el número de otros efectos especiales que puede producir la aplicación. El uso del búfer de galería de símbolos para aplicar lascales libera las fases de mezcla de textura para otros efectos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de galería de símbolos](stencil-buffer-techniques.md)
</dt> </dl>

 

 



