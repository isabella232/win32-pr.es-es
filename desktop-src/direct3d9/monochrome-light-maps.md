---
description: Algunas placas de aceleradores 3D anteriores no admiten la combinación de texturas mediante el valor alfa del píxel de destino.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Mapas de luz monocroma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696070"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Mapas de luz monocroma (Direct3D 9)

Algunas placas de aceleradores 3D anteriores no admiten la combinación de texturas mediante el valor alfa del píxel de destino. Consulte [combinación de texturas alfa (Direct3D 9)](alpha-texture-blending.md) para obtener más información. Normalmente, estos adaptadores no admiten la combinación de texturas múltiples. Si la aplicación se ejecuta en un adaptador como este, puede usar la combinación de texturas Multipass para realizar la asignación de luz monocromática.

Para realizar la asignación de luz monocromática, una aplicación almacena la información de iluminación en los datos alfa de sus texturas de mapa ligero. La aplicación utiliza las capacidades de filtrado de texturas de Direct3D para realizar una asignación desde cada píxel de la imagen de primitiva a un textura correspondiente en el mapa de luz. Establece el factor de fusión de origen en el valor alfa del textura correspondiente.

En el ejemplo siguiente se muestra cómo una aplicación puede usar una textura como mapa de luz monocroma:


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



Dado que los adaptadores de pantalla que no admiten la combinación alfa de destino normalmente no admiten la combinación de texturas múltiples, este ejemplo establece el mapa de luz como la primera textura, que está disponible en todas las tarjetas aceleradoras 3D. El código de ejemplo establece la operación de color para que la fase de fusión de la textura mezcle los datos de textura con el color existente del primitivo. A continuación, selecciona la primera textura y el color existente del primitivo como los datos de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de luz con texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



