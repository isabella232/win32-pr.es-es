---
title: Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 11)
description: Obtenga información sobre el valor de referencia de galería de símbolos en gráficos de Direct3D 11. La habilitación de sombreadores de píxeles para usar el valor de referencia de galería de símbolos permite un control preciso sobre las operaciones de galería de símbolos.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e8a34d53bc7f30dc2a91fafabb561dff7a1e96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060806"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 11)

La habilitación de sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control muy granular sobre las operaciones de galería de símbolos.

El valor especificado del sombreador reemplaza  el valor de referencia de galería de símbolos especificado por la API para esa invocación, lo que significa que el cambio afecta a la prueba de galería de símbolos y cuando stencil op D3D11 STENCIL OP REPLACE (un miembro de \_ \_ \_ [**D3D11 \_ STENCIL \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) se usa para escribir el valor de referencia en el búfer de la galería de símbolos.

En versiones anteriores de D3D11, el valor de referencia de la galería de símbolos solo se puede especificar mediante el método [**ID3D11DeviceContext::OMSetDepthStencilState.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) Esto significa que este valor solo se puede definir en una granularidad por dibujo. Esta característica D3D11.3 permite a los desarrolladores leer y usar el valor de referencia de galería de símbolos ( ) que se genera desde un sombreador de píxeles, lo que significa que se puede especificar en una granularidad por píxel o por `SV_StencilRef` ejemplo.

Esta característica es opcional en D3D11.3. Para comprobar su compatibilidad, compruebe el campo `PSSpecifiedStencilRefSupported` booleano [**de D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) con [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Este es un ejemplo del uso de en `SV_StencilRef` un sombreador de píxeles:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11.3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
