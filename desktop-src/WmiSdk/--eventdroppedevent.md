---
description: Representa la aparición de un evento que se ha eliminado. Un evento eliminado es un evento que no se entrega a un consumidor de eventos.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063963"
---
# <a name="__eventdroppedevent-class"></a>\_\_EventDroppedEvent (clase)

La **\_ \_ clase del sistema EventDroppedEvent** representa la aparición de un evento que se ha eliminado. Un evento eliminado es un evento que no se entrega a un consumidor de eventos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ clase EventDroppedEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase EventDroppedEvent** tiene estas propiedades.

<dl> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ Evento**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Evento que se ha eliminado.

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de [**\_ \_ EventConsumer que**](--eventconsumer.md) representa el consumidor permanente que se identifica para recibir un evento. Los distintos consumidores permanentes que se suscriben a un evento pueden seguir recibiendo el evento.

</dd> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor que usa un proveedor de eventos para determinar los usuarios que pueden recibir un evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se genera un evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\_ \_ clase EventDroppedEvent** se deriva de [**\_ \_ SystemEvent**](--systemevent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

