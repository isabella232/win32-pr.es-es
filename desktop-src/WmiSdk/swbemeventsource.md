---
description: El objeto SWbemEventSource recupera eventos de una consulta de evento junto con SWbemServices.ExecNotificationQuery.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Objeto SWbemEventSource (Wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706064"
---
# <a name="swbemeventsource-object"></a>Objeto SWbemEventSource

El objeto **SWbemEventSource** recupera eventos de una consulta de evento junto con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Obtiene un objeto **SWbemEventSource** si realiza una llamada a **SWbemServices.ExecNotificationQuery** para realizar una consulta de evento. Después, puede usar el método [**NextEvent**](swbemeventsource-nextevent.md) para recuperar los eventos a medida que llegan. Este objeto no se puede crear mediante la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.

## <a name="members"></a>Miembros

El objeto **SWbemEventSource** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemEventSource** tiene estos métodos.



| Método                                          | Descripción                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Se usa para recuperar un evento junto con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemEventSource** tiene estas propiedades.



| Propiedad                                                    | Tipo de acceso          | Descripción                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Seguridad\_**](swbemeventsource-security-.md)<br/> | Solo lectura<br/> | Se usa para leer o cambiar la configuración de seguridad.<br/> |



 

## <a name="examples"></a>Ejemplos

Este script usa los métodos de la clase **SWbemEventSource** y la clase [**SWbemServices**](swbemservices.md) junto con una consulta WQL para los eventos de aplicación. Para obtener más información acerca de la notificación de eventos WMI y las consultas, vea [supervisar eventos](monitoring-events.md), [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)y [recibir notificaciones de eventos asincrónicos](receiving-asynchronous-event-notifications.md).


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | \_ISWBEMEVENTSOURCE IID<br/>                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

