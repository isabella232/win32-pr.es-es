---
description: '\_ \_ mensaje genérico de tipo de contenido de \_ WPD \_'
ms.assetid: 8e58d15f-ee51-42c2-9d8b-6c3b9c730ff4
title: WPD_CONTENT_TYPE_GENERIC_MESSAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febde68787366dc0f84b1b187f1393017ceb9c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361078"
---
# <a name="wpd_content_type_generic_message"></a>\_ \_ mensaje genérico de tipo de contenido de \_ WPD \_

Un objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ \_ mensaje genérico representa un mensaje, por ejemplo, SMS, correo electrónico, etc.

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
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                     | Se recomienda si otro objeto hace referencia al objeto.                     |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                      |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                      |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                               | Obligatorio si el objeto se puede eliminar.                                         |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                          | Obligatorio u opcional                                  | Descripción        |
|--------------------------------------------------------|-------------------------------------------------------|--------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md) | Obligatorio si el objeto es compatible con los datos binarios. | Contiene los datos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



