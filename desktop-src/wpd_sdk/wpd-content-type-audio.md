---
description: AUDIO DE \_ TIPO DE \_ CONTENIDO WPD \_
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83d43fcef539579fc0a687a97ba51e52278e4da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466195"
---
# <a name="wpd_content_type_audio"></a>AUDIO DE \_ TIPO DE \_ CONTENIDO WPD \_

Un objeto que describe su tipo como WPD CONTENT TYPE AUDIO representa un archivo de audio, como un archivo \_ \_ Windows Media Audio \_ (WMA) o MP3.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.     |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Necesario.                                                                          |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                                          |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.     |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Necesario.                                                                          |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Necesario.                                                                          |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                  |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).              |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                  |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                          |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.              |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                            |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                          |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                          |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                             |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                           | Opcional.                                                                          |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                         | Se recomienda su uso.                                                                       |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                          |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                         |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                          |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md) | Opcional.                                                                          |
| [EL OBJETO \_ WPD \_ SE PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si el objeto se puede eliminar.                                             |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                                          |
| [VELOCIDAD DE BITS \_ \_ TOTAL DE MEDIOS \_ WPD](media-properties.md)                                            | Se recomienda su uso.                                                                       |
| [TIPO DE \_ VELOCIDAD DE BITS DE MEDIOS \_ WPD \_](media-properties.md)                                              | Opcional.                                                                          |
| [COPYRIGHT DE \_ WPD \_ MEDIA](media-properties.md)                                                     | Opcional.                                                                          |
| [IDENTIFICADOR DE \_ CONTENIDO DE LA SUSCRIPCIÓN DE \_ \_ \_ WPD MEDIA](media-properties.md)                       | Se recomienda si este objeto representa el contenido de un servicio de suscripción en línea. |
| [RECUENTO DE \_ USO DE MEDIOS DE \_ \_ WPD](media-properties.md)                                                    | Se recomienda su uso.                                                                       |
| [RECUENTO DE \_ SKIP \_ DE WPD \_ MEDIA](media-properties.md)                                                  | Opcional.                                                                          |
| [HORA DE \_ ÚLTIMO ACCESO A WPD \_ \_ \_ MEDIA](media-properties.md)                                 | Opcional.                                                                          |
| [CLASIFICACIÓN PARENTAL \_ DE WPD \_ MEDIA \_](media-properties.md)                                        | Opcional.                                                                          |
| [WPD \_ MEDIA \_ META \_ GENRE](media-properties.md)                                                  | Opcional.                                                                          |
| [WPD \_ MEDIA \_ COMPOSER](media-properties.md)                                                       | Opcional.                                                                          |
| [CLASIFICACIÓN EFICAZ DE MEDIOS WPD \_ \_ \_](media-properties.md)                                      | Opcional.                                                                          |
| [SUB TÍTULO DE \_ \_ WPD \_ MEDIA](media-properties.md)                                                    | Opcional.                                                                          |
| [FECHA DE LANZAMIENTO \_ DE WPD \_ \_ MEDIA](media-properties.md)                                              | Se recomienda su uso.                                                                       |
| [FRECUENCIA DE MUESTREO \_ DE \_ WPD \_ MEDIA](media-properties.md)                                                | Opcional.                                                                          |
| [CLASIFICACIÓN POR \_ ESTRELLAS DE WPD \_ \_ MEDIA](media-properties.md)                                                | Se recomienda su uso.                                                                       |
| [CLASIFICACIÓN EFECTIVA DEL USUARIO DE WPD \_ \_ \_ \_ MEDIA](media-properties.md)                           | Se recomienda su uso.                                                                       |
| [TÍTULO MULTIMEDIA \_ DE \_ WPD](media-properties.md)                                                             | Necesario.                                                                          |
| [DURACIÓN MULTIMEDIA \_ DE \_ WPD](media-properties.md)                                                       | Necesario.                                                                          |
| [WPD \_ MEDIA \_ BUY \_ NOW](media-properties.md)                                                        | Se recomienda su uso.                                                                       |
| [PERFIL DE \_ CODIFICACIÓN \_ MULTIMEDIA \_ WPD](media-properties.md)                                      | Opcional.                                                                          |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                                            | Se recomienda su uso.                                                                       |
| [WPD \_ MEDIA \_ ALBUM \_ ARTIST](media-properties.md)                                                                     | Se recomienda su uso.                                                                       |
| [DIRECCIÓN URL DE \_ ORIGEN \_ DE \_ WPD MEDIA](media-properties.md)                                                                       | Opcional.                                                                          |
| [DIRECCIÓN URL DE \_ DESTINO DE MEDIOS DE \_ \_ WPD](media-properties.md)                                                                  | Opcional.                                                                          |
| [DESCRIPCIÓN DE MEDIOS \_ DE \_ WPD](media-properties.md)                                                                       | Opcional.                                                                          |
| [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                                                                             | Opcional.                                                                          |
| [MARCADOR DE \_ TIEMPO MULTIMEDIA \_ DE WPD \_](media-properties.md)                                                                    | Opcional.                                                                          |
| [MARCADOR DE \_ BYTES MULTIMEDIA \_ WPD \_](media-properties.md)                                                                    | Opcional.                                                                          |
| [GUID DE \_ MEDIOS DE \_ WPD](media-properties.md)                                                                              | Opcional.                                                                          |
| [WPD \_ MEDIA \_ SUB \_ DESCRIPTION](media-properties.md)                                                                  | Opcional.                                                                          |
| [WPD \_ MUSIC \_ ALBUM](music-properties.md)                                                             | Se recomienda su uso.                                                                       |
| [WPD \_ MUSIC \_ TRACK](music-properties.md)                                                             | Se recomienda su uso.                                                                       |
| [WPD \_ MUSIC \_ LORÓN](music-properties.md)                                                           | Opcional.                                                                          |
| [WPD \_ MUSIC \_ MOOD](music-properties.md)                                                               | Opcional.                                                                          |
| [VELOCIDAD DE \_ BITS DE AUDIO \_ WPD](audio-properties.md)                                                         | Se recomienda su uso.                                                                       |
| [RECUENTO DE \_ CANALES DE AUDIO \_ \_ WPD](audio-properties.md)                                            | Opcional.                                                                          |
| [CÓDIGO DE \_ FORMATO DE AUDIO \_ \_ WPD](audio-properties.md)                                                | Opcional.                                                                          |
| [PROFUNDIDAD DE \_ BITS \_ DE AUDIO \_ WPD](audio-properties.md)                                                    | Opcional.                                                                          |
| [ALINEACIÓN DE \_ BLOQUES DE AUDIO \_ \_ WPD](audio-properties.md)                                        | Opcional.                                                                          |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                               | Obligatorio u opcional       | Descripción                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)      | Opcional.                  | Contiene el archivo de audio completo.                  |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md) | Recomendado, si está disponible. | Contiene la imagen del álbum.                |
| [**AUDIOCLIP \_ DE RECURSOS DE WPD \_**](wpd-resource-audio-clip.md) | Opcional.                  | Contiene un clip de ejemplo del archivo de audio completo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



