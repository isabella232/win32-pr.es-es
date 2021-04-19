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
# <a name="format-conversion-functions-hlsl-reference"></a>Funciones de conversión de formato (referencia de HLSL)

La sección contiene las funciones de conversión de formato utilizadas en los sombreadores de proceso y de píxeles.

-   [Funciones de convertidor](#converter-functions)
-   [Temas relacionados](#related-topics)

> El encabezado D3DX_DXGIFormatConvert. INL se incluye en el SDK de DirectX heredado y se basa en la compatibilidad con XNAMath para C++. También se incluye en el paquete NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) . La versión más reciente usa DirectXMath para la compatibilidad con C++ y todas las funciones se definen en el espacio de nombres de **DirectX** c++.

## <a name="converter-functions"></a>Funciones de convertidor

### <a name="dxgi_format_r10g10b10a2_unorm"></a>Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM

<dl>

[**D3DX \_ R10G10B10A2 \_ UNORM \_ a \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ a \_ R10G10B10A2 \_ UNORM**](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a>Formato de DXGI \_ \_ R10G10B10A2 \_ uint

<dl>

[**D3DX \_ R10G10B10A2 \_ uint \_ a \_ UINT4**](d3dx-r10g10b10a2-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ a \_ R10G10B10A2 \_ uint**](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a>Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM:

<dl>

[**D3DX \_ R8G8B8A8 \_ UNORM \_ a \_ FLOAT4**](d3dx-r8g8b8a8-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM**](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a>Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB

<dl>

[**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ inexacto**](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_ sRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a>Formato de DXGI \_ \_ R8G8B8A8 \_ uint

<dl>

[**D3DX \_ R8G8B8A8 \_ uint \_ a \_ UINT4**](d3dx-r8g8b8a8-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ a \_ R8G8B8A8 \_ uint**](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a>Formato de DXGI \_ \_ R8G8B8A8 \_ SNORM

<dl>

[**D3DX \_ R8G8B8A8 \_ SNORM \_ a \_ FLOAT4**](d3dx-r8g8b8a8-snorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ SNORM**](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a>Formato de DXGI \_ \_ R8G8B8A8 \_ Sint

<dl>

[**D3DX \_ R8G8B8A8 \_ Sint \_ a \_ INT4**](d3dx-r8g8b8a8-sint-to-int4.md)  
[**D3DX \_ INT4 \_ a \_ R8G8B8A8 \_ Sint**](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a>Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM

<dl>

[**D3DX \_ B8G8R8A8 \_ UNORM \_ a \_ FLOAT4**](d3dx-b8g8r8a8-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ a \_ B8G8R8A8 \_ UNORM**](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a>Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB

<dl>

[**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ inexacto**](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_ sRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a>Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM

<dl>

[**D3DX \_ B8G8R8X8 \_ UNORM \_ a \_ FLOAT3**](d3dx-b8g8r8x8-unorm-to-float3.md)  
[**\_FLOAT3 \_ de D3DX \_ B8G8R8X8 \_ UNORM**](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a>Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB

<dl>

[**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3 \_ inexacto**](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[**D3DX \_ FLOAT3 \_ a \_ B8G8R8X8 \_ UNORM \_ sRGB**](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a>Formato de DXGI \_ \_ R16G16 \_ float

<dl>

[**D3DX \_ R16G16 \_ float \_ a \_ FLOAT2**](d3dx-r16g16-float-to-float2.md)  
[**\_FLOAT2 \_ de D3DX a \_ R16G16 \_ float**](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a>Formato de DXGI \_ \_ R16G16 \_ UNORM

<dl>

[**D3DX \_ R16G16 \_ UNORM \_ a \_ FLOAT2**](d3dx-r16g16-unorm-to-float2.md)  
[**\_FLOAT2 \_ de D3DX \_ R16G16 \_ UNORM**](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a>Formato de DXGI \_ \_ R16G16 \_ uint

<dl>

[**D3DX \_ R16G16 \_ uint \_ a \_ UINT2**](d3dx-r16g16-uint-to-uint2.md)  
[**D3DX \_ UINT2 \_ a \_ R16G16 \_ uint**](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a>Formato de DXGI \_ \_ R16G16 \_ SNORM

<dl>

[**D3DX \_ R16G16 \_ SNORM \_ a \_ FLOAT2**](d3dx-r16g16-snorm-to-float2.md)  
[**\_FLOAT2 \_ de D3DX \_ R16G16 \_ SNORM**](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a>Formato de DXGI \_ \_ R16G16 \_ Sint

<dl>

[**D3DX \_ R16G16 \_ Sint \_ a \_ INT2**](d3dx-r16g16-sint-to-int2.md)  
[**D3DX \_ INT2 \_ a \_ R16G16 \_ Sint**](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de conversión de formato en línea](inline-format-conversion-reference.md)
</dt> <dt>

[Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
