---
description: '\_dispositivo de \_ categoría \_ funcional de WPD'
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb179311af5fb3c3eef063157e3615b21eeb66a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668281"
---
# <a name="wpd_functional_category_device"></a>\_dispositivo de \_ categoría \_ funcional de WPD

Un \_ \_ \_ objeto funcional de dispositivo de categoría funcional de WPD encapsula el dispositivo (es decir, el objeto de nivel superior del dispositivo). Si un dispositivo implementa esta categoría funcional, debe admitir estas propiedades, además de las que se enumeran para el [objeto de dispositivo](device-object.md).



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                      |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                                                           |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Obligatorio.                                                                                                           |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                      |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                                                           |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                                                           |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                                                   |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                               |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                   |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                                                           |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.                                               |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                             |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                                                           |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                           |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                              |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                                                           |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                                                        |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                                                           |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                          |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                                                           |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                                                           |
| [\_categoría de \_ objeto \_ funcional de WPD](miscellaneous-properties.md)                      | Obligatorio.                                                                                                           |
| [\_asociado de \_ sincronización de dispositivos de WPD \_](device-properties.md)                                           | Opcional.                                                                                                           |
| [\_versión de \_ firmware del dispositivo WPD \_](device-properties.md)                                   | Obligatorio.                                                                                                           |
| [\_nivel de \_ energía del dispositivo WPD \_](device-properties.md)                                             | Recomendado si el dispositivo tiene una batería.                                                                                |
| [\_fuente de \_ alimentación del dispositivo de WPD \_](device-properties.md)                                           | Se recomienda su uso.                                                                                                        |
| [\_Protocolo de dispositivo WPD \_](device-properties.md)                                                    | Se recomienda su uso.                                                                                                        |
| [\_ \_ fabricante del dispositivo WPD](device-properties.md)                                            | Obligatorio.                                                                                                           |
| [\_modelo de dispositivo de WPD \_](device-properties.md)                                                          | Obligatorio.                                                                                                           |
| [\_número de \_ serie del dispositivo WPD \_](device-properties.md)                                         | Obligatorio.                                                                                                           |
| [el \_ dispositivo WPD \_ admite valores \_ no \_ consumibles](device-properties.md)                    | Requerido si el dispositivo admite objetos no consumibles; es decir, si el dispositivo se puede usar para el almacenamiento de datos simple. |
| [\_ \_ fecha y hora del dispositivo WPD](device-properties.md)                                                    | Opcional.                                                                                                           |
| [\_ \_ nombre descriptivo del dispositivo WPD \_](device-properties.md)                                         | Se recomienda su uso.                                                                                                        |
| [\_ \_ \_ esquemas DRM admitidos por el dispositivo WPD \_](device-properties.md)                        | Se recomienda si el dispositivo es compatible con la tecnología DRM.                                                                  |
| [los \_ \_ formatos admitidos del dispositivo WPD \_ \_ están \_ ordenados](device-properties.md)       | Se recomienda si el dispositivo admite el orden de formato preferido.                                                       |
| [\_tipo de dispositivo WPD \_](device-properties.md)                                                            | Se recomienda su uso.                                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de contenido de \_ WPD \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



