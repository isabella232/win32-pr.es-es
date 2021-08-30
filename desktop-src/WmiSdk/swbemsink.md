---
description: Las aplicaciones cliente implementan el objeto SWbemSink para recibir los resultados de las operaciones asincrónicas y las notificaciones de eventos.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Objeto SWbemSink (Wbemdisp.h)
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
ms.openlocfilehash: 3f7b2c499716bb8da3d2cc9a7db5dd06a2341c5d75876468f5e81853a8120944
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071465"
---
# <a name="swbemsink-object"></a>Objeto SWbemSink

Las aplicaciones cliente implementan el objeto **SWbemSink** para recibir los resultados de las operaciones asincrónicas y las notificaciones de eventos. Para realizar una llamada asincrónica, debe crear una instancia de un objeto **SWbemSink** y pasarla como el *parámetro ObjWbemSink.* Los eventos de la implementación de **SWbemSink** se desencadenan cuando se devuelve el estado o los resultados, o cuando se completa la llamada. La llamada **CreateObject de** VBScript crea este objeto .

## <a name="members"></a>Miembros

El **objeto SWbemSink** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto SWbemSink** tiene estos métodos.



| Método                             | Descripción                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [**Cancelar**](swbemsink-cancel.md) | Cancela todas las operaciones asincrónicas asociadas a este receptor.<br/> |



 

## <a name="remarks"></a>Comentarios

Una devolución de llamada asincrónica permite a un usuario no autenticado proporcionar datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, use la comunicación semisincronosa o la comunicación sincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

### <a name="events"></a>Eventos

Puede implementar subrutinas a las que se llamará cuando se desencadene eventos. Por ejemplo, si desea procesar cada objeto devuelto por una llamada de consulta asincrónica como [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), cree una subrutina mediante el receptor especificado en la llamada asincrónica, como se muestra en el ejemplo siguiente.


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



Use la tabla siguiente como referencia para identificar eventos y descripciones de desencadenadores.



| Evento                                            | Descripción                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**OnCompleted**](swbemsink-oncompleted.md)     | Se desencadena cuando se completa una operación asincrónica.                   |
| [**OnObjectPut**](swbemsink-onobjectput.md)     | Se desencadena cuando se completa una operación put asincrónica.               |
| [**OnObjectReady**](swbemsink-onobjectready.md) | Se desencadena cuando un objeto proporcionado por una llamada asincrónica está disponible. |
| [**OnProgress**](swbemsink-onprogress.md)       | Se desencadena para proporcionar el estado de una operación asincrónica.            |



 

**Recuperación asincrónica de estadísticas del registro de eventos**

WMI admite scripts asincrónicos y semi sincrónicos. Al recuperar eventos de los registros de eventos, los scripts asincrónicos suelen recuperar estos datos mucho más rápido.

En un script asincrónico, se emite una consulta y el control se devuelve inmediatamente al script. La consulta continúa procesando en un subproceso independiente mientras el script comienza a actuar inmediatamente sobre la información que se devuelve. Los scripts asincrónicos están controlados por eventos: cada vez que se recupera un registro de eventos, se desencadena el evento OnObjectReady. Una vez completada la consulta, se activado el evento OnCompleted y el script puede continuar en función del hecho de que se han devuelto todos los registros disponibles.

En un script semi sincrónico, por el contrario, se emite una consulta y, a continuación, el script pone en cola una gran cantidad de información recuperada antes de actuar sobre ella. Para muchos objetos, el procesamiento semi sincrónico es adecuado; Por ejemplo, al consultar una unidad de disco para sus propiedades, podría haber solo una división de segundo entre el momento en que se emite la consulta y el momento en que se devuelve y se actúa sobre ella. Esto se debe en gran medida al hecho de que la cantidad de información devuelta es relativamente pequeña.

Sin embargo, al consultar un registro de eventos, el intervalo entre el momento en que se emite la consulta y el momento en que un script semi sincrónico puede terminar de devolver y actuar sobre la información puede tardar horas. Además, es posible que el script se queda sin memoria y se producirá un error por sí mismo antes de completarse.

En el caso de los registros de eventos con un gran número de registros, la diferencia en el tiempo de procesamiento puede ser considerable. En un equipo de prueba basado en Windows 2000 con 2000 registros en el registro de eventos, una consulta semi sincrónica que recuperó todos los eventos y los mostró en una ventana de comandos tardó 10 minutos y 45 segundos. Una consulta asincrónica que realizó la misma operación tardó un minuto 54 segundos.

## <a name="examples"></a>Ejemplos

El siguiente VBScript consulta de forma asincrónica los registros de eventos para todos los registros.


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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/> CLSID \_ SWbemSinkEvents<br/>                           |
| IID<br/>                      | IID \_ ISWbemSink<br/> IID \_ ISWbemSinkEvents<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




