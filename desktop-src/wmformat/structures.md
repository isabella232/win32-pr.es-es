---
title: Windows Estructuras del SDK de formato multimedia
description: Windows Estructuras del SDK de formato multimedia
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows SDK de formato multimedia, estructuras
- Formato de sistemas avanzados (ASF), estructuras
- ASF (formato de sistemas avanzados), estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f730ba3cbc5bd8bbec2a9f01c72df1fe46f0b64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359907"
---
# <a name="windows-media-format-sdk-structures"></a>Windows Estructuras del SDK de formato multimedia

El SDK Windows Media Format implementa las siguientes estructuras.



| Estructura                                                                                | Descripción                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPL \_ DE COPIA DE DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Contiene información de nivel de protección de salida que se aplica a la acción de copia en una licencia DRM.                                                                               |
| [**DATOS DE \_ ESTADO DE \_ LICENCIA DE DRM \_**](drm-license-state-data.md)                              | Contiene [*información de*](wmformat-glossary.md) licencia sobre un derecho [*DRM*](wmformat-glossary.md) especificado. |
| [**NIVELES \_ MÍNIMOS \_ DE PROTECCIÓN DE \_ SALIDA DE \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Contiene los niveles mínimos de protección de salida requeridos por una licencia DRM para reproducir contenido en varios formatos.                                                                      |
| [**IDENTIFICADORES \_ DE SALIDA DE OPL \_ \_ DE DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Contiene una matriz de identificadores de tecnología DRM. Esta estructura se usa para definir grupos de tecnologías en otras estructuras DRM.                                            |
| [**DRM \_ PLAY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Contiene información de nivel de protección de salida que se aplica a la acción de reproducción en una licencia DRM.                                                                               |
| [**IDENTIFICADOR DE \_ CONTENIDO DE LA LISTA DE REPRODUCCIÓN \_ \_ DE DRM**](drm-playlist-content-id.md)                            | Contiene información sobre el contenido que se va a copiar en CD como parte de una grabación de lista de reproducción.                                                                                 |
| [**DRM \_ VAL16**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Almacena un valor de 128 bits que se usa como identificador de dispositivo.                                                                                                                       |
| [**PROTECCIÓN DE \_ SALIDA \_ DE VÍDEO DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Contiene el identificador de una tecnología de protección de vídeo y los datos de configuración requeridos por esa tecnología.                                                             |
| [**IDENTIFICADORES \_ DE PROTECCIÓN DE SALIDA DE VÍDEO \_ \_ \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Contiene una matriz de estructuras **DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.**                                                                                                          |
| [**FORMA DE ONDAATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Define el formato de los datos de audio de forma de onda.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Define el formato de los datos de audio de forma de onda para los formatos que tienen más de dos canales.                                                                                      |
| [**WM \_ ADDRESS \_ ACCESSENTRY**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Especifica una entrada en una lista de acceso a direcciones IP.                                                                                                                          |
| [**PROPIEDADES \_ DE CLIENTE \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Registra información sobre el cliente.                                                                                                                                     |
| [**PROPIEDADES \_ DE CLIENTE \_ \_ WM, POR EJEMPLO,**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Registra información extendida sobre el cliente.                                                                                                                            |
| [**WM \_ GET \_ LICENSE \_ DATA**](wm-get-license-data.md)                                    | Contiene información sobre una licencia DRM.                                                                                                                                 |
| [**ESTADO \_ DE INDIVIDUALIZACIÓN \_ DE WM**](wm-individualize-status.md)                             | Registra el estado del proceso [*de individualización.*](wmformat-glossary.md)                                                                |
| [**PAR \_ DE CUBOS DE PÉRDIDA \_ DE \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable (VBR).                                                                                                  |
| [**WM \_ LICENSE \_ STATE \_ DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Encapsula una estructura DRM [**\_ LICENSE STATE \_ \_ DATA**](drm-license-state-data.md) que describe los datos de estado de licencia de DRM.                                              |
| [**TIPO \_ DE MEDIO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Describe un ejemplo multimedia.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Describe una secuencia de vídeo MPEG-2.                                                                                                                                         |
| [**IMAGEN \_ DE WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Contiene los datos del atributo [**de metadatos complejos WM/Picture.**](wmpicture.md)                                                                                     |
| [**INTERVALO DE \_ NÚMERO \_ DE PUERTO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Describe el intervalo de números de puerto usados por la **interfaz IWMReaderNetworkConfig.**                                                                                     |
| [**WM \_ READER \_ CLIENTINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Describe el lector cliente (reproductor) que accede a la secuencia multimedia.                                                                                                          |
| [**ESTADÍSTICAS \_ DEL \_ LECTOR WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Describe el rendimiento de una operación de lectura.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Define el formato de una secuencia de script.                                                                                                                                    |
| [**REGISTRO DE \_ PRIORIDAD DE SECUENCIA DE \_ \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Contiene un número de secuencia y especifica si la entrega de esa secuencia es obligatoria.                                                                                      |
| [**WM \_ STREAM \_ TYPE \_ INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Contiene los datos del atributo [**de metadatos complejos WM/StreamTypeInfo.**](wm-streamtypeinfo.md)                                                                      |
| [**WM \_ SYNCHRONISED \_ LOTIZA**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Contiene los datos para el [**atributo de metadatos complejos \_ wm/desastrosos**](wm-lyrics-synchronised.md) sincronizados.                                                           |
| [**TEXTO \_ DE USUARIO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Contiene los datos del atributo [**de metadatos complejos WM/Text.**](wm-text.md)                                                                                          |
| [**DIRECCIÓN \_ \_ URL WEB DE USUARIO \_ DE WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Contiene los datos del atributo [**de metadatos complejos WM/UserWebURL.**](wm-userweburl.md)                                                                              |
| [**ESTADÍSTICAS DE WM \_ \_ WRITER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Describe el rendimiento de una operación de escritura.                                                                                                                         |
| [**ESTADÍSTICAS DE WM \_ \_ \_ WRITER, POR EJEMPLO,**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Contiene estadísticas de escritura extendidas.                                                                                                                                      |
| [**CLAVE DE CONTENIDO \_ DE IMPORTACIÓN DE WMDRM \_ \_**](wmdrm-import-content-key.md)                          | Contiene la clave de contenido utilizada para importar contenido protegido.                                                                                                                |
| [**WMDRM \_ IMPORT \_ INIT \_ (STRUCT)**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Contiene la clave de sesión cifrada y la clave de contenido que se usan para importar contenido protegido.                                                                                      |
| [**CLAVE DE SESIÓN \_ DE IMPORTACIÓN DE WMDRM \_ \_**](wmdrm-import-session-key.md)                          | Contiene la clave de sesión para importar contenido protegido.                                                                                                                    |
| [**SEGMENTO DE \_ BÚFER WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Contiene la información necesaria para especificar un segmento en un paquete.                                                                                                      |
| [**DATOS DE EXTENSIÓN \_ COLORSPACEINFO \_ DE WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Contiene los datos de la extensión de unidad de datos Wm \_ SampleExtensionGUID \_ ColorSpaceInfo.                                                                                    |
| [**WMT \_ FILESINK \_ DATA \_ UNIT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Contiene información sobre un paquete.                                                                                                                                      |
| [**FRAGMENTO DE CARGA DE WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Contiene la información necesaria para extraer un fragmento de carga de un paquete.                                                                                           |
| [**DATOS DE EXTENSIÓN \_ DE CÓDIGO DE TIEMPO \_ DE WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Contiene un único código de tiempo SMPTE e información relacionada.                                                                                                                |
| [**EJEMPLO \_ DE VIDEOIMAGE DE WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Contiene información sobre un ejemplo de imagen de vídeo.                                                                                                                          |
| [**ENTRADA DE \_ MARCA DE AGUA WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Contiene información sobre un sistema de marca de agua.                                                                                                                         |
| [**FORMATO \_ WEBSTREAM DE \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Contiene información sobre una secuencia web.                                                                                                                                  |
| [**ENCABEZADO DE EJEMPLO \_ DE WEBSTREAM \_ DE WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Contiene información de encabezado para los ejemplos de flujo web.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Describe el mapa de bits y la información de color de una imagen de vídeo.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Describe la información de mapa de bits y color de una imagen de vídeo, incluidos [*el entrelazamiento,*](wmformat-glossary.md)la protección de copia y la relación de aspecto.       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 
