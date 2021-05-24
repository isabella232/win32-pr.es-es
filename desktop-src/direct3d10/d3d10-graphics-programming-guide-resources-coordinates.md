---
description: Los sistemas de coordenadas para Direct3D 10 se definen para píxeles y texturas.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemas de coordenadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3da846ae4b989f6d8cb4741f9df8f7228e8970
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335469"
---
# <a name="coordinate-systems-direct3d-10"></a>Sistemas de coordenadas (Direct3D 10)

Los sistemas de coordenadas para Direct3D 10 se definen para píxeles y texturas.



Diferencias entre Direct3D 9 y Direct3D 10:

- Direct3D 10 define la esquina superior izquierda del píxel superior izquierdo como el origen de un destino de representación.
- Direct3D 9 define el centro del píxel superior izquierdo como el origen de un destino de representación.



 

[Sistema de coordenadas de píxeles](#pixel-coordinate-system)
- [Sistema de coordenadas de píxeles para Direct3D 9](#pixel-coordinate-system-for-direct3d-9)

[Sistema de coordenadas de Texel](#texel-coordinate-system)
- [Sistema de coordenadas de Texel](#texel-coordinate-system)

[Temas relacionados](#related-topics)

## <a name="pixel-coordinate-system"></a>Sistema de coordenadas de píxeles

El sistema de coordenadas de píxeles de Direct3D 10 define el origen de un destino de representación en la esquina superior izquierda. como se muestra en el diagrama siguiente. Los centros de píxeles se desplazan por (0,5f,0,5f) desde ubicaciones de enteros.

![diagrama del sistema de coordenadas de píxeles en direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Sistema de coordenadas de píxeles para Direct3D 9

Como referencia, este es el sistema de coordenadas de píxeles para Direct3D 9, que definió el origen o un destino de representación como el centro del píxel superior izquierdo ,(0,5,0,5) fuera de la esquina superior izquierda, como se muestra en el diagrama siguiente. En Direct3D 9, los centros de píxeles están en ubicaciones enteras.

![diagrama del sistema de coordenadas de píxeles en direct3d 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Sistema de coordenadas de Texel

El sistema de coordenadas de texel tiene su origen en la esquina superior izquierda de la textura, como se muestra en el diagrama siguiente. Esto hace que la representación de texturas alineadas con la pantalla sea trivial (en Direct3D 10), ya que el sistema de coordenadas de píxeles está alineado con el sistema de coordenadas de texel.

![diagrama del sistema de coordenadas de texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Sistema de coordenadas de Texel

Las coordenadas de textura se representan con un número normalizado o escalado; Cada coordenada de textura se asigna a un elemento de textura específico como se muestra a continuación:

Para una coordenada normalizada:

-   Muestreo de punto: Texel \# = floor(U \* Width)
-   Muestreo lineal: Texel izquierdo \# = floor(U \* Width), Right Texel \# = Left Texel + \# 1

Para una coordenada a escala:

-   Muestreo de punto: Texel \# = floor(U)
-   Muestreo lineal: Texel izquierdo \# = floor(U - 0,5), Right Texel \# = Left Texel + \# 1

Donde el ancho es el ancho de la textura (en texturas).

El ajuste de la dirección de textura se produce después de calcular la ubicación del texel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




