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
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="cb543-103">Valor de referencia de estarcido del sombreador especificado (gráficos de Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="cb543-103">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="cb543-104">Habilitar los sombreadores de píxeles para generar el valor de referencia de la galería de símbolos, en lugar de usar el especificado por la API, permite un control pormenorizado muy fino sobre las operaciones de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="cb543-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="cb543-105">Normalmente, el valor de referencia de la galería de símbolos se especifica mediante el método [**ID3D12GraphicsCommandList:: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) .</span><span class="sxs-lookup"><span data-stu-id="cb543-105">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="cb543-106">Este método establece el valor de referencia de la galería de símbolos en una granularidad por dibujo.</span><span class="sxs-lookup"><span data-stu-id="cb543-106">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="cb543-107">Sin embargo, este valor se puede sobrescribir con el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="cb543-107">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="cb543-108">Esta característica D3D12 (y D3D 11.3) permite a los desarrolladores leer y usar el valor de referencia de la galería de símbolos (*VP \_ StencilRef*) que se genera desde un sombreador de píxeles, lo que permite una granularidad por píxel o por muestra.</span><span class="sxs-lookup"><span data-stu-id="cb543-108">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="cb543-109">El valor especificado del sombreador reemplaza el valor de referencia especificado por la API para esa invocación, lo que significa que el cambio afecta a la prueba de la galería de símbolos y, cuando la operación de estarcido D3D12 de la galería de símbolos de la operación \_ \_ de estarcido \_ Replace (un miembro de [**D3D12 \_ cliché \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) se usa para escribir el valor de referencia en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="cb543-109">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="cb543-110">Esta característica es opcional en D3D12 y D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="cb543-110">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="cb543-111">Para probar su compatibilidad, consulte el campo booleano *PSSpecifiedStencilRefSupported* de [**\_ \_ \_ \_ las opciones de D3D12 de datos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) con [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="cb543-111">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="cb543-112">Este es un ejemplo del uso de *\_ StencilRef de SV* en un sombreador de píxeles:</span><span class="sxs-lookup"><span data-stu-id="cb543-112">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="cb543-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb543-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb543-114">Representación</span><span class="sxs-lookup"><span data-stu-id="cb543-114">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="cb543-115">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="cb543-115">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="cb543-116">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="cb543-116">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="cb543-117">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="cb543-117">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
