---
description: '\_ \_ correo electrónico de tipo de contenido de WPD \_'
ms.assetid: 96f81477-5ec9-49c1-987a-348a92a7e638
title: WPD_CONTENT_TYPE_EMAIL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0cb274fdd4b4e9bd3e4d02d20afeda1ef871143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546451"
---
# <a name="wpd_content_type_email"></a>\_ \_ correo electrónico de tipo de contenido de WPD \_

Un objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ correo electrónico representa un correo electrónico.

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
| [\_asunto de \_ información \_ común de WPD](object-properties.md)                                                            | Obligatorio.                                                                      |
| [\_ \_ \_ texto del cuerpo de información común de WPD \_](object-properties.md)                                                         | Se recomienda su uso.                                                                   |
| [\_prioridad de \_ información \_ común de WPD](object-properties.md)                                                           | Se recomienda su uso.                                                                   |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                      |
| [\_correo electrónico \_ de WPD en \_ línea](email-properties.md)                                                        | Obligatorio.                                                                      |
| [\_línea CC de correo electrónico de WPD \_ \_](email-properties.md)                                                        | Opcional.                                                                      |
| [\_línea CCO de correo electrónico de WPD \_ \_](email-properties.md)                                                      | Opcional.                                                                      |
| [se \_ ha \_ \_ leído el correo electrónico de WPD \_](email-properties.md)                                           | Opcional.                                                                      |
| [\_hora de recepción de correo electrónico de WPD \_ \_](email-properties.md)                                            | Opcional.                                                                      |
| [el \_ correo electrónico de WPD \_ tiene \_ datos adjuntos](email-properties.md)                                        | Opcional.                                                                      |
| [\_dirección del remitente de correo electrónico de WPD \_ \_](email-properties.md)                                          | Obligatorio.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



