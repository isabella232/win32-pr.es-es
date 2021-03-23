---
title: Valor de referencia de estarcido del sombreador especificado (gráficos de Direct3D 12)
description: Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104549131"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Valor de referencia de estarcido del sombreador especificado (gráficos de Direct3D 12)

Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.

Normalmente, el valor de referencia de la galería de símbolos se especifica mediante el método [**ID3D12GraphicsCommandList:: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) . Este método establece el valor de referencia de la galería de símbolos en una granularidad por dibujo. Sin embargo, este valor se puede sobrescribir con el sombreador de píxeles.

Esta característica D3D12 (y D3D 11.3) permite a los desarrolladores leer y usar el valor de referencia de la galería de símbolos (*VP \_ StencilRef*) que se genera desde un sombreador de píxeles, lo que permite una granularidad por píxel o por muestra.

El valor especificado del sombreador reemplaza el valor de referencia especificado por la API para esa invocación, lo que significa que el cambio afecta a la prueba de la galería de símbolos y, cuando la operación de estarcido D3D12 de la galería de símbolos de la operación \_ \_ de estarcido \_ Replace (un miembro de [**D3D12 \_ cliché \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) se usa para escribir el valor de referencia en el búfer de estarcido.

Esta característica es opcional en D3D12 y D3D 11.3. Para probar su compatibilidad, consulte el campo booleano *PSSpecifiedStencilRefSupported* de [**\_ \_ \_ \_ las opciones de D3D12 de datos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) con [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Este es un ejemplo del uso de *\_ StencilRef de SV* en un sombreador de píxeles:

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

[Modelo de sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
