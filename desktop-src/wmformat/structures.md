---
title: Estructuras de SDK de Windows Media Format
description: Estructuras de SDK de Windows Media Format
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- SDK de Windows Media Format, estructuras
- Advanced Systems Format (ASF), estructuras
- ASF (formato de sistemas avanzados), estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f730ba3cbc5bd8bbec2a9f01c72df1fe46f0b64
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695836"
---
# <a name="windows-media-format-sdk-structures"></a>Estructuras de SDK de Windows Media Format

El SDK de Windows Media Format implementa las siguientes estructuras.



| Estructura                                                                                | Descripción                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**el \_ OPL de copia de DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Contiene información de nivel de protección de salida que se aplica a la acción de copia en una licencia de DRM.                                                                               |
| [**\_datos de \_ Estado de licencia de DRM \_**](drm-license-state-data.md)                              | Contiene la información de [*licencia*](wmformat-glossary.md) de un derecho [*DRM*](wmformat-glossary.md) especificado. |
| [**\_niveles de \_ protección de salida mínima \_ de DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Contiene los niveles de protección de salida mínimos requeridos por una licencia DRM para reproducir contenido en distintos formatos.                                                                      |
| [**ID. de salida de OPL de DRM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Contiene una matriz de identificadores de tecnología DRM. Esta estructura se usa para definir grupos de tecnologías en otras estructuras DRM.                                            |
| [**el \_ OPL de reproducción de DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Contiene información de nivel de protección de salida que se aplica a la acción Play en una licencia DRM.                                                                               |
| [**identificador de contenido de lista de \_ reproducción DRM \_ \_**](drm-playlist-content-id.md)                            | Contiene información sobre el contenido que se va a copiar en el CD como parte de la grabación de una lista de reproducción.                                                                                 |
| [**\_VAL16 DRM**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Almacena un valor de 128 bits usado como identificador de dispositivo.                                                                                                                       |
| [**\_protección de \_ salida de vídeo DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Contiene el identificador de una tecnología de protección de vídeo y los datos de configuración requeridos por esa tecnología.                                                             |
| [**\_ \_ \_ identificadores de protección de salida de vídeo DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Contiene una matriz de estructuras de **\_ protección de \_ salida \_ de vídeo DRM** .                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Define el formato de los datos de audio de forma de onda.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Define el formato de los datos de audio de forma de onda para los formatos que tienen más de dos canales.                                                                                      |
| [**\_ACCESSENTRY de dirección de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Especifica una entrada en una lista de acceso de direcciones IP.                                                                                                                          |
| [**\_propiedades de cliente de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Registra información sobre el cliente.                                                                                                                                     |
| [**propiedades de cliente de WM \_ \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Registra información extendida sobre el cliente.                                                                                                                            |
| [**\_datos de \_ licencia de obtención de WM \_**](wm-get-license-data.md)                                    | Contiene información sobre una licencia DRM.                                                                                                                                 |
| [**Estado de la \_ individualización de WM \_**](wm-individualize-status.md)                             | Registra el estado del proceso de [*individualización*](wmformat-glossary.md) .                                                                |
| [**\_par de depósitos de fugas de WM \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable (VBR).                                                                                                  |
| [**\_datos de \_ Estado de licencia de WM \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Encapsula una estructura [**de \_ \_ \_ datos de estado de licencia DRM**](drm-license-state-data.md) que describe los datos de estado de licencia de DRM.                                              |
| [**\_tipo de medio de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Describe un ejemplo multimedia.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Describe una secuencia de vídeo MPEG-2.                                                                                                                                         |
| [**imagen de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Contiene los datos del atributo de metadatos de [**WM/imagen**](wmpicture.md) complejos.                                                                                     |
| [**\_intervalo de \_ número de puerto de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Describe el intervalo de números de puerto que usa la interfaz **IWMReaderNetworkConfig** .                                                                                     |
| [**lector de WM \_ \_ ClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Describe el lector de cliente (reproductor) que tiene acceso a la secuencia de medios.                                                                                                          |
| [**\_estadísticas del lector de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Describe el rendimiento de una operación de lectura.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Define el formato de un flujo de script.                                                                                                                                    |
| [**\_registro de \_ prioridad de secuencia de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Contiene un número de secuencia y especifica si la entrega de esa secuencia es obligatoria.                                                                                      |
| [**\_información de \_ tipo de flujo de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Contiene los datos del atributo de metadatos complejos [**WM/StreamTypeInfo**](wm-streamtypeinfo.md) .                                                                      |
| [**\_Letras sincronizadas de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Contiene los datos del atributo de metadatos complejos [**\_ sincronizado de WM/letra**](wm-lyrics-synchronised.md) .                                                           |
| [**\_texto de usuario de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Contiene los datos del atributo de metadatos de [**WM/texto**](wm-text.md) complejo.                                                                                          |
| [**\_URL de \_ Web de usuario de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Contiene los datos del atributo de metadatos complejos [**WM/UserWebURL**](wm-userweburl.md) .                                                                              |
| [**\_estadísticas del escritor de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Describe el rendimiento de una operación de escritura.                                                                                                                         |
| [**Estadísticas del escritor de WM \_ \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Contiene estadísticas extendidas del escritor.                                                                                                                                      |
| [**\_clave de \_ contenido de importación de WMDRM \_**](wmdrm-import-content-key.md)                          | Contiene la clave de contenido utilizada en la importación de contenido protegido.                                                                                                                |
| [**\_ \_ struct init de importación de WMDRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Contiene la clave de sesión cifrada y la clave de contenido que se usan en la importación de contenido protegido.                                                                                      |
| [**\_clave de \_ sesión de importación de WMDRM \_**](wmdrm-import-session-key.md)                          | Contiene la clave de sesión para importar contenido protegido.                                                                                                                    |
| [**\_segmento del búfer WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Contiene la información necesaria para especificar un segmento en un paquete.                                                                                                      |
| [**\_datos de \_ extensión de COLORSPACEINFO WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Contiene los datos de la \_ extensión de unidad de datos de SampleExtensionGUID ColorSpaceInfo de WM \_ .                                                                                    |
| [**\_unidad de \_ datos de FILESINK WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Contiene información sobre un paquete.                                                                                                                                      |
| [**\_fragmento de carga de WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Contiene la información necesaria para extraer un fragmento de carga de un paquete.                                                                                           |
| [**datos de extensión de código de \_ tiempo WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Contiene un solo código de tiempo de SMPTE e información relacionada.                                                                                                                |
| [**\_ejemplo de VIDEOimage de WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Contiene información sobre un ejemplo de imagen de vídeo.                                                                                                                          |
| [**\_entrada de marca de agua WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Contiene información acerca de un sistema de marcas de agua.                                                                                                                         |
| [**\_formato de WEBstream de WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Contiene información sobre una secuencia Web.                                                                                                                                  |
| [**\_encabezado de ejemplo de WEBSTREAM WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Contiene información de encabezado para los ejemplos de secuencias Web.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Describe la información de color y de mapa de bits de una imagen de vídeo.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Describe la información del mapa de bits y del color de una imagen de vídeo, incluido el [*entrelazado*](wmformat-glossary.md), la protección contra copia y la relación de aspecto.       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 
