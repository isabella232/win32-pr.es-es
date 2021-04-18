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
# <a name="swbemeventsource-object"></a><span data-ttu-id="b58c7-103">Objeto SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="b58c7-103">SWbemEventSource object</span></span>

<span data-ttu-id="b58c7-104">El objeto **SWbemEventSource** recupera eventos de una consulta de evento junto con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="b58c7-104">The **SWbemEventSource** object retrieves events from an event query in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="b58c7-105">Obtiene un objeto **SWbemEventSource** si realiza una llamada a **SWbemServices.ExecNotificationQuery** para realizar una consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="b58c7-105">You get an **SWbemEventSource** object if you make a call to **SWbemServices.ExecNotificationQuery** to make an event query.</span></span> <span data-ttu-id="b58c7-106">Después, puede usar el método [**NextEvent**](swbemeventsource-nextevent.md) para recuperar los eventos a medida que llegan.</span><span class="sxs-lookup"><span data-stu-id="b58c7-106">You can then use the [**NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span> <span data-ttu-id="b58c7-107">Este objeto no se puede crear mediante la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="b58c7-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="b58c7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b58c7-108">Members</span></span>

<span data-ttu-id="b58c7-109">El objeto **SWbemEventSource** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b58c7-109">The **SWbemEventSource** object has these types of members:</span></span>

-   [<span data-ttu-id="b58c7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b58c7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b58c7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b58c7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b58c7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b58c7-112">Methods</span></span>

<span data-ttu-id="b58c7-113">El objeto **SWbemEventSource** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b58c7-113">The **SWbemEventSource** object has these methods.</span></span>



| <span data-ttu-id="b58c7-114">Método</span><span class="sxs-lookup"><span data-stu-id="b58c7-114">Method</span></span>                                          | <span data-ttu-id="b58c7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b58c7-115">Description</span></span>                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b58c7-116">**NextEvent**</span><span class="sxs-lookup"><span data-stu-id="b58c7-116">**NextEvent**</span></span>](swbemeventsource-nextevent.md) | <span data-ttu-id="b58c7-117">Se usa para recuperar un evento junto con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="b58c7-117">Used to retrieve an event in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b58c7-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b58c7-118">Properties</span></span>

<span data-ttu-id="b58c7-119">El objeto **SWbemEventSource** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b58c7-119">The **SWbemEventSource** object has these properties.</span></span>



| <span data-ttu-id="b58c7-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b58c7-120">Property</span></span>                                                    | <span data-ttu-id="b58c7-121">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="b58c7-121">Access type</span></span>          | <span data-ttu-id="b58c7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b58c7-122">Description</span></span>                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="b58c7-123">**Seguridad\_**</span><span class="sxs-lookup"><span data-stu-id="b58c7-123">**Security\_**</span></span>](swbemeventsource-security-.md)<br/> | <span data-ttu-id="b58c7-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b58c7-124">Read-only</span></span><br/> | <span data-ttu-id="b58c7-125">Se usa para leer o cambiar la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b58c7-125">Used to read or change the security settings.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="b58c7-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b58c7-126">Examples</span></span>

<span data-ttu-id="b58c7-127">Este script usa los métodos de la clase **SWbemEventSource** y la clase [**SWbemServices**](swbemservices.md) junto con una consulta WQL para los eventos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b58c7-127">This script uses the methods of the **SWbemEventSource** class and the [**SWbemServices**](swbemservices.md) class in conjunction with a WQL query for application events.</span></span> <span data-ttu-id="b58c7-128">Para obtener más información acerca de la notificación de eventos WMI y las consultas, vea [supervisar eventos](monitoring-events.md), [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)y [recibir notificaciones de eventos asincrónicos](receiving-asynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b58c7-128">For more information about WMI event notification and queries see [Monitoring Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md), and [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b58c7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b58c7-129">Requirements</span></span>



| <span data-ttu-id="b58c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b58c7-130">Requirement</span></span> | <span data-ttu-id="b58c7-131">Value</span><span class="sxs-lookup"><span data-stu-id="b58c7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b58c7-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b58c7-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b58c7-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b58c7-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b58c7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b58c7-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b58c7-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b58c7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b58c7-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b58c7-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b58c7-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b58c7-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="b58c7-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b58c7-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b58c7-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b58c7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b58c7-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b58c7-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b58c7-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="b58c7-142">CLSID</span></span><br/>                    | <span data-ttu-id="b58c7-143">CLSID \_ SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="b58c7-143">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="b58c7-144">IID</span><span class="sxs-lookup"><span data-stu-id="b58c7-144">IID</span></span><br/>                      | <span data-ttu-id="b58c7-145">\_ISWBEMEVENTSOURCE IID</span><span class="sxs-lookup"><span data-stu-id="b58c7-145">IID\_ISWbemEventSource</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="b58c7-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b58c7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58c7-147">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="b58c7-147">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

