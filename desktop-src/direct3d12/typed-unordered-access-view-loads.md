---
title: Cargas de vista de acceso no ordenada (UAV) con tipo
description: La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con un formato de DXGI específico \_ .
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549106"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="0e7ba-103">Cargas de vista de acceso no ordenada (UAV) con tipo</span><span class="sxs-lookup"><span data-stu-id="0e7ba-103">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="0e7ba-104">La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con [**un \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)específico.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="0e7ba-105">Información general</span><span class="sxs-lookup"><span data-stu-id="0e7ba-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="0e7ba-106">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="0e7ba-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="0e7ba-107">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="0e7ba-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="0e7ba-108">Usar UNORM y SNORM con tipo UAV se carga desde HLSL</span><span class="sxs-lookup"><span data-stu-id="0e7ba-108">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="0e7ba-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e7ba-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="0e7ba-110">Información general</span><span class="sxs-lookup"><span data-stu-id="0e7ba-110">Overview</span></span>

<span data-ttu-id="0e7ba-111">Una vista de acceso desordenado (UAV) es una vista de un recurso de acceso desordenado (que puede incluir búferes, texturas y matrices de texturas, pero sin muestreo múltiple).</span><span class="sxs-lookup"><span data-stu-id="0e7ba-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="0e7ba-112">Un UAV permite el acceso de lectura y escritura sin ordenar de forma temporal desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="0e7ba-113">Esto significa que varios subprocesos pueden leer o escribir este tipo de recurso simultáneamente sin generar conflictos de memoria.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="0e7ba-114">Este acceso simultáneo se controla mediante el uso de [funciones atómicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="0e7ba-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="0e7ba-115">D3D12 (y D3D 11.3) se expande en la lista de formatos que se pueden usar con las cargas de UAV con tipo.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-115">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="0e7ba-116">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="0e7ba-116">Supported formats and API calls</span></span>

<span data-ttu-id="0e7ba-117">Anteriormente, los tres formatos siguientes admitieron cargas de UAV con tipo y eran necesarios para el hardware D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="0e7ba-118">Son compatibles con todos los hardware D3D 11.3 y D3D12.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="0e7ba-119">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0e7ba-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="0e7ba-120">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-120">R32\_UINT</span></span>
-   <span data-ttu-id="0e7ba-121">R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-121">R32\_SINT</span></span>

<span data-ttu-id="0e7ba-122">Los formatos siguientes se admiten como un conjunto en el hardware de D3D12 o D3D 11.3, por lo que si se admite cualquiera de ellos, se admiten todos.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="0e7ba-123">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0e7ba-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="0e7ba-124">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="0e7ba-125">R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="0e7ba-126">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0e7ba-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="0e7ba-127">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="0e7ba-128">R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="0e7ba-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-130">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="0e7ba-131">R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="0e7ba-132">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0e7ba-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="0e7ba-133">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-133">R16\_UINT</span></span>
-   <span data-ttu-id="0e7ba-134">R16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-134">R16\_SINT</span></span>
-   <span data-ttu-id="0e7ba-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-135">R8\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-136">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-136">R8\_UINT</span></span>
-   <span data-ttu-id="0e7ba-137">R8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-137">R8\_SINT</span></span>

<span data-ttu-id="0e7ba-138">Los siguientes formatos se admiten opcional y de forma individual en el hardware D3D12 y D3D 11.3, por lo que es necesario realizar una sola consulta en cada formato para probar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="0e7ba-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-140">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="0e7ba-141">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0e7ba-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="0e7ba-142">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="0e7ba-143">R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="0e7ba-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-145">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="0e7ba-146">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="0e7ba-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="0e7ba-147">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="0e7ba-148">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0e7ba-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="0e7ba-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-150">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="0e7ba-151">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="0e7ba-152">R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="0e7ba-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-154">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="0e7ba-155">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="0e7ba-156">R8G8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="0e7ba-156">R8G8\_SINT</span></span>
-   <span data-ttu-id="0e7ba-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-157">R16\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-158">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-158">R16\_SNORM</span></span>
-   <span data-ttu-id="0e7ba-159">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-159">R8\_SNORM</span></span>
-   <span data-ttu-id="0e7ba-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-160">A8\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="0e7ba-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0e7ba-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="0e7ba-164">Para determinar la compatibilidad con cualquier otro formato, llame a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la estructura de [**\_ \_ \_ \_ Opciones D3D12 de datos de la característica D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) como primer parámetro (consulte consultas de [capacidad](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="0e7ba-164">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="0e7ba-165">El campo *TypedUAVLoadAdditionalFormats* se establecerá si se admite la lista "compatible como conjunto" anterior.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-165">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="0e7ba-166">Realice una segunda llamada a **CheckFeatureSupport**, usando una estructura de [**\_ \_ \_ \_ compatibilidad con el formato de datos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) de las características de D3D12 (con la comprobación de la estructura devuelta con el miembro de carga D3D12 con el formato de \_ \_ \_ \_ determinante UAV con tipo \_ de la enumeración de [**\_ format \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) ) para determinar la compatibilidad en la lista de formatos admitidos opcionalmente, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0e7ba-166">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="0e7ba-167">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="0e7ba-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="0e7ba-168">En el caso de UAVs con tipo, la marca de HLSL es el \_ sombreador D3D que \_ requiere un \_ tipo \_ UAV \_ cargar \_ \_ formatos adicionales.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="0e7ba-169">Este es un ejemplo de código de sombreador para procesar una carga de UAV con tipo:</span><span class="sxs-lookup"><span data-stu-id="0e7ba-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="0e7ba-170">Usar UNORM y SNORM con tipo UAV se carga desde HLSL</span><span class="sxs-lookup"><span data-stu-id="0e7ba-170">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="0e7ba-171">Al usar cargas UAV con tipo para leer desde un recurso UNORM o SNORM, debe declarar correctamente el tipo de elemento del objeto HLSL como `unorm` o `snorm` .</span><span class="sxs-lookup"><span data-stu-id="0e7ba-171">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="0e7ba-172">Se especifica como comportamiento no definido para no coincidir con el tipo de elemento declarado en HLSL con el tipo de datos de recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-172">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="0e7ba-173">Por ejemplo, si usa cargas UAV con tipo en un recurso de búfer con datos de R8 \_ UNORM, debe declarar el tipo de elemento como `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="0e7ba-173">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="0e7ba-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e7ba-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e7ba-175">Representación</span><span class="sxs-lookup"><span data-stu-id="0e7ba-175">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="0e7ba-176">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="0e7ba-176">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="0e7ba-177">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="0e7ba-177">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="0e7ba-178">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="0e7ba-178">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="0e7ba-179">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="0e7ba-179">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 