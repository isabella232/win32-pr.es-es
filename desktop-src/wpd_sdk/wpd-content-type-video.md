---
description: VÍDEO DE \_ TIPO DE \_ CONTENIDO \_ WPD
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aacf30a9e646a6089058104bd39577fad832e31
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424126"
---
# <a name="wpd_content_type_video"></a>VÍDEO DE \_ TIPO DE \_ CONTENIDO \_ WPD

Un objeto que describe su tipo como WPD \_ CONTENT TYPE VIDEO representa un archivo de \_ \_ vídeo.

Este tipo de objeto admite las siguientes propiedades.



|  Nombre de la propiedad                             | Obligatorio u opcional              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                               |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Necesario.                                                                                                                    |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                                                                                    |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                               |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Necesario.                                                                                                                    |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Necesario.                                                                                                                    |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                                                            |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                        |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                            |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                                                                    |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                                                        |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                                      |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                                                                    |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                                    |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                       |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                           | Opcional.                                                                                                                    |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Se recomienda su uso.                                                                                                                 |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                                                                    |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                                   |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                                    |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md) | Opcional.                                                                                                                    |
| [EL OBJETO \_ WPD \_ SE PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                                                                    |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                                                                                    |
| [VELOCIDAD DE BITS \_ \_ TOTAL DE MEDIOS \_ WPD](media-properties.md)                                            | Se recomienda su uso.                                                                                                                 |
| [TIPO DE \_ VELOCIDAD DE BITS DE MEDIOS \_ WPD \_](media-properties.md)                                              | Opcional.                                                                                                                    |
| [COPYRIGHT DE \_ WPD \_ MEDIA](media-properties.md)                                                     | Opcional.                                                                                                                    |
| [IDENTIFICADOR DE \_ CONTENIDO DE LA SUSCRIPCIÓN DE \_ \_ \_ WPD MEDIA](media-properties.md)                       | Se recomienda si este objeto representa el contenido de un servicio de suscripción en línea.                                          |
| [RECUENTO DE \_ USO DE MEDIOS DE \_ \_ WPD](media-properties.md)                                                    | Se recomienda su uso.                                                                                                                 |
| [RECUENTO DE \_ SKIP \_ DE WPD \_ MEDIA](media-properties.md)                                                  | Opcional.                                                                                                                    |
| [HORA DE \_ ÚLTIMO ACCESO A WPD \_ \_ \_ MEDIA](media-properties.md)                                 | Opcional.                                                                                                                    |
| [CLASIFICACIÓN PARENTAL \_ DE WPD \_ MEDIA \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [WPD \_ MEDIA \_ META \_ GENRE](media-properties.md)                                                  | Opcional.                                                                                                                    |
| [WPD \_ MEDIA \_ COMPOSER](media-properties.md)                                                       | Opcional.                                                                                                                    |
| [CLASIFICACIÓN EFICAZ DE MEDIOS WPD \_ \_ \_](media-properties.md)                                      | Opcional.                                                                                                                    |
| [SUB TÍTULO DE \_ \_ WPD \_ MEDIA](media-properties.md)                                                    | Opcional.                                                                                                                    |
| [FECHA DE LANZAMIENTO \_ DE WPD \_ \_ MEDIA](media-properties.md)                                              | Se recomienda su uso.                                                                                                                 |
| [FRECUENCIA DE MUESTREO \_ DE \_ WPD \_ MEDIA](media-properties.md)                                                | Opcional.                                                                                                                    |
| [CLASIFICACIÓN POR \_ ESTRELLAS DE WPD \_ \_ MEDIA](media-properties.md)                                                | Se recomienda su uso.                                                                                                                 |
| [CLASIFICACIÓN EFECTIVA DEL USUARIO DE WPD \_ \_ \_ \_ MEDIA](media-properties.md)                           | Se recomienda su uso.                                                                                                                 |
| [TÍTULO MULTIMEDIA \_ DE \_ WPD](media-properties.md)                                                             | Necesario.                                                                                                                    |
| [DURACIÓN DE \_ LOS MEDIOS \_ WPD](media-properties.md)                                                       | Necesario.                                                                                                                    |
| [WPD \_ MEDIA \_ BUY \_ NOW](media-properties.md)                                                        | Se recomienda su uso.                                                                                                                 |
| [PERFIL DE \_ CODIFICACIÓN \_ MULTIMEDIA \_ WPD](media-properties.md)                                      | Opcional.                                                                                                                    |
| [ANCHO DE MEDIOS \_ \_ WPD](media-properties.md)                                                             | Necesario.                                                                                                                    |
| [ALTO DE \_ MEDIOS \_ WPD](media-properties.md)                                                           | Necesario.                                                                                                                    |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                           | Se recomienda su uso.                                                                                                                 |
| [DIRECCIÓN URL DE \_ ORIGEN MULTIMEDIA DE \_ \_ WPD](media-properties.md)                                                  | Se recomienda su uso.                                                                                                                 |
| [DIRECCIÓN URL DE \_ DESTINO DE MEDIOS DE \_ \_ WPD](media-properties.md)                                        | Opcional.                                                                                                                    |
| [DESCRIPCIÓN DE MEDIOS \_ DE \_ WPD](media-properties.md)                                                 | Opcional.                                                                                                                    |
| [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                                                             | Opcional.                                                                                                                    |
| [MARCADOR DE \_ TIEMPO MULTIMEDIA \_ DE WPD \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [MARCADOR DE \_ BYTES MULTIMEDIA \_ WPD \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [GUID DE \_ MEDIOS DE \_ WPD](media-properties.md)                                                               | Opcional.                                                                                                                    |
| [WPD \_ MEDIA \_ SUB \_ DESCRIPTION](media-properties.md)                                        | Opcional.                                                                                                                    |
| [WPD \_ VIDEO \_ AUTHOR](video-properties.md)                                                           | Opcional.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ STATION \_ NAME](video-properties.md)                       | Opcional.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ CHANNEL \_ NUMBER](video-properties.md)                   | Opcional.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT](video-properties.md)                                    | Opcional.                                                                                                                    |
| [TAMAÑO DEL BÚFER \_ DE \_ VÍDEO \_ WPD](video-properties.md)                                                | Opcional.                                                                                                                    |
| [CRÉDITOS DE VÍDEO DE WPD \_ \_](video-properties.md)                                                         | Opcional.                                                                                                                    |
| [DISTANCIA ENTRE \_ \_ FOTOGRAMAS CLAVE \_ DE VÍDEO WPD \_](video-properties.md)                                 | Opcional.                                                                                                                    |
| [CONFIGURACIÓN DE CALIDAD \_ DE \_ VÍDEO WPD \_](video-properties.md)                                        | Opcional.                                                                                                                    |
| [TIPO DE \_ EXAMEN \_ DE VÍDEO \_ WPD](video-properties.md)                                                    | Necesario.                                                                                                                    |
| [VELOCIDAD DE BITS \_ \_ DE VÍDEO WPD](video-properties.md)                                                         | Necesario.                                                                                                                    |
| [WPD \_ VIDEO \_ FOURCC \_ CODE](video-properties.md)                                                | Obligatorio si el códec es compatible con Microsoft Video para Windows (VFW), Microsoft DirectShow y Windows Media Format. |
| [VELOCIDAD DE \_ \_ FOTOGRAMAS DE VÍDEO WPD](video-properties.md)                                                     | Opcional.                                                                                                                    |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                              | Obligatorio u opcional       | Descripción                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)     | Necesario.                  | Contiene los datos de vídeo (archivo).                                      |
| [**MINIATURA DE RECURSOS DE WPD \_ \_**](wpd-resource-thumbnail.md) | Se recomienda, si está disponible. | Contiene el fotograma clave u otro marco de ejemplo no en pantalla para el vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



