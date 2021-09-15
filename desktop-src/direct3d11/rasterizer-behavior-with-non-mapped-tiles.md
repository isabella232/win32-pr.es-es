---
title: Comportamiento de rasterizador con iconos sin asignar
description: En esta sección se describe el comportamiento del rasterizador con iconos no asignados.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566216"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Comportamiento de rasterizador con iconos sin asignar

En esta sección se describe el comportamiento del rasterizador con iconos no asignados.

## <a name="depthstencilview"></a>DepthStencilView

El comportamiento de lecturas y escrituras de la vista de galería de símbolos de profundidad (DSV) depende del nivel de compatibilidad con hardware. Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura de los niveles [de características de recursos en mosaico.](tiled-resources-features-tiers.md)

Este es el comportamiento ideal:

Si un icono no está asignado en DepthStencilView, el valor devuelto de la profundidad de lectura es 0, que luego se introduce en las operaciones configuradas para el valor de lectura de profundidad. Se descartan las escrituras en el icono de profundidad que falta. Esta definición ideal para el control de escritura no es necesaria para [el nivel 2](tier-2.md); Las escrituras en iconos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recoger.

## <a name="rendertargetview"></a>RenderTargetView

El comportamiento de las lecturas y escrituras de la vista de destino de representación (RTV) depende del nivel de compatibilidad de hardware. Para ver un desglose de los requisitos, consulte el comportamiento general de lectura y escritura de los niveles [de características de recursos en mosaico.](tiled-resources-features-tiers.md)

En todas las implementaciones, diferentes RTV (y DSV) enlazados simultáneamente pueden tener distintas áreas asignadas frente a no asignadas y pueden tener diferentes formatos de superficie de tamaño (lo que significa diferentes formas de mosaico).

Este es el comportamiento ideal:

Las lecturas de RTV devuelven 0 en los iconos que faltan y las escrituras se descartan. Esta definición ideal para el control de escritura no es necesaria para [el nivel 2](tier-2.md); Las escrituras en iconos no asignados pueden acabar en una memoria caché que las lecturas posteriores podrían recoger.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




