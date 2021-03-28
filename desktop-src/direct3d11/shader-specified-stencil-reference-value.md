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
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="9c66e-103">Valor de referencia de estarcido del sombreador especificado (gráficos de Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="9c66e-103">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="9c66e-104">Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="9c66e-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="9c66e-105">El valor especificado del sombreador reemplaza el valor de *referencia* de la galería de símbolos especificada por la API para esa invocación, lo que significa que el cambio afecta a la prueba de la galería de símbolos, y al D3D11 de la galería de símbolos operación de molde de la galería de símbolos de OP \_ \_ \_ (se usa un miembro de [**D3D11 \_ cliché \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) para escribir el valor de referencia en el búfer</span><span class="sxs-lookup"><span data-stu-id="9c66e-105">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="9c66e-106">En versiones anteriores de D3D11, el valor de referencia de la galería de símbolos solo puede especificarse mediante el método [**ID3D11DeviceContext:: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) .</span><span class="sxs-lookup"><span data-stu-id="9c66e-106">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="9c66e-107">Esto significa que este valor solo se puede definir en una granularidad por dibujo.</span><span class="sxs-lookup"><span data-stu-id="9c66e-107">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="9c66e-108">Esta característica D3D 11.3 permite a los desarrolladores leer y usar el valor de referencia de la galería de símbolos ( `SV_StencilRef` ) que se genera a partir de un sombreador de píxeles, lo que significa que se puede especificar en una granularidad por píxel o por muestra.</span><span class="sxs-lookup"><span data-stu-id="9c66e-108">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="9c66e-109">Esta característica es opcional en D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="9c66e-109">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="9c66e-110">Para probar su compatibilidad, compruebe el `PSSpecifiedStencilRefSupported` campo booleano de [**D3D11 de \_ D3D11 de datos de características \_ \_ \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) mediante [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="9c66e-110">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="9c66e-111">Este es un ejemplo del uso de `SV_StencilRef` en un sombreador de píxeles:</span><span class="sxs-lookup"><span data-stu-id="9c66e-111">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="9c66e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c66e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c66e-113">Características de Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="9c66e-113">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="9c66e-114">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="9c66e-114">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
