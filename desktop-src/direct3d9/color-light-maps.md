---
description: Normalmente, la aplicación representará escenas 3D de forma más realista si usa mapas claros de color. Un mapa de luz coloreado usa los datos RGB en el mapa de luz para su información de iluminación.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Color Light Mapas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbff9fe246131fc90bda8ac9b5f1c49cd2413c412a7b3da5c013b1e936aa6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989305"
---
# <a name="color-light-maps-direct3d-9"></a>Color Light Mapas (Direct3D 9)

Normalmente, la aplicación representará escenas 3D de forma más realista si usa mapas claros de color. Un mapa de luz coloreado usa los datos RGB en el mapa de luz para su información de iluminación.

En el siguiente ejemplo de código de C++ se muestra la asignación de luz con datos de color RGB.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



En este ejemplo se establece el mapa claro como la primera textura. A continuación, establece el estado de la primera fase de mezcla para modular los datos de textura entrantes. Usa la primera textura y el color actual de la primitiva como argumentos para la operación de modular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de luz con texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



