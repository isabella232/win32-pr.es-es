---
title: Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 11)
description: Obtenga información sobre el valor de referencia de galería de símbolos en gráficos de Direct3D 11. La habilitación de sombreadores de píxeles para usar el valor de referencia de galería de símbolos permite un control preciso sobre las operaciones de galería de símbolos.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e8a34d53bc7f30dc2a91fafabb561dff7a1e96
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408108"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="f6a0a-104">Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f6a0a-104">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="f6a0a-105">La habilitación de sombreadores de píxeles para generar el valor de referencia de galería de símbolos, en lugar de usar el especificado por la API, permite un control muy específico sobre las operaciones de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="f6a0a-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="f6a0a-106">El valor especificado del sombreador reemplaza  el valor de referencia de galería de símbolos especificado por la API para esa invocación, lo que significa que el cambio afecta tanto a la prueba de galería de símbolos como cuando se usa stencil op D3D11 STENCIL OP REPLACE (un miembro de \_ \_ \_ [**D3D11 \_ STENCIL \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) para escribir el valor de referencia en el búfer de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="f6a0a-106">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="f6a0a-107">En versiones anteriores de D3D11, el valor de referencia de la galería de símbolos solo se puede especificar mediante el [**método ID3D11DeviceContext::OMSetDepthStencilState.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate)</span><span class="sxs-lookup"><span data-stu-id="f6a0a-107">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="f6a0a-108">Esto significa que este valor solo se puede definir en una granularidad por dibujo.</span><span class="sxs-lookup"><span data-stu-id="f6a0a-108">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="f6a0a-109">Esta característica D3D11.3 permite a los desarrolladores leer y usar el valor de referencia de galería de símbolos ( ) que se genera desde un sombreador de píxeles, lo que significa que se puede especificar en una granularidad por píxel o por `SV_StencilRef` ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f6a0a-109">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="f6a0a-110">Esta característica es opcional en D3D11.3.</span><span class="sxs-lookup"><span data-stu-id="f6a0a-110">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="f6a0a-111">Para comprobar su compatibilidad, compruebe el campo `PSSpecifiedStencilRefSupported` booleano [**de D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) con [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="f6a0a-111">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="f6a0a-112">Este es un ejemplo del uso de en `SV_StencilRef` un sombreador de píxeles:</span><span class="sxs-lookup"><span data-stu-id="f6a0a-112">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="f6a0a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6a0a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a0a-114">Características de Direct3D 11.3</span><span class="sxs-lookup"><span data-stu-id="f6a0a-114">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="f6a0a-115">Shader Model 5.1</span><span class="sxs-lookup"><span data-stu-id="f6a0a-115">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
