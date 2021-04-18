---
description: Genera eventos a intervalos, similar a un \_ mensaje del temporizador de WM en la programación de Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707111"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_Clase IntervalTimerInstruction

La clase del sistema **\_ \_ IntervalTimerInstruction** genera eventos a intervalos, similar a un \_ mensaje del temporizador de WM en la programación de Windows. Un consumidor de eventos se registra en eventos de temporizador de intervalo de recepción mediante la creación de una consulta de evento que hace referencia a esta clase. Debido al comportamiento del sistema operativo, no hay ninguna garantía de que los eventos se entreguen exactamente el intervalo solicitado.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ IntervalTimerInstruction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ IntervalTimerInstruction** tiene estas propiedades.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](standard-qualifiers.md) (milisegundos)
</dt> </dl>

Número de milisegundos entre las desencadenaciones de eventos.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, este evento se omitirá si ya se ha pasado el intervalo. El valor predeterminado es **false**. Esta propiedad se hereda de [**\_ \_ TimerInstruction**](--timerinstruction.md).

<dt>

false
</dt> <dd>

Cuando WMI o el consumidor vuelva a estar disponible, se generará y recibirá un evento de notificación.

</dd> <dt>

TRUE
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

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Identificador único de este objeto **\_ \_ IntervalTimerInstruction** . Esta propiedad se hereda de [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ IntervalTimerInstruction** se deriva de [**\_ \_ TimerInstruction**](--timerinstruction.md).

La consulta de eventos especificada para registrarse para un evento de temporizador de intervalo se basa normalmente en la propiedad **TimerId** . Los eventos de notificación generados a partir de un evento de temporizador de intervalo contienen la propiedad **NumFirings** , que contiene los datos que reflejan el número de eventos desencadenados durante el tiempo que no se pudieron recibir los eventos. Si **SkipIfPassed** se establece en **true**, se descarta esa información.

El valor de la propiedad **IntervalBetweenEvents** debe ser razonablemente grande. Si es demasiado pequeño, WMI puede omitirlo y no generar el evento debido a las limitaciones en algunos sistemas operativos.

WMI genera el evento de temporizador de intervalo mediante la creación de una instancia de la clase [**\_ \_ TimerEvent**](--timerevent.md) .

Para recibir estos eventos de temporizador en un consumidor de eventos temporal, ejecute [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) con la siguiente cadena de consulta de eventos:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Para recibir estos eventos de temporizador en un consumidor de eventos permanente, debe cargar la consulta anterior en un filtro de eventos, definir un consumidor lógico y crear un enlace de filtro a consumidor para el filtro y el consumidor. Para obtener más información, consulte [recibir eventos en todo momento](receiving-events-at-all-times.md).

## <a name="examples"></a>Ejemplos

La siguiente declaración de MOF muestra cómo generar un evento de temporizador de intervalo con la propiedad clave establecida en "DoEvents" cada 10 segundos:


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Recibir eventos de tiempo o repetición](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

