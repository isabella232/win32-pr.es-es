---
description: Representa un evento de modificación de clase, que es un tipo de evento intrínseco que se genera cuando se cambia una clase en el espacio de nombres.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: __ClassModificationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706475"
---
# <a name="__classmodificationevent-class"></a>\_\_Clase ClassModificationEvent

La clase del sistema **\_ \_ ClassModificationEvent** representa un evento de modificación de clase, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se cambia una clase en el espacio de nombres.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ ClassModificationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ ClassModificationEvent** tiene estas propiedades.

<dl> <dt>

**PreviousClass**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la versión original de la clase.

</dd> <dt>

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

Copia de la clase recién modificada indicada por el evento de modificación de clase. Esta propiedad se hereda de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información está en el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ ClassModificationEvent** se deriva de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

El evento informa de las versiones nuevas y antiguas de la definición de clase.

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

 

