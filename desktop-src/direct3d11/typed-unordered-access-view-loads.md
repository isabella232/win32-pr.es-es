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
# <a name="typed-unordered-access-view-loads"></a>Cargas de la vista de acceso sin ordenar con tipo

La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad de un sombreador de leer desde un UAV con un FORMATO DXGI \_ específico.

-   [Información general](#overview)
-   [Formatos admitidos y llamadas API](#supported-formats-and-api-calls)
-   [Uso de cargas UAV con tipo desde HLSL](#using-typed-uav-loads-from-hlsl)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Una vista de acceso no ordenado (UAV) es una vista de un recurso de acceso desordenado (que puede incluir búferes, texturas y matrices de texturas, aunque sin muestreo múltiple). Un UAV permite el acceso de lectura y escritura sin ordenar temporalmente desde varios subprocesos. Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria. Este acceso simultáneo se controla mediante el uso de [funciones atómicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 y D3D11.3 se expanden en la lista de formatos que se pueden usar con cargas UAV con tipo.

## <a name="supported-formats-and-api-calls"></a>Formatos admitidos y llamadas API

Anteriormente, los tres formatos siguientes admiten cargas UAV con tipo y eran necesarias para el hardware D3D11.0. Se admiten para todo el hardware D3D11.3 y D3D12.

-   R32 \_ FLOAT
-   R32 \_ UINT
-   R32 \_ SINT

Los siguientes formatos se admiten como un conjunto en hardware D3D12 o D3D11.3, por lo que si se admite alguno, se admiten todos.

-   R32G32B32A32 \_ FLOAT
-   R32G32B32A32 \_ UINT
-   R32G32B32A32 \_ SINT
-   R16G16B16A16 \_ FLOAT
-   R16G16B16A16 \_ UINT
-   R16G16B16A16 \_ SINT
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ UINT
-   R8G8B8A8 \_ SINT
-   R16 \_ FLOAT
-   R16 \_ UINT
-   R16 \_ SINT
-   R8 \_ UNORM
-   R8 \_ UINT
-   R8 \_ SINT

Los siguientes formatos se admiten opcionalmente e individualmente en hardware D3D12 y D3D11.3, por lo que se tendría que realizar una única consulta en cada formato para probar la compatibilidad.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ SNORM
-   R32G32 \_ FLOAT
-   R32G32 \_ UINT
-   R32G32 \_ SINT
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ UINT
-   R11G11B10 \_ FLOAT
-   R8G8B8A8 \_ SNORM
-   R16G16 \_ FLOAT
-   R16G16 \_ UNORM
-   R16G16 \_ UINT
-   R16G16 \_ SNORM
-   R16G16 \_ SINT
-   R8G8 \_ UNORM
-   R8G8 \_ UINT
-   R8G8 \_ SNORM
-   8G8 \_ SINT
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Para determinar la compatibilidad con cualquier formato adicional, llame a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con la estructura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) como primer parámetro. El bit se establecerá si se admite la lista "compatible como `TypedUAVLoadAdditionalFormats` conjunto" anterior. Realice una segunda llamada a **CheckFeatureSupport** mediante una estructura [**FEATURE DATA FORMAT \_ \_ \_ \_ SUPPORT2 de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (comprobando la estructura devuelta con el miembro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD de la enumeración \_ \_ \_ \_ \_ [**D3D11 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) para determinar la compatibilidad en la lista de formatos admitidos opcionalmente anteriormente, por ejemplo:

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

## <a name="using-typed-uav-loads-from-hlsl"></a>Uso de cargas UAV con tipo desde HLSL

Para los UAV con tipo, la marca HLSL es D3D SHADER REQUIERE FORMATOS ADICIONALES DE CARGA DE \_ \_ \_ \_ UAV \_ CON \_ \_ TIPO.

Este es un ejemplo de código de sombreador para procesar una carga de UAV con tipo:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11.3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 