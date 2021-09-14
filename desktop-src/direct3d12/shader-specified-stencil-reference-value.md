---
title: Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 12)
description: Obtenga información sobre el valor de referencia de galería de símbolos en gráficos de Direct3D 12. La habilitación de sombreadores de píxeles para usar el valor de referencia de galería de símbolos permite un control preciso sobre las operaciones de galería de símbolos.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072872"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 12)

La habilitación de sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control muy granular sobre las operaciones de galería de símbolos.

Normalmente, el método [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) especifica el valor de referencia de la galería de símbolos. Este método establece el valor de referencia de la galería de símbolos en una granularidad por dibujo. Sin embargo, el sombreador de píxeles puede sobrescribir este valor.

Esta característica D3D12 (y D3D11.3) permite a los desarrolladores leer y usar el valor de referencia de galería de símbolos *(SV \_ StencilRef)* que se genera desde un sombreador de píxeles, lo que permite una granularidad por píxel o por ejemplo.

El valor especificado del sombreador reemplaza el valor de referencia especificado por la API para esa invocación, lo que significa que el cambio afecta a la prueba de galería de símbolos y cuando se usa la operación de galería de símbolos D3D12 STENCIL OP REPLACE (un miembro de \_ \_ \_ [**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) para escribir el valor de referencia en el búfer de la galería de símbolos.

Esta característica es opcional en D3D12 y D3D11.3. Para comprobar su compatibilidad, compruebe el campo booleano *PSSpecifiedStencilRefSupported* de [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) mediante [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Este es un ejemplo del uso de *SV \_ StencilRef en* un sombreador de píxeles:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación](rendering.md)
</dt> <dt>

[Enlace de recursos en HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
