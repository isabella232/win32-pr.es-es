---
description: Normalmente, la aplicación representará escenas 3D de manera más realista si usa mapas de colores claros. Una asignación de luz en color utiliza los datos RGB en el mapa de luz para su información de iluminación.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Mapas de luz de color (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496133"
---
# <a name="color-light-maps-direct3d-9"></a>Mapas de luz de color (Direct3D 9)

Normalmente, la aplicación representará escenas 3D de manera más realista si usa mapas de colores claros. Una asignación de luz en color utiliza los datos RGB en el mapa de luz para su información de iluminación.

En el ejemplo de código de C++ siguiente se muestra la asignación de luz con datos de color RGB.


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



En este ejemplo se establece el mapa de luz como la primera textura. A continuación, establece el estado de la primera fase de mezcla para modular los datos de texturas entrantes. Usa la primera textura y el color actual de la primitiva como argumentos para la operación modular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de luz con texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



