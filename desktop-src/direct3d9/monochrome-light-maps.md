---
description: Algunos paneles de aceleradores 3D anteriores no admiten la combinación de texturas con el valor alfa del píxel de destino.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Monocromática Light Mapas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac6f62aaba08ac6c8e1116a0bc5059fed3dea19da51d83b034bfae79653ed5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728242"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Monocromática Light Mapas (Direct3D 9)

Algunos paneles de aceleradores 3D anteriores no admiten la combinación de texturas con el valor alfa del píxel de destino. Consulte [Alpha Texture Blending (Direct3D 9) para](alpha-texture-blending.md) obtener más información. Por lo general, estos adaptadores no admiten la combinación de varias texturas. Si la aplicación se ejecuta en un adaptador como este, puede usar la combinación de textura multipass para realizar la asignación de luz monocromática.

Para realizar la asignación de luz monocromática, una aplicación almacena la información de iluminación en los datos alfa de sus texturas de mapa claro. La aplicación usa las funcionalidades de filtrado de textura de Direct3D para realizar una asignación de cada píxel de la imagen primitiva a un elemento texel correspondiente en el mapa claro. Establece el factor de combinación de origen en el valor alfa del elemento de textura correspondiente.

En el ejemplo siguiente se muestra cómo una aplicación puede usar una textura como mapa de luz monocromática:


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



Dado que los adaptadores de pantalla que no admiten la combinación alfa de destino normalmente no admiten la combinación de varias texturas, en este ejemplo se establece el mapa claro como la primera textura, que está disponible en todas las tarjetas de acelerador 3D. El código de ejemplo establece la operación de color de la fase de mezcla de la textura para combinar los datos de textura con el color existente de la primitiva. A continuación, selecciona la primera textura y el color existente de la primitiva como datos de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de luz con texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



