---
title: Consulta de funcionalidad
description: 'La aplicación puede detectar el nivel de compatibilidad con el enlace de recursos y muchas otras características, con una llamada a ID3D12Device \: \: CheckFeatureSupport.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: a99174515883f8995167a7b866ab1ef8b77b56f7a0be2bb83f960abd06e47713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851405"
---
# <a name="capability-querying"></a>Consulta de funcionalidad

La aplicación puede detectar el nivel de compatibilidad para el enlace de recursos (así como el nivel de compatibilidad para muchas otras características), con una llamada a [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

## <a name="how-to-query-for-the-resource-binding-tier"></a>Cómo consultar el nivel de enlace de recursos

Este primer ejemplo se centra en el enlace de recursos. Cada nivel de enlace de recursos es un superconjunto de niveles inferiores de funcionalidad, por lo que el código que funciona en un nivel determinado funciona sin cambios en cualquier nivel superior.

Los niveles de enlace de recursos son constantes en la [**enumeración D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) recursos.

Para consultar el nivel de enlace de recursos, use código como este. En este ejemplo de código se muestra el patrón general para consultar cualquiera de los distintos tipos de compatibilidad con características.

```cppwinrt
D3D12_RESOURCE_BINDING_TIER get_resource_binding_tier(::ID3D12Device* pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &featureSupport, sizeof(featureSupport))
    );

    switch (featureSupport.ResourceBindingTier)
    {
    case D3D12_RESOURCE_BINDING_TIER_1:
        // Tier 1 is supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_2:
        // Tiers 1 and 2 are supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_3:
        // Tiers 1, 2, and 3 are supported.
        break;
    }

    return featureSupport.ResourceBindingTier;
}
```

Tenga en cuenta que cualquier constante enumerada que pase [**(D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), en este caso) tiene una estructura de datos correspondiente que recibe información sobre esa característica o conjunto de características [**(D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), en este caso). Pase siempre un puntero a la estructura que coincida con la constante enumerada que se pasa.

## <a name="how-to-query-for-any-feature-level"></a>Consulta de cualquier nivel de característica

Además del nivel de enlace de recursos, hay muchas otras características cuyo nivel de compatibilidad puede consultar para usar el mismo patrón que se muestra en el ejemplo de código anterior. Solo tiene que pasar una constante diferente de la enumeración [**D3D12_FEATURE a**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (para decir a la API sobre qué característica solicitar información de soporte técnico) y pasar un puntero a una instancia de la estructura de coincidencia (en la que se va a recibir la información solicitada).

- Pase **D3D12_FEATURE_ARCHITECTURE** y [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).
- Pase **D3D12_FEATURE_ARCHITECTURE1** y [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).
- Pase **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** y [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).
- Pase **D3D12_FEATURE_CROSS_NODE** y [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).
- Pase **D3D12_FEATURE_D3D12_OPTIONS** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).
- Pase **D3D12_FEATURE_D3D12_OPTIONS1** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).
- Pase **D3D12_FEATURE_D3D12_OPTIONS2** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).
- Pase **D3D12_FEATURE_D3D12_OPTIONS3** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).
- Pase **D3D12_FEATURE_D3D12_OPTIONS4** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).
- Pase **D3D12_FEATURE_D3D12_OPTIONS5** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).
- Pase **D3D12_FEATURE_EXISTING_HEAPS** y [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).
- Pase **D3D12_FEATURE_FEATURE_LEVELS** y [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).
- Pase **D3D12_FEATURE_FORMAT_INFO** y [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).
- Pase **D3D12_FEATURE_FORMAT_SUPPORT** y [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).
- Pase **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** y [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).
- Pase **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** y [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).
- Pase **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** y [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).
- Pase **D3D12_FEATURE_ROOT_SIGNATURE** y [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).
- Pase **D3D12_FEATURE_SERIALIZATION** y [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).
- Pase **D3D12_FEATURE_SHADER_CACHE** y [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).
- Pase **D3D12_FEATURE_SHADER_MODEL** y [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).

## <a name="hardware-support-for-dxgi-formats"></a>Compatibilidad de hardware con formatos DXGI

Para ver tablas de formatos DXGI y características de hardware, consulte estos temas.

- [Compatibilidad con formato DXGI para hardware de nivel 12.1 de características de Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [Compatibilidad con formato DXGI para hardware de nivel 12.0 de características de Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [Compatibilidad con el formato DXGI para hardware de nivel 11.1 de características de Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [Compatibilidad con formato DXGI para hardware de nivel 11.0 de características de Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Compatibilidad de hardware con formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
- [Compatibilidad de hardware con formatos de Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
- [Compatibilidad de hardware con formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

* [Enlace de recursos en Direct3D 12](resource-binding.md)
* [Niveles de características de hardware](hardware-feature-levels.md)
* [Firmas raíz](root-signatures.md)