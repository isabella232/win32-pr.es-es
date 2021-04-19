---
title: Funciones de conversión de formato (referencia de HLSL)
description: La sección contiene las funciones de conversión de formato utilizadas en los sombreadores de proceso y de píxeles.
ms.assetid: 05575ee8-4428-437f-bfb6-e5c676405d65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 355fb59aa6a94e144daf05942b40d3f685daff51
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222883"
---
# <a name="format-conversion-functions-hlsl-reference"></a><span data-ttu-id="43249-103">Funciones de conversión de formato (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="43249-103">Format conversion functions (HLSL reference)</span></span>

<span data-ttu-id="43249-104">La sección contiene las funciones de conversión de formato utilizadas en los sombreadores de proceso y de píxeles.</span><span class="sxs-lookup"><span data-stu-id="43249-104">The section contains the format conversion functions used in Compute and Pixel Shaders.</span></span>

-   [<span data-ttu-id="43249-105">Funciones de convertidor</span><span class="sxs-lookup"><span data-stu-id="43249-105">Converter Functions</span></span>](#converter-functions)
-   [<span data-ttu-id="43249-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43249-106">Related topics</span></span>](#related-topics)

> <span data-ttu-id="43249-107">El encabezado D3DX_DXGIFormatConvert. INL se incluye en el SDK de DirectX heredado y se basa en la compatibilidad con XNAMath para C++.</span><span class="sxs-lookup"><span data-stu-id="43249-107">The D3DX_DXGIFormatConvert.inl header ships in the legacy DirectX SDK and relied on XNAMath for C++ support.</span></span> <span data-ttu-id="43249-108">También se incluye en el paquete NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) .</span><span class="sxs-lookup"><span data-stu-id="43249-108">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span> <span data-ttu-id="43249-109">La versión más reciente usa DirectXMath para la compatibilidad con C++ y todas las funciones se definen en el espacio de nombres de **DirectX** c++.</span><span class="sxs-lookup"><span data-stu-id="43249-109">The latest version uses DirectXMath for C++ support, and all functions are defined in the **DirectX** C++ namespace.</span></span>

## <a name="converter-functions"></a><span data-ttu-id="43249-110">Funciones de convertidor</span><span class="sxs-lookup"><span data-stu-id="43249-110">Converter Functions</span></span>

### <a name="dxgi_format_r10g10b10a2_unorm"></a><span data-ttu-id="43249-111">Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="43249-111">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>

<dl>

[<span data-ttu-id="43249-112">**D3DX \_ R10G10B10A2 \_ UNORM \_ a \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="43249-112">**D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r10g10b10a2-unorm-to-float4.md)  
[<span data-ttu-id="43249-113">**D3DX \_ FLOAT4 \_ a \_ R10G10B10A2 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="43249-113">**D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM**</span></span>](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a><span data-ttu-id="43249-114">Formato de DXGI \_ \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="43249-114">DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>

<dl>

[<span data-ttu-id="43249-115">**D3DX \_ R10G10B10A2 \_ uint \_ a \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="43249-115">**D3DX\_R10G10B10A2\_UINT\_to\_UINT4**</span></span>](d3dx-r10g10b10a2-uint-to-uint4.md)  
[<span data-ttu-id="43249-116">**D3DX \_ UINT4 \_ a \_ R10G10B10A2 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="43249-116">**D3DX\_UINT4\_to\_R10G10B10A2\_UINT**</span></span>](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a><span data-ttu-id="43249-117">Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM:</span><span class="sxs-lookup"><span data-stu-id="43249-117">DXGI\_FORMAT\_R8G8B8A8\_UNORM:</span></span>

<dl>

[<span data-ttu-id="43249-118">**D3DX \_ R8G8B8A8 \_ UNORM \_ a \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="43249-118">**D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-to-float4.md)  
[<span data-ttu-id="43249-119">**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="43249-119">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM**</span></span>](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a><span data-ttu-id="43249-120">Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="43249-120">DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="43249-121">**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ inexacto**</span><span class="sxs-lookup"><span data-stu-id="43249-121">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="43249-122">**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="43249-122">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="43249-123">**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="43249-123">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a><span data-ttu-id="43249-124">Formato de DXGI \_ \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="43249-124">DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>

<dl>

[<span data-ttu-id="43249-125">**D3DX \_ R8G8B8A8 \_ uint \_ a \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="43249-125">**D3DX\_R8G8B8A8\_UINT\_to\_UINT4**</span></span>](d3dx-r8g8b8a8-uint-to-uint4.md)  
[<span data-ttu-id="43249-126">**D3DX \_ UINT4 \_ a \_ R8G8B8A8 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="43249-126">**D3DX\_UINT4\_to\_R8G8B8A8\_UINT**</span></span>](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a><span data-ttu-id="43249-127">Formato de DXGI \_ \_ R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="43249-127">DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>

<dl>

[<span data-ttu-id="43249-128">**D3DX \_ R8G8B8A8 \_ SNORM \_ a \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="43249-128">**D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-snorm-to-float4.md)  
[<span data-ttu-id="43249-129">**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="43249-129">**D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM**</span></span>](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a><span data-ttu-id="43249-130">Formato de DXGI \_ \_ R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="43249-130">DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>

<dl>

[<span data-ttu-id="43249-131">**D3DX \_ R8G8B8A8 \_ Sint \_ a \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="43249-131">**D3DX\_R8G8B8A8\_SINT\_to\_INT4**</span></span>](d3dx-r8g8b8a8-sint-to-int4.md)  
[<span data-ttu-id="43249-132">**D3DX \_ INT4 \_ a \_ R8G8B8A8 \_ Sint**</span><span class="sxs-lookup"><span data-stu-id="43249-132">**D3DX\_INT4\_to\_R8G8B8A8\_SINT**</span></span>](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a><span data-ttu-id="43249-133">Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="43249-133">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>

<dl>

[<span data-ttu-id="43249-134">**D3DX \_ B8G8R8A8 \_ UNORM \_ a \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="43249-134">**D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-to-float4.md)  
[<span data-ttu-id="43249-135">**D3DX \_ FLOAT4 \_ a \_ B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="43249-135">**D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM**</span></span>](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a><span data-ttu-id="43249-136">Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="43249-136">DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="43249-137">**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ inexacto**</span><span class="sxs-lookup"><span data-stu-id="43249-137">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="43249-138">**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="43249-138">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="43249-139">**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="43249-139">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a><span data-ttu-id="43249-140">Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="43249-140">DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>

<dl>

[<span data-ttu-id="43249-141">**D3DX \_ B8G8R8X8 \_ UNORM \_ a \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="43249-141">**D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-to-float3.md)  
[<span data-ttu-id="43249-142">**\_FLOAT3 \_ de D3DX \_ B8G8R8X8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="43249-142">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM**</span></span>](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a><span data-ttu-id="43249-143">Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="43249-143">DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="43249-144">**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3 \_ inexacto**</span><span class="sxs-lookup"><span data-stu-id="43249-144">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[<span data-ttu-id="43249-145">**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="43249-145">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[<span data-ttu-id="43249-146">**D3DX \_ FLOAT3 \_ a \_ B8G8R8X8 \_ UNORM \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="43249-146">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB**</span></span>](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a><span data-ttu-id="43249-147">Formato de DXGI \_ \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="43249-147">DXGI\_FORMAT\_R16G16\_FLOAT</span></span>

<dl>

[<span data-ttu-id="43249-148">**D3DX \_ R16G16 \_ float \_ a \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="43249-148">**D3DX\_R16G16\_FLOAT\_to\_FLOAT2**</span></span>](d3dx-r16g16-float-to-float2.md)  
[<span data-ttu-id="43249-149">**\_FLOAT2 \_ de D3DX a \_ R16G16 \_ float**</span><span class="sxs-lookup"><span data-stu-id="43249-149">**D3DX\_FLOAT2\_to\_R16G16\_FLOAT**</span></span>](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a><span data-ttu-id="43249-150">Formato de DXGI \_ \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="43249-150">DXGI\_FORMAT\_R16G16\_UNORM</span></span>

<dl>

[<span data-ttu-id="43249-151">**D3DX \_ R16G16 \_ UNORM \_ a \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="43249-151">**D3DX\_R16G16\_UNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-unorm-to-float2.md)  
[<span data-ttu-id="43249-152">**\_FLOAT2 \_ de D3DX \_ R16G16 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="43249-152">**D3DX\_FLOAT2\_to\_R16G16\_UNORM**</span></span>](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a><span data-ttu-id="43249-153">Formato de DXGI \_ \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="43249-153">DXGI\_FORMAT\_R16G16\_UINT</span></span>

<dl>

[<span data-ttu-id="43249-154">**D3DX \_ R16G16 \_ uint \_ a \_ UINT2**</span><span class="sxs-lookup"><span data-stu-id="43249-154">**D3DX\_R16G16\_UINT\_to\_UINT2**</span></span>](d3dx-r16g16-uint-to-uint2.md)  
[<span data-ttu-id="43249-155">**D3DX \_ UINT2 \_ a \_ R16G16 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="43249-155">**D3DX\_UINT2\_to\_R16G16\_UINT**</span></span>](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a><span data-ttu-id="43249-156">Formato de DXGI \_ \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="43249-156">DXGI\_FORMAT\_R16G16\_SNORM</span></span>

<dl>

[<span data-ttu-id="43249-157">**D3DX \_ R16G16 \_ SNORM \_ a \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="43249-157">**D3DX\_R16G16\_SNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-snorm-to-float2.md)  
[<span data-ttu-id="43249-158">**\_FLOAT2 \_ de D3DX \_ R16G16 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="43249-158">**D3DX\_FLOAT2\_to\_R16G16\_SNORM**</span></span>](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a><span data-ttu-id="43249-159">Formato de DXGI \_ \_ R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="43249-159">DXGI\_FORMAT\_R16G16\_SINT</span></span>

<dl>

[<span data-ttu-id="43249-160">**D3DX \_ R16G16 \_ Sint \_ a \_ INT2**</span><span class="sxs-lookup"><span data-stu-id="43249-160">**D3DX\_R16G16\_SINT\_to\_INT2**</span></span>](d3dx-r16g16-sint-to-int2.md)  
[<span data-ttu-id="43249-161">**D3DX \_ INT2 \_ a \_ R16G16 \_ Sint**</span><span class="sxs-lookup"><span data-stu-id="43249-161">**D3DX\_INT2\_to\_R16G16\_SINT**</span></span>](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="43249-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43249-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43249-163">Referencia de conversión de formato en línea</span><span class="sxs-lookup"><span data-stu-id="43249-163">Inline Format Conversion Reference</span></span>](inline-format-conversion-reference.md)
</dt> <dt>

[<span data-ttu-id="43249-164">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="43249-164">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
