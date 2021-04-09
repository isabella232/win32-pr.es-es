---
description: Especifica un tipo de recurso que no se define de otro modo en dispositivos portátiles de Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154161"
---
# <a name="wpd_resource_generic"></a>\_recursos genéricos del recurso WPD \_

Especifica un tipo de recurso que no se define de otro modo en dispositivos portátiles de Windows. Puede definir sus propios recursos personalizados que admitan cualquier atributo personalizado o dispositivos portátiles definidos por Windows. Sin embargo, cualquier recurso que cree debe admitir los siguientes atributos.



| Nombre del atributo                                                                                                            | Obligatorio u opcional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_ \_ Tamaño total del atributo de recursos de \_ WPD \_](resource-attribute-properties.md)              | Obligatorio.                                              |
| [el \_ atributo del recurso WPD \_ \_ puede \_ leer](attributes.md)                                     | Obligatorio si los clientes pueden leer este recurso.            |
| [el \_ atributo del recurso WPD \_ \_ puede \_ escribir](attributes.md)                                   | Obligatorio si los clientes pueden escribir en este recurso.        |
| [el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar](attributes.md)                                 | Obligatorio si los clientes pueden eliminar este recurso.          |
| [\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD](attributes.md)   | Obligatorio si los clientes tienen acceso de lectura al recurso.  |
| [\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD](attributes.md) | Obligatorio si los clientes tienen acceso de escritura al recurso. |
| [\_formato de \_ atributo de recurso de WPD \_](resource-attribute-properties.md)                       | Obligatorio.                                              |
| [\_clave de \_ recurso de atributo de recurso WPD \_ \_](resource-attribute-properties.md)                                              | Se recomienda su uso.                                           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Requisitos para recursos**](requirements-for-resources.md)
</dt> </dl>

 

 



