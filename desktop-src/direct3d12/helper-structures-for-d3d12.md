---
title: Estructuras auxiliares para Direct3D 12
description: Estas estructuras auxiliares ayudan a inicializar muchas de las estructuras de Direct3D 12. Se declaran en `d3dx12.h` .
ms.assetid: 822CACCE-4A45-4104-91BD-4968A657662E
keywords:
- Estructuras auxiliares
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 07/28/2021
ms.openlocfilehash: 16dfa0349a815a07db810d67c21747cb767f7c39
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812367"
---
# <a name="helper-structures-for-direct3d-12"></a>Estructuras auxiliares para Direct3D 12

Estas estructuras auxiliares ayudan a inicializar muchas de las estructuras de Direct3D 12. Se declaran en `d3dx12.h` .

`d3dx12.h` está disponible por separado de los encabezados de Direct3D 12. Puede descargar desde `d3dx12.h` [la biblioteca auxiliar D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**CD3DX12_BLEND_DESC**](cd3dx12-blend-desc.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc) estructura. |
| [**CD3DX12_BOX**](cd3dx12-box.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box) estructura. |
| [**CD3DX12_CLEAR_VALUE**](cd3dx12-clear-value.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value) estructura. |
| [**CD3DX12_CPU_DESCRIPTOR_HANDLE**](cd3dx12-cpu-descriptor-handle.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) estructura. |
| [**CD3DX12_DEFAULT**](cd3dx12-default.md) | Pasa **D3D12_DEFAULT** a un constructor para cada estructura auxiliar. Esta estructura se usa simplemente como mecanismo para establecer parámetros predeterminados en las otras estructuras auxiliares. |
| [**CD3DX12_DEPTH_STENCIL_DESC**](cd3dx12-depth-stencil-desc.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) estructura. |
| [**CD3DX12_DEPTH_STENCIL_DESC1**](cd3dx12-depth-stencil-desc1.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) estructura. |
| [**CD3DX12_DESCRIPTOR_RANGE**](cd3dx12-descriptor-range.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range) estructura. |
| [**CD3DX12_DESCRIPTOR_RANGE1**](cd3dx12-descriptor-range1.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1) estructura. |
| [**CD3DX12_DXIL_LIBRARY_SUBOBJECT**](cd3dx12-dxil-library-subobject.md) | Clase auxiliar para crear un subobjeto de estado de biblioteca DXIL. |
| [**CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**](cd3dx12-dxil-subobject-to-exports-association.md) | Clase auxiliar para crear un subobjeto de estado de asociación DXIL-subobject-to-exports. |
| [**CD3DX12_EXISTING_COLLECTION_SUBOBJECT**](cd3dx12-existing-collection-subobject.md) | Clase auxiliar para crear un subobjeto de estado de colección existente. |
| [**CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-global-root-signature-subobject.md) | Clase auxiliar para crear un suboject de estado de firma raíz global. |
| [**CD3DX12_GPU_DESCRIPTOR_HANDLE**](cd3dx12-gpu-descriptor-handle.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) estructura. |
| [**CD3DX12_HEAP_DESC**](cd3dx12-heap-desc.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc) estructura. |
| [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) estructura. |
| [**CD3DX12_HIT_GROUP_SUBOBJECT**](cd3dx12-hit-group-subobject.md) | Clase auxiliar para crear un subobjeto de estado del grupo de impacto. |
| [**CD3DX12_NODE_MASK_SUBOBJECT**](cd3dx12-node-mask-subobject.md) | Clase auxiliar para crear un subobjeto de estado que identifica los nodos de GPU a los que se aplica el objeto de estado. |
| [**CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-local-root-signature-subobject.md) | Clase auxiliar para crear un suboject de estado de firma raíz local. |
| [**CD3DX12_PACKED_MIP_INFO**](cd3dx12-packed-mip-info.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info) estructura. |
| [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md) | Estructura auxiliar para crear y trabajar con estados de canalización de gráficos y proceso a través de una interfaz combinada. Vea [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) y [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM1**](cd3dx12-pipeline-state-stream1.md) | Estructura auxiliar para crear y trabajar con estados de canalización de gráficos y proceso a través de una interfaz combinada. Vea [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) y [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM2**](cd3dx12-pipeline-state-stream2.md) | Estructura auxiliar para crear y trabajar con estados de canalización de gráficos y proceso a través de una interfaz combinada. |
| [**CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) | Estructura auxiliar que se usa para describir una descripción de mezcla como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO**](cd3dx12-pipeline-state-stream-cached-pso.md) | Estructura auxiliar que se usa para describir un PSO almacenado en caché como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CS**](cd3dx12-pipeline-state-stream-cs.md) | Estructura auxiliar que se usa para describir un sombreador de proceso como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md) | Estructura auxiliar que se usa para describir una descripción de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md) | Estructura auxiliar que se usa para describir una descripción de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md) | Estructura auxiliar que se usa para describir el formato de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DS**](cd3dx12-pipeline-state-stream-ds.md) | Estructura auxiliar que se usa para describir un sombreador de dominio como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_FLAGS**](cd3dx12-pipeline-state-stream-flags.md) | Estructura auxiliar que se usa para describir las marcas de estado de canalización como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_GS**](cd3dx12-pipeline-state-stream-gs.md) | Estructura auxiliar que se usa para describir un sombreador de geometría como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_HS**](cd3dx12-pipeline-state-stream-hs.md) | Estructura auxiliar que se usa para describir un sombreador de casco como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md) | Estructura auxiliar que se usa para describir el valor de corte de franja del búfer de índice como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md) | Estructura auxiliar que se usa para describir un diseño de entrada como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK**](cd3dx12-pipeline-state-stream-node-mask.md) | Estructura auxiliar que se usa para describir una máscara de nodo como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER**](cd3dx12-pipeline-state-stream-parse-helper.md) | Compila un objeto CD3DX12_PIPELINE_STATE_STREAM a partir de los detalles del subobjeto pasados a las funciones miembro correspondientes. Esta estructura implementa la interfaz [**ID3DX12PipelineParserCallbacks.**](id3dx12pipelineparsercallbacks.md) |
| [**CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY**](cd3dx12-pipeline-state-stream-primitive-topology.md) | Estructura auxiliar que se usa para describir la topología primitiva como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PS**](cd3dx12-pipeline-state-stream-ps.md) | Estructura auxiliar que se usa para describir un sombreador de píxeles como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) | Estructura auxiliar que se usa para describir una descripción de rasterizador como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS**](cd3dx12-pipeline-state-stream-render-target-formats.md) | Estructura auxiliar que se usa para describir los formatos de destino de representación como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE**](cd3dx12-pipeline-state-stream-root-signature.md) | Estructura auxiliar que se usa para describir la firma raíz como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC**](cd3dx12-pipeline-state-stream-sample-desc.md) | Estructura auxiliar que se usa para describir una descripción de ejemplo como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK**](cd3dx12-pipeline-state-stream-sample-mask.md) | Estructura auxiliar que se usa para describir una máscara de ejemplo como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md) | Estructura auxiliar que se usa para describir la descripción de salida del flujo como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) | Estructura auxiliar con plantilla que se usa para encapsular pares de datos de subobjeto y subobjeto como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING**](cd3dx12-pipeline-state-stream-view-instancing.md) | Estructura auxiliar que se usa para encapsular una [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) estructura. Permite que los sombreadores se representen en varias vistas con una sola llamada a draw; útil para la visión estéreo o la generación de mapas de cubo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VS**](cd3dx12-pipeline-state-stream-vs.md) | Estructura auxiliar que se usa para describir un sombreador de vértices como un único objeto adecuado para una descripción de secuencia. |
| [**CD3DX12_RANGE**](cd3dx12-range.md) | Una estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range) estructura. |
| [**CD3DX12_RANGE_UINT64**](cd3dx12-range-uint64.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64) estructura. |
| [**CD3DX12_RASTERIZER_DESC**](cd3dx12-rasterizer-desc.md) | Una estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) estructura. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**](cd3dx12-raytracing-pipeline-config-subobject.md) | Clase auxiliar para crear un subobjeto de estado de configuración de canalización de rayos. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**](cd3dx12-raytracing-pipeline-config1-subobject.md) | Clase auxiliar para crear un subobjeto de estado de configuración de canalización de rayos, con marcas. |
| [**CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**](cd3dx12-raytracing-shader-config-subobject.md) | Clase auxiliar para crear un subobjeto de estado de configuración de sombreador de rayos. |
| [**CD3DX12_RECT**](cd3dx12-rect.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RECT**](d3d12-rect.md) estructura. |
| [**CD3DX12_RESOURCE_ALLOCATION_INFO**](cd3dx12-resource-allocation-info.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) estructura. |
| [**CD3DX12_RESOURCE_BARRIER**](cd3dx12-resource-barrier.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier) estructura. |
| [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc) estructura. |
| [**CD3DX12_RESOURCE_DESC1**](cd3dx12-resource-desc1.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) estructura. |
| [**CD3DX12_ROOT_CONSTANTS**](cd3dx12-root-constants.md) | Una estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants) estructura. |
| [**CD3DX12_ROOT_DESCRIPTOR**](cd3dx12-root-descriptor.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor) estructura. |
| [**CD3DX12_ROOT_DESCRIPTOR1**](cd3dx12-root-descriptor1.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1) estructura. |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE**](cd3dx12-root-descriptor-table.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) estructura. |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE1**](cd3dx12-root-descriptor-table1.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) estructura. |
| [**CD3DX12_ROOT_PARAMETER**](cd3dx12-root-parameter.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter) estructura. |
| [**CD3DX12_ROOT_PARAMETER1**](cd3dx12-root-parameter1.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1) estructura. |
| [**CD3DX12_ROOT_SIGNATURE_DESC**](cd3dx12-root-signature-desc.md) | Una estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) estructura. |
| [**CD3DX12_RT_FORMAT_ARRAY**](cd3dx12-rt-format-array.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array) estructura. |
| [**CD3DX12_SHADER_BYTECODE**](cd3dx12-shader-bytecode.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) estructura. |
| [**CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**](cd3dx12-state-object-config-subobject.md) | Clase auxiliar para crear un subobjeto que define las propiedades generales de un objeto de estado. |
| [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) | Clase central de los asistentes de creación de objetos de estado D3DX12, que son clases auxiliares para crear objetos de estado a través de un conjunto arbitrario de subobjetos. |
| [**CD3DX12_STATIC_SAMPLER_DESC**](cd3dx12-static-sampler-desc.md) | Estructura auxiliar para permitir la inicialización sencilla de una [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) estructura. |
| [**CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**](cd3dx12-subobject-to-exports-association-subobject.md) | Clase auxiliar para crear un subobjeto de estado de asociación de subobjeto a exportaciones. |
| [**CD3DX12_SUBRESOURCE_FOOTPRINT**](cd3dx12-subresource-footprint.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) estructura. |
| [**CD3DX12_SUBRESOURCE_RANGE_UINT64**](cd3dx12-subresource-range-uint64.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) estructura. |
| [**CD3DX12_SUBRESOURCE_TILING**](cd3dx12-subresource-tiling.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling) estructura. |
| [**CD3DX12_TEXTURE_COPY_LOCATION**](cd3dx12-texture-copy-location.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location) estructura. |
| [**CD3DX12_TILE_REGION_SIZE**](cd3dx12-tile-region-size.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) estructura. |
| [**CD3DX12_TILE_SHAPE**](cd3dx12-tile-shape.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) estructura. |
| [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) estructura. |
| [**CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC**](cd3dx12-versioned-root-signature-desc.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) estructura. |
| [**CD3DX12_VIEW_INSTANCING_DESC**](cd3dx12-view-instancing-desc.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) estructura. |
| [**CD3DX12_VIEWPORT**](cd3dx12-viewport.md) | Estructura auxiliar para permitir la inicialización sencilla de [**una D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport) estructura. |
| [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) | Para [los sombreadores mesh/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html), puede usar los datos de [effectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), con **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, para proporcionar todo el estado. |

## <a name="related-topics"></a>Temas relacionados

* [Estructuras y funciones auxiliares para D3D12](helper-structures-and-functions-for-d3d12.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
