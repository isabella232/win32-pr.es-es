---
title: Enumeraciones básicas
description: Las enumeraciones siguientes se declaran en d3d12. h.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 7f34266e4afdec14e97caa81f393733f1c1ec684
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "105705073"
---
# <a name="core-enumerations"></a>Enumeraciones básicas

Las enumeraciones siguientes se declaran en d3d12. h.

## <a name="in-this-section"></a>En esta sección

| Tema y descripción |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Especifica la versión del diseño de la firma raíz. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Especifica un modelo de sombreador. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Define constantes que especifican las operaciones de la GPU de proceso o de representación. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Define constantes que especifican un nivel de optimización dinámica para aplicar al trabajo de GPU que se envía posteriormente. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Especifica factores de mezcla, que son los valores modulares del sombreador de píxeles y el destino de representación. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Especifica operaciones de combinación RGB o alfa. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Identifica cómo ver un recurso de búfer. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Identifica las opciones de vista de acceso desordenado para un recurso de búfer. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Especifica lo que se va a borrar de la vista de galería de símbolos de profundidad. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Identifica qué componentes de cada píxel de un destino de representación se pueden escribir durante la mezcla. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Se usa para determinar qué tipos de listas de comandos pueden admitir diversas operaciones. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Especifica el tipo de una lista de comandos. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Especifica las marcas que se van a usar al crear una cola de comandos. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Define los niveles de prioridad para una cola de comandos. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Especifica las opciones de comparación. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Identifica si la rasterización conservadora está activada o desactivada. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Identifica el nivel de la rasterización conservadora. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Especifica las propiedades de la página de la CPU del montón. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Especifica el nivel de uso compartido entre los nodos de un adaptador, como el nivel 1 emulado, el nivel 1 o el nivel 2.  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Especifica que los triángulos orientados a una dirección determinada no se dibujan. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Especifica el tipo de datos de la memoria a la que apunta el parámetro *pdata* de [**ID3D12DebugDevice1:: SetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) y [**ID3D12DebugDevice1:: GetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter). |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Identifica la parte de un búfer de estarcido de profundidad para escribir datos de profundidad. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Especifica las opciones para un montón. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Especifica un tipo de montón de descriptores.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Especifica la volatilidad de los descriptores y los datos a los que hacen referencia en una firma raíz 1,1 Descripción, que puede habilitar algunas optimizaciones del controlador. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Especifica un intervalo de modo que, por ejemplo, si parte de una tabla de descriptores tiene 100 vistas de recursos del sombreador (SRVs) que se pueden declarar en una entrada en lugar de 100.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Define constantes que especifican las operaciones de la GPU de proceso o de representación. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Define constantes (utilizadas por la [interfaz ID3D12DeviceRemovedExtendedDataSettings](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)) que especifican cómo se habilitan las características de datos extendidos quitados del dispositivo individual (Dred). |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Define las constantes utilizadas en la [estructura D3D12_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) para especificar las marcas de control para el tiempo de ejecución de Direct3D. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Define constantes que especifican una versión del dispositivo que ha quitado los datos extendidos (DRED), tal y como se usa en la [estructura de D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Especifica cómo obtener acceso a un recurso usado en una vista de galería de símbolos de profundidad. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Especifica las opciones de la vista de galería de símbolos de profundidad. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Opciones de características de Direct3D 12 que son compatibles con el controlador de gráficos actual.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Especifica las opciones de barrera.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Especifica el modo de relleno que se va a utilizar al representar triángulos. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Especifica las opciones de filtrado durante el muestreo de textura. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Especifica el tipo de reducción del filtro.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Especifica el tipo de filtros de muestra de ampliación o minificación.  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Especifica los recursos que se admiten para un formato proporcionado. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Especifica qué opciones de recursos no ordenados se admiten en un formato proporcionado. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Define las marcas que especifican los Estados relacionados con una lista de comandos de gráficos. Los valores pueden ser bit a bit o juntos. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Especifica las opciones del montón, como si el montón puede contener texturas y si los recursos se comparten entre los adaptadores.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Define constantes que especifican la compatibilidad de serialización del montón. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Especifica el tipo de montón. Cuando residen, los montones residen en un grupo de memoria física determinado con determinadas propiedades de la memoria caché de la CPU.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). Cuando se usa la topología de franja triangular primitiva, las posiciones de los vértices se interpretan como vértices de una franja triangular continua. Hay un valor de índice especial que representa el deseo de tener una discontinuidad en la franja, el valor del índice de corte. Esta enumeración enumera los valores de corte admitidos.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Especifica el tipo del parámetro indirecto.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Identifica el tipo de datos contenidos en una ranura de entrada. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Define constantes que especifican el estado de duración de un objeto del que se realiza un seguimiento de la duración. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Especifica las operaciones lógicas que se van a configurar para un destino de representación. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Define constantes que especifican lo que se debe hacer con los resultados de la instrumentación de carga de trabajo anterior. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Especifica el bloque de memoria del montón. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Define constantes que especifican las marcas de un parámetro en un comando meta. Los valores pueden ser bit a bit o juntos. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Define constantes que especifican la fase de un parámetro en un comando meta. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Define constantes que especifican el tipo de datos de un parámetro en un comando meta. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Especifica varias marcas de espera para varias barreras. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Especifica las opciones para determinar los niveles de calidad.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Marcas para controlar el estado de la canalización.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Especifica el tipo de un subobjeto en una descripción de flujo de estado de canalización. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Especifica la operación predication que se va a aplicar.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Especifica cómo la canalización interpreta los primitivos de entrada de sombreador de tipo Geometry o de casco. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Especifica el nivel de compatibilidad para las posiciones de ejemplo programables que ofrece el adaptador. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Define constantes que especifican marcas de sesión de recursos protegidos. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Define constantes que especifican la compatibilidad con sesiones de recursos protegidos. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Define constantes que especifican el estado de la sesión protegida. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Especifica el tipo de montón de consulta que se va a crear. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Especifica el tipo de consulta. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Marcas que se pasan a la función [**TraceRay**](./traceray-function.md) para invalidar la transparencia, la selección y el comportamiento de tiempo de espera. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Especifica las marcas para la compilación de una estructura de aceleración de raytracing. Use un valor de esta enumeración con la estructura [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) que proporciona la entrada a la operación de compilación de la estructura de aceleración. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Especifica el tipo de operación de copia realizada al llamar a [**CopyRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Especifica el tipo de información posterior a la compilación de la estructura de aceleración que se puede recuperar con llamadas a [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) y [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Especifica el tipo de una estructura de aceleración de raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Especifica marcas para geometría de raytracing en una estructura de [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) . |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Especifica el tipo de geometría que se usa para raytracing. Use un valor de esta enumeración para especificar el tipo de geometría en un [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Marcas para una instancia de la estructura de aceleración raytracing. Estas marcas se pueden usar para invalidar [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) para instancias individuales. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Especifica el nivel de compatibilidad del seguimiento de Ray en el dispositivo gráfico. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Especifica el tipo de acceso que se asigna a una aplicación a los recursos especificados en la transición a una fase de representación. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Especifica el tipo de acceso que se asigna a una aplicación a los recursos especificados en la transición de una fase de representación. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Especifica la naturaleza de la fase de representación; por ejemplo, si se trata de un paso de representación de suspensión o de reanudación. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Se usa con la función EnqueueMakeResident para elegir cómo continúan las operaciones de residencia cuando se supera el presupuesto de memoria. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Especifica los depósitos de prioridad de residencia amplios útiles para establecer rápidamente un esquema de prioridad de la aplicación. |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Especifica una operación de resolución. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Marcas para establecer barreras de recursos divididos.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Especifica un tipo de barrera de recursos (transición en el uso de recursos). |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Identifica el nivel de enlace de recursos que se está usando.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Identifica el tipo de recurso que se está usando. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Especifica las opciones para trabajar con recursos.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Especifica qué nivel de montón de recursos admite el hardware y el controlador.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Especifica el estado de un recurso con respecto a cómo se utiliza el recurso.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Especifica la volatilidad de los datos a los que hacen referencia los descriptores en una firma raíz 1,1 Descripción, que puede habilitar algunas optimizaciones del controlador. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Especifica el tipo de ranura de la firma raíz.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Especifica las opciones para el diseño de la firma raíz.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Identifica el tipo de recurso que se va a ver como destino de representación. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Describe el nivel de compatibilidad para el almacenamiento en caché del sombreador en el controlador de gráficos actual. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Especifica cómo se enruta la memoria mediante una vista de recursos del sombreador (SRV).  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Describe las opciones de compatibilidad de precisión mínima para los sombreadores en el controlador de gráficos actual.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Especifica los sombreadores que pueden tener acceso al contenido de una ranura de firma raíz determinada. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Define constantes que especifican un nivel de compatibilidad de uso compartido entre API. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Identifica el tipo de recurso que se va a ver como un recurso de sombreador. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Especifica el color del borde de una muestra estática.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Identifica las operaciones de estarcido que se pueden realizar durante las pruebas de la galería de símbolos de profundidad. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Identifica una técnica para resolver las coordenadas de textura que están fuera de los límites de una textura.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Especifica qué tipo de copia de textura debe tener lugar. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Especifica las opciones de diseño de textura.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Especifica cómo copiar un icono.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Especifica cómo realizar una operación de asignación de mosaicos.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Especifica un intervalo de asignaciones de mosaicos.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Identifica el nivel de nivel en el que se admiten los recursos en mosaico.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Identifica las opciones de vista de acceso no ordenada. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Especifica las opciones para la creación de instancias de la vista. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Indica el nivel de nivel en el que se admite la creación de instancias de la vista. |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Especifica el modo utilizado por una operación **WriteBufferImmediate** . |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)