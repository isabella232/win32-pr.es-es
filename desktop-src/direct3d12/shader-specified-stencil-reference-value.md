---
title: Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 12)
description: Obtenga información sobre el valor de referencia de galería de símbolos en gráficos de Direct3D 12. La habilitación de sombreadores de píxeles para usar el valor de referencia de galería de símbolos permite un control preciso sobre las operaciones de galería de símbolos.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408318"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="007fc-104">Valor de referencia de galería de símbolos especificado por el sombreador (gráficos de Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="007fc-104">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="007fc-105">La habilitación de sombreadores de píxeles para generar el valor de referencia de galería de símbolos, en lugar de usar el especificado por la API, permite un control muy específico sobre las operaciones de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="007fc-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="007fc-106">Normalmente, el método [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) especifica el valor de referencia de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="007fc-106">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="007fc-107">Este método establece el valor de referencia de galería de símbolos en una granularidad por dibujo.</span><span class="sxs-lookup"><span data-stu-id="007fc-107">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="007fc-108">Sin embargo, el sombreador de píxeles puede sobrescribir este valor.</span><span class="sxs-lookup"><span data-stu-id="007fc-108">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="007fc-109">Esta característica D3D12 (y D3D11.3) permite a los desarrolladores leer y usar el valor de referencia de galería de símbolos *(SV \_ StencilRef)* que se genera desde un sombreador de píxeles, lo que permite una granularidad por píxel o por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="007fc-109">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="007fc-110">El valor especificado del sombreador reemplaza el valor de referencia especificado por la API para esa invocación, lo que significa que el cambio afecta tanto a la prueba de galería de símbolos como cuando se usa la operación de galería de símbolos D3D12 STENCIL OP REPLACE (un miembro de \_ \_ \_ [**D3D12 \_ STENCIL \_ OP)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)para escribir el valor de referencia en el búfer de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="007fc-110">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="007fc-111">Esta característica es opcional en D3D12 y D3D11.3.</span><span class="sxs-lookup"><span data-stu-id="007fc-111">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="007fc-112">Para comprobar su compatibilidad, compruebe el campo booleano *PSSpecifiedStencilRefSupported* de [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) mediante [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="007fc-112">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="007fc-113">Este es un ejemplo del uso de *SV \_ StencilRef en* un sombreador de píxeles:</span><span class="sxs-lookup"><span data-stu-id="007fc-113">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="007fc-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="007fc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="007fc-115">Representación</span><span class="sxs-lookup"><span data-stu-id="007fc-115">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="007fc-116">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="007fc-116">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="007fc-117">Shader Model 5.1</span><span class="sxs-lookup"><span data-stu-id="007fc-117">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="007fc-118">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="007fc-118">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
