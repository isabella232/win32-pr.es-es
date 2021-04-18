---
description: Especifica instrucciones sobre cómo se deben generar los eventos de temporizador para los consumidores.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: __TimerInstruction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361618"
---
# <a name="__timerinstruction-class"></a>\_\_Clase TimerInstruction

La clase **\_ \_ TimerInstruction** Abstract System especifica instrucciones sobre cómo se deben generar [los eventos de temporizador para los](receiving-a-timed-or-repeating-event.md) consumidores.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ TimerInstruction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ TimerInstruction** tiene estas propiedades.

<dl> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe si se generará un evento de notificación y se recibirá cuando un consumidor esté disponible.

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

Cadena única asignada por el usuario que identifica este evento de temporizador determinado. Para evitar conflictos de nombres con otros identificadores de temporizador, se puede usar la forma de cadena de un GUID de estilo de entorno de equipo distribuido (DCE). Esta propiedad forma parte de la instancia de [**\_ \_ TimerEvent**](--timerevent.md) que representa el evento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ TimerInstruction** se deriva de [**\_ \_ EventGenerator**](--eventgenerator.md).

Las subclases **\_ \_ TimerInstruction** son [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), usadas por los consumidores para registrarse para un evento de temporizador absoluto y [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), que se usan para registrarse para un evento de temporizador de intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_EventGenerator**](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

