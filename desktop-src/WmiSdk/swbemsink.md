---
description: Las aplicaciones cliente implementan el objeto SWbemSink para recibir los resultados de las operaciones asincrónicas y las notificaciones de eventos.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Objeto SWbemSink (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715709"
---
# <a name="swbemsink-object"></a>Objeto SWbemSink

Las aplicaciones cliente implementan el objeto **SWbemSink** para recibir los resultados de las operaciones asincrónicas y las notificaciones de eventos. Para hacer una llamada asincrónica, debe crear una instancia de un objeto **SWbemSink** y pasarlo como el parámetro *ObjWbemSink* . Los eventos de la implementación de **SWbemSink** se desencadenan cuando se devuelven el estado o los resultados, o cuando finaliza la llamada. La llamada **CreateObject** de VBScript crea este objeto.

## <a name="members"></a>Miembros

El objeto **SWbemSink** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **SWbemSink** tiene estos métodos.



| Método                             | Descripción                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [**Cancelar**](swbemsink-cancel.md) | Cancela todas las operaciones asincrónicas que están asociadas a este receptor.<br/> |



 

## <a name="remarks"></a>Observaciones

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

### <a name="events"></a>Events

Puede implementar subrutinas a las que se llamará cuando se desencadene el evento. Por ejemplo, si desea procesar cada objeto devuelto por una llamada de consulta asincrónica como [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), cree una subrutina usando el receptor especificado en la llamada asincrónica, tal como se muestra en el ejemplo siguiente.


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



Utilice la tabla siguiente como referencia para identificar los eventos y las descripciones de los desencadenadores.



| Evento                                            | Descripción                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**OnCompleted**](swbemsink-oncompleted.md)     | Se desencadena cuando se completa una operación asincrónica.                   |
| [**OnObjectPut**](swbemsink-onobjectput.md)     | Se desencadena cuando se completa una operación PUT asincrónica.               |
| [**OnObjectReady**](swbemsink-onobjectready.md) | Se desencadena cuando un objeto proporcionado por una llamada asincrónica está disponible. |
| [**OnProgress**](swbemsink-onprogress.md)       | Se desencadena para proporcionar el estado de una operación asincrónica.            |



 

**Recuperación asincrónica de las estadísticas del registro de eventos**

WMI admite scripts asincrónicos y semisincrónicos. Al recuperar eventos de los registros de eventos, los scripts asincrónicos suelen recuperar estos datos con mucha más rapidez.

En un script asincrónico, se emite una consulta y el control se devuelve inmediatamente al script. La consulta continúa procesándose en un subproceso independiente mientras el script empieza a actuar inmediatamente en la información que se devuelve. Los scripts asincrónicos se controlan mediante eventos: cada vez que se recupera un registro de eventos, se desencadena el evento OnObjectReady. Una vez finalizada la consulta, se activará el evento alfinalizard y el script podrá continuar basándose en el hecho de que se han devuelto todos los registros disponibles.

En un script semisincrónico, por el contrario, se emite una consulta y, después, el script pone en cola una gran cantidad de información recuperada antes de actuar sobre ella. Para muchos objetos, el procesamiento semisincrónico es adecuado. por ejemplo, al consultar las propiedades de una unidad de disco, es posible que solo haya una división en segundos entre el momento en que se emite la consulta y el momento en que se devuelve la información y se actúa sobre ella. Esto se debe en gran medida al hecho de que la cantidad de información devuelta es relativamente pequeña.

Sin embargo, al consultar un registro de eventos, se genera el intervalo entre el momento en que se emite la consulta y el tiempo que puede tardar en finalizar la devolución de un script semisincrónico y actuar en la información. Además, el script podría quedarse sin memoria y producir un error por sí mismo antes de completarse.

En el caso de los registros de eventos con un gran número de registros, la diferencia en el tiempo de procesamiento puede ser considerable. En un equipo de prueba basado en Windows 2000 con 2.000 registros en el registro de eventos, una consulta semisincrónica que recupere todos los eventos y los muestre en una ventana de comandos tardó 10 minutos 45 segundos. Una consulta asincrónica que realizó la misma operación tardó un minuto 54 segundos.

## <a name="examples"></a>Ejemplos

El siguiente VBScript consulta asincrónicamente los registros de eventos para todos los registros.


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/> CLSID \_ SWbemSinkEvents<br/>                           |
| IID<br/>                      | \_ISWBEMSINK IID<br/> \_ISWBEMSINKEVENTS IID<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




