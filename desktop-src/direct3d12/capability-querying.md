---
title: Consulta de funcionalidades
description: 'La aplicación puede detectar el nivel de compatibilidad para el enlace de recursos y muchas otras características, con una llamada a ID3D12Device \: \: CheckFeatureSupport.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: eaf451f91d51cfa6e900f328898c3418f0974a2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549094"
---
# <a name="capability-querying"></a><span data-ttu-id="f6e4e-103">Consulta de funcionalidades</span><span class="sxs-lookup"><span data-stu-id="f6e4e-103">Capability querying</span></span>

<span data-ttu-id="f6e4e-104">La aplicación puede detectar el nivel de compatibilidad para el enlace de recursos (así como el nivel de compatibilidad para muchas otras características), con una llamada a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-104">Your application can discover the level of support for resource binding (as well as the level of support for many other features), with a call to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

## <a name="how-to-query-for-the-resource-binding-tier"></a><span data-ttu-id="f6e4e-105">Cómo consultar el nivel de enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="f6e4e-105">How to query for the resource binding tier</span></span>

<span data-ttu-id="f6e4e-106">Este primer ejemplo se centra en el enlace de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6e4e-106">This first example focuses on resource binding.</span></span> <span data-ttu-id="f6e4e-107">Cada nivel de enlace de recursos es un superconjunto de niveles inferiores en funcionalidad, por lo que el código que funciona en un nivel determinado funciona sin cambios en cualquier nivel superior.</span><span class="sxs-lookup"><span data-stu-id="f6e4e-107">Each resource binding tier is a superset of lower tiers in functionality, so code that works on a given tier works unchanged on any higher tier.</span></span>

<span data-ttu-id="f6e4e-108">Los niveles de enlace de recursos son constantes en la enumeración [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) .</span><span class="sxs-lookup"><span data-stu-id="f6e4e-108">The resource binding tiers are constants in the [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) enumeration.</span></span>

<span data-ttu-id="f6e4e-109">Para consultar el nivel de enlace de recursos, use código como este.</span><span class="sxs-lookup"><span data-stu-id="f6e4e-109">To query for the resource binding tier, use code such as this.</span></span> <span data-ttu-id="f6e4e-110">En este ejemplo de código se muestra el patrón general para consultar cualquiera de los diversos tipos de compatibilidad de características.</span><span class="sxs-lookup"><span data-stu-id="f6e4e-110">This code example demonstrates the general pattern for querying for any of the various kinds of feature support.</span></span>

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

<span data-ttu-id="f6e4e-111">Tenga en cuenta que cualquier constante enumerada que pase ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), en este caso) tiene una estructura de datos correspondiente que recibe información sobre esa característica o conjunto de características ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), en este caso).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-111">Note that any enumerated constant that you pass ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), in this case) has a corresponding data structure that receives info about that feature or set of features ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), in this case).</span></span> <span data-ttu-id="f6e4e-112">Pase siempre un puntero a la estructura que coincida con la constante enumerada que se pasa.</span><span class="sxs-lookup"><span data-stu-id="f6e4e-112">Always pass a pointer to the structure that matches the enumerated constant that you pass.</span></span>

## <a name="how-to-query-for-any-feature-level"></a><span data-ttu-id="f6e4e-113">Cómo consultar cualquier nivel de características</span><span class="sxs-lookup"><span data-stu-id="f6e4e-113">How to query for any feature level</span></span>

<span data-ttu-id="f6e4e-114">Además del nivel de enlace de recursos, hay muchas otras características cuyo nivel de compatibilidad se puede consultar con el mismo patrón que se muestra en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="f6e4e-114">As well as the resource binding tier, there are many other features whose level of support you can query for using the same pattern shown in the code example above.</span></span> <span data-ttu-id="f6e4e-115">Solo tiene que pasar una constante diferente de la enumeración [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (para indicar a la API Qué característica solicitar información de soporte técnico) y pasar un puntero a una instancia de la estructura coincidente (en la que se va a recibir la información solicitada).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-115">You just pass a different constant from the [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) enumeration to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (to tell the API what feature to request support information on), and you pass a pointer to an instance of the matching structure (in which to receive the requested info).</span></span>

- <span data-ttu-id="f6e4e-116">Pase **D3D12_FEATURE_ARCHITECTURE** y [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-116">Pass **D3D12_FEATURE_ARCHITECTURE** and [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span></span>
- <span data-ttu-id="f6e4e-117">Pase **D3D12_FEATURE_ARCHITECTURE1** y [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-117">Pass **D3D12_FEATURE_ARCHITECTURE1** and [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span></span>
- <span data-ttu-id="f6e4e-118">Pase **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** y [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-118">Pass **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** and [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span></span>
- <span data-ttu-id="f6e4e-119">Pase **D3D12_FEATURE_CROSS_NODE** y [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-119">Pass **D3D12_FEATURE_CROSS_NODE** and [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span></span>
- <span data-ttu-id="f6e4e-120">Pase **D3D12_FEATURE_D3D12_OPTIONS** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-120">Pass **D3D12_FEATURE_D3D12_OPTIONS** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span></span>
- <span data-ttu-id="f6e4e-121">Pase **D3D12_FEATURE_D3D12_OPTIONS1** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-121">Pass **D3D12_FEATURE_D3D12_OPTIONS1** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span></span>
- <span data-ttu-id="f6e4e-122">Pase **D3D12_FEATURE_D3D12_OPTIONS2** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-122">Pass **D3D12_FEATURE_D3D12_OPTIONS2** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span></span>
- <span data-ttu-id="f6e4e-123">Pase **D3D12_FEATURE_D3D12_OPTIONS3** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-123">Pass **D3D12_FEATURE_D3D12_OPTIONS3** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span></span>
- <span data-ttu-id="f6e4e-124">Pase **D3D12_FEATURE_D3D12_OPTIONS4** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-124">Pass **D3D12_FEATURE_D3D12_OPTIONS4** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span></span>
- <span data-ttu-id="f6e4e-125">Pase **D3D12_FEATURE_D3D12_OPTIONS5** y [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-125">Pass **D3D12_FEATURE_D3D12_OPTIONS5** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span></span>
- <span data-ttu-id="f6e4e-126">Pase **D3D12_FEATURE_EXISTING_HEAPS** y [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-126">Pass **D3D12_FEATURE_EXISTING_HEAPS** and [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span></span>
- <span data-ttu-id="f6e4e-127">Pase **D3D12_FEATURE_FEATURE_LEVELS** y [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-127">Pass **D3D12_FEATURE_FEATURE_LEVELS** and [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span></span>
- <span data-ttu-id="f6e4e-128">Pase **D3D12_FEATURE_FORMAT_INFO** y [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-128">Pass **D3D12_FEATURE_FORMAT_INFO** and [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span></span>
- <span data-ttu-id="f6e4e-129">Pase **D3D12_FEATURE_FORMAT_SUPPORT** y [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-129">Pass **D3D12_FEATURE_FORMAT_SUPPORT** and [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span></span>
- <span data-ttu-id="f6e4e-130">Pase **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** y [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-130">Pass **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** and [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span></span>
- <span data-ttu-id="f6e4e-131">Pase **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** y [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-131">Pass **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** and [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span></span>
- <span data-ttu-id="f6e4e-132">Pase **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** y [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-132">Pass **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** and [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span></span>
- <span data-ttu-id="f6e4e-133">Pase **D3D12_FEATURE_ROOT_SIGNATURE** y [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-133">Pass **D3D12_FEATURE_ROOT_SIGNATURE** and [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span></span>
- <span data-ttu-id="f6e4e-134">Pase **D3D12_FEATURE_SERIALIZATION** y [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-134">Pass **D3D12_FEATURE_SERIALIZATION** and [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span></span>
- <span data-ttu-id="f6e4e-135">Pase **D3D12_FEATURE_SHADER_CACHE** y [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-135">Pass **D3D12_FEATURE_SHADER_CACHE** and [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span></span>
- <span data-ttu-id="f6e4e-136">Pase **D3D12_FEATURE_SHADER_MODEL** y [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span><span class="sxs-lookup"><span data-stu-id="f6e4e-136">Pass **D3D12_FEATURE_SHADER_MODEL** and [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span></span>

## <a name="hardware-support-for-dxgi-formats"></a><span data-ttu-id="f6e4e-137">Compatibilidad de hardware con formatos de DXGI</span><span class="sxs-lookup"><span data-stu-id="f6e4e-137">Hardware support for DXGI Formats</span></span>

<span data-ttu-id="f6e4e-138">Para ver tablas de formatos y características de hardware de DXGI, consulte estos temas.</span><span class="sxs-lookup"><span data-stu-id="f6e4e-138">To view tables of DXGI formats and hardware features, refer to these topics.</span></span>

- [<span data-ttu-id="f6e4e-139">Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,1</span><span class="sxs-lookup"><span data-stu-id="f6e4e-139">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [<span data-ttu-id="f6e4e-140">Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,0</span><span class="sxs-lookup"><span data-stu-id="f6e4e-140">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [<span data-ttu-id="f6e4e-141">Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="f6e4e-141">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [<span data-ttu-id="f6e4e-142">Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,0</span><span class="sxs-lookup"><span data-stu-id="f6e4e-142">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- <span data-ttu-id="f6e4e-143">[Compatibilidad de hardware con formatos 10Level9 de Direct3D](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6e4e-143">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
- <span data-ttu-id="f6e4e-144">[Compatibilidad de hardware con formatos de Direct3D 10,1](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6e4e-144">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
- <span data-ttu-id="f6e4e-145">[Compatibilidad de hardware con formatos de Direct3D 10](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6e4e-145">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6e4e-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6e4e-146">Related topics</span></span>

* [<span data-ttu-id="f6e4e-147">Enlace de recursos en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f6e4e-147">Resource binding in Direct3D 12</span></span>](resource-binding.md)
* [<span data-ttu-id="f6e4e-148">Niveles de características de hardware</span><span class="sxs-lookup"><span data-stu-id="f6e4e-148">Hardware feature levels</span></span>](hardware-feature-levels.md)
* [<span data-ttu-id="f6e4e-149">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="f6e4e-149">Root signatures</span></span>](root-signatures.md)