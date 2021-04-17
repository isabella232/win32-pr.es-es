---
description: '\_álbum de \_ imagen del tipo de contenido de WPD \_ \_'
ms.assetid: e2ae9f89-5a71-4443-b0c1-81e4c650e1bb
title: WPD_CONTENT_TYPE_IMAGE_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67a20f6a6628008e31b23a0ceb05fee4931793a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716652"
---
# <a name="wpd_content_type_image_album"></a>\_álbum de \_ imagen del tipo de contenido de WPD \_ \_

Objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ \_ álbum de imagen representa una colección de imágenes fijas. Un álbum de imagen es equivalente funcionalmente a una lista de reproducción de archivos de imagen, pero se usa para representar un álbum de fotos físico para el usuario final.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                              |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.    |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                         |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                                         |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad incluso en el momento de la creación.     |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                         |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                         |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                 |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (es decir, representa un archivo del sistema). |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                 |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                         |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.             |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                           |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                         |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                         |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                            |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                         |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                      |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                         |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                        |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                         |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcionales                                                                          |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                     | Es obligatorio si no se puede eliminar el objeto.                                         |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                         |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



