---
description: Obtenga información sobre la compatibilidad con texturas en D3DX. D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Compatibilidad con texturas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ba518a5e9158c0337d45485852675d4ab91ef3585f027bd78fc51164c40466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026025"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Compatibilidad con texturas en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

## <a name="textures"></a>Texturas

En los temas siguientes se admiten muchas texturas diferentes.

-   Compatibilidad con textura mipmapped estándar. Consulte [Generación automática de mapas Mip (Direct3D 9).](automatic-generation-of-mipmaps.md)
-   Compatibilidad con mapas de cubos. Vea [Asignación de entorno cúbica (Direct3D 9).](cubic-environment-mapping.md)
-   Compatibilidad con texturas de volumen. Consulte [Recursos de textura de volumen (Direct3D 9).](volume-texture-resources.md)
-   Compatibilidad con la asignación de entornos. Consulte [Asignación de entorno (Direct3D 9).](environment-mapping.md)
-   Compatibilidad con la asignación de protuberancias. Consulte [Asignación de protuberancias (Direct3D 9).](bump-mapping.md)

### <a name="texture-color-conversion"></a>Conversión de color de textura

Al usar cualquiera de las funciones D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, es posible que sea necesario realizar la conversión de color. Por ejemplo, una superficie podría ser de tipo RGBA y la otra podría ser UVWQ. Para los casos de formatos diferentes, la secuencia de conversión es la siguiente:

### <a name="mapping-rgba-to-uvwq"></a>Asignación de RGBA a UVWQ

-   R <-> U, el canal de R se asigna al canal U o viceversa.
-   G <-> V, el canal G se asigna al canal V o viceversa.
-   B <-> W, el canal B se asigna al canal W o viceversa.
-   Un <-> Q/L, un canal se asigna al canal Q o L (dependiendo de cuál esté disponible en el formato de destino) o viceversa.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Asignación de UV a RGBA

-   U <-> R, el canal U se asigna al canal de R o viceversa.
-   V <-> G, el canal V se asigna al canal G o viceversa.
-   1 <-> B, 1 se asigna al canal B o viceversa.
-   1 <-> A, 1 se asigna al canal A o viceversa.

Si un canal no existe en el origen, se supone que es 1 (a excepción de A8, donde se supone que R,G,B es 0). Por ejemplo:


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

 

 



