---
description: Hace que un evento se genere en una fecha específica en un momento específico.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: __AbsoluteTimerInstruction clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967188"
---
# <a name="__absolutetimerinstruction-class"></a>\_\_AbsoluteTimerInstruction (clase)

La **\_ \_ clase del sistema AbsoluteTimerInstruction** hace que se genere un evento en una fecha específica en un momento específico. Un consumidor de eventos se registra para recibir un evento de temporizador absoluto mediante la creación de una instancia de esta clase. El evento se genera una vez.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a>Members

La **\_ \_ clase AbsoluteTimerInstruction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase AbsoluteTimerInstruction** tiene estas propiedades.

<dl> <dt>

**EventDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Cadena de longitud fija en [formato DMTF](date-and-time-format.md) que especifica cuándo se activo el temporizador.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el evento de temporizador se produce si WMI no puede generarlo en el intervalo de tiempo correcto o el consumidor que solicita recibir el evento no está disponible. Si **es TRUE,** el evento no se producirá. El valor predeterminado es **FALSE.** Cuando WMI o el consumidor están disponibles, se genera y recibe un evento de notificación. Esta propiedad se hereda de [**\_ \_ TimerInstruction.**](--timerinstruction.md)

<dt>

false
</dt> <dd>

Cuando WMI o el consumidor vuelvan a estar disponibles, se generará y recibirá un evento de notificación.

</dd> <dt>

true
</dt> <dd>

El evento de temporizador no se produce si WMI no está disponible para generarlo en el intervalo de tiempo adecuado o el consumidor que solicita recibir el evento no está disponible.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](standard-qualifiers.md)
</dt> </dl>

Cadena única asignada por el usuario que identifica un evento de temporizador específico. Para evitar conflictos de nomenclatura con otros identificadores de temporizador, se puede usar la forma de cadena de un GUID de estilo de entorno de equipo distribuido. Esta propiedad se hereda de [**\_ \_ TimerInstruction.**](--timerinstruction.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\_ \_ clase AbsoluteTimerInstruction** se deriva de [**\_ \_ TimerInstruction**](--timerinstruction.md).

WMI genera el evento de temporizador absoluto mediante la creación de una instancia de la [**\_ \_ clase TimerEvent.**](--timerevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Recepción de eventos con tiempo o repeticiones](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[Recepción de eventos durante la duración de la aplicación](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

