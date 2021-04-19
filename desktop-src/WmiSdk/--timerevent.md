---
description: Notifica un evento generado por WMI en respuesta a una solicitud de consumidor para un evento de temporizador de intervalo o un evento de temporizador absoluto.
ms.assetid: 5ae29312-cfda-42c9-a154-e5bb31819be0
ms.tgt_platform: multiple
title: __TimerEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2de8967110568e968bb241ebbf4942bf1504b332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688664"
---
# <a name="__timerevent-class"></a>\_\_TimerEvent (clase)

La clase de sistema **\_ \_ TimerEvent** informa de un evento generado por WMI en respuesta a la solicitud de un consumidor de un evento de temporizador de intervalo o un evento de temporizador absoluto. Un evento de temporizador de intervalo es un evento que se produce a intervalos regulares. Un evento de temporizador absoluto es un evento que se produce en un momento determinado. Los eventos de temporizador pueden producirse en cualquier espacio de nombres.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __TimerEvent : __Event
{
  uint32 NumFirings;
  uint8  SECURITY_DESCRIPTOR[];
  string TimerId;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ TimerEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ TimerEvent** tiene estas propiedades.

<dl> <dt>

**NumFirings**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de veces que se produjo el evento antes de que se entregara una notificación al consumidor.

</dd> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información está en el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Instancia de la subclase [**\_ \_ TimerInstruction**](--timerinstruction.md) que causó que WMI desencadenara este evento. Los consumidores especifican una identificación del temporizador en la propiedad **TimerId** de la subclase **\_ \_ TimerInstruction** que crean para registrarse.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ TimerEvent** se deriva de [**\_ \_ Event**](--event.md).

Los consumidores de eventos se registran para un evento de temporizador absoluto mediante la creación de una instancia de la clase del sistema [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) . Se registran para un evento de temporizador de intervalo mediante la creación de una instancia de la clase del sistema [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

Durante el funcionamiento normal, la propiedad **NumFirings** se establece en 1. Cuando no es posible llegar al consumidor o el intervalo de activación es mucho más rápido que la capacidad de entrega del evento, **NumFirings** se establece en un número mayor que 1. Cuando **NumFirings** es mayor que 1, WMI combina automáticamente muchos eventos de temporizador en el mismo evento. Esta combinación es similar a lo que sucede con los mensajes [**\_ del temporizador de WM**](/windows/desktop/winmsg/wm-timer) en la programación de Windows.

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

[Recibir eventos de tiempo o repetición](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[Recepción de eventos mientras dure la aplicación](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

