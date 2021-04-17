---
description: '\_imagen de \_ tipo de contenido de WPD \_'
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d547a6190df01f495c0a340010b4305f5c77bf5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716651"
---
# <a name="wpd_content_type_image"></a>\_imagen de \_ tipo de contenido de WPD \_

Un objeto que describe su tipo como imagen de tipo de contenido de WPD \_ \_ \_ representa una imagen fija.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                   |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                                        |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                                                        |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                   |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                                        |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                                        |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                                |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                            |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                                        |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.                            |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                          |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                                        |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                        |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                           |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                                        |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                                     |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                                        |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                       |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                                        |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                                        |
| [\_BITDEPTH de imagen de WPD \_](image-properties.md)                                                       | Se recomienda su uso.                                                                                     |
| [\_ \_ Estado recortado de imagen de WPD \_](image-properties.md)                                          | Opcional.                                                                                        |
| [\_ \_ \_ Estado corregido de color de imagen de WPD \_](image-properties.md)                         | Opcional.                                                                                        |
| [\_FNUMBER de imagen de WPD \_](image-properties.md)                                                                           | Opcional.                                                                                        |
| [tiempo de exposición de la imagen de WPD \_ \_ \_](image-properties.md)                                                                    | Opcional.                                                                                        |
| [\_Índice de \_ exposición de imagen de WPD \_](image-properties.md)                                                                   | Opcional.                                                                                        |
| [\_ \_ resolución horizontal de imagen de WPD \_](image-properties.md)                                                            | Opcional.                                                                                        |
| [\_ \_ resolución vertical de imagen de WPD \_](image-properties.md)                                                              | Opcional.                                                                                        |
| [COPYRIGHT de los medios de WPD \_ \_](media-properties.md)                                                     | Opcional.                                                                                        |
| [\_ancho de medios de WPD \_](media-properties.md)                                                             | Obligatorio.                                                                                        |
| [altura de los medios de WPD \_ \_](media-properties.md)                                                           | Obligatorio.                                                                                        |
| [\_intérprete multimedia de WPD \_](media-properties.md)                                                                            | Se recomienda su uso.                                                                                     |
| [\_intérprete del \_ álbum \_ multimedia de WPD](media-properties.md)                                                                     | Se recomienda su uso. Esta propiedad identifica la persona, o personas, que creó originalmente este objeto. |
| [\_URL de \_ origen de medios de WPD \_](media-properties.md)                                                                       | Opcional.                                                                                        |
| [\_URL de \_ destino de medios de WPD \_](media-properties.md)                                                                  | Opcional.                                                                                        |
| [\_Descripción de medios de WPD \_](media-properties.md)                                                                       | Opcional.                                                                                        |
| [\_género multimedia de WPD \_](media-properties.md)                                                                             | Opcional.                                                                                        |
| [\_marcador de \_ bytes multimedia de WPD \_](media-properties.md)                                                                    | Opcional.                                                                                        |
| [\_GUID de medios de WPD \_](media-properties.md)                                                                              | Opcional.                                                                                        |
| [subdescripción de los medios de WPD \_ \_ \_](media-properties.md)                                                                  | Opcional.                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                                 | Obligatorio u opcional | Descripción                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md)        | Obligatorio.            | Contiene los datos de la imagen.                                                                 |
| [**\_miniatura de recursos de WPD \_**](wpd-resource-thumbnail.md)    | Se recomienda su uso.         | Contiene la miniatura de la imagen.                                                    |
| [**\_clip de \_ audio de recursos de WPD \_**](wpd-resource-audio-clip.md) | Opcional.            | Si esta imagen tiene una anotación de audio asociada, este recurso contiene los datos de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



