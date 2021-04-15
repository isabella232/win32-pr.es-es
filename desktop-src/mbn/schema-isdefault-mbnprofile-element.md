---
description: Especifica si este es el perfil predeterminado para el dispositivo.
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
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497374"
---
# <a name="isdefault-mbnprofile-element"></a>Elemento IsDefault (MBNProfile)

El elemento **IsDefault (MBNProfile)** especifica si este es el perfil predeterminado para el dispositivo.

Este es un elemento opcional y, si no se especifica, el perfil no se establecerá como el perfil predeterminado.

El servicio de banda ancha móvil usa el perfil predeterminado para los siguientes fines

-   El servicio de banda ancha móvil usa la configuración de conexión del perfil predeterminado al realizar conexiones de red automáticas. Esta configuración incluye el nombre del punto de acceso, el nombre de usuario, la contraseña, etc.
-   La Directiva de conexión automática para un dispositivo de banda ancha móvil se toma del perfil predeterminado.
-   La interfaz de usuario de conexión de red del sistema operativo también usa datos de conexión del perfil predeterminado para las operaciones de conexión.

Los proveedores de servicios móviles pueden proporcionar los detalles de conexión en un perfil y configurarlos como perfil predeterminado. El servicio de banda ancha móvil usará esta configuración de conexión sin preguntar al usuario.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

El elemento **IsDefault** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

 




