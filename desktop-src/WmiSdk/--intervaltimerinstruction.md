---
description: Genera eventos a intervalos, de forma similar a un mensaje WM \_ TIMER en Windows programación.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction clase
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
ms.openlocfilehash: 17f0c55edceb3c5fb009f49ae97e3765ec3e0255a82f8c75e133344379c24d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640765"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_IntervalTimerInstruction (clase)

La **\_ \_ clase del sistema IntervalTimerInstruction** genera eventos a intervalos, de forma similar a un mensaje WM \_ TIMER Windows programación. Un consumidor de eventos se registra para recibir eventos de temporizador de intervalo mediante la creación de una consulta de eventos que hace referencia a esta clase. Debido al comportamiento del sistema operativo, no hay ninguna garantía de que los eventos se entreguen exactamente en el intervalo solicitado.

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

La **\_ \_ clase IntervalTimerInstruction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase IntervalTimerInstruction** tiene estas propiedades.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](standard-qualifiers.md) (milisegundos)
</dt> </dl>

Número de milisegundos entre la activación de eventos.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** este evento se omitirá si el intervalo ya se ha pasado. El valor predeterminado es **FALSE.** Esta propiedad se hereda de [**\_ \_ TimerInstruction.**](--timerinstruction.md)

<dt>

FALSE
</dt> <dd>

Cuando WMI o el consumidor vuelvan a estar disponibles, se generará y recibirá un evento de notificación.

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

Calificadores: [ **Clave**](standard-qualifiers.md)
</dt> </dl>

Identificador único para este **\_ \_ objeto IntervalTimerInstruction.** Esta propiedad se hereda de [**\_ \_ TimerInstruction.**](--timerinstruction.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase IntervalTimerInstruction** se deriva de [**\_ \_ TimerInstruction**](--timerinstruction.md).

La consulta de eventos especificada para registrarse para un evento de temporizador de intervalo normalmente se basa en la **propiedad TimerId.** Los eventos de notificación generados a partir de un evento de temporizador de intervalo contienen la propiedad **NumFirings,** que contiene datos que reflejan el número de eventos desencadenados durante el tiempo en que no se pudieron recibir los eventos. Si **SkipIfPassed** se establece en **TRUE,** esa información se descarta.

El valor de la **propiedad IntervalBetweenEvents** debe ser razonablemente grande. Si es demasiado pequeño, WMI puede omitirlo y no generar el evento debido a limitaciones en algunos sistemas operativos.

WMI genera el evento de temporizador de intervalo mediante la creación de una instancia de la [**\_ \_ clase TimerEvent.**](--timerevent.md)

Para recibir estos eventos de temporizador en un consumidor de eventos temporal, ejecute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) con la siguiente cadena de consulta de eventos:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Para recibir estos eventos de temporizador en un consumidor de eventos permanente, debe cargar la consulta anterior en un filtro de eventos, definir un consumidor lógico y crear un enlace de filtro a consumidor para el filtro y el consumidor. Para obtener más información, vea [Recepción de eventos en todo momento.](receiving-events-at-all-times.md)

## <a name="examples"></a>Ejemplos

La siguiente declaración MOF muestra cómo generar un evento de temporizador de intervalo con la propiedad de clave establecida en "MyEvent" cada 10 segundos:


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

[Recepción de eventos con tiempo o repetición](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

