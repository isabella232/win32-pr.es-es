---
description: Representa la aparición de algún otro evento que se está descartando debido al error de un consumidor de eventos.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: __ConsumerFailureEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e8276716a1ca706a0027f35f9b554b960efebadacf3d8841b23415a43a9663c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732943"
---
# <a name="__consumerfailureevent-class"></a>\_\_ConsumerFailureEvent (clase)

La clase del sistema **\_ \_ ConsumerFailureEvent** representa la aparición de algún otro evento que se está descartando debido al error de un consumidor de eventos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase ConsumerFailureEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase ConsumerFailureEvent** tiene estas propiedades.

<dl> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Código de error devuelto por el consumidor.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del código de error extendido, si está disponible.

</dd> <dt>

**ErrorObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Objeto con error.

</dd> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Evento con error. Esta propiedad se hereda de [**\_ \_ EventDroppedEvent.**](--eventdroppedevent.md)

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al consumidor previsto. Esta propiedad se hereda de [**\_ \_ EventDroppedEvent.**](--eventdroppedevent.md)

</dd> <dt>

**\_DESCRIPTOR DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase ConsumerFailureEvent** se deriva de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_EventDroppedEvent**](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

