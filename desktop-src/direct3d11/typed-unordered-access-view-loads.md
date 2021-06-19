---
title: Cargas de la vista de acceso sin ordenar con tipo
description: Obtenga información sobre la carga con tipo de vista de acceso desordenado (UAV) en Direct3D 11. La carga con tipo UAV es la capacidad de un sombreador de leer desde un UAV con una DXGI_FORMAT.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396290"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="5beff-104">Cargas de la vista de acceso sin ordenar con tipo</span><span class="sxs-lookup"><span data-stu-id="5beff-104">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="5beff-105">La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad de un sombreador de leer desde un UAV con un FORMATO DXGI \_ específico.</span><span class="sxs-lookup"><span data-stu-id="5beff-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="5beff-106">Información general</span><span class="sxs-lookup"><span data-stu-id="5beff-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="5beff-107">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="5beff-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="5beff-108">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="5beff-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="5beff-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5beff-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="5beff-110">Información general</span><span class="sxs-lookup"><span data-stu-id="5beff-110">Overview</span></span>

<span data-ttu-id="5beff-111">Una vista de acceso no ordenado (UAV) es una vista de un recurso de acceso desordenado (que puede incluir búferes, texturas y matrices de texturas, aunque sin muestreo múltiple).</span><span class="sxs-lookup"><span data-stu-id="5beff-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="5beff-112">Un UAV permite el acceso de lectura y escritura sin ordenar temporalmente desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5beff-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="5beff-113">Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria.</span><span class="sxs-lookup"><span data-stu-id="5beff-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="5beff-114">Este acceso simultáneo se controla mediante el uso de [funciones atómicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="5beff-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="5beff-115">D3D12 y D3D11.3 se expanden en la lista de formatos que se pueden usar con cargas UAV con tipo.</span><span class="sxs-lookup"><span data-stu-id="5beff-115">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="5beff-116">Formatos admitidos y llamadas API</span><span class="sxs-lookup"><span data-stu-id="5beff-116">Supported formats and API calls</span></span>

<span data-ttu-id="5beff-117">Anteriormente, los tres formatos siguientes admiten cargas UAV con tipo y eran necesarias para el hardware D3D11.0.</span><span class="sxs-lookup"><span data-stu-id="5beff-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="5beff-118">Se admiten para todo el hardware D3D11.3 y D3D12.</span><span class="sxs-lookup"><span data-stu-id="5beff-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="5beff-119">R32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="5beff-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="5beff-120">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-120">R32\_UINT</span></span>
-   <span data-ttu-id="5beff-121">R32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-121">R32\_SINT</span></span>

<span data-ttu-id="5beff-122">Los siguientes formatos se admiten como un conjunto en hardware D3D12 o D3D11.3, por lo que si se admite alguno, se admiten todos.</span><span class="sxs-lookup"><span data-stu-id="5beff-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="5beff-123">R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="5beff-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="5beff-124">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="5beff-125">R32G32B32A32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="5beff-126">R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="5beff-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="5beff-127">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="5beff-128">R16G16B16A16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="5beff-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="5beff-130">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="5beff-131">R8G8B8A8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="5beff-132">R16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="5beff-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="5beff-133">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-133">R16\_UINT</span></span>
-   <span data-ttu-id="5beff-134">R16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-134">R16\_SINT</span></span>
-   <span data-ttu-id="5beff-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-135">R8\_UNORM</span></span>
-   <span data-ttu-id="5beff-136">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-136">R8\_UINT</span></span>
-   <span data-ttu-id="5beff-137">R8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-137">R8\_SINT</span></span>

<span data-ttu-id="5beff-138">Los siguientes formatos se admiten opcionalmente e individualmente en hardware D3D12 y D3D11.3, por lo que se tendría que realizar una única consulta en cada formato para probar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="5beff-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="5beff-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="5beff-140">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="5beff-141">R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="5beff-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="5beff-142">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="5beff-143">R32G32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="5beff-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="5beff-145">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="5beff-146">R11G11B10 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="5beff-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="5beff-147">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="5beff-148">R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="5beff-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="5beff-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="5beff-150">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="5beff-151">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="5beff-152">R16G16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="5beff-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="5beff-154">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="5beff-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="5beff-155">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="5beff-156">8G8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="5beff-156">8G8\_SINT</span></span>
-   <span data-ttu-id="5beff-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-157">R16\_UNORM</span></span>
-   <span data-ttu-id="5beff-158">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-158">R16\_SNORM</span></span>
-   <span data-ttu-id="5beff-159">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-159">R8\_SNORM</span></span>
-   <span data-ttu-id="5beff-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-160">A8\_UNORM</span></span>
-   <span data-ttu-id="5beff-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="5beff-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="5beff-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5beff-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="5beff-164">Para determinar la compatibilidad con cualquier formato adicional, llame a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con la estructura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="5beff-164">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="5beff-165">El bit se establecerá si se admite la lista "compatible como `TypedUAVLoadAdditionalFormats` conjunto" anterior.</span><span class="sxs-lookup"><span data-stu-id="5beff-165">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="5beff-166">Realice una segunda llamada a **CheckFeatureSupport** mediante una estructura [**FEATURE DATA FORMAT \_ \_ \_ \_ SUPPORT2 de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (comprobando la estructura devuelta con el miembro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD de la enumeración \_ \_ \_ \_ \_ [**D3D11 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) para determinar la compatibilidad en la lista de formatos admitidos opcionalmente anteriormente, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5beff-166">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="5beff-167">Uso de cargas UAV con tipo desde HLSL</span><span class="sxs-lookup"><span data-stu-id="5beff-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="5beff-168">Para los UAV con tipo, la marca HLSL es D3D SHADER REQUIERE FORMATOS ADICIONALES DE CARGA DE \_ \_ \_ \_ UAV \_ CON \_ \_ TIPO.</span><span class="sxs-lookup"><span data-stu-id="5beff-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="5beff-169">Este es un ejemplo de código de sombreador para procesar una carga de UAV con tipo:</span><span class="sxs-lookup"><span data-stu-id="5beff-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="5beff-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5beff-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5beff-171">Características de Direct3D 11.3</span><span class="sxs-lookup"><span data-stu-id="5beff-171">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="5beff-172">Modelo de sombreador 5.1</span><span class="sxs-lookup"><span data-stu-id="5beff-172">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 