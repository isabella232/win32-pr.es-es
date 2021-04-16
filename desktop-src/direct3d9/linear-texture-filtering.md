---
description: Direct3D usa una forma de filtrado de textura lineal denominada filtrado bilineal.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtrado de textura lineal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537599"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Filtrado de textura lineal (Direct3D 9)

Direct3D usa una forma de filtrado de textura lineal denominada filtrado bilineal. Al igual que [el muestreo de punto más cercano (Direct3D 9)](nearest-point-sampling.md), el filtrado de textura bilineal calcula primero una dirección textura, que normalmente no es una dirección entera. A continuación, el filtrado bilineal busca el textura cuya dirección de entero está más cercana a la dirección calculada. Además, el módulo de representación de Direct3D calcula una media ponderada de los textura que están inmediatamente por encima, a la izquierda y a la derecha del punto de ejemplo más próximo.

Seleccione el filtrado de textura bilineal invocando el método [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que está seleccionando un método de filtrado de textura. Pase D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER para el segundo parámetro con el fin de establecer el filtro de ampliación, minificación o mipmapping. Pase D3DTEXF \_ linear en el tercer parámetro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de textura](texture-filtering.md)
</dt> </dl>

 

 
