---
description: Representa un evento de creación de clase, que es un tipo de evento intrínseco que se genera cuando se agrega una nueva clase al espacio de nombres.
ms.assetid: a946a8eb-498c-4104-b80f-e520b0e62e36
ms.tgt_platform: multiple
title: __ClassCreationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 18994ee7067e44a9199de9b62f7ff278a8bece00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706477"
---
# <a name="__classcreationevent-class"></a>\_\_Clase ClassCreationEvent

La clase del sistema **\_ \_ ClassCreationEvent** representa un evento de creación de clase, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se agrega una nueva clase al espacio de nombres.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __ClassCreationEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ ClassCreationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ ClassCreationEvent** tiene estas propiedades.

<dl> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetClass**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la clase recién creada que se muestra en el evento de creación de clases. Esta propiedad se hereda de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información está en el formato de coordenadas de hora universal (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ ClassCreationEvent** se deriva de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ClassOperationEvent**](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

