---
title: Comportamiento de rasterizador con iconos sin asignar
description: En esta sección se describe el comportamiento de rasterizador con mosaicos no asignados.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996773"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Comportamiento de rasterizador con iconos sin asignar

En esta sección se describe el comportamiento de rasterizador con mosaicos no asignados.

## <a name="depthstencilview"></a>DepthStencilView

El comportamiento de las lecturas y escrituras de la vista de galería de símbolos de profundidad (DSV) depende del nivel de compatibilidad de hardware. Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura para [los niveles de características de los recursos en mosaico](tiled-resources-features-tiers.md).

Este es el comportamiento ideal:

Si un mosaico no se asigna en DepthStencilView, el valor devuelto de la profundidad de lectura es 0, que se introduce en las operaciones configuradas para el valor de lectura de profundidad. Las escrituras en el icono de profundidad que falta se quitan. Esta definición ideal para el control de escritura no es necesaria en el [nivel 2](tier-2.md); las escrituras en mosaicos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recogerse.

## <a name="rendertargetview"></a>RenderTargetView

El comportamiento de las lecturas y escrituras de la vista de destino de representación (RTV) depende del nivel de compatibilidad de hardware. Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura para [los niveles de características de los recursos en mosaico](tiled-resources-features-tiers.md).

En todas las implementaciones, los distintos RTVs (y DSV) enlazados simultáneamente pueden tener distintas áreas asignadas frente a no asignadas y pueden tener formatos de superficie de tamaño diferentes (lo que significa diferentes formas de mosaico).

Este es el comportamiento ideal:

Las lecturas de RTVs devuelven 0 en los mosaicos que faltan y las escrituras se quitan. Esta definición ideal para el control de escritura no es necesaria en el [nivel 2](tier-2.md); las escrituras en mosaicos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recogerse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




