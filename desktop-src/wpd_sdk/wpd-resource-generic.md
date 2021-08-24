---
description: Especifica un tipo de recurso no definido de otro modo por Windows portables.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c418299474373d8b960d15c429ea98d887cc404be49c8d38c7d2bb83611c4ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805875"
---
# <a name="wpd_resource_generic"></a>WPD \_ RESOURCE \_ GENERIC

Especifica un tipo de recurso no definido de otro modo por Windows portables. Puede definir sus propios recursos personalizados que admitan cualquier atributo personalizado Windows definido por dispositivos portátiles. Sin embargo, cualquier recurso que cree debe admitir los atributos siguientes.



| Nombre del atributo                                                                                                            | Obligatorio u opcional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [TAMAÑO TOTAL DEL \_ ATRIBUTO \_ DE RECURSO \_ \_ WPD](resource-attribute-properties.md)              | Obligatorio.                                              |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ LEER](attributes.md)                                     | Obligatorio si los clientes pueden leer este recurso.            |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ ESCRIBIR](attributes.md)                                   | Obligatorio si los clientes pueden escribir en este recurso.        |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ ELIMINAR](attributes.md)                                 | Obligatorio si los clientes pueden eliminar este recurso.          |
| [TAMAÑO ÓPTIMO DEL BÚFER DE LECTURA \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ \_ \_ WPD](attributes.md)   | Obligatorio si los clientes tienen acceso de lectura al recurso.  |
| [TAMAÑO ÓPTIMO DEL BÚFER DE ESCRITURA \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ \_ \_ WPD](attributes.md) | Obligatorio si los clientes tienen acceso de escritura al recurso. |
| [FORMATO DE ATRIBUTO \_ DE \_ RECURSO \_ WPD](resource-attribute-properties.md)                       | Obligatorio.                                              |
| [CLAVE DE RECURSO \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ WPD](resource-attribute-properties.md)                                              | Se recomienda su uso.                                           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Requisitos de recursos**](requirements-for-resources.md)
</dt> </dl>

 

 



