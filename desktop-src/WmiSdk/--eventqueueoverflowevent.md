---
description: Notifica cuándo se descarta un evento como resultado del desbordamiento de la cola de entrega.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: __EventQueueOverflowEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6fd31df9f84883c8b677ea4fef0431ed762b4cec2155cb3d600893a40e3e1d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612635"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_Clase EventQueueOverflowEvent

La clase del sistema **\_ \_ EventQueueOverflowEvent** notifica cuándo se quita un evento como resultado del desbordamiento de la cola de entrega.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase EventQueueOverflowEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase EventQueueOverflowEvent** tiene estas propiedades.

<dl> <dt>

**CurrentQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño de cola actual, en bytes. Esta propiedad tiene como valor predeterminado 10 MB para todas las colas combinadas.

</dd> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Evento de interés. Esta propiedad se hereda de [**\_ \_ EventDroppedEvent.**](--eventdroppedevent.md)

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al consumidor previsto. Esta propiedad se hereda de [**\_ \_ EventDroppedEvent.**](--eventdroppedevent.md)

</dd> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
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

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Solo los usuarios con privilegios de administrador pueden recibir este evento. La **\_ \_ clase EventQueueOverflowEvent** se deriva de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

Para obtener más información, vea la [**propiedad MaximumQueueSize**](--eventconsumer.md) en la clase [**\_ \_ EventConsumer**](--eventconsumer.md) y la [**propiedad HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) en la **clase \_ WMISetting de Win32.**

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

 

