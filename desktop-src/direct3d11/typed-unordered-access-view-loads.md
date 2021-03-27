---
title: Cargas de vista de acceso no ordenada con tipo
description: La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con un formato de DXGI específico \_ .
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0958b3563ab8001fd7b34ae62c9bcc37ad75c07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359080"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="3406b-103">Cargas de vista de acceso no ordenada con tipo</span><span class="sxs-lookup"><span data-stu-id="3406b-103">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="3406b-104">La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con un formato de DXGI específico \_ .</span><span class="sxs-lookup"><span data-stu-id="3406b-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="3406b-105">Información general</span><span class="sxs-lookup"><span data-stu-id="3406b-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="3406b-106">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="3406b-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="3406b-107">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="3406b-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="3406b-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3406b-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="3406b-109">Información general</span><span class="sxs-lookup"><span data-stu-id="3406b-109">Overview</span></span>

<span data-ttu-id="3406b-110">Una vista de acceso desordenado (UAV) es una vista de un recurso de acceso desordenado (que puede incluir búferes, texturas y matrices de texturas, pero sin muestreo múltiple).</span><span class="sxs-lookup"><span data-stu-id="3406b-110">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="3406b-111">Un UAV permite el acceso de lectura y escritura sin ordenar de forma temporal desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3406b-111">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="3406b-112">Esto significa que varios subprocesos pueden leer o escribir este tipo de recurso simultáneamente sin generar conflictos de memoria.</span><span class="sxs-lookup"><span data-stu-id="3406b-112">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="3406b-113">Este acceso simultáneo se controla mediante el uso de [funciones atómicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="3406b-113">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="3406b-114">D3D12 y D3D 11.3 se expanden en la lista de formatos que se pueden usar con las cargas de UAV con tipo.</span><span class="sxs-lookup"><span data-stu-id="3406b-114">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="3406b-115">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="3406b-115">Supported formats and API calls</span></span>

<span data-ttu-id="3406b-116">Anteriormente, los tres formatos siguientes admitieron cargas de UAV con tipo y eran necesarios para el hardware D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="3406b-116">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="3406b-117">Son compatibles con todos los hardware D3D 11.3 y D3D12.</span><span class="sxs-lookup"><span data-stu-id="3406b-117">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="3406b-118">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="3406b-118">R32\_FLOAT</span></span>
-   <span data-ttu-id="3406b-119">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-119">R32\_UINT</span></span>
-   <span data-ttu-id="3406b-120">R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-120">R32\_SINT</span></span>

<span data-ttu-id="3406b-121">Los formatos siguientes se admiten como un conjunto en el hardware de D3D12 o D3D 11.3, por lo que si se admite cualquiera de ellos, se admiten todos.</span><span class="sxs-lookup"><span data-stu-id="3406b-121">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="3406b-122">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="3406b-122">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="3406b-123">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-123">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="3406b-124">R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-124">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="3406b-125">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="3406b-125">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="3406b-126">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-126">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="3406b-127">R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-127">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="3406b-128">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-128">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="3406b-129">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-129">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="3406b-130">R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-130">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="3406b-131">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="3406b-131">R16\_FLOAT</span></span>
-   <span data-ttu-id="3406b-132">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-132">R16\_UINT</span></span>
-   <span data-ttu-id="3406b-133">R16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-133">R16\_SINT</span></span>
-   <span data-ttu-id="3406b-134">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-134">R8\_UNORM</span></span>
-   <span data-ttu-id="3406b-135">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-135">R8\_UINT</span></span>
-   <span data-ttu-id="3406b-136">R8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-136">R8\_SINT</span></span>

<span data-ttu-id="3406b-137">Los siguientes formatos se admiten opcional y de forma individual en el hardware D3D12 y D3D 11.3, por lo que es necesario realizar una sola consulta en cada formato para probar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3406b-137">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="3406b-138">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-138">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="3406b-139">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-139">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="3406b-140">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="3406b-140">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="3406b-141">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-141">R32G32\_UINT</span></span>
-   <span data-ttu-id="3406b-142">R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-142">R32G32\_SINT</span></span>
-   <span data-ttu-id="3406b-143">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-143">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="3406b-144">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-144">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="3406b-145">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="3406b-145">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="3406b-146">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-146">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="3406b-147">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="3406b-147">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="3406b-148">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-148">R16G16\_UNORM</span></span>
-   <span data-ttu-id="3406b-149">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-149">R16G16\_UINT</span></span>
-   <span data-ttu-id="3406b-150">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-150">R16G16\_SNORM</span></span>
-   <span data-ttu-id="3406b-151">R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-151">R16G16\_SINT</span></span>
-   <span data-ttu-id="3406b-152">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-152">R8G8\_UNORM</span></span>
-   <span data-ttu-id="3406b-153">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3406b-153">R8G8\_UINT</span></span>
-   <span data-ttu-id="3406b-154">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-154">R8G8\_SNORM</span></span>
-   <span data-ttu-id="3406b-155">8G8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3406b-155">8G8\_SINT</span></span>
-   <span data-ttu-id="3406b-156">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-156">R16\_UNORM</span></span>
-   <span data-ttu-id="3406b-157">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-157">R16\_SNORM</span></span>
-   <span data-ttu-id="3406b-158">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-158">R8\_SNORM</span></span>
-   <span data-ttu-id="3406b-159">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-159">A8\_UNORM</span></span>
-   <span data-ttu-id="3406b-160">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-160">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="3406b-161">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-161">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="3406b-162">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3406b-162">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="3406b-163">Para determinar la compatibilidad con cualquier otro formato, llame a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con la estructura [**\_ \_ \_ D3D11 \_ OPTIONS2 de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="3406b-163">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="3406b-164">El `TypedUAVLoadAdditionalFormats` bit se establecerá si se admite la lista "compatible como conjunto" anterior.</span><span class="sxs-lookup"><span data-stu-id="3406b-164">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="3406b-165">Realice una segunda llamada a **CheckFeatureSupport**, usando una estructura de tipo de datos de características de D3D11 (con el fin de establecer la estructura devuelta con el [**\_ \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) \_ \_ \_ miembro de carga D3D12 Format UAVd \_ upload typeed \_ de la enumeración de [**D3D11 \_ format \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) ) para determinar la compatibilidad en la lista de formatos admitidos opcionalmente, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3406b-165">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="3406b-166">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="3406b-166">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="3406b-167">En el caso de UAVs con tipo, la marca de HLSL es el \_ sombreador D3D que \_ requiere un \_ tipo \_ UAV \_ cargar \_ \_ formatos adicionales.</span><span class="sxs-lookup"><span data-stu-id="3406b-167">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="3406b-168">Este es un ejemplo de código de sombreador para procesar una carga de UAV con tipo:</span><span class="sxs-lookup"><span data-stu-id="3406b-168">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="3406b-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3406b-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3406b-170">Características de Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="3406b-170">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="3406b-171">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="3406b-171">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 