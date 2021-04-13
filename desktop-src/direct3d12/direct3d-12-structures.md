---
title: Estructuras principales (gráficos de Direct3D 12)
description: Las siguientes estructuras se declaran en d3d12. h.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 456ca501426142182d9823427c7d13599e4a92db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105648151"
---
# <a name="core-structures"></a>Estructuras principales

Las siguientes estructuras se declaran en d3d12. h.

## <a name="in-this-section"></a>En esta sección

| Tema y descripción |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Representa los datos de ruta de navegación automática del dispositivo quitado (DRED) como un nodo en una lista vinculada. |
| [**D3D12_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc). Describe el estado de Blend. |
| [**D3D12_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box). Describe un cuadro 3D. |
| [**D3D12_BUFFER_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Describe los elementos de un recurso de búfer para usar en una vista de destino de representación. |
| [**D3D12_BUFFER_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv). Describe los elementos de un recurso de búfer para usar en una vista de recursos de sombreador. |
| [**D3D12_BUFFER_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav). Describe los elementos de un búfer que se van a usar en una vista de acceso desordenado. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Almacena un estado de canalización. |
| [**D3D12_CLEAR_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value). Describe un valor que se usa para optimizar las operaciones de borrado para un recurso determinado. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Describe una cola de comandos. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Describe los argumentos (parámetros) de una firma de comando. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Describe un objeto de estado de canalización de proceso. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Describe un búfer de constantes que se va a ver. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Describe un identificador de descriptor de CPU. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Describe el estado de la galería de símbolos de profundidad. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Describe el estado de la galería de símbolos de profundidad. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Especifica una profundidad y un valor de estarcido. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Describe los Subrecursos de una textura a la que se puede tener acceso desde una vista de galería de símbolos de profundidad. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Describe las operaciones de estarcido que se pueden realizar en función de los resultados de la prueba de estarcido. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Describe el montón de descriptores. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Describe un intervalo de descriptores. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Describe un intervalo de descriptores, con marcas para determinar su volatilidad. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Representa datos de la versión 1,0 de los datos extendidos quitados del dispositivo (DRED). |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Representa los datos de eliminación de dispositivos de la versión 1,1 de los datos extendidos del dispositivo (DRED), para que los depuradores y las extensiones del depurador puedan acceder a los datos de DRED. |
| [**D3D12_DISCARD_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region). Describe los detalles de la operación de descartar recursos. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Describe los parámetros de envío, para su uso por parte del sombreador de cálculo. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments). Describe los parámetros para dibujar instancias de. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Describe los parámetros para dibujar instancias indizadas. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Describe, como un nodo de una lista vinculada, datos sobre una asignación a la que realiza un seguimiento el dispositivo quitó datos extendidos (DRED). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Contiene un puntero al encabezado de una lista vinculada de objetos [D3D12_AUTO_BREADCRUMB_NODE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) . La lista representa el estado de la ruta de navegación automática antes de la eliminación del dispositivo. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Describe los datos de asignación relacionados con un error de página de GPU en una dirección virtual determinada (VA). |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Proporcione detalles sobre la arquitectura del adaptador y ayude a las aplicaciones a optimizar mejor para ciertas propiedades de adaptador. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Proporcione detalles sobre la arquitectura del adaptador y ayude a las aplicaciones a optimizar mejor para ciertas propiedades de adaptador. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Detalla la compatibilidad del adaptador con la priorización de diferentes tipos de cola de comandos. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Indica el nivel de compatibilidad para el uso compartido de recursos entre distintos adaptadores. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Describe las opciones de características de Direct3D 12 en el controlador de gráficos actual. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Describe el nivel de compatibilidad para las operaciones de onda de HLSL 6,0. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Detalla la compatibilidad del adaptador con ciertas características opcionales de Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Se usa para indicar el nivel de compatibilidad que proporciona el adaptador para las características opcionales de Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Indica el nivel de compatibilidad para las texturas de MSAA basadas en 64 KB, el uso compartido entre API y las operaciones nativas de sombreador de 16 bits. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Indica el nivel de compatibilidad que proporciona el adaptador para las fases de representación, el seguimiento de rayos y los recursos en mosaico del nivel 3 de la vista de recursos del sombreador. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Indica el nivel de compatibilidad que proporciona el adaptador para el sombreado de velocidad variable (VRS) e indica si se admite o no el procesamiento en segundo plano. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Se usa para determinine si el adaptador admite la creación de montones a partir de la memoria del sistema existente. Estos montones no están pensados para uso general, pero son excepcionalmente útiles para fines de diagnóstico, ya que se garantiza que se conservan incluso después de que se produzcan errores en el adaptador o que experimenten un evento de eliminación de dispositivos. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Describe la información sobre los [niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) admitidos por el controlador de gráficos actual. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Describe el formato de datos de DXGI. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Describe qué recursos son compatibles con el controlador de gráficos actual para un formato determinado. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Detalla las limitaciones del espacio de direcciones virtuales de GPU del adaptador, incluidos los bits de dirección máximos por recurso y por proceso. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Describe los niveles de calidad de la imagen para un formato determinado y el recuento de muestras. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Indica el nivel de compatibilidad para las sesiones de recursos protegidos. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Indica el nivel de compatibilidad que proporciona el adaptador para los metacomandos. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Pase esta estructura a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) para comprobar la compatibilidad con la versión de la firma raíz. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Indica el nivel de compatibilidad para la serialización del montón. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Describe el nivel de almacenamiento en caché del sombreador que se admite en el controlador de gráficos actual. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Contiene el modelo de sombreador compatible. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Describe un identificador de descriptor de GPU. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Describe un objeto de estado de canalización de gráficos. |
| [**D3D12_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc). Describe un montón. |
| [**D3D12_HEAP_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties). Describe las propiedades del montón. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Describe el búfer de índice que se va a ver. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Describe un argumento indirecto (un parámetro indirecto), para su uso con una firma de comando. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_element_desc). Describe un elemento único para la fase del ensamblador de entrada de la canalización de gráficos. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Describe los datos del búfer de entrada para la fase del ensamblador de entrada. |
| [**D3D12_MEMCPY_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Describe el destino de una operación de copia de memoria. |
| [**D3D12_META_COMMAND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Describe un comando meta. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Describe un parámetro para un comando meta. |
| [**D3D12_PACKED_MIP_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Describe la estructura de mosaico de un recurso en mosaico con mapas MIP. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Describe una secuencia de estado de la canalización. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Describe la superficie de un subrecurso colocado, incluidos el desplazamiento y el D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Describe las marcas de una sesión de recursos protegidos, por adaptador. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Consulte la información sobre la actividad de la canalización de gráficos entre las llamadas a [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery). |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Describe los datos de la consulta para la salida de flujo. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Describe el propósito de un montón de consulta. Un montón de consulta contiene una matriz de consultas individuales. |
| [**D3D12_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range). Describe un intervalo de memoria. |
| [**D3D12_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64). Describe un intervalo de memoria en un espacio de direcciones de 64 bits. |
| [**D3D12_RASTERIZER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Describe el estado de rasterizador. |
| [**D3D12_RAYTRACING_AABB**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Representa un cuadro de límite alineado con el eje (AABB) que se usa como geometría de raytracing. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Describe el requisito de espacio para la estructura de aceleración después de la compactación. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Describe el espacio actualmente utilizado por una estructura de aceleración. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Descripción de la información posterior a la compilación que se va a generar a partir de una estructura de aceleración. Use esta estructura en las llamadas a [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) y [**BuildRaytracingAccelerationStructure**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Describe el tamaño y el diseño de la estructura de aceleración serializada y el encabezado |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Describe el requisito de espacio para descodificar una estructura de aceleración en un formulario que se puede visualizar mediante herramientas. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Representa información de precompilación sobre una estructura de aceleración de raytracing. Obtiene una instancia de este estructura llamando a [**GetRaytracingAccelerationStructurePrebuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Una estructura de vista de recursos del sombreador (SRV) para almacenar una estructura de aceleración de raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Describe un conjunto de cuadros de límite alineados con el eje que se utilizan en la estructura de [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) para proporcionar datos de entrada a una operación de compilación de la estructura de aceleración de RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Describe un conjunto de geometría que se usa en la estructura [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) para proporcionar datos de entrada a una operación de compilación de la estructura de aceleración de RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Describe un conjunto de triángulos que se usa como geometría raytracing. La geometría señalada por este struct siempre está en forma de lista de triángulos, indizada o no indizada. No se admiten bandas de triángulos. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Describe una instancia de una estructura de aceleración de raytracing usada en la memoria de GPU durante el proceso de compilación de la estructura de aceleración. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Un subobjeto de estado que representa una configuración de canalización raytracing. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Un subobjeto de estado que representa una configuración de sombreador. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT se declara como un rectángulo. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Describe el acceso a los recursos solicitados por una aplicación en la transición a una fase de representación. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Describe el valor sin cifrar en el que se deben borrar los recursos al principio de una fase de representación. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Describe un enlace (fijo para la duración de la fase de representación) a una vista de galería de símbolos de profundidad (DSV), así como sus características de acceso inicial y final. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Describe el acceso a los recursos solicitados por una aplicación en la transición de una fase de representación. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Describe un recurso que se va a resolver en la finalización de una fase de representación. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Describe los Subrecursos implicados en la resolución de una fase de representación. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Describe los enlaces (fijos para la duración de la fase de representación) a una o varias vistas de destino de representación (RTVs), así como sus características de acceso inicial y final. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Describe el estado de Blend para un destino de representación. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Describe los Subrecursos de un recurso al que se puede tener acceso mediante una vista de destino de representación. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Describe la transición entre los usos de dos recursos diferentes que tienen asignaciones en el mismo montón. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Describe los parámetros necesarios para asignar recursos. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Describe los parámetros necesarios para asignar recursos, incluido el desplazamiento. |
| [**D3D12_RESOURCE_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier). Describe una barrera de recursos (transición en el uso de recursos). |
| [**D3D12_RESOURCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc). Describe un recurso, como una textura. Esta estructura se usa con frecuencia. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Describe la transición de Subrecursos entre distintos usos. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Representa un recurso en el que todos los accesos de UAV deben completarse antes de que pueda comenzar cualquier acceso futuro a UAV. |
| [**D3D12_ROOT_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants). Describe las constantes alineadas en la firma raíz que aparecen en los sombreadores como un búfer de constantes. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor). Describe los descriptores alineados en la versión 1,0 de la firma raíz que aparecen en los sombreadores. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Describe los descriptores alineados en la versión 1,1 de la firma raíz que aparecen en los sombreadores. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Describe el diseño de la firma raíz 1,0 de una tabla de descriptores como una colección de intervalos de descriptor que aparecen uno tras otro en un montón de descriptores. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Describe el diseño de la firma raíz 1,1 de una tabla de descriptores como una colección de intervalos de descriptor que aparecen uno tras otro en un montón de descriptores. |
| [**D3D12_ROOT_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter). Describe la ranura de la versión 1,0 de la firma raíz. |
| [**D3D12_ROOT_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1). Describe la ranura de la versión 1,1 de la firma raíz. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Describe el diseño de la versión 1,0 de la firma raíz. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Describe el diseño de la versión 1,1 de la firma raíz. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array). Incluye una matriz de formatos de destino de representación. |
| [**D3D12_SAMPLE_POSITION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sample_position). Describe una posición de ejemplo de subpíxeles para su uso con posiciones de ejemplo programables. |
| [**D3D12_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc). Describe un estado de muestra. |
| [**D3D12_SHADER_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Describe los datos del sombreador. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Describe una vista de recursos de sombreador. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Describe un elemento de vértice en un búfer de vértice en una ranura de salida. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Describe una muestra estática. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Describe un búfer de salida de flujo. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Describe un búfer de salida de streaming. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data). Describe los datos de los Subrecursos. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Describe el formato, el ancho, el alto, la profundidad y el tono de fila del subrecurso en el recurso primario. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info). Describe los datos de los Subrecursos. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Describe un intervalo de memoria de subrecurso. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Describe un volumen de Subrecursos en mosaico. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Describe los Subrecursos de una matriz de texturas 1D que se van a usar en una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Describe los Subrecursos de una matriz de texturas 1D que se van a usar en una vista de destino de representación. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Describe los Subrecursos de una matriz de texturas 1D que se van a usar en una vista de recursos de sombreador. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Describe una matriz de recursos de textura 1D de acceso desordenado. |
| [**D3D12_TEX1D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Describe el subrecurso de una textura 1D que es accesible para una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX1D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Describe el subrecurso de una textura 1D para usarlo en una vista de destino de representación. |
| [**D3D12_TEX1D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Especifica el subrecurso de una textura 1D que se va a usar en una vista de recursos de sombreador. |
| [**D3D12_TEX1D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Describe un recurso de textura 1D de acceso desordenado. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Describe los Subrecursos de una matriz de texturas 2D a las que se puede tener acceso desde una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Describe los Subrecursos de una matriz de texturas 2D que se van a usar en una vista de destino de representación. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Describe los Subrecursos de una matriz de texturas 2D que se van a usar en una vista de recursos de sombreador. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Describe una matriz de recursos de textura 2D de acceso desordenado. |
| [**D3D12_TEX2D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Describe el subrecurso de una textura 2D que es accesible para una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Describe el subrecurso de una textura 2D para usarlo en una vista de destino de representación. |
| [**D3D12_TEX2D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Describe el subrecurso de una textura 2D para usarlo en una vista de recursos de sombreador. |
| [**D3D12_TEX2D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Describe un recurso de textura 2D de acceso desordenado. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Describe los Subrecursos de una matriz de texturas 2D de varias muestras para una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Describe los Subrecursos de una matriz de texturas 2D de varias muestras para usar en una vista de destino de representación. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Describe los Subrecursos de una matriz de texturas 2D de varios muestreados que se van a usar en una vista de recursos de sombreador. |
| [**D3D12_TEX2DMS_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Describe el subrecurso de una textura 2D de muestreo múltiple a la que se puede acceder desde una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2DMS_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Describe el subrecurso de una textura 2D de muestreo múltiple para usarlo en una vista de destino de representación. |
| [**D3D12_TEX2DMS_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Describe los Subrecursos de una textura 2D multimuestreada para usarlos en una vista de recursos de sombreador. |
| [**D3D12_TEX3D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Describe los Subrecursos de una textura 3D para utilizarlos en una vista de destino de representación. |
| [**D3D12_TEX3D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Describe los Subrecursos de una textura 3D para utilizarlos en una vista de recursos de sombreador. |
| [**D3D12_TEX3D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Describe un recurso de textura 3D de acceso desordenado. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Describe los Subrecursos de una matriz de texturas de cubo que se van a usar en una vista de recursos de sombreador. |
| [**D3D12_TEXCUBE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv). Describe el subrecurso de una textura del cubo que se va a usar en una vista de recursos de sombreador. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Describe una parte de una textura con el fin de copiar las texturas. |
| [**D3D12_TILE_REGION_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size). Describe el tamaño de una región en mosaico. |
| [**D3D12_TILE_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape). Describe la forma de un mosaico mediante la especificación de sus dimensiones. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Describe las coordenadas de un recurso en mosaico. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Describe los Subrecursos de un recurso al que se puede tener acceso mediante una vista de acceso desordenado. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Describe una vista de búfer de vértices. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Representa los datos de datos extendidos quitados del dispositivo con versión (DRED), para que los depuradores y las extensiones del depurador puedan acceder a los datos de DRED. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Contiene cualquier versión de una descripción de la firma raíz y está diseñada para usarse con las funciones de serialización y deserialización. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instance_location). Especifica la ventanilla/estarcido y el destino de presentación asociados a una instancia de vista. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Especifica los parámetros usados durante la configuración de la creación de instancias de la vista. |
| [**D3D12_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport). Describe las dimensiones de una ventanilla. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Especifica el valor inmediato y la dirección de destino escrita mediante [**ID3D12CommandList2:: WriteBufferImmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2). |

## <a name="related-topics"></a>Temas relacionados

* [Referencia básica](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)