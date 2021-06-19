---
title: Cargas de la vista de acceso sin ordenar (UAV) con tipo
description: Obtenga información sobre la carga con tipo de vista de acceso desordenado (UAV) en Direct3D 12. La carga con tipo UAV es la capacidad de que un sombreador lea desde un UAV con un DXGI_FORMAT.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128354132a58e0b8648fba2b4e1e6babb95535
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394770"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="e91fc-104">Cargas de la vista de acceso sin ordenar (UAV) con tipo</span><span class="sxs-lookup"><span data-stu-id="e91fc-104">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="e91fc-105">La carga con tipo de vista de acceso no ordenado (UAV) es la capacidad de que un sombreador lea desde un UAV con un [**FORMATO DXGI \_ específico.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="e91fc-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="e91fc-106">Información general</span><span class="sxs-lookup"><span data-stu-id="e91fc-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="e91fc-107">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="e91fc-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="e91fc-108">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="e91fc-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="e91fc-109">Uso de cargas UAV con tipo UNORM y SNORM desde HLSL</span><span class="sxs-lookup"><span data-stu-id="e91fc-109">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="e91fc-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e91fc-110">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="e91fc-111">Información general</span><span class="sxs-lookup"><span data-stu-id="e91fc-111">Overview</span></span>

<span data-ttu-id="e91fc-112">Una vista de acceso desordenado (UAV) es una vista de un recurso de acceso desordenado (que puede incluir búferes, texturas y matrices de texturas, aunque sin muestreo múltiple).</span><span class="sxs-lookup"><span data-stu-id="e91fc-112">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="e91fc-113">Un UAV permite el acceso de lectura y escritura sin ordenar temporalmente desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e91fc-113">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="e91fc-114">Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria.</span><span class="sxs-lookup"><span data-stu-id="e91fc-114">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="e91fc-115">Este acceso simultáneo se controla mediante el uso de [Funciones atómicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="e91fc-115">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="e91fc-116">D3D12 (y D3D11.3) se expande en la lista de formatos que se pueden usar con cargas UAV con tipo.</span><span class="sxs-lookup"><span data-stu-id="e91fc-116">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="e91fc-117">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="e91fc-117">Supported formats and API calls</span></span>

<span data-ttu-id="e91fc-118">Anteriormente, los tres formatos siguientes admiten cargas UAV con tipo y eran necesarios para el hardware D3D11.0.</span><span class="sxs-lookup"><span data-stu-id="e91fc-118">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="e91fc-119">Se admiten para todo el hardware D3D11.3 y D3D12.</span><span class="sxs-lookup"><span data-stu-id="e91fc-119">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="e91fc-120">R32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e91fc-120">R32\_FLOAT</span></span>
-   <span data-ttu-id="e91fc-121">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-121">R32\_UINT</span></span>
-   <span data-ttu-id="e91fc-122">R32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-122">R32\_SINT</span></span>

<span data-ttu-id="e91fc-123">Los siguientes formatos se admiten como un conjunto en hardware D3D12 o D3D11.3, por lo que si se admite alguno, se admiten todos.</span><span class="sxs-lookup"><span data-stu-id="e91fc-123">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="e91fc-124">R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e91fc-124">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="e91fc-125">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-125">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="e91fc-126">R32G32B32A32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-126">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="e91fc-127">R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e91fc-127">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="e91fc-128">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-128">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="e91fc-129">R16G16B16A16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-129">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="e91fc-130">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-130">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="e91fc-131">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-131">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="e91fc-132">R8G8B8A8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-132">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="e91fc-133">R16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e91fc-133">R16\_FLOAT</span></span>
-   <span data-ttu-id="e91fc-134">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-134">R16\_UINT</span></span>
-   <span data-ttu-id="e91fc-135">R16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-135">R16\_SINT</span></span>
-   <span data-ttu-id="e91fc-136">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-136">R8\_UNORM</span></span>
-   <span data-ttu-id="e91fc-137">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-137">R8\_UINT</span></span>
-   <span data-ttu-id="e91fc-138">R8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-138">R8\_SINT</span></span>

<span data-ttu-id="e91fc-139">Los siguientes formatos se admiten opcionalmente e individualmente en hardware D3D12 y D3D11.3, por lo que se tendría que realizar una consulta única en cada formato para probar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="e91fc-139">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="e91fc-140">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-140">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="e91fc-141">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-141">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="e91fc-142">R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e91fc-142">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="e91fc-143">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-143">R32G32\_UINT</span></span>
-   <span data-ttu-id="e91fc-144">R32G32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-144">R32G32\_SINT</span></span>
-   <span data-ttu-id="e91fc-145">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-145">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="e91fc-146">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-146">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="e91fc-147">R11G11B10 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e91fc-147">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="e91fc-148">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-148">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="e91fc-149">R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e91fc-149">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="e91fc-150">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-150">R16G16\_UNORM</span></span>
-   <span data-ttu-id="e91fc-151">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-151">R16G16\_UINT</span></span>
-   <span data-ttu-id="e91fc-152">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-152">R16G16\_SNORM</span></span>
-   <span data-ttu-id="e91fc-153">R16G16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-153">R16G16\_SINT</span></span>
-   <span data-ttu-id="e91fc-154">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-154">R8G8\_UNORM</span></span>
-   <span data-ttu-id="e91fc-155">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-155">R8G8\_UINT</span></span>
-   <span data-ttu-id="e91fc-156">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-156">R8G8\_SNORM</span></span>
-   <span data-ttu-id="e91fc-157">R8G8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="e91fc-157">R8G8\_SINT</span></span>
-   <span data-ttu-id="e91fc-158">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-158">R16\_UNORM</span></span>
-   <span data-ttu-id="e91fc-159">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-159">R16\_SNORM</span></span>
-   <span data-ttu-id="e91fc-160">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-160">R8\_SNORM</span></span>
-   <span data-ttu-id="e91fc-161">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-161">A8\_UNORM</span></span>
-   <span data-ttu-id="e91fc-162">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-162">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="e91fc-163">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-163">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="e91fc-164">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e91fc-164">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="e91fc-165">Para determinar la compatibilidad con cualquier formato adicional, llame a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la estructura [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) como primer parámetro (consulte [Capability Querying](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="e91fc-165">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="e91fc-166">El *campo TypedUAVLoadAdditionalFormats* se establecerá si se admite la lista "compatible como conjunto" anterior.</span><span class="sxs-lookup"><span data-stu-id="e91fc-166">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="e91fc-167">Realice una segunda llamada a **CheckFeatureSupport** mediante una estructura [**D3D12 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (comprobando la estructura devuelta con el miembro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD de la enumeración \_ \_ \_ \_ \_ [**D3D12 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) para determinar la compatibilidad en la lista de formatos compatibles opcionalmente mencionados anteriormente, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e91fc-167">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="e91fc-168">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="e91fc-168">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="e91fc-169">Para los UAV con tipo, la marca HLSL es D3D SHADER REQUIRES TYPED UAV LOAD ADDITIONAL FORMATS (SOMBREADOR D3D REQUIERE FORMATOS \_ \_ \_ \_ ADICIONALES DE CARGA DE UAV \_ CON \_ \_ TIPO).</span><span class="sxs-lookup"><span data-stu-id="e91fc-169">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="e91fc-170">Este es un ejemplo de código de sombreador para procesar una carga de UAV con tipo:</span><span class="sxs-lookup"><span data-stu-id="e91fc-170">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="e91fc-171">Uso de cargas UAV con tipo UNORM y SNORM desde HLSL</span><span class="sxs-lookup"><span data-stu-id="e91fc-171">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="e91fc-172">Al usar cargas UAV con tipo para leer desde un recurso UNORM o SNORM, debe declarar correctamente el tipo de elemento del objeto HLSL como `unorm` o `snorm` .</span><span class="sxs-lookup"><span data-stu-id="e91fc-172">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="e91fc-173">Se especifica como comportamiento indefinido para no coincide el tipo de elemento declarado en HLSL con el tipo de datos de recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="e91fc-173">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="e91fc-174">Por ejemplo, si usa cargas UAV con tipo en un recurso de búfer con datos \_ R8 UNORM, debe declarar el tipo de elemento como `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="e91fc-174">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="e91fc-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e91fc-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e91fc-176">Representación</span><span class="sxs-lookup"><span data-stu-id="e91fc-176">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="e91fc-177">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="e91fc-177">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="e91fc-178">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="e91fc-178">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="e91fc-179">Shader Model 5.1</span><span class="sxs-lookup"><span data-stu-id="e91fc-179">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="e91fc-180">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="e91fc-180">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 