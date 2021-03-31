---
description: Los sistemas de coordenadas para Direct3D 10 se definen para los píxeles y textura.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemas de coordenadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807879"
---
# <a name="coordinate-systems-direct3d-10"></a>Sistemas de coordenadas (Direct3D 10)

Los sistemas de coordenadas para Direct3D 10 se definen para los píxeles y textura.



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> Direct3D 10 define la esquina superior izquierda del píxel superior izquierdo como el origen de un destino de representación.<br/> Direct3D 9 define el centro del píxel superior izquierdo como el origen de un destino de representación.<br/> |



 

-   [Sistema de coordenadas de píxeles](#pixel-coordinate-system)
    -   [Sistema de coordenadas de píxeles para Direct3D 9](#pixel-coordinate-system-for-direct3d-9)
-   [Sistema de coordenadas textura](#texel-coordinate-system)
    -   [Sistema de coordenadas textura](#texel-coordinate-system)
-   [Temas relacionados](#related-topics)

## <a name="pixel-coordinate-system"></a>Sistema de coordenadas de píxeles

El sistema de coordenadas de píxeles en Direct3D 10 define el origen de un destino de representación en la esquina superior izquierda. tal y como se muestra en el diagrama siguiente. Los centros de píxeles se desplazan por (0.5 f, 0.5 f) desde las ubicaciones de enteros.

![diagrama del sistema de coordenadas de píxeles en Direct3D 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Sistema de coordenadas de píxeles para Direct3D 9

Como referencia, este es el sistema de coordenadas de píxeles para Direct3D 9, que definía el origen o un destino de representación como centro del píxel superior izquierdo, (0.5, 0.5) fuera de la esquina superior izquierda, como se muestra en el diagrama siguiente. En Direct3D 9, los centros de píxeles están en ubicaciones de enteros.

![diagrama del sistema de coordenadas de píxeles en Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Sistema de coordenadas textura

El sistema de coordenadas textura tiene su origen en la esquina superior izquierda de la textura, tal como se muestra en el diagrama siguiente. Esto hace que la representación de las texturas alineadas en la pantalla sea trivial (en Direct3D 10), ya que el sistema de coordenadas de píxeles se alinea con el sistema de coordenadas textura.

![diagrama del sistema de coordenadas textura](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Sistema de coordenadas textura

Las coordenadas de textura se representan con un número normalizado o escalado; cada coordenada de textura se asigna a un textura específico como se indica a continuación:

Para una coordenada normalizada:

-   Muestreo de punto: textura \# = Floor (U \* ancho)
-   Muestreo lineal: Left textura \# = Floor (U \* width), Right textura \# = left textura \# + 1

Para una coordenada escalada:

-   Muestreo de punto: textura \# = Floor (U)
-   Muestreo lineal: Left textura \# = Floor (U-0,5), Right textura \# = left textura \# + 1

Donde el ancho es el ancho de la textura (en textura).

El ajuste de la dirección de textura se produce después de calcular la ubicación de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




