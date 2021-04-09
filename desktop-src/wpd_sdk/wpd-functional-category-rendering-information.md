---
description: '\_información de \_ representación de categoría funcional \_ de WPD \_'
ms.assetid: 84ec6f14-fe90-42a5-ba2b-6c4cc406935c
title: WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf2a5b981b75820b566e3133faab22c2f35860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002612"
---
# <a name="wpd_functional_category_rendering_information"></a>\_información de \_ representación de categoría funcional \_ de WPD \_

Un \_ \_ \_ objeto funcional información de representación de una categoría funcional de WPD \_ describe el tipo de archivos multimedia que el dispositivo puede representar.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                                                         |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                                                                                              |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Obligatorio.                                                                                                                                              |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                                                         |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                                                                                              |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                                                                                              |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                                                                                      |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                                                  |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                                                      |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                                                                                              |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.                                                                                  |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                                                                |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                                                                                              |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                                                              |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                                                 |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                                                                                              |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                                                                                           |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                                                                                              |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                                                             |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                                                                                              |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                                                                                              |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                     | Es obligatorio si no se puede eliminar el objeto.                                                                                                              |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [\_categoría de \_ objeto \_ funcional de WPD](miscellaneous-properties.md)                      | Obligatorio. Vea [**\_ \_ \_ \_ objeto funcional de tipo de contenido de WPD**](wpd-content-type-functional-object.md) para las categorías definidas por dispositivos portátiles de Windows. |
| [perfiles de información de representación de WPD \_ \_ \_](miscellaneous-properties.md)              | Obligatorio.                                                                                                                                              |
| [\_tipo de entrada de Perfil de información de representación de WPD \_ \_ \_ \_](miscellaneous-properties.md)                                     | Opcional.                                                                                                                                              |
| [\_ \_ \_ \_ \_ recurso creatable de entrada de Perfil de información de representación \_ de WPD](miscellaneous-properties.md)                      | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de contenido de \_ WPD \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



