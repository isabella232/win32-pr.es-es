---
description: vídeo sobre el tipo de contenido de WPD \_ \_ \_
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afde065ef233ff64a4eb72af8be5f7308050ff75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706857"
---
# <a name="wpd_content_type_video"></a>vídeo sobre el tipo de contenido de WPD \_ \_ \_

Un objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ vídeo representa un archivo de vídeo.

Este tipo de objeto admite las siguientes propiedades.



|                                                                                                                       |                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Nombre de la propiedad**                                                                                                     | **Obligatorio u opcional**                                                                                                     |
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                               |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                                                                    |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                                                                                    |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                               |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                                                                    |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                                                                    |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                                                            |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                        |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                            |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                                                                    |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.                                                        |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                                      |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                                                                    |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                                    |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                       |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                                                                    |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                                                                 |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                                                                    |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                                   |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                                                                    |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                                                                    |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                     | Es obligatorio si no se puede eliminar el objeto.                                                                                    |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                                                                    |
| [\_velocidad de \_ bits total de medios de WPD \_](media-properties.md)                                            | Se recomienda su uso.                                                                                                                 |
| [\_tipo de \_ velocidad de bits de medios de WPD \_](media-properties.md)                                              | Opcional.                                                                                                                    |
| [COPYRIGHT de los medios de WPD \_ \_](media-properties.md)                                                     | Opcional.                                                                                                                    |
| [\_ \_ \_ ID. de contenido de suscripción de medios de WPD \_](media-properties.md)                       | Recomendado, si este objeto representa el contenido de un servicio de suscripción en línea.                                          |
| [recuento de uso de medios de WPD \_ \_ \_](media-properties.md)                                                    | Se recomienda su uso.                                                                                                                 |
| [recuento de omisiones de medios de WPD \_ \_ \_](media-properties.md)                                                  | Opcional.                                                                                                                    |
| [\_ \_ última hora de \_ acceso a los medios \_ de WPD](media-properties.md)                                 | Opcional.                                                                                                                    |
| [\_ \_ clasificación parental de medios de \_ WPD](media-properties.md)                                        | Opcional.                                                                                                                    |
| [metagénero de multimedia de WPD \_ \_ \_](media-properties.md)                                                  | Opcional.                                                                                                                    |
| [\_compositor de medios de WPD \_](media-properties.md)                                                       | Opcional.                                                                                                                    |
| [\_ \_ clasificación efectiva de medios de WPD \_](media-properties.md)                                      | Opcional.                                                                                                                    |
| [subtítulo de medios de WPD \_ \_ \_](media-properties.md)                                                    | Opcional.                                                                                                                    |
| [\_fecha de \_ lanzamiento de medios de WPD \_](media-properties.md)                                              | Se recomienda su uso.                                                                                                                 |
| [\_velocidad de \_ muestra \_ multimedia de WPD](media-properties.md)                                                | Opcional.                                                                                                                    |
| [\_clasificación de media \_ Star \_ de WPD](media-properties.md)                                                | Se recomienda su uso.                                                                                                                 |
| [\_ \_ \_ clasificación efectiva del usuario \_ de los medios de WPD](media-properties.md)                           | Se recomienda su uso.                                                                                                                 |
| [título de los medios de WPD \_ \_](media-properties.md)                                                             | Obligatorio.                                                                                                                    |
| [duración de los medios de WPD \_ \_](media-properties.md)                                                       | Obligatorio.                                                                                                                    |
| [\_compra multimedia \_ WPD \_ Now](media-properties.md)                                                        | Se recomienda su uso.                                                                                                                 |
| [\_Perfil de \_ codificación multimedia \_ WPD](media-properties.md)                                      | Opcional.                                                                                                                    |
| [\_ancho de medios de WPD \_](media-properties.md)                                                             | Obligatorio.                                                                                                                    |
| [altura de los medios de WPD \_ \_](media-properties.md)                                                           | Obligatorio.                                                                                                                    |
| [\_intérprete multimedia de WPD \_](media-properties.md)                                                           | Se recomienda su uso.                                                                                                                 |
| [\_URL de \_ origen de medios de WPD \_](media-properties.md)                                                  | Se recomienda su uso.                                                                                                                 |
| [\_URL de \_ destino de medios de WPD \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [\_Descripción de medios de WPD \_](media-properties.md)                                                 | Opcional.                                                                                                                    |
| [\_género multimedia de WPD \_](media-properties.md)                                                             | Opcional.                                                                                                                    |
| [\_marcador de \_ tiempo de medio de WPD \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [\_marcador de \_ bytes multimedia de WPD \_](media-properties.md)                                            | Opcional.                                                                                                                    |
| [\_GUID de medios de WPD \_](media-properties.md)                                                               | Opcional.                                                                                                                    |
| [subdescripción de los medios de WPD \_ \_ \_](media-properties.md)                                        | Opcional.                                                                                                                    |
| [\_autor de vídeo de WPD \_](video-properties.md)                                                           | Opcional.                                                                                                                    |
| [\_nombre de \_ la \_ estación \_ RECORDEDTV de vídeo de WPD](video-properties.md)                       | Opcional.                                                                                                                    |
| [\_número de \_ canal de RECORDEDTV de vídeo de WPD \_ \_](video-properties.md)                   | Opcional.                                                                                                                    |
| [RECORDEDTV de vídeo de WPD \_ \_ \_ repite](video-properties.md)                                    | Opcional.                                                                                                                    |
| [\_tamaño del \_ búfer de vídeo de WPD \_](video-properties.md)                                                | Opcional.                                                                                                                    |
| [\_créditos de vídeo de WPD \_](video-properties.md)                                                         | Opcional.                                                                                                                    |
| [\_distancia de \_ \_ fotogramas de clave de vídeo de WPD \_](video-properties.md)                                 | Opcional.                                                                                                                    |
| [\_configuración de \_ calidad de vídeo de WPD \_](video-properties.md)                                        | Opcional.                                                                                                                    |
| [\_tipo de \_ examen de vídeo de WPD \_](video-properties.md)                                                    | Obligatorio.                                                                                                                    |
| [velocidad de bits de \_ vídeo WPD \_](video-properties.md)                                                         | Obligatorio.                                                                                                                    |
| [\_ \_ código FourCC de vídeo de WPD \_](video-properties.md)                                                | Se requiere si el códec es compatible con Microsoft vídeo para Windows (VFW), Microsoft DirectShow y el formato de Windows Media. |
| [fotogramas de vídeo de WPD \_ \_](video-properties.md)                                                     | Opcional.                                                                                                                    |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                              | Obligatorio u opcional       | Descripción                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md)     | Obligatorio.                  | Contiene los datos de vídeo (archivo).                                      |
| [**\_miniatura de recursos de WPD \_**](wpd-resource-thumbnail.md) | Recomendado, si está disponible. | Contiene el fotograma clave u otro marco de ejemplo que no esté en blanco para el vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



