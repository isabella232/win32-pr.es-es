---
description: Esta sección contiene información de referencia para las estructuras de api de vídeo de Microsoft Direct3D 12.
ms.assetid: ''
title: Estructuras de vídeo de Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: dd73ba1cf374dade90963513ddbc92317cd3b05c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574937"
---
# <a name="direct3d-12-video-structures"></a>Estructuras de vídeo de Direct3D 12

Esta sección contiene información de referencia para las estructuras de api de vídeo de Microsoft Direct3D 12.

## <a name="in-this-section"></a>En esta sección

| Tema                                                                                | Descripción                                                                                              |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support)  | Recupera la lista de perfiles admitidos.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats)  | Recupera la lista de formatos admitidos.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_histogram)  | Proporciona datos para las llamadas a ID3D12VideoDevice::CheckFeatureSupport cuando la característica especificada se D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles)  | Recupera la lista de perfiles admitidos.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_support)  | Recupera la información de soporte técnico para lacoding de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_codec)  | Recupera un valor que indica si el códec especificado es compatible con la codificación de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_codec_configuration_support)  | Recupera un valor que indica si se admiten los parámetros de compatibilidad de configuración de códec especificados para 
la configuración de codificación HEVC proporcionada o recupera la configuración admitida para la codificación H.264.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_codec_picture_control_support)  | Recupera la compatibilidad del control de imagen con el códec y el perfil especificados.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_frame_subregion_layout_mode)  | Recupera un valor que indica si se admite el modo de diseño de subregión de marco especificado para el especificado. 
código, perfil y nivel.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_heap_size)  | Recupera un valor que indica si el códec especificado es compatible con la codificación de vídeo, así como L0 y 
Tamaños L1 del objeto de montón.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_input_format)  | Recupera un valor que indica si el códec, el perfil y el formato especificados son compatibles con la codificación de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_INTRA_REFRESH_MODE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_intra_refresh_mode)  | Recupera un valor que indica si el modo de actualización intra especificado es compatible con el códec especificado, 
profile y level.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_output_resolution)  | Recupera la lista de resoluciones admitidas para el códec especificado.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION_RATIOS_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_output_resolution_ratios_count)  | |
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_profile_level)  | Recupera un valor que indica si el perfil especificado es compatible con la codificación de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_MODE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_rate_control_mode)  | Recupera un valor que indica si se admite el modo de control de velocidad especificado para la codificación de vídeo con 
códec especificado|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits)  | Representa los límites de compatibilidad de resolución de codificadores de vídeo para un D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT 
Estructura.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements)  | Recupera valores que indican los requisitos de recursos para la codificación de vídeo con la codificación especificada. 
.|
| [D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_encoder_support)  | Recupera valores que indican la compatibilidad con las características de codificación de vídeo y los valores de configuración especificados.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_count)  | Recupera el número de comandos de extensión de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameter_count)  | Recupera el número admitido de parámetros para la fase de parámetros especificada.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameters)  | Recupera la lista de parámetros de comando de extensión de vídeo para la fase de parámetros especificada.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_size)  | Comprueba el tamaño de asignación de un comando de extensión de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_support)  | Recupera la compatibilidad con comandos de extensión de vídeo mediante estructuras de entrada y salida definidas por comandos.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_commands)  | Recupera la lista de comandos de extensión de vídeo del controlador.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator)  | Proporciona datos para las llamadas a ID3D12VideoDevice::CheckFeatureSupport cuando la característica especificada se D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR. Recupera las funcionalidades de estimación de movimiento para un codificador de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_protected_resources)  | Proporciona datos para las llamadas a ID3D12VideoDevice::CheckFeatureSupport cuando la característica especificada se D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES. Recupera la compatibilidad de recursos protegidos para la estimación del movimiento de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_size)  | Describe el tamaño de asignación de un montón de estimador de movimiento de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_max_input_streams)  | Recupera el número máximo de flujos de entrada habilitados admitidos por el procesador de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_reference_info)  | Recupera el número de fotogramas de referencia pasados y futuros necesarios para las características de modo de desinterlace, filtro, conversión de velocidad o procesamiento automático especificados.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_support)  | Proporciona datos para las llamadas a ID3D12VideoDevice::CheckFeatureSupport cuando la característica especificada D3D12_FEATURE_VIDEO_PROCESS_SUPPORT.|
| [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics)  | Representa los datos de una consulta de estadísticas de descodificación de vídeo invocada mediante una llamada a ID3D12VideoDecodeCommandList::EndQuery.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_input)  | Proporciona datos de entrada para las llamadas a ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_output)  | Recibe datos de salida de llamadas a ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap.|
| [D3D12_RESOURCE_COORDINATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resource_coordinate)  | Describe las coordenadas de un recurso.|
| [D3D12_VIDEO_DECODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_desc)  | Describe un ID3D12VideoDecoder.|
| [D3D12_VIDEO_DECODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc)  | Describe un ID3D12VideoDecoderHeap.|
| [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream)  | Representa una secuencia de bits comprimida desde la que se descodifica el vídeo.|
| [D3D12_VIDEO_DECODE_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_configuration)  | Describe la configuración de un descodificador de vídeo.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments)  | Especifica los parámetros para descodificar la conversión de salida.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments1)  | Especifica los parámetros para descodificar la conversión de salida.|
| [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument)  | Representa los parámetros de descodificación de un marco.|
| [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)  | Especifica los parámetros del flujo de entrada para una operación de descodificación de vídeo.|
| [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)  | Representa el búfer de salida del histograma para un único componente.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)  | Especifica los parámetros del flujo de salida para una operación de descodificación de vídeo.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1)  | Especifica los parámetros del flujo de salida para una operación de descodificación de vídeo.|
| [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames)  | Contiene la lista de marcos de referencia para la operación de descodificación actual.|
| [D3D12_VIDEO_DECODE_SUB_SAMPLE_MAPPING_BLOCK](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_sub_sample_mapping_block)  | Define la asignación de bytes de cifrado de sub samples para la codificación de vídeo.|
| [D3D12_VIDEO_ENCODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encode_reference_frames)  | Representa las imágenes de referencia reconstruidas para una operación de codificación.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration)  | Representa una estructura de configuración de códec para la codificación de vídeo.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_h264)  | Representa la configuración del códec para la codificación H.264.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_hevc)  | Representa la configuración del códec para la codificación HEVC.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_support)  | Representa una estructura de compatibilidad con la configuración de códecs para la codificación de vídeo.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_support_h264)  | Representa la compatibilidad con la configuración del códec del codificador para la codificación H.264.|
| [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration_support_hevc)  | Representa la compatibilidad con la configuración del códec del codificador para la codificación HEVC.|
| [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_picture_control_support)  | Representa la estructura de compatibilidad del control de imagen para varios códecs.|
| [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_picture_control_support_h264)  | Representa la configuración de compatibilidad del control de imagen para la codificación de vídeo H.264.|
| [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_picture_control_support_hevc)  | Representa la configuración de compatibilidad del control de imagen para la codificación de vídeo HEVC.|
| [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_compressed_bitstream)  | Encapsula la salida de secuencia de bits comprimida para la operación de codificación.|
| [D3D12_VIDEO_ENCODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_desc)  | Describe un ID3D12VideoEncoder.|
| [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer)  | Representa un búfer que contiene metadatos sobre una operación ID3D12VideoEncodeCommandList2::EncodeFrame.|
| [D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_encodeframe_input_arguments)  | Representa argumentos de entrada para ID3D12VideoEncodeCommandList2::EncodeFrame.|
| [D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_encodeframe_output_arguments)  | Representa argumentos de salida para ID3D12VideoEncodeCommandList2::EncodeFrame.|
| [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_frame_subregion_metadata)  | Representa los metadatos de la subregión del marco del codificador de vídeo.|
| [D3D12_VIDEO_ENCODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_heap_desc)  | Describe un ID3D12VideoEncoderHeap.|
| [D3D12_VIDEO_ENCODER_INTRA_REFRESH](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_intra_refresh)  | Representa la configuración de actualización dentro de la codificación de vídeo.|
| [D3D12_VIDEO_ENCODER_LEVEL_SETTING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_level_setting)  | Representa una configuración de nivel de codificador de vídeo.|
| [D3D12_VIDEO_ENCODER_LEVEL_TIER_CONSTRAINTS_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_level_tier_constraints_hevc)  | Asocia un nivel y un nivel para la configuración de nivel de codificación de vídeo de alta eficacia (HEVC).|
| [D3D12_VIDEO_ENCODER_OUTPUT_METADATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_output_metadata)  | Representa metadatos sobre una operación ID3D12VideoEncodeCommandList2::EncodeFrame.|
| [D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_output_metadata_statistics)  | Representa estadísticas de codificación sobre una operación ID3D12VideoEncodeCommandList2::EncodeFrame.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data)  | Representa los elementos de control de nivel de imagen para el comando EncodeFrame asociado para varios códecs.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264)  | Representa los elementos de control de nivel de imagen para el comando EncodeFrame asociado para la codificación H.264.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264_reference_picture_list_modification_operation)  | Representa una operación de modificación de la lista de imágenes para la codificación de vídeo H264.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_MARKING_OPERATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264_reference_picture_marking_operation)  | Describe los cambios en las imágenes de referencia como operaciones de memoria como una tupla de un identificador de operación. 
y los parámetros asociados necesarios para la operación.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_hevc)  | Representa los elementos de control de nivel de imagen para el comando EncodeFrame asociado para la codificación HEVC.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_desc)  | 06/30/2021|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_subregions_layout_data)  | Define subregiones de control de imagen como segmentos para varios códecs.|
| [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_subregions_layout_data_slices)  | Define subregiones como segmentos para códecs que admiten este modo de creación de particiones.|
| [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_resolution_desc)  | Define una resolución de imágenes del codificador de vídeo.|
| [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_RATIO_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_resolution_ratio_desc)  | Define una relación de resolución como una fracción irreducible.|
| [D3D12_VIDEO_ENCODER_PROFILE_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_profile_desc)  | Describe un perfil de codificador.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control)  | Representa una configuración de control de velocidad del codificador de vídeo.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_cbr)  | Representa una definición de estructura de control de velocidad para el modo de velocidad de bits constante.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_configuration_params)  | Representa definiciones de estructura de control de velocidad del codificador de vídeo para un D3D12_VIDEO_ENCODER_RATE_CONTROL 
Estructura.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_cqp)  | Representa una definición de estructura de control de velocidad para el modo de parámetro de cuantificación constante.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_QVBR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_qvbr)  | Representa una definición de estructura de control de velocidad para el destino de calidad constante con velocidad de bits restringida.|
| [D3D12_VIDEO_ENCODER_RATE_CONTROL_VBR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control_vbr)  | Representa una definición de estructura de control de velocidad para el modo de velocidad de bits variable.|
| [D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_reconstructed_picture)  | Representa la imagen reconstruida generada a partir del marco de entrada pasado a la operación de codificación.|
| [D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_reference_picture_descriptor_h264)  | Representa un descriptor de imagen de referencia para la codificación de vídeo H.264.|
| [D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_reference_picture_descriptor_hevc)  | Representa un descriptor de imagen de referencia para la codificación de vídeo HEVC.|
| [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments)  | Representa los argumentos de entrada para una llamada a ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata.|
| [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments)  | Representa los argumentos de salida de una llamada a ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata.|
| [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_control_desc)  | |
| [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_gop_structure)  | Representa la estructura de GOP para varios códecs de vídeo.|
| [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_gop_structure_h264)  | Representa la estructura GOP para la codificación de vídeo H.264.|
| [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_HEVC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_gop_structure_hevc)  | Representa la estructura GOP para la codificación de vídeo HEVC.|
| [D3D12_VIDEO_EXTENSION_COMMAND_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_desc)  | Describe un comando de extensión de vídeo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_info)  | Describe un comando de extensión de vídeo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_parameter_info)  | Describe un parámetro de comando de extensión de vídeo.|
| [D3D12_VIDEO_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_format)  | Define la combinación de un formato de píxel y un espacio de color para una descripción del contenido del recurso.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_desc)  | Describe un ID3D12VideoMotionEstimator. Pase esta estructura a ID3D12VideoDevice1::CreateVideoMotionEstimator para crear una instancia de ID3D12VideoMotionEstimator.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input)  | Proporciona datos de entrada para las llamadas a ID3D12VideoEncodeCommandList::EstimateMotion.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output)  | Recibe datos de salida de llamadas a ID3D12VideoEncodeCommandList::EstimateMotion.|
| [D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_vector_heap_desc)  | Describe un id3D12VideoMotionEstimatorHeap. Pase esta estructura a ID3D12VideoDevice1::CreateVideoMotionEstimatorHeap para crear una instancia de ID3D12VideoMotionEstimatorHeap.|
| [D3D12_VIDEO_PROCESS_ALPHA_BLENDING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending)  | Especifica parámetros de combinación alfa para el procesamiento de vídeo.|
| [D3D12_VIDEO_PROCESS_FILTER_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_filter_range)  | Define el intervalo de valores admitidos para un filtro de imagen.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream)  | Contiene información de entrada para la funcionalidad de mezcla del procesador de vídeo.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)  | Especifica argumentos de flujo de entrada para un flujo de entrada pasado a ID3D12VideoCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc)  | Especifica los parámetros del flujo de entrada para una operación de proceso de vídeo.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_RATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_rate)  | Proporciona información sobre la velocidad de transmisión.|
| [D3D12_VIDEO_PROCESS_LUMA_KEY](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_luma_key)  | Especifica la configuración que se usa para la clave de luma.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream)  | Representa el flujo de salida para los comandos de procesamiento de vídeo.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments)  | Especifica argumentos de flujo de salida para la salida pasada a ID3D12VideoCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  | Especifica argumentos de flujo de salida para la salida pasada a ID3D12VideoProcessCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_REFERENCE_SET](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_reference_set)  | Contiene los fotogramas de referencia necesarios para realizar el procesamiento de vídeo.|
| [D3D12_VIDEO_PROCESS_TRANSFORM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_transform)  | Especifica los parámetros de transformación para el procesamiento de vídeo.|
| [D3D12_VIDEO_SAMPLE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_sample)  | Describe el ancho, alto, formato y espacio de color de un búfer de imagen.|
| [D3D12_VIDEO_SCALE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_scale_support)  | Describe el intervalo de escalado admitido de tamaños de salida para un escalador de vídeo.|
| [D3D12_VIDEO_SIZE_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_size_range)  | Describe la gama de tamaños admitidos para un escalador de vídeo.|



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D 12](direct3d-12-video-apis.md)
</dt> </dl>

 

 



