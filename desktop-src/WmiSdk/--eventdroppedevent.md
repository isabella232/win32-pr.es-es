---
description: Representa la aparición de un evento que se ha quitado. Un evento quitado es un evento que no se entrega a un consumidor de eventos.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent (clase)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706847"
---
# <a name="__eventdroppedevent-class"></a>\_\_Clase EventDroppedEvent

La clase del sistema **\_ \_ EventDroppedEvent** representa la aparición de un evento que se ha quitado. Un evento quitado es un evento que no se entrega a un consumidor de eventos.

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

## <a name="members"></a>Miembros

La clase **\_ \_ EventDroppedEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventDroppedEvent** tiene estas propiedades.

<dl> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ evento**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Evento que se quita.

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa el consumidor permanente que se identifica para recibir un evento. Los distintos consumidores permanentes que se suscriben a un evento pueden seguir recibiendo el evento.

</dd> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor que un proveedor de eventos utiliza para determinar los usuarios que pueden recibir un evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se genera un evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información tiene el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ EventDroppedEvent** se deriva de [**\_ \_ SystemEvent**](--systemevent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

