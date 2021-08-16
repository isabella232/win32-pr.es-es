---
title: Windows Tipos de enumeración del SDK de formato multimedia
description: Obtenga información sobre los tipos de enumeración que implementa Windows SDK de formato multimedia, como DRM_HTTP_STATUS y DRM_LICENSE_STATE_CATEGORY.
ms.assetid: cd28f608-25ba-44a7-868b-b1cd4dfcfa45
keywords:
- Windows SDK de formato multimedia, tipos de enumeración
- Formato de sistemas avanzados (ASF), tipos de enumeración
- ASF (formato de sistemas avanzados), tipos de enumeración
- tipos de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b3a53688e21e58b0d9509cc901a72399f26b9d758cac89511e66a76d740db1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848164"
---
# <a name="windows-media-format-sdk-enumeration-types"></a>Windows Tipos de enumeración del SDK de formato multimedia

El SDK Windows Media Format implementa los siguientes tipos de enumeración.



| Tipo de enumeración                                                               | Descripción                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ESTADO \_ HTTP DE DRM \_**](drm-http-status.md)                                   | Define un intervalo de estados para una solicitud DRM.                                                                                     |
| [**CATEGORÍA ESTADO \_ DE \_ LICENCIA \_ DE DRM**](drm-license-state-category.md)            | Define las categorías para las cadenas de licencia de DRM.                                                                                  |
| [**ESTADO \_ DE INDIVIDUALIZACIÓN DE DRM \_**](drm-individualization-status.md)         | Define los estados válidos para la individualización de DRM.                                                                              |
| [**CONFIGURACIÓN DE \_ NETSOURCE URLCREDPOLICY \_**](/previous-versions/windows/desktop/api/wmsinternaladminnetsource/ne-wmsinternaladminnetsource-netsource_urlcredpolicy_settings) | Define la posible configuración de directiva de seguridad que puede existir en un equipo cliente.                                                   |
| [**WM \_ AETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wm_aetype)                                                | Especifica los permisos para una entrada en una lista de acceso de direcciones IP.                                                             |
| [**WMT \_ ATTR \_ DATATYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype)                               | Define un intervalo de tipos de datos básicos. Estos valores se usan para identificar el tipo de datos devuelto por varios métodos de este SDK. |
| [**WMT \_ ATTR \_ IMAGETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_imagetype)                             | Define un intervalo de tipos de imagen que se pueden almacenar en un encabezado de archivo ASF.                                                         |
| [**TIPO DE INFORMACIÓN \_ DE CÓDEC \_ WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_codec_info_type)                          | Define un intervalo de tamaños de datos usados por un códec.                                                                                   |
| [**MARCAS DE \_ CREDENCIALES WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_credential_flags)                         | Define las marcas que se pueden usar al adquirir credenciales.                                                                   |
| [**CONFIANZA \_ DRMLA de WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust)                                   | Define el estado de confianza de una dirección URL de adquisición de licencias DRM.                                                                        |
| [**WMT \_ FILESINK \_ MODE**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_filesink_mode)                               | Define los tipos de entrada aceptados por el receptor de archivos.                                                                            |
| [**TIPO DE \_ IMAGEN \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_image_type)                                     | Define los posibles tipos de imagen usados para los anuncios de banner.                                                                            |
| [**TIPO DE \_ ÍNDICE WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_index_type)                                     | Define el objeto al que se puede asociar un índice basado en el tiempo.                                                              |
| [**TIPO \_ DE INDEXADOR WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_indexer_type)                                 | Define los tipos de indexación admitidos por el indexador.                                                                          |
| [**PROTOCOLO WMT \_ NET \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_net_protocol)                                 | Define los tipos de protocolos que admite el receptor de red.                                                                   |
| [**MODO DE \_ CLASE MUSICSPEECH \_ DE WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_musicspeech_class_mode)            | Define los modos de compresión disponibles para el códec Windows Media Audio 9 Voice.                                                |
| [**FORMATO DE \_ DESPLAZAMIENTO WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_offset_format)                               | Define los tipos de desplazamientos usados en este SDK.                                                                                   |
| [**MODO DE \_ REPRODUCCIÓN \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_play_mode)                                       | Define las opciones de reproducción del lector.                                                                                      |
| [**CONFIGURACIÓN DEL \_ PROXY WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_proxy_settings)                             | Define la configuración del proxy de red para su uso con un objeto de lector.                                                                 |
| [**DERECHOS \_ DE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights)                                              | Define los derechos que se pueden especificar en una licencia DRM.                                                                       |
| [**ESTADO \_ DE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)                                              | Define un intervalo de marcas de estado.                                                                                                 |
| [**FORMATO DE \_ ALMACENAMIENTO \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format)                             | Define los tipos de archivo que se pueden manipular con este SDK.                                                                    |
| [**SELECCIÓN DE SECUENCIA DE WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection)                         | Define el estado de una secuencia.                                                                                                  |
| [**TIPO DE \_ TRANSPORTE \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_transport_type)                             | Define los tipos de transporte admitidos por este SDK.                                                                               |
| [**VERSIÓN \_ DE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version)                                            | Define los números de versión del SDK Windows Media Format.                                                                     |
| [**TIPO DE \_ ENTRADA WMT WATERMARK \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_watermark_entry_type)                | Define los tipos de marcas de agua admitidas.                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 




