---
description: La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Combinación alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153307"
---
# <a name="alpha-blending-direct3d-9"></a>Combinación alfa (Direct3D 9)

La combinación alfa se usa para mostrar una imagen que tiene píxeles transparentes o semitransparentes. Además de un canal de color rojo, verde y azul, cada píxel de un mapa de bits alfa tiene un componente de transparencia conocido como canal alfa. Normalmente, el canal alfa contiene tantos bits como un canal de color. Por ejemplo, un canal alfa de 8 bits puede representar 256 niveles de transparencia, desde 0 (todo el píxel es transparente) hasta 255 (todo el píxel es opaco). En la siguiente lista se muestran algunos efectos especiales que se pueden crear mediante la combinación alfa.

El color puede definirse con o sin valores alfa. El color sin alfa es un color RGB con alfa almacenado como ARGB. Los datos de vértices, datos de materiales y datos de textura se pueden usar para proporcionar transparencia del objeto. El búfer de fotogramas también se puede utilizar para generar efectos de transparencia.

-   [Vértice alfa (Direct3D 9)](vertex-alpha.md)
-   [Material alfa (Direct3D 9)](material-alpha.md)
-   [Textura alfa (Direct3D 9)](texture-alpha.md)
-   [Búfer de trama alfa (Direct3D 9)](frame-buffer-alpha.md)
-   [Alfa de destino de representación (Direct3D 9)](render-target-alpha.md)

Los ejemplos que muestran Alpha incluyen:

-   [Cartelera (Direct3D 9)](billboarding.md)
-   [Nubes, humo y rastros de vapor (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Fuego, destellos y explosiones (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación en Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



