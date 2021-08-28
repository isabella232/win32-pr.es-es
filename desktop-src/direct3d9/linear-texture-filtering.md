---
description: Direct3D usa una forma de filtrado de textura lineal denominado filtrado bilineal.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtrado de textura lineal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5177af653c74383ef87468dbb43167fa2962cd093410a6a63f85da2233e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628535"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Filtrado de textura lineal (Direct3D 9)

Direct3D usa una forma de filtrado de textura lineal denominado filtrado bilineal. Al igual que el muestreo de punto más cercano [(Direct3D 9),](nearest-point-sampling.md)el filtrado de textura bilineal calcula primero una dirección de textura, que normalmente no es una dirección entera. A continuación, el filtrado bilineal busca el texel cuya dirección de entero está más cercana a la dirección calculada. Además, el módulo de representación de Direct3D calcula una media ponderada de los elementos de textura que están inmediatamente por encima, debajo, a la izquierda de y a la derecha del punto de muestra más cercano.

Seleccione el filtrado de texturas bilineal invocando el [**método IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que va a seleccionar un método de filtrado de textura. Pase D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER para el segundo parámetro para establecer el filtro \_ \_ de ampliación, minificación o mipmapping. Pase D3DTEXF \_ LINEAR en el tercer parámetro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de texturas](texture-filtering.md)
</dt> </dl>

 

 
