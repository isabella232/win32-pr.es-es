---
description: Cuando se encienden con una fuente de luz, los objetos desalmados (aquellos que usan materiales altamente reflectantes) reciben resaltados especulares.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Specular Light Mapas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55b4bf34baae0e73c2d072d62470533fc99827a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160434"
---
# <a name="specular-light-maps-direct3d-9"></a>Specular Light Mapas (Direct3D 9)

Cuando se encienden con una fuente de luz, los objetos desalmados (aquellos que usan materiales altamente reflectantes) reciben resaltados especulares. En algunos casos, los resaltados especulares generados por el módulo de iluminación no son precisos. Para generar un resaltado más atractivo, muchas aplicaciones de Direct3D aplican mapas de luz especulares a las primitivas.

Para realizar la asignación de luz especular, agregue el mapa de luz especular a la textura de la primitiva y luego modular (multiplique el resultado por) el mapa de luz RGB.

En el ejemplo de código siguiente se muestra este proceso en C++.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de luz con texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



