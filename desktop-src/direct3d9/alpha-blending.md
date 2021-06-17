---
description: Obtenga información sobre la combinación alfa. La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Combinación alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262007"
---
# <a name="alpha-blending-direct3d-9"></a>Combinación alfa (Direct3D 9)

La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes. Además de un canal de color rojo, verde y azul, cada píxel de un mapa de bits alfa tiene un componente de transparencia conocido como su canal alfa. El canal alfa normalmente contiene tantos bits como un canal de color. Por ejemplo, un canal alfa de 8 bits puede representar 256 niveles de transparencia, de 0 (el píxel completo es transparente) a 255 (el píxel completo es opaco). En la lista siguiente se muestran algunos efectos especiales que puede crear mediante la combinación alfa.

El color se puede definir con o sin valores alfa. Color sin alfa es color RGB con alfa se almacena como ARGB. Los datos de vértice, los datos de material y los datos de textura se pueden usar para proporcionar transparencia al objeto. El búfer de fotogramas también se puede usar para generar efectos de transparencia.

-   [Vértice alfa (Direct3D 9)](vertex-alpha.md)
-   [Material Alfa (Direct3D 9)](material-alpha.md)
-   [Alfa de textura (Direct3D 9)](texture-alpha.md)
-   [Búfer de fotogramas alfa (Direct3D 9)](frame-buffer-alpha.md)
-   [Destino de representación alfa (Direct3D 9)](render-target-alpha.md)

Entre los ejemplos que muestran alfa se incluyen:

-   [Afición (Direct3D 9)](billboarding.md)
-   [Nubes, humo y pistas de Esquí (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Fire, Fires, and Explosions (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



