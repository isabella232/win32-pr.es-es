---
title: Estructuras principales (gráficos de Direct3D 12)
description: Las estructuras siguientes se declaran en d3d12.h.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5dd546055c22711ecd9a3796e520ad034e9e46c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249123"
---
# <a name="core-structures"></a>Estructuras principales

Las estructuras siguientes se declaran en d3d12.h.

## <a name="in-this-section"></a>En esta sección

| Tema y descripción |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Representa los datos de ruta de navegación automática de datos extendidos (DRED) quitados por el dispositivo como un nodo de una lista vinculada. |
| [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc). Describe el estado de mezcla. |
| [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box). Describe un cuadro 3D. |
| [**D3D12_BUFFER_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Describe los elementos de un recurso de búfer que se usarán en una vista de destino de representación. |
| [**D3D12_BUFFER_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_srv). Describe los elementos de un recurso de búfer que se usarán en una vista de sombreador y recurso. |
| [**D3D12_BUFFER_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav). Describe los elementos de un búfer que se usarán en una vista de acceso desordenado. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Almacena un estado de canalización. |
| [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value). Describe un valor que se usa para optimizar las operaciones claras para un recurso determinado. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Describe una cola de comandos. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Describe los argumentos (parámetros) de una firma de comando. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Describe un objeto de estado de canalización de proceso. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Describe un búfer constante que se debe ver. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Describe un identificador de descriptor de CPU. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Describe el estado de la galería de símbolos de profundidad. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Describe el estado de la galería de símbolos de profundidad. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Especifica un valor de profundidad y galería de símbolos. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Describe los subrecursos de una textura a los que se puede acceder desde una vista de galería de símbolos de profundidad. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Describe las operaciones de galería de símbolos que se pueden realizar en función de los resultados de la prueba de galería de símbolos. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Describe el montón del descriptor. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range). Describe un intervalo de descriptores. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Describe un intervalo de descriptores, con marcas para determinar su inestabilidad. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Representa los datos de la versión 1.0 de Datos extendidos quitados del dispositivo (DRED). |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Representa los datos de eliminación de dispositivos de la versión 1.1 de Datos extendidos quitados del dispositivo (DRED), para que los depuradores y las extensiones del depurador puedan acceder a los datos de DRED. |
| [**D3D12_DISCARD_REGION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region). Describe los detalles de la operación discard-resource. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Describe los parámetros de distribución, para que los use el sombreador de proceso. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_arguments). Describe los parámetros para dibujar instancias de . |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Describe los parámetros para dibujar instancias indizadas. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Describe, como nodo de una lista vinculada, los datos sobre una asignación de la que se realiza un seguimiento mediante datos extendidos eliminados por dispositivo (DRED). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Contiene un puntero al final de una lista vinculada de [D3D12_AUTO_BREADCRUMB_NODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) objetos. La lista representa el estado de la ruta de navegación automática antes de la eliminación del dispositivo. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Describe los datos de asignación relacionados con un error de página de GPU en una dirección virtual (VA) determinada. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Proporcione detalles sobre la arquitectura del adaptador, lo que ayuda a las aplicaciones a optimizar mejor determinadas propiedades del adaptador. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Proporcione detalles sobre la arquitectura del adaptador, lo que ayuda a las aplicaciones a optimizar mejor determinadas propiedades del adaptador. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Detalla la compatibilidad del adaptador con la priorización de los distintos tipos de cola de comandos. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Indica el nivel de compatibilidad para el uso compartido de recursos entre distintos adaptadores. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Describe las opciones de características de Direct3D 12 en el controlador de gráficos actual. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Describe el nivel de compatibilidad con las operaciones de onda HLSL 6.0. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Detalla la compatibilidad del adaptador con determinadas características opcionales de Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Se usa para indicar el nivel de compatibilidad que proporciona el adaptador para las características opcionales de Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Indica el nivel de compatibilidad para texturas MSAA alineadas con 64 KB, uso compartido entre API y operaciones nativas de sombreador de 16 bits. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Indica el nivel de compatibilidad que proporciona el adaptador para los pases de representación, el seguimiento de rayos y los recursos en mosaico de nivel 3 de vista de recursos de sombreador. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Indica el nivel de compatibilidad que proporciona el adaptador para el sombreado de velocidad variable (VRS) e indica si se admite o no el procesamiento en segundo plano. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS7**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7). Indica el nivel de compatibilidad que proporciona el adaptador para los sombreadores de malla y amplificación, y para los comentarios del muestreador. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS8**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options8). Indica si se admiten texturas comprimidas por bloques no alineadas o no. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS9**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9). Indica si existe o no compatibilidad con sombreadores de malla, valores de *SV_RenderTargetArrayIndex* de 8 o más, atomics enteros de recursos con tipo de 64 bits, operaciones de ejemplo de textura derivadas y dependientes de derivados, y el nivel de compatibilidad para las operaciones WaveMMA (wave_matrix). |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS10**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options10). Indica si se puede usar o no el combinador SUM y si SV_ShadingRate se puede establecer desde un sombreador de malla.  |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS11**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options11). Indica si se admiten o no enteros atómicos de 64 bits en recursos en montones de descriptores. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Se usa para determinar si el adaptador admite la creación de montones a partir de la memoria del sistema existente. Estos montones no están diseñados para uso general, pero son excepcionalmente útiles para fines de diagnóstico, ya que se garantiza que persistirán incluso después de que el adaptador produce errores o experimenta un evento de eliminación de dispositivos. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Describe información sobre los niveles [de características admitidos](/windows/win32/direct3d11/overviews-direct3d-11-devices-downlevel-intro) por el controlador de gráficos actual. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Describe el formato de datos DXGI. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Describe qué recursos son compatibles con el controlador de gráficos actual para un formato determinado. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Detalla las limitaciones de espacio de direcciones virtuales de GPU del adaptador, incluidos los bits de dirección máximos por recurso y por proceso. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Describe los niveles de calidad de la imagen para un formato y recuento de muestras determinados. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Indica el nivel de compatibilidad con las sesiones de recursos protegidos. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPE_COUNT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_type_count). Indica un recuento de tipos de sesión de recursos protegidos. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_types). Indica una lista de tipos de sesión de recursos protegidos. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Indica el nivel de compatibilidad que proporciona el adaptador para los metacomandos. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Pase esta estructura a [**CheckFeatureSupport para comprobar**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) la compatibilidad con la versión de firma raíz. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Indica el nivel de compatibilidad para la serialización del montón. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Describe el nivel de almacenamiento en caché del sombreador admitido en el controlador de gráficos actual. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Contiene el modelo de sombreador admitido. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Describe un identificador de descriptor de GPU. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Describe un objeto de estado de canalización de gráficos. |
| [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc). Describe un montón. |
| [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties). Describe las propiedades del montón. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Describe el búfer de índice que se debe ver. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Describe un argumento indirecto (un parámetro indirecto) para su uso con una firma de comando. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc). Describe un único elemento para la fase de ensamblador de entrada de la canalización de gráficos. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Describe los datos del búfer de entrada para la fase de ensamblador de entrada. |
| [**D3D12_MEMCPY_DEST**](/windows/win32/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Describe el destino de una operación de copia de memoria. |
| [**D3D12_META_COMMAND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Describe un meta comando. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Describe un parámetro para un meta comando. |
| [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Describe la estructura de mosaico de un recurso en mosaico con mapas mip. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Describe una secuencia de estado de canalización. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Describe la superficie de un subrecurso colocado, incluidos el desplazamiento y el D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Describe las marcas de una sesión de recursos protegidos, por adaptador. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Consultar información sobre la actividad de canalización de gráficos entre llamadas a [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery). |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Describe los datos de consulta para la salida del flujo. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Describe el propósito de un montón de consultas. Un montón de consultas contiene una matriz de consultas individuales. |
| [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range). Describe un intervalo de memoria. |
| [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64). Describe un intervalo de memoria en un espacio de direcciones de 64 bits. |
| [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Describe el estado del rasterizador. |
| [**D3D12_RAYTRACING_AABB**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Representa un rectángulo de selección alineado con el eje (AABB) que se usa como geometría de trazado. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Describe el requisito de espacio para la estructura de aceleración después de la compactación. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Describe el espacio utilizado actualmente por una estructura de aceleración. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Descripción de la información posterior a la compilación que se generará a partir de una estructura de aceleración. Use esta estructura en las llamadas a [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) y [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Describe el tamaño y el diseño de la estructura de aceleración serializada y el encabezado |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Describe el requisito de espacio para la decodización de una estructura de aceleración en un formulario que las herramientas pueden visualizar. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Representa información previa a la construcción sobre una estructura de aceleración de rayos. Obtenga una instancia de esta estructura mediante una llamada [**a GetRaytracingAccelerationStructurePrebuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Estructura de vista de recursos de sombreador (SRV) para almacenar una estructura de aceleración de rayos. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Describe un conjunto de rectángulos delimitadores alineados con ejes que se usan en la estructura [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) para proporcionar datos de entrada a una operación de compilación de estructura de aceleración de rayos. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Describe un conjunto de geometría que se usa en la estructura [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) para proporcionar datos de entrada a una operación de compilación de estructura de aceleración de rayos. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Describe un conjunto de triángulos que se usan como geometría de trazado. La geometría a la que apunta este struct siempre está en forma de lista de triángulos, indizada o no indizada. No se admiten franjas de triángulos. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Describe una instancia de una estructura de aceleración de rayos que se usa en la memoria de GPU durante el proceso de compilación de la estructura de aceleración. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Subobjeto de estado que representa una configuración de canalización de raytracing. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config1). Subobjeto de estado que representa una configuración de canalización de raytracing, con marcas. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Subobjeto de estado que representa una configuración de sombreador. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT se declara como UN RECT. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Describe el acceso a los recursos solicitados por una aplicación en la transición a un paso de representación. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Describe el valor claro al que se deben borrar los recursos al principio de un paso de representación. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Describe un enlace (fijo durante el paso de representación) a una vista de galería de símbolos de profundidad (DSV), así como sus características de acceso inicial y final. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Describe el acceso a los recursos solicitados por una aplicación en la transición fuera de un paso de representación. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Describe un recurso en el que resolver al finalizar un paso de representación. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Describe los subrecursos implicados en la resolución al finalizar un paso de representación. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Describe los enlaces (fijos durante el paso de representación) a una o varias vistas de destino de representación (RTV), así como sus características de acceso inicial y final. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Describe el estado de mezcla de un destino de representación. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Describe los subrecursos de un recurso al que se puede acceder mediante una vista de destino de representación. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Describe la transición entre los usos de dos recursos diferentes que tienen asignaciones en el mismo montón. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Describe los parámetros necesarios para asignar recursos. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Describe los parámetros necesarios para asignar recursos, incluido el desplazamiento. |
| [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier). Describe una barrera de recursos (transición en el uso de recursos). |
| [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc). Describe un recurso, como una textura. Esta estructura se usa ampliamente. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Describe la transición de los subrecursos entre distintos usos. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Representa un recurso en el que todos los accesos UAV deben completarse antes de que puedan comenzar los futuros accesos UAV. |
| [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants). Describe las constantes insertas en la firma raíz que aparecen en los sombreadores como un búfer constante. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor). Describe los descriptores en línea en la versión 1.0 de la firma raíz que aparecen en los sombreadores. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Describe los descriptores en línea en la versión 1.1 de la firma raíz que aparecen en los sombreadores. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Describe el diseño de la firma raíz 1.0 de una tabla de descriptores como una colección de intervalos de descriptores que aparecen uno tras otro en un montón de descriptores. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Describe el diseño de la firma raíz 1.1 de una tabla de descriptores como una colección de intervalos de descriptores que aparecen uno tras otro en un montón de descriptores. |
| [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter). Describe la ranura de una firma raíz versión 1.0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1). Describe la ranura de una firma raíz versión 1.1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Describe el diseño de una firma raíz versión 1.0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Describe el diseño de una firma raíz versión 1.1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array). Encapsula una matriz de formatos de destino de representación. |
| [**D3D12_SAMPLE_POSITION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sample_position). Describe una posición de muestra de subpíxeles para su uso con posiciones de ejemplo programables. |
| [**D3D12_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sampler_desc). Describe un estado de muestreador. |
| [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Describe los datos del sombreador. |
| [**D3D12_SHADER_CACHE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_cache_session_desc). Describe una sesión de caché de sombreador. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Describe una vista de sombreador y recurso. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Describe un elemento de vértice en un búfer de vértices en una ranura de salida. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Describe un muestreador estático. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Describe un búfer de salida de flujo. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Describe un búfer de salida de streaming. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_data). Describe los datos de subrecursos. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Describe el formato, el ancho, el alto, la profundidad y el tono de fila del subcurso en el recurso primario. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_info). Describe los datos de subrecursos. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Describe un intervalo de memoria de subrecursos. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Describe un volumen de subrecurso en mosaico. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Describe los subrecursos de una matriz de texturas 1D que se usarán en una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Describe los subrecursos de una matriz de texturas 1D que se usarán en una vista de destino de representación. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Describe los subrecursos de una matriz de texturas 1D que se usarán en una vista de recursos de sombreador. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Describe una matriz de recursos de textura 1D de acceso desordenado. |
| [**D3D12_TEX1D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Describe el subrecurso de una textura 1D a la que puede acceder una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX1D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Describe el subrecurso de una textura 1D que se usará en una vista de destino de representación. |
| [**D3D12_TEX1D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Especifica el subrecurso de una textura 1D que se usará en una vista de recursos de sombreador. |
| [**D3D12_TEX1D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Describe un recurso de textura 1D de acceso desordenado. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Describe los subrecursos de una matriz de texturas 2D accesibles para una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Describe los subrecursos de una matriz de texturas 2D que se usarán en una vista de destino de representación. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Describe los subrecursos de una matriz de texturas 2D que se usarán en una vista de recursos de sombreador. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Describe una matriz de recursos de textura 2D de acceso desordenado. |
| [**D3D12_TEX2D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Describe el subrecurso de una textura 2D accesible para una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Describe el subrecurso de una textura 2D que se usará en una vista de destino de representación. |
| [**D3D12_TEX2D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Describe el subrecurso de una textura 2D que se usará en una vista de recursos de sombreador. |
| [**D3D12_TEX2D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Describe un recurso de textura 2D de acceso desordenado. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Describe los subrecursos de una matriz de texturas 2D de muestreo múltiple para una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Describe los subrecursos de una matriz de texturas 2D de muestreo múltiple para usarlas en una vista de destino de representación. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Describe los subrecursos de una matriz de texturas 2D de muestreo múltiple que se usan en una vista de recursos de sombreador. |
| [**D3D12_TEX2DMS_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Describe el subrecurso de una textura 2D muestreada múltiple a la que puede acceder una vista de galería de símbolos de profundidad. |
| [**D3D12_TEX2DMS_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Describe el subrecurso de una textura 2D muestreada múltiple que se usará en una vista de destino de representación. |
| [**D3D12_TEX2DMS_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Describe los subrecursos de una textura 2D muestreada múltiple que se usará en una vista de recursos de sombreador. |
| [**D3D12_TEX3D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Describe los subrecursos de una textura 3D que se usarán en una vista render-target. |
| [**D3D12_TEX3D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Describe los subrecursos de una textura 3D que se usarán en una vista de recursos de sombreador. |
| [**D3D12_TEX3D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Describe un recurso de textura 3D de acceso desordenado. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Describe los subrecursos de una matriz de texturas de cubo que se usarán en una vista de recursos de sombreador. |
| [**D3D12_TEXCUBE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_srv). Describe el subrecurso de una textura de cubo que se usará en una vista de recursos de sombreador. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Describe una parte de una textura para las copias de textura. |
| [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size). Describe el tamaño de una región en mosaico. |
| [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape). Describe la forma de un icono especificando sus dimensiones. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Describe las coordenadas de un recurso en mosaico. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Describe los subrecursos de un recurso al que se puede acceder mediante una vista de acceso desordenado. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Describe una vista de búfer de vértices. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Representa los datos de datos extendidos (DRED) eliminados del dispositivo con versiones, de modo que los depuradores y las extensiones del depurador puedan acceder a los datos dred. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Contiene cualquier versión de una descripción de firma raíz y está diseñado para usarse con funciones de serialización y deserialización. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instance_location). Especifica la ventanilla o galería de símbolos y el destino de representación asociados a una instancia de vista. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Especifica los parámetros usados durante la configuración de creación de instancias de vista. |
| [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport). Describe las dimensiones de una ventanilla. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Especifica el valor inmediato y la dirección de destino escritos [**mediante ID3D12CommandList2::WriteBufferImmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2). |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)