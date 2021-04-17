---
description: '\_contacto del \_ tipo de contenido de WPD \_'
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fed10e0abb36a482141e5c796f5494b00b99f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706861"
---
# <a name="wpd_content_type_contact"></a>\_contacto del \_ tipo de contenido de WPD \_

Un objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ contacto representa datos de contacto personales.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                                   | Obligatorio u opcional                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación. |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                           | Obligatorio.                                                                      |
| [\_nombre del objeto WPD \_](object-properties.md)                                                                      | Es obligatorio si el objeto representa un archivo.                                      |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                                    | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación. |
| [\_formato de objeto WPD \_](object-properties.md)                                                                  | Obligatorio.                                                                      |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                                     | Obligatorio.                                                                      |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                              | Es obligatorio si el objeto está oculto.                                              |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                              | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                                      | Obligatorio si el objeto tiene al menos un recurso.                              |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                                        | Es obligatorio si el objeto representa un archivo.                                      |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                                 | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.          |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                          | Obligatorio si el objeto tiene referencias a otros objetos.                        |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                              | Opcional.                                                                      |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                               | Opcional.                                                                      |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                            | Obligatorio si el objeto está protegido por la tecnología DRM.                         |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                                     | Opcional.                                                                      |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                                   | Se recomienda su uso.                                                                   |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                                   | Opcional.                                                                      |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                          | Se recomienda si otro objeto hace referencia al objeto.                     |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)               | Opcional.                                                                      |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md)           | Opcional.                                                                      |
| [\_nombre para \_ Mostrar del contacto de WPD \_](contact-properties.md)                                                  | Obligatorio.                                                                      |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                               | Es obligatorio si no se puede eliminar el objeto.                                      |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                          | Opcional.                                                                      |
| [\_nombre para \_ Mostrar del contacto de WPD \_](contact-properties.md)                                                                           | Obligatorio.                                                                      |
| [\_nombre de contacto de WPD \_ \_](contact-properties.md)                                                      | Se recomienda su uso.                                                                   |
| [\_nombres de \_ los centros de contacto de WPD \_](contact-properties.md)                                                  | Se recomienda su uso.                                                                   |
| [\_apellido del contacto de WPD \_ \_](contact-properties.md)                                                        | Se recomienda su uso.                                                                   |
| [prefijo del contacto de WPD \_ \_](contact-properties.md)                                                               | Se recomienda su uso.                                                                   |
| [\_sufijo del contacto de WPD \_](contact-properties.md)                                                               | Se recomienda su uso.                                                                   |
| [\_ \_ nombre fonético del contacto de \_ WPD \_](contact-properties.md)                                   | Opcional.                                                                      |
| [\_ \_ Apellido fonético del contacto de \_ WPD \_](contact-properties.md)                                     | Opcional.                                                                      |
| [\_ \_ \_ \_ dirección postal completa personal del contacto de WPD \_](contact-properties.md)                | Se recomienda su uso.                                                                   |
| [\_ \_ Dirección postal personal del contacto de WPD \_ \_ \_ línea1](contact-properties.md)              | Opcional.                                                                      |
| [\_ \_ Dirección postal personal del contacto de WPD- \_ \_ \_ línea2](contact-properties.md)              | Opcional.                                                                      |
| [\_ciudad de \_ \_ dirección postal \_ personal \_ del contacto de WPD](contact-properties.md)                | Opcional.                                                                      |
| [\_región de \_ \_ dirección postal \_ personal \_ del contacto de WPD](contact-properties.md)            | Opcional.                                                                      |
| [\_código postal de la \_ \_ \_ dirección postal personal \_ \_ del contacto de WPD](contact-properties.md) | Opcional.                                                                      |
| [\_país de \_ la \_ dirección postal personal \_ del contacto \_ de WPD](contact-properties.md)          | Opcional.                                                                      |
| [\_ \_ \_ \_ dirección postal completa del negocio de WPD \_](contact-properties.md)                | Opcional.                                                                      |
| [\_ \_ \_ Dirección postal del negocio \_ de \_ WPD](contact-properties.md)              | Opcional.                                                                      |
| [\_Dirección del \_ \_ correo postal \_ del \_ negocio de WPD](contact-properties.md)              | Opcional.                                                                      |
| [\_ciudad de \_ \_ dirección postal \_ comercial \_ del contacto de WPD](contact-properties.md)                | Opcional.                                                                      |
| [\_región de \_ \_ dirección postal \_ comercial \_ del contacto de WPD](contact-properties.md)            | Opcional.                                                                      |
| [\_código postal de la \_ \_ \_ dirección postal comercial \_ \_ del contacto de WPD](contact-properties.md) | Opcional.                                                                      |
| [\_país de \_ la \_ dirección postal comercial \_ del contacto \_ de WPD](contact-properties.md)          | Opcional.                                                                      |
| [el \_ contacto de WPD con \_ otra \_ \_ dirección postal completa \_](contact-properties.md)                      | Opcional.                                                                      |
| [El \_ contacto de WPD con \_ otra \_ \_ dirección postal \_ línea1](contact-properties.md)                    | Opcional.                                                                      |
| [El \_ contacto de WPD con \_ otra \_ \_ dirección postal \_ línea2](contact-properties.md)                    | Opcional.                                                                      |
| [\_ciudad de contacto con \_ otra \_ \_ dirección postal \_](contact-properties.md)                      | Opcional.                                                                      |
| [el \_ contacto de WPD con \_ otra \_ región de \_ dirección postal \_](contact-properties.md)                  | Opcional.                                                                      |
| [\_código postal de la \_ \_ \_ dirección \_ postal del contacto \_ de WPD](contact-properties.md)       | Opcional.                                                                      |
| [el \_ contacto de WPD con \_ otro \_ \_ \_ país postal de dirección postal \_](contact-properties.md) | Opcional.                                                                      |
| [\_dirección de \_ \_ correo electrónico \_ principal del contacto de WPD](contact-properties.md)                               | Se recomienda su uso.                                                                   |
| [\_ \_ correo electrónico personal del contacto de WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [EMAIL2 de contacto de WPD \_ \_ personal \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_ \_ correo electrónico empresarial del contacto de WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [\_EMAIL2 de \_ negocio del contacto de WPD \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_correo electrónico de WPD en \_ otros \_ correos electrónicos](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_ \_ teléfono principal del contacto de WPD \_](contact-properties.md)                                                | Se recomienda su uso.                                                                   |
| [\_ \_ teléfono personal del contacto de WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [Phone2 de contacto de WPD \_ \_ personal \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_teléfono del \_ trabajo del contacto de WPD \_](contact-properties.md)                                              | Opcional.                                                                      |
| [\_Phone2 de \_ negocio del contacto de WPD \_](contact-properties.md)                                            | Opcional.                                                                      |
| [\_ \_ teléfono móvil del contacto de WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_ \_ Phone2 Mobile del contacto de WPD \_](contact-properties.md)                                                | Opcional.                                                                      |
| [\_ \_ Fax personal de el contacto de WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_ \_ fax empresarial del contacto de WPD \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_buscapersonas de contacto de WPD \_](contact-properties.md)                                                                 | Opcional.                                                                      |
| [\_ponerse en contacto con \_ otros \_ teléfonos](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_ \_ \_ dirección web principal del contacto de WPD \_](contact-properties.md)                                   | Se recomienda su uso.                                                                   |
| [\_ \_ \_ dirección web personal del contacto de WPD \_](contact-properties.md)                                 | Opcional.                                                                      |
| [\_ \_ \_ dirección web empresarial de contacto de WPD \_](contact-properties.md)                                 | Opcional.                                                                      |
| [\_ponerse en contacto con \_ Instant \_ Messenger](contact-properties.md)                                        | Recomendado                                                                    |
| [\_MESSENGER2 de contacto \_ instantáneo \_ de WPD](contact-properties.md)                                      | Opcional.                                                                      |
| [\_MESSENGER3 de contacto \_ instantáneo \_ de WPD](contact-properties.md)                                      | Opcional.                                                                      |
| [nombre de la empresa del contacto de WPD \_ \_ \_](contact-properties.md)                                                  | Opcional.                                                                      |
| [\_nombre de \_ la \_ compañía \_ fonética del contacto de WPD](contact-properties.md)                               | Opcionales                                                                       |
| [\_rol de contacto de WPD \_](contact-properties.md)                                                                   | Opcional.                                                                      |
| [\_FechaNacimiento de contacto de WPD \_](contact-properties.md)                                                         | Opcional.                                                                      |
| [\_ \_ fax principal del contacto de WPD \_](contact-properties.md)                                                                            | Opcional.                                                                      |
| [\_cónyuge del contacto de WPD \_](contact-properties.md)                                                                                  | Opcional.                                                                      |
| [\_secundarios de contacto de WPD \_](contact-properties.md)                                                                                | Opcional.                                                                      |
| [\_Asistente para contactos de WPD \_](contact-properties.md)                                                                               | Opcional.                                                                      |
| [\_fecha de \_ aniversario del contacto de WPD \_](contact-properties.md)                                                                       | Opcional.                                                                      |
| [\_tono de contacto de WPD \_](contact-properties.md)                                                                                | Opcional.                                                                      |
| [\_notas de \_ información \_ común de WPD](object-properties.md)                                                                        | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                                       | Obligatorio u opcional       | Descripción                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md)              | Opcional.                  | Contiene los datos de contacto.         |
| [**\_foto de \_ contacto de recursos de WPD \_**](wpd-resource-contact-photo.md) | Recomendado, si está disponible. | Contiene una imagen del contacto. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



