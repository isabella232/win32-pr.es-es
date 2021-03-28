---
title: Valor de referencia de estarcido del sombreador especificado (gráficos de Direct3D 11)
description: Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a089ec8ab56a1cf00021f97bb40cf86fe42f04
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359599"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Valor de referencia de estarcido del sombreador especificado (gráficos de Direct3D 11)

Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.

El valor especificado del sombreador reemplaza el valor de *referencia* de la galería de símbolos especificada por la API para esa invocación, lo que significa que el cambio afecta a la prueba de la galería de símbolos, y al D3D11 de la galería de símbolos operación de molde de la galería de símbolos de OP \_ \_ \_ (se usa un miembro de [**D3D11 \_ cliché \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) para escribir el valor de referencia en el búfer

En versiones anteriores de D3D11, el valor de referencia de la galería de símbolos solo puede especificarse mediante el método [**ID3D11DeviceContext:: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) . Esto significa que este valor solo se puede definir en una granularidad por dibujo. Esta característica D3D 11.3 permite a los desarrolladores leer y usar el valor de referencia de la galería de símbolos ( `SV_StencilRef` ) que se genera a partir de un sombreador de píxeles, lo que significa que se puede especificar en una granularidad por píxel o por muestra.

Esta característica es opcional en D3D 11.3. Para probar su compatibilidad, compruebe el `PSSpecifiedStencilRefSupported` campo booleano de [**D3D11 de \_ D3D11 de datos de características \_ \_ \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) mediante [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Este es un ejemplo del uso de `SV_StencilRef` en un sombreador de píxeles:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo de sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
