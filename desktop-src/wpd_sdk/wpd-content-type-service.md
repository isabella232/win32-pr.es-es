---
description: SERVICIO DE TIPO \_ DE \_ CONTENIDO \_ WPD
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc302c8bf884b58cab092a0a0e87a79f556b3b8178df0628622e2c3a323d49f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703925"
---
# <a name="wpd_content_type_service"></a>SERVICIO DE TIPO \_ DE \_ CONTENIDO \_ WPD

Un objeto que describe su tipo como WPD \_ CONTENT TYPE SERVICE representa un servicio de \_ \_ dispositivo.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                        | Obligatorio u opcional                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                               | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                | Obligatorio.                                                                      |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                           | Obligatorio si el objeto representa un archivo.                                      |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)         | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                   | Obligatorio si el servicio no se debe mostrar al usuario.                       |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                   | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE WPD \_](object-properties.md) | Obligatorio. Representa el tipo de servicio de dispositivo.                             |
| [VERSIÓN DEL SERVICIO WPD \_ \_](object-properties.md)           | Obligatorio.                                                                      |
| [TIPO DE \_ ALMACENAMIENTO WPD \_](object-properties.md)                                                          | Obligatorio si el servicio se usa para almacenar objetos.                              |
| [CAPACIDAD DE \_ ALMACENAMIENTO DE \_ WPD](object-properties.md)                                                      | Obligatorio si el servicio se usa para almacenar objetos.                              |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



