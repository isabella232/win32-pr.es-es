---
description: El motor de iluminación combina el color del material, el color del vértice y la información de iluminación para generar un color por vértice.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Mezcla de textura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060788"
---
# <a name="alpha-texture-blending-direct3d-9"></a>Mezcla de textura alfa (Direct3D 9)

El motor de iluminación combina el color del material, el color del vértice y la información de iluminación para generar un color por vértice. Una vez interpolado, se genera un color por píxel que se escribe en el búfer de fotogramas. Si una aplicación habilita la mezcla de texturas, el color de píxel se convertirá en una combinación del píxel actual en el búfer del marco y un color de textura.

Esta fórmula determina el color final de píxel combinado:


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



Donde:

-   Color es el color de píxel de salida.
-   TexelColor es el color de entrada después del filtrado de textura.
-   SourceBlend es el porcentaje del color del píxel final que se forma con el color de textura de origen.
-   CurrentPixelColor es el color del píxel actual.
-   DestBlend es el porcentaje del color del píxel final que se forma con el color de píxel actual.

La ecuación de mezcla final se establece llamando a [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) y especificando el estado de representación de mezcla (D3DRS BLENDXXX) con un factor de mezcla correspondiente \_ ([**D3DBLEND**](./d3dblend.md)). Los valores de SourceBlend y DestBlend oscilan entre 0,0 (transparente) y 1,0 (opaco) ambos inclusive. Además, una aplicación puede controlar la transparencia de un píxel estableciendo el valor alfa en una textura. En este caso, use lo siguiente:


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



La ecuación de mezcla hará que el píxel representado sea transparente. Los valores predeterminados son:


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mezcla de texturas](texture-blending.md)
</dt> <dt>

[Filtrado de texturas (Direct3D 9)](texture-filtering.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
