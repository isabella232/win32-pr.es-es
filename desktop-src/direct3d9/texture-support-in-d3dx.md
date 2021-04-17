---
description: D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Compatibilidad con texturas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705189"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Compatibilidad con texturas en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

## <a name="textures"></a>Texturas

En los temas siguientes se admiten muchas texturas diferentes.

-   Compatibilidad con la textura de mipmapped estándar. Vea [generación automática de mapas MIP (Direct3D 9)](automatic-generation-of-mipmaps.md).
-   Compatibilidad con mapas de cubos. Vea [asignación de entorno cúbica (Direct3D 9)](cubic-environment-mapping.md).
-   Compatibilidad con texturas de volumen. Vea [recursos de textura de volumen (Direct3D 9)](volume-texture-resources.md).
-   Compatibilidad con la asignación de entorno. Consulte [asignación de entorno (Direct3D 9)](environment-mapping.md).
-   Compatibilidad con la asignación de rugosidad. Vea [asignación de rugosidad (Direct3D 9)](bump-mapping.md).

### <a name="texture-color-conversion"></a>Conversión de color de textura

Al usar cualquiera de las funciones D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, es posible que sea necesario realizar la conversión de colores. Por ejemplo, una superficie podría ser de tipo RGBA y la otra podría ser UVWQ. En los casos de formatos distintos, la secuencia de conversión es la siguiente:

### <a name="mapping-rgba-to-uvwq"></a>Asignación de RGBA a UVWQ

-   R <-> U, el canal R está asignado al canal U, o viceversa.
-   G <-> V, el canal G está asignado al canal V, o viceversa.
-   B <-> W, el canal B está asignado al canal W, o viceversa.
-   Una < > Q/L, se asigna un canal al canal Q o L (en función de cuál esté disponible en el formato de destino), o viceversa.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Asignación de UV a RGBA

-   U <-> R, el canal U está asignado al canal R, o viceversa.
-   V <-> G, el canal V está asignado al canal G, o viceversa.
-   1 <-> B, 1 se asigna al canal B, o viceversa.
-   1 <-> a, 1 se asigna a un canal, o viceversa.

Si un canal no existe en el origen, se supone que es 1 (con la excepción de A8, donde R, G, B se supone que es 0). Por ejemplo:


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



