---
description: '\_servicio de \_ tipo de contenido de WPD \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002617"
---
# <a name="wpd_content_type_service"></a>\_servicio de \_ tipo de contenido de WPD \_

Objeto que describe su tipo como servicio de \_ tipo de contenido WPD \_ \_ representa un servicio de dispositivo.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                        | Obligatorio u opcional                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                               | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación. |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                | Obligatorio.                                                                      |
| [\_nombre del objeto WPD \_](object-properties.md)                                           | Es obligatorio si el objeto representa un archivo.                                      |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)         | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación. |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                   | Obligatorio si el servicio no se debe mostrar al usuario.                       |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                   | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [\_categoría de \_ objeto \_ funcional de WPD](object-properties.md) | Obligatorio. Representa el tipo de servicio de dispositivo.                             |
| [\_versión del servicio WPD \_](object-properties.md)           | Obligatorio.                                                                      |
| [\_tipo de almacenamiento de WPD \_](object-properties.md)                                                          | Obligatorio si el servicio se utiliza para almacenar objetos.                              |
| [\_capacidad de almacenamiento de WPD \_](object-properties.md)                                                      | Obligatorio si el servicio se utiliza para almacenar objetos.                              |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



