---
description: tipo de contenido de WPD ( \_ \_ \_ audio)
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83d43fcef539579fc0a687a97ba51e52278e4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706864"
---
# <a name="wpd_content_type_audio"></a>tipo de contenido de WPD ( \_ \_ \_ audio)

Un objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ audio representa un archivo de audio, como un archivo Windows Media Audio (WMA) o MP3.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.     |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                          |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                                          |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.     |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                          |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                          |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                  |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).              |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                  |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                          |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.              |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                            |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                          |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                          |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                             |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                          |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                       |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                          |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                         |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                          |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                          |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                     | Obligatorio si el objeto se puede eliminar.                                             |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                          |
| [\_velocidad de \_ bits total de medios de WPD \_](media-properties.md)                                            | Se recomienda su uso.                                                                       |
| [\_tipo de \_ velocidad de bits de medios de WPD \_](media-properties.md)                                              | Opcional.                                                                          |
| [COPYRIGHT de los medios de WPD \_ \_](media-properties.md)                                                     | Opcional.                                                                          |
| [\_ \_ \_ ID. de contenido de suscripción de medios de WPD \_](media-properties.md)                       | Se recomienda si este objeto representa el contenido de un servicio de suscripción en línea. |
| [recuento de uso de medios de WPD \_ \_ \_](media-properties.md)                                                    | Se recomienda su uso.                                                                       |
| [recuento de omisiones de medios de WPD \_ \_ \_](media-properties.md)                                                  | Opcional.                                                                          |
| [\_ \_ última hora de \_ acceso a los medios \_ de WPD](media-properties.md)                                 | Opcional.                                                                          |
| [\_ \_ clasificación parental de medios de \_ WPD](media-properties.md)                                        | Opcional.                                                                          |
| [metagénero de multimedia de WPD \_ \_ \_](media-properties.md)                                                  | Opcional.                                                                          |
| [\_compositor de medios de WPD \_](media-properties.md)                                                       | Opcional.                                                                          |
| [\_ \_ clasificación efectiva de medios de WPD \_](media-properties.md)                                      | Opcional.                                                                          |
| [subtítulo de medios de WPD \_ \_ \_](media-properties.md)                                                    | Opcional.                                                                          |
| [\_fecha de \_ lanzamiento de medios de WPD \_](media-properties.md)                                              | Se recomienda su uso.                                                                       |
| [\_velocidad de \_ muestra \_ multimedia de WPD](media-properties.md)                                                | Opcional.                                                                          |
| [\_clasificación de media \_ Star \_ de WPD](media-properties.md)                                                | Se recomienda su uso.                                                                       |
| [\_ \_ \_ clasificación efectiva del usuario \_ de los medios de WPD](media-properties.md)                           | Se recomienda su uso.                                                                       |
| [título de los medios de WPD \_ \_](media-properties.md)                                                             | Obligatorio.                                                                          |
| [duración de los medios de WPD \_ \_](media-properties.md)                                                       | Obligatorio.                                                                          |
| [\_compra multimedia \_ WPD \_ Now](media-properties.md)                                                        | Se recomienda su uso.                                                                       |
| [\_Perfil de \_ codificación multimedia \_ WPD](media-properties.md)                                      | Opcional.                                                                          |
| [\_intérprete multimedia de WPD \_](media-properties.md)                                                                            | Se recomienda su uso.                                                                       |
| [\_intérprete del \_ álbum \_ multimedia de WPD](media-properties.md)                                                                     | Se recomienda su uso.                                                                       |
| [\_URL de \_ origen de medios de WPD \_](media-properties.md)                                                                       | Opcional.                                                                          |
| [\_URL de \_ destino de medios de WPD \_](media-properties.md)                                                                  | Opcional.                                                                          |
| [\_Descripción de medios de WPD \_](media-properties.md)                                                                       | Opcional.                                                                          |
| [\_género multimedia de WPD \_](media-properties.md)                                                                             | Opcional.                                                                          |
| [\_marcador de \_ tiempo de medio de WPD \_](media-properties.md)                                                                    | Opcional.                                                                          |
| [\_marcador de \_ bytes multimedia de WPD \_](media-properties.md)                                                                    | Opcional.                                                                          |
| [\_GUID de medios de WPD \_](media-properties.md)                                                                              | Opcional.                                                                          |
| [subdescripción de los medios de WPD \_ \_ \_](media-properties.md)                                                                  | Opcional.                                                                          |
| [\_álbum de música de WPD \_](music-properties.md)                                                             | Se recomienda su uso.                                                                       |
| [\_pista de música de WPD \_](music-properties.md)                                                             | Se recomienda su uso.                                                                       |
| [\_Letras de música de WPD \_](music-properties.md)                                                           | Opcional.                                                                          |
| [\_ánimo de música de WPD \_](music-properties.md)                                                               | Opcional.                                                                          |
| [velocidad de bits de \_ audio WPD \_](audio-properties.md)                                                         | Se recomienda su uso.                                                                       |
| [recuento de canales de audio de WPD \_ \_ \_](audio-properties.md)                                            | Opcional.                                                                          |
| [\_código de \_ formato de audio de WPD \_](audio-properties.md)                                                | Opcional.                                                                          |
| [\_profundidad de \_ bits de audio de WPD \_](audio-properties.md)                                                    | Opcional.                                                                          |
| [\_alineación del \_ bloque de audio de WPD \_](audio-properties.md)                                        | Opcional.                                                                          |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                               | Obligatorio u opcional       | Descripción                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md)      | Opcional.                  | Contiene el archivo de audio completo.                  |
| [**\_carátula de \_ álbum de recursos de WPD \_**](wpd-resource-album-art.md) | Recomendado, si está disponible. | Contiene la imagen del álbum.                |
| [**\_AUDIOCLIP de recursos de WPD \_**](wpd-resource-audio-clip.md) | Opcional.                  | Contiene un clip de ejemplo del archivo de audio completo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



