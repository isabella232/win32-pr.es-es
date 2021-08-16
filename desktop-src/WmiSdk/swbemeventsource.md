---
description: El objeto SWbemEventSource recupera eventos de una consulta de eventos junto con SWbemServices.ExecNotificationQuery.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Objeto SWbemEventSource (Wbemdisp.h)
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
ms.openlocfilehash: e38dab258ebccacb24cf92b7445752102b297ab1207b99e40355c30fde99113d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992145"
---
# <a name="swbemeventsource-object"></a>Objeto SWbemEventSource

El **objeto SWbemEventSource** recupera eventos de una consulta de eventos junto con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Obtiene un objeto **SWbemEventSource** si realiza una llamada a **SWbemServices.ExecNotificationQuery** para realizar una consulta de eventos. A continuación, puede usar [**el método NextEvent**](swbemeventsource-nextevent.md) para recuperar eventos a medida que llegan. La llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript no puede crear este objeto.

## <a name="members"></a>Miembros

El **objeto SWbemEventSource** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemEventSource** tiene estos métodos.



| Método                                          | Descripción                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Se usa para recuperar un evento junto con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemEventSource** tiene estas propiedades.



| Propiedad                                                    | Tipo de acceso          | Descripción                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Seguridad\_**](swbemeventsource-security-.md)<br/> | Solo lectura<br/> | Se usa para leer o cambiar la configuración de seguridad.<br/> |



 

## <a name="examples"></a>Ejemplos

Este script usa los métodos de la **clase SWbemEventSource** y la clase [**SWbemServices**](swbemservices.md) junto con una consulta WQL para eventos de aplicación. Para obtener más información sobre las consultas y la notificación de eventos WMI, vea Monitoring [Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md)y Receiving Asynchronous Event [Notifications](receiving-asynchronous-event-notifications.md).


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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

