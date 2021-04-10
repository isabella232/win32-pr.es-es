---
description: Las aplicaciones de Direct3D usan las marcas para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación. Las aplicaciones aplican marcas a las imágenes de primitivas para permitir que los polígonos coplanoles se representen correctamente.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Marcas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152121"
---
# <a name="decaling-direct3d-9"></a>Marcas (Direct3D 9)

Las aplicaciones de Direct3D usan las marcas para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación. Las aplicaciones aplican marcas a las imágenes de primitivas para permitir que los polígonos coplanoles se representen correctamente.

Por ejemplo, al aplicar las marcas de neumático y las líneas amarillas a un Roadway, las marcas deben aparecer directamente encima de la carretera. Sin embargo, los valores z de las marcas y la carretera son los mismos. Por lo tanto, es posible que el búfer de profundidad no produzca una separación limpia entre ambos. Algunos píxeles de la primitiva inversa se pueden representar encima de la primitiva delantera y viceversa. La imagen resultante parece Shimmer de fotograma a fotograma. Este efecto se denomina *lucha z* o *flimmering*.

Para solucionar este problema, use una galería de símbolos para enmascarar la sección de la primitiva inversa en la que aparecerá la calcomanía. Desactive el almacenamiento en búfer z y represente la imagen de la primitiva delantera en el área enmascarada de la superficie de representación-destino.

Aunque se puede usar varias combinaciones de texturas para solucionar este problema, al hacerlo se limita el número de otros efectos especiales que puede producir la aplicación. El uso del búfer de la galería de símbolos para aplicar marcas libera las fases de fusión de texturas para otros efectos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de estarcido](stencil-buffer-techniques.md)
</dt> </dl>

 

 



