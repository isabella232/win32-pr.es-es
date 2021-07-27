---
title: Enumeraciones básicas
description: Las enumeraciones siguientes se declaran en d3d12.h.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 31cac62c8dfa6b1126d8ff2a7c134490c0c58038
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436230"
---
# <a name="core-enumerations"></a>Enumeraciones básicas

Las enumeraciones siguientes se declaran en d3d12.h.

## <a name="in-this-section"></a>En esta sección

| Tema y descripción |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Especifica la versión del diseño de firma raíz. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Especifica un modelo de sombreador. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Define constantes que especifican operaciones de gpu de representación o proceso. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Define constantes que especifican un nivel de optimización dinámica que se va a aplicar al trabajo de GPU que se envía posteriormente. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Especifica los factores de mezcla, que modularán los valores para el sombreador de píxeles y el destino de representación. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Especifica operaciones de combinación RGB o alfa. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Identifica cómo ver un recurso de búfer. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Identifica las opciones de vista de acceso desordenado para un recurso de búfer. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Especifica lo que se debe borrar de la vista de galería de símbolos de profundidad. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Identifica qué componentes de cada píxel de un destino de representación se pueden escribir durante la mezcla. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Se usa para determinar qué tipos de listas de comandos son capaces de admitir varias operaciones. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Especifica el tipo de una lista de comandos. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Especifica las marcas que se usarán al crear una cola de comandos. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Define los niveles de prioridad para una cola de comandos. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Especifica las opciones de comparación. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Identifica si la rasterización conservadora está desactivada o no. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Identifica el nivel de rasterización conservadora. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Especifica las propiedades de la página de CPU para el montón. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Especifica el nivel de uso compartido entre nodos de un adaptador, como Nivel 1 emulado, Nivel 1 o Nivel 2.  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Especifica que los triángulos orientados a una dirección determinada no se dibujan. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Especifica el tipo de datos de la memoria a la que apunta el parámetro *pData* de [**ID3D12DebugDevice1::SetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) e [**ID3D12DebugDevice1::GetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter). |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Identifica la parte de un búfer de galería de símbolos de profundidad para escribir datos de profundidad. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Especifica las opciones de un montón. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Especifica un tipo de montón de descriptores.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Especifica la inestabilidad de ambos descriptores y los datos a los que hacen referencia en una descripción de firma raíz 1.1, que puede habilitar algunas optimizaciones de controladores. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Especifica un intervalo para que, por ejemplo, si parte de una tabla de descriptores tiene 100 vistas de recursos de sombreador (SRV), ese intervalo se puede declarar en una entrada en lugar de 100.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Define constantes que especifican operaciones de gpu de representación o proceso. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Define constantes (usadas por la interfaz [ID3D12DeviceRemovedExtendedDataSettings)](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)que especifican cómo se habilitan las características individuales de datos extendidos (DRED) quitados del dispositivo. |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Define las constantes usadas en la [estructura D3D12_DEVICE_REMOVED_EXTENDED_DATA para](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) especificar marcas de control para el tiempo de ejecución de Direct3D. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Define constantes que especifican una versión de Datos extendidos quitados del dispositivo (DRED), tal como [se usa en la D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA estructura](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Especifica cómo acceder a un recurso usado en una vista de galería de símbolos de profundidad. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Especifica las opciones de vista de galería de símbolos de profundidad. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Opciones de características de Direct3D 12 compatibles con el controlador de gráficos actual.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Especifica las opciones de barrera.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Especifica el modo de relleno que se usará al representar triángulos. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Especifica las opciones de filtrado durante el muestreo de textura. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Especifica el tipo de reducción de filtro.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Especifica el tipo de filtros de sampler de ampliación o minificación.  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Especifica los recursos que se admiten para un formato proporcionado. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Especifica qué opciones de recursos no ordenados se admiten para un formato proporcionado. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Define marcas que especifican los estados relacionados con una lista de comandos gráficos. Los valores pueden ser OR bit a bit juntos. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Especifica opciones del montón, como si el montón puede contener texturas y si los recursos se comparten entre adaptadores.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Define constantes que especifican la compatibilidad con la serialización del montón. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Especifica el tipo de montón. Cuando residen, los montones residen en un grupo de memoria física determinado con determinadas propiedades de caché de CPU.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). Al usar la topología primitiva de franja de triángulo, las posiciones de vértice se interpretan como vértices de una franja de triángulo continua. Hay un valor de índice especial que representa el deseo de tener una discontinuidad en la franja, el valor del índice de corte. Esta enumeración enumera los valores de corte admitidos.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Especifica el tipo del parámetro indirecto.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Identifica el tipo de datos contenidos en una ranura de entrada. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Define constantes que especifican el estado de duración de un objeto de seguimiento de duración. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Especifica las operaciones lógicas que se configuran para un destino de representación. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Define constantes que especifican lo que se debe hacer con los resultados de la instrumentación de carga de trabajo anterior. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Especifica el grupo de memoria para el montón. |
| [**D3D12_MESH_SHADER_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_mesh_shader_tier). Define constantes que especifican la compatibilidad del sombreador de malla y de amplificación. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Define constantes que especifican las marcas de un parámetro en un meta comando. Los valores pueden ser or bit a bit juntos. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Define constantes que especifican la fase de un parámetro en un meta comando. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Define constantes que especifican el tipo de datos de un parámetro para un meta comando. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Especifica varias marcas de espera para varias barreras. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Especifica las opciones para determinar los niveles de calidad.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Marcas para controlar el estado de la canalización.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Especifica el tipo de un sub object en una descripción de flujo de estado de canalización. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Especifica la operación de predicado que se va a aplicar.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Especifica cómo interpreta la canalización las primitivas de entrada de geometría o sombreador de casco. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Especifica el nivel de compatibilidad para las posiciones de ejemplo programables que ofrece el adaptador. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Define constantes que especifican marcas de sesión de recursos protegidos. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Define constantes que especifican la compatibilidad con la sesión de recursos protegidos. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Define constantes que especifican el estado de la sesión protegida. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Especifica el tipo de montón de consultas que se va a crear. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Especifica el tipo de consulta. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Marcas que se pasan a la [**función TraceRay**](./traceray-function.md) para invalidar la transparencia, la selección y el comportamiento de salida anticipada. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Especifica marcas para la compilación de una estructura de aceleración de rayos. Use un valor de esta enumeración con la [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) estructura que proporciona entrada a la operación de compilación de la estructura de aceleración. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Especifica el tipo de operación de copia realizada al llamar [**a CopyRaytracingAccelerationStructure.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure) |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Especifica el tipo de información posterior a la compilación de la estructura de aceleración que se puede recuperar con llamadas a [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) y [**BuildRaytracingAccelerationStructure.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure) |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Especifica el tipo de una estructura de aceleración de rayos. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Especifica marcas para la geometría de trazado de rayos en una [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) estructura. |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Especifica el tipo de geometría que se usa para la traza de rayos. Use un valor de esta enumeración para especificar el tipo geometry en un [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Marcas para una instancia de estructura de aceleración de rayos. Estas marcas se pueden usar para invalidar [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) para instancias individuales. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Especifica el nivel de compatibilidad con el seguimiento de rayos en el dispositivo gráfico. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Especifica el tipo de acceso que se proporciona a una aplicación a los recursos especificados en la transición a un paso de representación. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Especifica el tipo de acceso que se da a una aplicación a los recursos especificados en la transición fuera de un paso de representación. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Especifica la naturaleza del paso de representación; por ejemplo, tanto si se trata de un paso de representación de suspensión como de reanudación. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Se usa con la función EnqueueMakeResident para elegir cómo se proceden las operaciones de residencia cuando se supera el presupuesto de memoria. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Especifica cubos de prioridad de residencia amplios útiles para establecer rápidamente un esquema de prioridad de aplicación. |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Especifica una operación de resolución. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Marcas para establecer barreras de recursos divididos.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Especifica un tipo de descripción de barrera de recursos (transición en el uso de recursos). |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Identifica el nivel de enlace de recursos que se usa.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Identifica el tipo de recurso que se usa. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Especifica las opciones para trabajar con recursos.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Especifica qué nivel de montón de recursos admiten el hardware y el controlador.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Especifica el estado de un recurso con respecto a cómo se usa el recurso.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Especifica la inestabilidad de los datos a los que hacen referencia los descriptores en una descripción de firma raíz 1.1, que puede habilitar algunas optimizaciones de controladores. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Especifica el tipo de ranura de firma raíz.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Especifica las opciones para el diseño de la firma raíz.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Identifica el tipo de recurso que se debe ver como destino de representación. |
| [**D3D12_SAMPLER_FEEDBACK_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_sampler_feedback_tier). Define constantes que especifican la compatibilidad con comentarios del muestreador. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Describe el nivel de compatibilidad con el almacenamiento en caché del sombreador en el controlador de gráficos actual. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Especifica cómo se enruta la memoria mediante una vista de recursos de sombreador (SRV).  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Describe las opciones de compatibilidad de precisión mínima para sombreadores en el controlador de gráficos actual.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Especifica los sombreadores que pueden tener acceso al contenido de una ranura de firma raíz determinada. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Define constantes que especifican un nivel de compatibilidad de uso compartido entre API. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Identifica el tipo de recurso que se verá como un recurso de sombreador. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Especifica el color del borde para un muestreador estático.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Identifica las operaciones de galería de símbolos que se pueden realizar durante las pruebas de galería de símbolos de profundidad. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Identifica una técnica para resolver coordenadas de textura que están fuera de los límites de una textura.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Especifica qué tipo de copia de textura se va a realizar. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Especifica las opciones de diseño de textura.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Especifica cómo copiar un icono.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Especifica cómo realizar una operación de asignación de mosaicos.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Especifica un intervalo de asignaciones de mosaicos.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Identifica el nivel en el que se admiten los recursos en mosaico.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Identifica las opciones de vista de acceso no ordenado. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Especifica las opciones para la creación de instancias de vistas. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Indica el nivel en el que se admite la creación de instancias de vista. |
| [**D3D12_WAVE_MMA_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_wave_mma_tier). Define constantes que especifican un nivel de compatibilidad para las operaciones WaveMMA (wave_matrix). |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Especifica el modo utilizado por una **operación WriteBufferImmediate.** |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
