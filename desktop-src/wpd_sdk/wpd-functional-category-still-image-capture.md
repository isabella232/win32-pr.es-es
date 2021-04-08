---
description: '\_captura de \_ imagen de categoría funcional de \_ WPD \_ \_'
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d821f1182012fbf29960fae4fc06b14ec53ecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002707"
---
# <a name="wpd_functional_category_still_image_capture"></a>\_captura de \_ imagen de categoría funcional de \_ WPD \_ \_

Un \_ \_ \_ \_ objeto funcional de captura de imagen de categoría funcional \_ de WPD encapsula la funcionalidad de captura de imágenes fijas en un dispositivo, como un archivo adjunto de cámara o cámara.



| Nombre de la propiedad                                                                                                            | Obligatorio u opcional                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                   | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                                                         |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                    | Obligatorio.                                                                                                                                              |
| [\_nombre del objeto WPD \_](object-properties.md)                                                               | Obligatorio.                                                                                                                                              |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                             | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                                                         |
| [\_formato de objeto WPD \_](object-properties.md)                                                           | Obligatorio.                                                                                                                                              |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                              | Obligatorio.                                                                                                                                              |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                       | Es obligatorio si el objeto está oculto.                                                                                                                      |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                       | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                                                  |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                               | Obligatorio si el objeto tiene al menos un recurso.                                                                                                      |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                                 | Es obligatorio si el objeto representa un archivo.                                                                                                              |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                          | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.                                                                                  |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                   | Obligatorio si el objeto tiene referencias a otros objetos.                                                                                                |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                       | Opcional.                                                                                                                                              |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                        | Opcional.                                                                                                                                              |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                     | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                                                 |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                              | Opcional.                                                                                                                                              |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                            | Se recomienda su uso.                                                                                                                                           |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                            | Opcional.                                                                                                                                              |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                   | Se recomienda si otro objeto hace referencia al objeto.                                                                                             |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)        | Opcional.                                                                                                                                              |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md)    | Opcional.                                                                                                                                              |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                        | Es obligatorio si no se puede eliminar el objeto.                                                                                                              |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                   | Opcional.                                                                                                                                              |
| [\_categoría de \_ objeto \_ funcional de WPD](miscellaneous-properties.md)                         | Obligatorio. Vea [**\_ \_ \_ \_ objeto funcional de tipo de contenido de WPD**](wpd-content-type-functional-object.md) para las categorías definidas por dispositivos portátiles de Windows. |
| [la resolución de captura de imagen de WPD \_ sigue siendo \_ \_ \_](still-image-properties.md)                  | Obligatorio.                                                                                                                                              |
| [\_formato de \_ captura de imagen \_ \_ de WPD](still-image-properties.md)                          | Obligatorio.                                                                                                                                              |
| [\_configuración de \_ compresión de imagen \_ \_ de WPD](still-image-properties.md)                | Opcional.                                                                                                                                              |
| [\_ \_ \_ equilibrio en blanco de la imagen de WPD \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [\_ganancia de \_ Image \_ RGB de imagen fija \_](still-image-properties.md)                                      | Opcional.                                                                                                                                              |
| [\_ \_ \_ FNUMBER Image](still-image-properties.md)                                         | Opcional.                                                                                                                                              |
| [la \_ \_ \_ \_ longitud focal de la imagen de WPD sigue siendo](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [la \_ \_ distancia del \_ foco \_ de la imagen de WPD](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [\_modo de \_ enfoque de imagen \_ \_ de WPD](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [\_modo de \_ medición de exposición de imagen \_ de \_ WPD \_](still-image-properties.md)         | Opcional.                                                                                                                                              |
| [\_modo de \_ imagen \_ del \_ modo Flash de WPD](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [tiempo de exposición de la \_ \_ imagen de WPD \_ \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [\_modo de \_ programa de exposición de imagen \_ \_ de WPD \_](still-image-properties.md)           | Opcional.                                                                                                                                              |
| [\_Índice de \_ exposición de imagen \_ \_ de WPD](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [compensación de la \_ \_ tendencia de exposición de imagen \_ \_ \_ de WPD](still-image-properties.md) | Opcional.                                                                                                                                              |
| [\_retraso de \_ captura de imagen \_ \_ de WPD](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [\_modo de \_ captura de imagen \_ \_ de WPD](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [contraste de la imagen de WPD \_ \_ \_](still-image-properties.md)                                       | Opcional.                                                                                                                                              |
| [la nitidez de la imagen de WPD \_ sigue siendo \_ \_](still-image-properties.md)                                     | Opcional.                                                                                                                                              |
| [el \_ \_ \_ zoom digital Image \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [\_modo de \_ efecto de imagen \_ \_ de WPD](still-image-properties.md)                                | Opcional.                                                                                                                                              |
| [\_número de \_ ráfaga de imagen \_ \_ de WPD](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [\_intervalo de \_ ráfaga de imagen \_ \_ de WPD](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [número de TIMELAPSE de la \_ \_ imagen de WPD \_ \_](still-image-properties.md)                      | Opcional.                                                                                                                                              |
| [\_ \_ \_ intervalo TIMELAPSE de la imagen de WPD \_](still-image-properties.md)                  | Opcional.                                                                                                                                              |
| [\_modo de \_ medición de foco de imagen \_ de \_ WPD \_](still-image-properties.md)               | Opcional.                                                                                                                                              |
| [\_URL de \_ carga de imagen \_ \_ de WPD](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [el \_ intérprete de imágenes de la imagen de WPD \_ \_](still-image-properties.md)                                           | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

Muchas de estas propiedades tienen efectos interconectados. Por ejemplo, si el **modo de medición de exposición de imagen de WPD \_ sigue \_ \_ \_ \_ siendo** automático, se vinculará el valor de detención de f, tiempo de exposición y exposición; la variación de la misma hará que los demás varíen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de contenido de \_ WPD \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



