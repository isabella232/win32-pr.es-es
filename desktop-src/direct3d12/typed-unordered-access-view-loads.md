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
# <a name="typed-unordered-access-view-uav-loads"></a>Cargas de la vista de acceso sin ordenar (UAV) con tipo

La carga con tipo de vista de acceso no ordenado (UAV) es la capacidad de que un sombreador lea desde un UAV con un [**FORMATO DXGI \_ específico.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

-   [Información general](#overview)
-   [Formatos admitidos y llamadas API](#supported-formats-and-api-calls)
-   [Uso de cargas UAV con tipo desde HLSL](#using-typed-uav-loads-from-hlsl)
-   [Uso de cargas UAV con tipo UNORM y SNORM desde HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Una vista de acceso desordenado (UAV) es una vista de un recurso de acceso desordenado (que puede incluir búferes, texturas y matrices de texturas, aunque sin muestreo múltiple). Un UAV permite el acceso de lectura y escritura sin ordenar temporalmente desde varios subprocesos. Esto significa que varios subprocesos pueden leer o escribir simultáneamente este tipo de recurso sin generar conflictos de memoria. Este acceso simultáneo se controla mediante el uso de [Funciones atómicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 (y D3D11.3) se expande en la lista de formatos que se pueden usar con cargas UAV con tipo.

## <a name="supported-formats-and-api-calls"></a>Formatos admitidos y llamadas API

Anteriormente, los tres formatos siguientes admiten cargas UAV con tipo y eran necesarios para el hardware D3D11.0. Se admiten para todo el hardware D3D11.3 y D3D12.

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

Los siguientes formatos se admiten opcionalmente e individualmente en hardware D3D12 y D3D11.3, por lo que se tendría que realizar una consulta única en cada formato para probar la compatibilidad.

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
-   R8G8 \_ SINT
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Para determinar la compatibilidad con cualquier formato adicional, llame a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la estructura [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) como primer parámetro (consulte [Capability Querying](capability-querying.md)). El *campo TypedUAVLoadAdditionalFormats* se establecerá si se admite la lista "compatible como conjunto" anterior. Realice una segunda llamada a **CheckFeatureSupport** mediante una estructura [**D3D12 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (comprobando la estructura devuelta con el miembro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD de la enumeración \_ \_ \_ \_ \_ [**D3D12 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) para determinar la compatibilidad en la lista de formatos compatibles opcionalmente mencionados anteriormente, por ejemplo:

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

## <a name="using-typed-uav-loads-from-hlsl"></a>Uso de cargas UAV con tipo desde HLSL

Para los UAV con tipo, la marca HLSL es D3D SHADER REQUIRES TYPED UAV LOAD ADDITIONAL FORMATS (SOMBREADOR D3D REQUIERE FORMATOS \_ \_ \_ \_ ADICIONALES DE CARGA DE UAV \_ CON \_ \_ TIPO).

Este es un ejemplo de código de sombreador para procesar una carga de UAV con tipo:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Uso de cargas UAV con tipo UNORM y SNORM desde HLSL

Al usar cargas UAV con tipo para leer desde un recurso UNORM o SNORM, debe declarar correctamente el tipo de elemento del objeto HLSL como `unorm` o `snorm` . Se especifica como comportamiento indefinido para no coincide el tipo de elemento declarado en HLSL con el tipo de datos de recurso subyacente. Por ejemplo, si usa cargas UAV con tipo en un recurso de búfer con datos \_ R8 UNORM, debe declarar el tipo de elemento como `unorm float` :

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación](rendering.md)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> <dt>

[Enlace de recursos en HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 