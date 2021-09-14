---
description: Win32 \_ PowerManagementEvent &\# 32; La clase WMI representa los eventos de administración de energía resultantes de los cambios de estado de energía.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Win32_PowerManagementEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261631"
---
# <a name="win32_powermanagementevent-class"></a>Clase PowerManagementEvent de Win32 \_

La clase WMI **\_ Win32 PowerManagementEvent** [representa](../wmisdk/retrieving-a-class.md) los eventos de administración de energía resultantes de los cambios de estado de energía. Estos cambios de estado están asociados a los protocolos de administración avanzada de energía (APM) o Interfaz avanzada de configuración y energía (ACPI).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a>Members

La **clase \_ PowerManagementEvent de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PowerManagementEvent de Win32** tiene estas propiedades.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Power Management Events")
</dt> </dl>

Tipo de cambio en el estado de energía del sistema.

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Especificar suspender** (4)


</dt> <dd>

Mientras está suspendido, el equipo parece estar desactivado; sin embargo, se puede "desatrase" en respuesta a varios eventos, incluida la entrada del usuario (como mover el mouse o presionar una tecla en el teclado). Mientras se suspende el equipo, el consumo de energía se reduce a uno de varios niveles en función de cómo se va a usar el sistema. Mientras menor sea el nivel de consumo de energía, más tiempo tarda el sistema en volver al estado de funcionamiento. Cuando el equipo entra en el estado de suspensión, el escritorio está bloqueado y debe presionar CTRL+ALT+SUPR y proporcionar un nombre de usuario y una contraseña válidos para reanudar las operaciones.

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Reanudar desde suspender** (7)


</dt> <dd>

Indica que se ha enviado un mensaje Reanudar desde suspender, lo que permite que el equipo vuelva a su estado de energía normal.

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Cambio de estado de** energía (10)


</dt> <dd>

Indica un cambio en el estado de energía del equipo, como un cambio de la alimentación de la batería a la ca, o de la ca a una fuente de alimentación ininterrumpida. El sistema difunde también este evento cuando la energía de la batería restante queda por debajo del umbral especificado por el usuario o cuando la energía de la batería cambia en un porcentaje especificado.

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Evento de OEM** (11)


</dt> <dd>

Indica que un BIOS de Administración avanzada de energía (APM) ha enviado un evento oem. El valor del evento se capturará en la **propiedad OEMEventCode.** Dado que algunas implementaciones de BIOS de APM no proporcionan notificaciones de eventos de OEM, es posible que este evento nunca se difunda en algunos equipos. APM es un esquema de administración de energía heredado. Aunque todavía se admite, APM se ha reemplazado en gran medida por ACPI (Interfaz avanzada de configuración y energía).

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Reanudar automático** (18)


</dt> <dd>

Indica que el equipo se ha convertido en respuesta a un evento. Si el sistema detecta la actividad del usuario (por ejemplo, un clic del mouse), se difundirá el mensaje ResumeSuspend, lo que permitirá a las aplicaciones saber que pueden reanudar la interactividad completa con el usuario.

</dd> </dl>

</dd> <dt>

**OEMEventCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Power Management Events")
</dt> </dl>

Estado de energía del sistema definido por el fabricante de equipos originales (OEM) cuando la propiedad **EventType** de esta clase se establece en 11 (evento oem); de lo contrario, esta propiedad se establece en **NULL.** Los eventos de OEM se generan cuando un BIOS de APM señala un evento oem de APM. Los códigos de evento de OEM están en el intervalo 0x0200h - 0x02FFFh.

</dd> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Constantes de seguridad wmi](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC).

Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ PowerManagementEvent de Win32** se deriva de [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).

Los cambios en el estado de energía a menudo indican que se ha producido un problema con un equipo o con otro dispositivo administrado. Si un servidor cambia repentinamente de la alimentación de CA a una fuente de alimentación ininterrumpida, este cambio puede indicar que se ha producido un problema eléctrico de algún tipo, ya sea con el propio equipo o con el sistema eléctrico en la sala en la que se mantiene el equipo.

Los administradores deben supervisar estos cambios en el estado de energía y recibir una notificación de estos cambios inmediatamente. Esto les permite tomar medidas antes de que el dispositivo pierda completamente la energía. (Los sistemas de alimentación ininterrumpidas, por ejemplo, pueden ejecutarse durante unos 15 minutos aproximadamente antes de apagarse).

La **clase \_ PowerManagementEvent de Win32** se puede usar para supervisar los cambios en el estado de energía en un equipo. Estos cambios pueden incluir un cambio de una fuente de alimentación a otra, así como un cambio en el estado de energía del equipo (por ejemplo, entrar o salir del modo de suspensión).

La clase **\_ PowerManagementEvent de Win32** solo tiene dos propiedades: EventType, que se usa para indicar el tipo de evento de cambio de energía que se produjo, y OEMEventType, que usan algunos fabricantes de equipos originales para definir eventos de cambio de energía adicionales.

Para obtener más información sobre cómo responder Windows eventos de energía, consulte el artículo Supervisión y respuesta a eventos de Windows PowerShell con [PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) en hey! Scripting Guy! .

## <a name="examples"></a>Ejemplos

El siguiente VBScript supervisa los cambios en el estado de energía en un equipo.


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Supervisión de cambios en el estado de energía del equipo](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
