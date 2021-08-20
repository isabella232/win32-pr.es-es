---
description: Especifica si este es el perfil predeterminado del dispositivo.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Elemento IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: 7dada4789b0a1c1f11676359972eeff074928ca064c04679e35fb7e83132ef53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065909"
---
# <a name="isdefault-mbnprofile-element"></a>Elemento IsDefault (MBNProfile)

El **elemento IsDefault (MBNProfile)** especifica si este es el perfil predeterminado del dispositivo.

Se trata de un elemento opcional y, si no se especifica, el perfil no se establecerá como perfil predeterminado.

El servicio banda ancha móvil usa el perfil predeterminado para los siguientes fines:

-   El servicio banda ancha móvil usa la configuración de conexión del perfil predeterminado al realizar conexiones de red automáticas. Esta configuración incluye el nombre del punto de acceso, el nombre de usuario, la contraseña, etc.
-   La directiva de conexión automática para un dispositivo de banda ancha móvil se toma del perfil predeterminado.
-   La interfaz de usuario de conexión de red del sistema operativo también usa datos de conexión del perfil predeterminado para las operaciones de conexión.

Los proveedores de servicios móviles pueden proporcionar los detalles de conexión en un perfil y configurar ese perfil como perfil predeterminado. El servicio banda ancha móvil usará esta configuración de conexión sin pedir detalles al usuario.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

El **elemento IsDefault** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




