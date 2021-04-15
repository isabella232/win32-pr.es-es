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
# <a name="swbemsink-object"></a><span data-ttu-id="2e6da-103">Objeto SWbemSink</span><span class="sxs-lookup"><span data-stu-id="2e6da-103">SWbemSink object</span></span>

<span data-ttu-id="2e6da-104">Las aplicaciones cliente implementan el objeto **SWbemSink** para recibir los resultados de las operaciones asincrónicas y las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="2e6da-104">The **SWbemSink** object is implemented by client applications to receive the results of asynchronous operations and event notifications.</span></span> <span data-ttu-id="2e6da-105">Para hacer una llamada asincrónica, debe crear una instancia de un objeto **SWbemSink** y pasarlo como el parámetro *ObjWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="2e6da-105">To make an asynchronous call, you must create an instance of an **SWbemSink** object and pass it as the *ObjWbemSink* parameter.</span></span> <span data-ttu-id="2e6da-106">Los eventos de la implementación de **SWbemSink** se desencadenan cuando se devuelven el estado o los resultados, o cuando finaliza la llamada.</span><span class="sxs-lookup"><span data-stu-id="2e6da-106">The events in your implementation of **SWbemSink** are triggered when status or results are returned, or when the call is complete.</span></span> <span data-ttu-id="2e6da-107">La llamada **CreateObject** de VBScript crea este objeto.</span><span class="sxs-lookup"><span data-stu-id="2e6da-107">The VBScript **CreateObject** call creates this object.</span></span>

## <a name="members"></a><span data-ttu-id="2e6da-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e6da-108">Members</span></span>

<span data-ttu-id="2e6da-109">El objeto **SWbemSink** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2e6da-109">The **SWbemSink** object has these types of members:</span></span>

-   [<span data-ttu-id="2e6da-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e6da-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e6da-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e6da-111">Methods</span></span>

<span data-ttu-id="2e6da-112">El objeto **SWbemSink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2e6da-112">The **SWbemSink** object has these methods.</span></span>



| <span data-ttu-id="2e6da-113">Método</span><span class="sxs-lookup"><span data-stu-id="2e6da-113">Method</span></span>                             | <span data-ttu-id="2e6da-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e6da-114">Description</span></span>                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2e6da-115">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="2e6da-115">**Cancel**</span></span>](swbemsink-cancel.md) | <span data-ttu-id="2e6da-116">Cancela todas las operaciones asincrónicas que están asociadas a este receptor.</span><span class="sxs-lookup"><span data-stu-id="2e6da-116">Cancels all asynchronous operations that are associated with this sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e6da-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e6da-117">Remarks</span></span>

<span data-ttu-id="2e6da-118">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="2e6da-118">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="2e6da-119">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2e6da-119">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="2e6da-120">Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="2e6da-120">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="2e6da-121">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2e6da-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

### <a name="events"></a><span data-ttu-id="2e6da-122">Events</span><span class="sxs-lookup"><span data-stu-id="2e6da-122">Events</span></span>

<span data-ttu-id="2e6da-123">Puede implementar subrutinas a las que se llamará cuando se desencadene el evento.</span><span class="sxs-lookup"><span data-stu-id="2e6da-123">You can implement subroutines to be called when events are triggered.</span></span> <span data-ttu-id="2e6da-124">Por ejemplo, si desea procesar cada objeto devuelto por una llamada de consulta asincrónica como [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), cree una subrutina usando el receptor especificado en la llamada asincrónica, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2e6da-124">For example, if you want to process each object that is returned by an asynchronous query call such as [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), create a subroutine using the sink that is specified in the asynchronous call, as shown in the following example.</span></span>


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



<span data-ttu-id="2e6da-125">Utilice la tabla siguiente como referencia para identificar los eventos y las descripciones de los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="2e6da-125">Use the following table as a reference to identify events and trigger descriptions.</span></span>



| <span data-ttu-id="2e6da-126">Evento</span><span class="sxs-lookup"><span data-stu-id="2e6da-126">Event</span></span>                                            | <span data-ttu-id="2e6da-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e6da-127">Description</span></span>                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="2e6da-128">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="2e6da-128">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="2e6da-129">Se desencadena cuando se completa una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="2e6da-129">Triggered when an asynchronous operation is complete.</span></span>                   |
| [<span data-ttu-id="2e6da-130">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="2e6da-130">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="2e6da-131">Se desencadena cuando se completa una operación PUT asincrónica.</span><span class="sxs-lookup"><span data-stu-id="2e6da-131">Triggered when an asynchronous Put operation is complete.</span></span>               |
| [<span data-ttu-id="2e6da-132">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="2e6da-132">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="2e6da-133">Se desencadena cuando un objeto proporcionado por una llamada asincrónica está disponible.</span><span class="sxs-lookup"><span data-stu-id="2e6da-133">Triggered when an object provided by an asynchronous call is available.</span></span> |
| [<span data-ttu-id="2e6da-134">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="2e6da-134">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="2e6da-135">Se desencadena para proporcionar el estado de una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="2e6da-135">Triggered to provide the status of a asynchronous operation.</span></span>            |



 

<span data-ttu-id="2e6da-136">**Recuperación asincrónica de las estadísticas del registro de eventos**</span><span class="sxs-lookup"><span data-stu-id="2e6da-136">**Asynchronously Retrieving Event Log Statistics**</span></span>

<span data-ttu-id="2e6da-137">WMI admite scripts asincrónicos y semisincrónicos.</span><span class="sxs-lookup"><span data-stu-id="2e6da-137">WMI supports both asynchronous and semi-synchronous scripts.</span></span> <span data-ttu-id="2e6da-138">Al recuperar eventos de los registros de eventos, los scripts asincrónicos suelen recuperar estos datos con mucha más rapidez.</span><span class="sxs-lookup"><span data-stu-id="2e6da-138">When retrieving events from the event logs, asynchronous scripts often retrieve this data much faster.</span></span>

<span data-ttu-id="2e6da-139">En un script asincrónico, se emite una consulta y el control se devuelve inmediatamente al script.</span><span class="sxs-lookup"><span data-stu-id="2e6da-139">In an asynchronous script, a query is issued and control is immediately returned to the script.</span></span> <span data-ttu-id="2e6da-140">La consulta continúa procesándose en un subproceso independiente mientras el script empieza a actuar inmediatamente en la información que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="2e6da-140">The query continues to process on a separate thread while the script begins to immediately act on the information that is returned.</span></span> <span data-ttu-id="2e6da-141">Los scripts asincrónicos se controlan mediante eventos: cada vez que se recupera un registro de eventos, se desencadena el evento OnObjectReady.</span><span class="sxs-lookup"><span data-stu-id="2e6da-141">Asynchronous scripts are event driven: each time an event record is retrieved, the OnObjectReady event is fired.</span></span> <span data-ttu-id="2e6da-142">Una vez finalizada la consulta, se activará el evento alfinalizard y el script podrá continuar basándose en el hecho de que se han devuelto todos los registros disponibles.</span><span class="sxs-lookup"><span data-stu-id="2e6da-142">When the query has completed, the OnCompleted event will fire, and the script can continue based on the fact that all the available records have been returned.</span></span>

<span data-ttu-id="2e6da-143">En un script semisincrónico, por el contrario, se emite una consulta y, después, el script pone en cola una gran cantidad de información recuperada antes de actuar sobre ella.</span><span class="sxs-lookup"><span data-stu-id="2e6da-143">In a semi-synchronous script, by contrast, a query is issued and the script then queues a large amount of retrieved information before acting upon it.</span></span> <span data-ttu-id="2e6da-144">Para muchos objetos, el procesamiento semisincrónico es adecuado. por ejemplo, al consultar las propiedades de una unidad de disco, es posible que solo haya una división en segundos entre el momento en que se emite la consulta y el momento en que se devuelve la información y se actúa sobre ella.</span><span class="sxs-lookup"><span data-stu-id="2e6da-144">For many objects, semi-synchronous processing is adequate; for example, when querying a disk drive for its properties, there might be only a split second between the time the query is issued and the time the information is returned and acted upon.</span></span> <span data-ttu-id="2e6da-145">Esto se debe en gran medida al hecho de que la cantidad de información devuelta es relativamente pequeña.</span><span class="sxs-lookup"><span data-stu-id="2e6da-145">This is due in large part to the fact that the amount of information returned is relatively small.</span></span>

<span data-ttu-id="2e6da-146">Sin embargo, al consultar un registro de eventos, se genera el intervalo entre el momento en que se emite la consulta y el tiempo que puede tardar en finalizar la devolución de un script semisincrónico y actuar en la información.</span><span class="sxs-lookup"><span data-stu-id="2e6da-146">When querying an event log, however, the interval between the time the query is issued and the time that a semi-synchronous script can finish returning and acting on the information can take hours.</span></span> <span data-ttu-id="2e6da-147">Además, el script podría quedarse sin memoria y producir un error por sí mismo antes de completarse.</span><span class="sxs-lookup"><span data-stu-id="2e6da-147">On top of that, the script might run out of memory and fail on its own before completing.</span></span>

<span data-ttu-id="2e6da-148">En el caso de los registros de eventos con un gran número de registros, la diferencia en el tiempo de procesamiento puede ser considerable.</span><span class="sxs-lookup"><span data-stu-id="2e6da-148">For event logs with a large number of records, the difference in processing time can be considerable.</span></span> <span data-ttu-id="2e6da-149">En un equipo de prueba basado en Windows 2000 con 2.000 registros en el registro de eventos, una consulta semisincrónica que recupere todos los eventos y los muestre en una ventana de comandos tardó 10 minutos 45 segundos.</span><span class="sxs-lookup"><span data-stu-id="2e6da-149">On a Windows 2000-based test computer with 2,000 records in the event log, a semi-synchronous query that retrieved all the events and displayed them in a command window took 10 minutes 45 seconds.</span></span> <span data-ttu-id="2e6da-150">Una consulta asincrónica que realizó la misma operación tardó un minuto 54 segundos.</span><span class="sxs-lookup"><span data-stu-id="2e6da-150">An asynchronous query that performed the same operation took one minute 54 seconds.</span></span>

## <a name="examples"></a><span data-ttu-id="2e6da-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e6da-151">Examples</span></span>

<span data-ttu-id="2e6da-152">El siguiente VBScript consulta asincrónicamente los registros de eventos para todos los registros.</span><span class="sxs-lookup"><span data-stu-id="2e6da-152">The following VBScript asynchronously queries the event logs for all records.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2e6da-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e6da-153">Requirements</span></span>



| <span data-ttu-id="2e6da-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e6da-154">Requirement</span></span> | <span data-ttu-id="2e6da-155">Value</span><span class="sxs-lookup"><span data-stu-id="2e6da-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6da-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6da-156">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6da-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e6da-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e6da-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6da-158">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6da-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e6da-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e6da-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e6da-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e6da-161"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e6da-161"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e6da-162">IDL</span><span class="sxs-lookup"><span data-stu-id="2e6da-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e6da-163"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e6da-163"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2e6da-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e6da-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e6da-165"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e6da-165"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e6da-166">CLSID</span><span class="sxs-lookup"><span data-stu-id="2e6da-166">CLSID</span></span><br/>                    | <span data-ttu-id="2e6da-167">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="2e6da-167">CLSID\_SWbemSink</span></span><br/> <span data-ttu-id="2e6da-168">CLSID \_ SWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="2e6da-168">CLSID\_SWbemSinkEvents</span></span><br/>                           |
| <span data-ttu-id="2e6da-169">IID</span><span class="sxs-lookup"><span data-stu-id="2e6da-169">IID</span></span><br/>                      | <span data-ttu-id="2e6da-170">\_ISWBEMSINK IID</span><span class="sxs-lookup"><span data-stu-id="2e6da-170">IID\_ISWbemSink</span></span><br/> <span data-ttu-id="2e6da-171">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="2e6da-171">IID\_ISWbemSinkEvents</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="2e6da-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e6da-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6da-173">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="2e6da-173">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




