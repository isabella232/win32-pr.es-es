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
# <a name="typed-unordered-access-view-uav-loads"></a>Cargas de vista de acceso no ordenada (UAV) con tipo

La carga con tipo de vista de acceso sin ordenar (UAV) es la capacidad para que un sombreador lea desde un UAV con [**un \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)específico.

-   [Información general](#overview)
-   [Formatos admitidos y llamadas API](#supported-formats-and-api-calls)
-   [Uso de cargas UAV con tipo desde HLSL](#using-typed-uav-loads-from-hlsl)
-   [Usar UNORM y SNORM con tipo UAV se carga desde HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Una vista de acceso desordenado (UAV) es una vista de un recurso de acceso desordenado (que puede incluir búferes, texturas y matrices de texturas, pero sin muestreo múltiple). Un UAV permite el acceso de lectura y escritura sin ordenar de forma temporal desde varios subprocesos. Esto significa que varios subprocesos pueden leer o escribir este tipo de recurso simultáneamente sin generar conflictos de memoria. Este acceso simultáneo se controla mediante el uso de [funciones atómicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 (y D3D 11.3) se expande en la lista de formatos que se pueden usar con las cargas de UAV con tipo.

## <a name="supported-formats-and-api-calls"></a>Formatos admitidos y llamadas API

Anteriormente, los tres formatos siguientes admitieron cargas de UAV con tipo y eran necesarios para el hardware D3D 11.0. Son compatibles con todos los hardware D3D 11.3 y D3D12.

-   R32 \_ float
-   R32 \_ uint
-   R32 \_ Sint

Los formatos siguientes se admiten como un conjunto en el hardware de D3D12 o D3D 11.3, por lo que si se admite cualquiera de ellos, se admiten todos.

-   R32G32B32A32 \_ float
-   R32G32B32A32 \_ uint
-   R32G32B32A32 \_ Sint
-   R16G16B16A16 \_ float
-   R16G16B16A16 \_ uint
-   R16G16B16A16 \_ Sint
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ uint
-   R8G8B8A8 \_ Sint
-   R16 \_ float
-   R16 \_ uint
-   R16 \_ Sint
-   R8 \_ UNORM
-   R8 \_ uint
-   R8 \_ Sint

Los siguientes formatos se admiten opcional y de forma individual en el hardware D3D12 y D3D 11.3, por lo que es necesario realizar una sola consulta en cada formato para probar la compatibilidad.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ SNORM
-   R32G32 \_ float
-   R32G32 \_ uint
-   R32G32 \_ Sint
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ uint
-   R11G11B10 \_ float
-   R8G8B8A8 \_ SNORM
-   R16G16 \_ float
-   R16G16 \_ UNORM
-   R16G16 \_ uint
-   R16G16 \_ SNORM
-   R16G16 \_ Sint
-   R8G8 \_ UNORM
-   R8G8 \_ uint
-   R8G8 \_ SNORM
-   R8G8 \_ Sint
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Para determinar la compatibilidad con cualquier otro formato, llame a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la estructura de [**\_ \_ \_ \_ Opciones D3D12 de datos de la característica D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) como primer parámetro (consulte consultas de [capacidad](capability-querying.md)). El campo *TypedUAVLoadAdditionalFormats* se establecerá si se admite la lista "compatible como conjunto" anterior. Realice una segunda llamada a **CheckFeatureSupport**, usando una estructura de [**\_ \_ \_ \_ compatibilidad con el formato de datos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) de las características de D3D12 (con la comprobación de la estructura devuelta con el miembro de carga D3D12 con el formato de \_ \_ \_ \_ determinante UAV con tipo \_ de la enumeración de [**\_ format \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) ) para determinar la compatibilidad en la lista de formatos admitidos opcionalmente, por ejemplo:

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

En el caso de UAVs con tipo, la marca de HLSL es el \_ sombreador D3D que \_ requiere un \_ tipo \_ UAV \_ cargar \_ \_ formatos adicionales.

Este es un ejemplo de código de sombreador para procesar una carga de UAV con tipo:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Usar UNORM y SNORM con tipo UAV se carga desde HLSL

Al usar cargas UAV con tipo para leer desde un recurso UNORM o SNORM, debe declarar correctamente el tipo de elemento del objeto HLSL como `unorm` o `snorm` . Se especifica como comportamiento no definido para no coincidir con el tipo de elemento declarado en HLSL con el tipo de datos de recurso subyacente. Por ejemplo, si usa cargas UAV con tipo en un recurso de búfer con datos de R8 \_ UNORM, debe declarar el tipo de elemento como `unorm float` :

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

[Modelo de sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 