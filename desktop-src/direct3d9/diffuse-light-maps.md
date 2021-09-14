---
description: Cuando se encienden con una fuente de luz, las superficies de superficie de superficie muestran reflexión de luz difusa.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Difuso Mapas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab6a85fb93bc1ebcc15735431c1d54be4482a1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888620"
---
# <a name="diffuse-light-maps-direct3d-9"></a>Difuso Mapas (Direct3D 9)

Cuando se encienden con una fuente de luz, las superficies de superficie de superficie muestran reflexión de luz difusa. El brillo de la luz difusa depende de la distancia desde la fuente de luz y del ángulo entre la superficie normal y el vector de dirección de la fuente de luz. Los efectos de iluminación difusa simulados por los cálculos de iluminación solo producen efectos generales.

La aplicación puede simular una iluminación difusa más compleja con mapas de luz de textura. Para ello, agregue el mapa de luz difuso a la textura base, como se muestra en el siguiente ejemplo de código de C++.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de luz con texturas](light-mapping-with-textures.md)
</dt> </dl>

 

 



