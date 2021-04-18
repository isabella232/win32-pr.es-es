---
description: '\_ \_ archivo genérico de tipo de contenido de \_ WPD \_'
ms.assetid: e652bebc-fb3d-48cd-af59-3ad97a79711d
title: WPD_CONTENT_TYPE_GENERIC_FILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8575eba29f5b4b92570f6ee8e39a4ad6405ebf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716653"
---
# <a name="wpd_content_type_generic_file"></a>\_ \_ archivo genérico de tipo de contenido de \_ WPD \_

Objeto que describe su tipo como \_ archivo genérico de tipo de contenido de WPD \_ \_ \_ representa un objeto genérico con un archivo físico subyacente. La diferencia entre este tipo y el tipo de contenido de WPD sin \_ \_ \_ especificar es que un objeto no especificado es más genérico y no es necesario tener un archivo subyacente. Este tipo de objeto se puede crear para contener datos de un tipo no especificado que el dispositivo no está diseñado para consumir.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación. |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                      |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                                      |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación. |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                      |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                      |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                              |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                              |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                      |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.          |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                        |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                      |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                      |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                         |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                      |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                   |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                      |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                     |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                      |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                      |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                     | Es obligatorio si no se puede eliminar el objeto.                                      |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                          | Obligatorio u opcional | Descripción             |
|--------------------------------------------------------|----------------------|-------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md) | Obligatorio.            | Contiene los datos del archivo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



