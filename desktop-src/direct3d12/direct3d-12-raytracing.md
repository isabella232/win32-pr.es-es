---
title: Direct3D 12 Raytracing
description: En este artículo se proporciona una lista de la documentación que está disponible para el raytracing de Direct3D.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d7896153f37a776faeddd00d78fbe0c1f3a120
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466343"
---
# <a name="direct3d-12-raytracing"></a>Direct3D 12 Raytracing

En este artículo se proporciona una lista de la documentación que está disponible para el raytracing de Direct3D.

## <a name="c-raytracing-reference"></a>Referencia de trazado de rayos de C++

En esta sección se incluyen vínculos a las API de C++ que se usan para implementar el raytracing de Direct3D 12.

### <a name="c-raytracing-interfaces"></a>Interfaces de control de rayos de C++

* [ID3D12Device5](/windows/desktop/api/d3d12/nn-d3d12-id3d12device5)
* [ID3D12GraphicsCommandList4](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist4)
* [ID3D12StateObject](/windows/desktop/api/d3d12/nn-d3d12-id3d12stateobject)
* [ID3D12StateObjectProperties](/windows/desktop/api/d3d12/nn-d3d12-id3d12stateobjectproperties)


### <a name="c-raytracing-structures"></a>Estructuras de trazado de rayos de C++


* [D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_desc)
* [D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs)
* [D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_TOOLS_VISUALIZATION_HEADER](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_tools_visualization_header)
* [D3D12_DISPATCH_RAYS_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_rays_desc)
* [D3D12_DXIL_LIBRARY_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dxil_library_desc)
* [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association)
* [D3D12_EXISTING_COLLECTION_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_existing_collection_desc)
* [D3D12_EXPORT_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_existing_collection_desc)
* [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_global_root_signature)
* [D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_virtual_address_and_stride)
* [D3D12_GPU_VIRTUAL_ADDRESS_RANGE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_virtual_address_range)
* [D3D12_GPU_VIRTUAL_ADDRESS_RANGE_AND_STRIDE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_virtual_address_range_and_stride)
* [D3D12_HIT_GROUP_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_hit_group_desc)
* [D3D12_LOCAL_ROOT_SIGNATURE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_local_root_signature)
* [D3D12_NODE_MASK](/windows/desktop/api/d3d12/ns-d3d12-d3d12_node_mask)
* [D3D12_RAYTRACING_AABB](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_aabb)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv)
* [D3D12_RAYTRACING_GEOMETRY_AABBS_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc)
* [D3D12_RAYTRACING_GEOMETRY_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc)
* [D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc)
* [D3D12_RAYTRACING_INSTANCE_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc)
* [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config)
* [D3D12_RAYTRACING_SHADER_CONFIG](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config)
* [D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER](/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_data_driver_matching_identifier)
* [D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER](/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_raytracing_acceleration_structure_header)
* [D3D12_STATE_OBJECT_CONFIG](/windows/desktop/api/d3d12/ns-d3d12-d3d12_state_object_config)
* [D3D12_STATE_OBJECT_DESC](/windows/desktop/api/d3d12/ns-d3d12-d3d12_state_object_desc)
* [D3D12_STATE_SUBOBJECT](/windows/desktop/api/d3d12/ns-d3d12-d3d12_state_subobject)
* [D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subobject_to_exports_association)
 

### <a name="c-raytracing-enumerations"></a>Enumeraciones de trazado de rayos de C++

* [D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_driver_matching_identifier_status)
* [D3D12_ELEMENTS_LAYOUT](/windows/desktop/api/d3d12/ne-d3d12-d3d12_elements_layout)
* [D3D12_EXPORT_FLAGS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_export_flags)
* [D3D12_HIT_GROUP_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_hit_group_type)
* [D3D12_RAY_FLAGS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_ray_flags)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type)
* [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type)
* [D3D12_RAYTRACING_GEOMETRY_FLAGS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags)
* [D3D12_RAYTRACING_GEOMETRY_TYPE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type)
* [D3D12_RAYTRACING_INSTANCE_FLAGS](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags)
* [D3D12_RAYTRACING_TIER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_tier)

## <a name="hlsl-raytracing-reference"></a>Referencia de rayos HLSL

Para obtener información sobre las construcciones HLSL usadas para implementar el trazado de rayos de Direct3D 12, vea Referencia de [HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia principal](direct3d-12-core-reference.md)
</dt> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





