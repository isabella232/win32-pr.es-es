---
description: Es una clase base para todos los eventos intrínsecos relacionados con una clase.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: __ClassOperationEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 52ff5854d5510b22eaf264bcdbbfd39bbb02c7d2a2766eb3fbd8f336bd0b8074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860615"
---
# <a name="__classoperationevent-class"></a>\_\_Clase ClassOperationEvent

La **\_ \_ clase del sistema ClassOperationEvent** es una clase base para todos los eventos intrínsecos relacionados con una clase.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase ClassOperationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase ClassOperationEvent** tiene estas propiedades.

<dl> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
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

Clase afectada por el evento . Para los eventos de creación, se trata de la clase recién creada. Para los eventos de modificación, esta es la nueva versión de la clase modificada. Para los eventos de eliminación, esta es la clase eliminada.

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase ClassOperationEvent** se deriva del [**\_ \_ evento**](--event.md).

No se crean **\_ \_ instancias de ClassOperationEvent;** solo se crean instancias de sus subclases. Las clases siguientes derivan de **\_ \_ ClassOperationEvent**:

[**\_\_ClassCreationEvent**](--classcreationevent.md)

[**\_\_ClassModificationEvent**](--classmodificationevent.md)

[**\_\_ClassDeletionEvent**](--classdeletionevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Determinar el tipo de evento que se recibirá](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

