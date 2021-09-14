---
description: SERVICIO DE TIPO \_ \_ DE CONTENIDO \_ WPD
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262060"
---
# <a name="wpd_content_type_service"></a>SERVICIO DE TIPO \_ \_ DE CONTENIDO \_ WPD

Objeto que describe su tipo como WPD \_ CONTENT TYPE SERVICE representa un servicio de \_ \_ dispositivo.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                        | Obligatorio u opcional                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                               | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                | Necesario.                                                                      |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                           | Obligatorio si el objeto representa un archivo.                                      |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)         | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                   | Obligatorio si el servicio no se debe mostrar al usuario.                       |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                   | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE \_ WPD](object-properties.md) | Necesario. Representa el tipo de servicio del dispositivo.                             |
| [VERSIÓN DEL \_ SERVICIO \_ WPD](object-properties.md)           | Necesario.                                                                      |
| [TIPO DE \_ ALMACENAMIENTO \_ WPD](object-properties.md)                                                          | Obligatorio si el servicio se usa para almacenar objetos.                              |
| [CAPACIDAD DE \_ ALMACENAMIENTO DE \_ WPD](object-properties.md)                                                      | Obligatorio si el servicio se usa para almacenar objetos.                              |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



