---
description: Los administradores del sistema pueden utilizar WMI para supervisar los eventos de una red.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Supervisión de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155240"
---
# <a name="monitoring-events"></a><span data-ttu-id="f9b0f-103">Supervisión de eventos</span><span class="sxs-lookup"><span data-stu-id="f9b0f-103">Monitoring Events</span></span>

<span data-ttu-id="f9b0f-104">Los administradores del sistema pueden utilizar WMI para supervisar los eventos de una red.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-104">System administrators can use WMI to monitor events on a network.</span></span> <span data-ttu-id="f9b0f-105">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f9b0f-105">For example:</span></span>

-   <span data-ttu-id="f9b0f-106">Un servicio se detiene inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-106">A service stops unexpectedly.</span></span>
-   <span data-ttu-id="f9b0f-107">Un servidor deja de estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-107">A server becomes unavailable.</span></span>
-   <span data-ttu-id="f9b0f-108">Una unidad de disco se llena hasta el 80% de la capacidad.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-108">A disk drive fills to 80% capacity.</span></span>
-   <span data-ttu-id="f9b0f-109">Los eventos de seguridad se registran en un registro de eventos de NT.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-109">Security events are reported to an NT Event Log.</span></span>

<span data-ttu-id="f9b0f-110">WMI admite la detección y entrega de eventos a los consumidores de eventos porque algunos proveedores de WMI son proveedores de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-110">WMI supports event detection and delivery to event consumers because some WMI providers are event providers.</span></span> <span data-ttu-id="f9b0f-111">Para obtener más información, consulte [recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-111">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="f9b0f-112">Los [*consumidores de eventos*](gloss-e.md) son aplicaciones o scripts que solicitan notificación de eventos y, a continuación, realizan tareas cuando se producen eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-112">[*Event consumers*](gloss-e.md) are applications or scripts that request notification of events, and then perform tasks when specific events occur.</span></span> <span data-ttu-id="f9b0f-113">Puede crear scripts o aplicaciones de supervisión de eventos que se supervisan temporalmente cuando se producen eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-113">You can create event monitoring scripts or applications that temporarily monitor when events occur.</span></span> <span data-ttu-id="f9b0f-114">WMI también proporciona un conjunto de proveedores de eventos permanentes preinstalados y las clases de consumidor permanentes que permiten supervisar eventos de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-114">WMI also supplies a set of preinstalled permanent event providers and the permanent consumer classes that enable you to permanently monitor events.</span></span> <span data-ttu-id="f9b0f-115">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-115">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="f9b0f-116">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="f9b0f-116">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="f9b0f-117">Usar consumidores de eventos temporales</span><span class="sxs-lookup"><span data-stu-id="f9b0f-117">Using Temporary Event Consumers</span></span>](#using-temporary-event-consumers)
-   [<span data-ttu-id="f9b0f-118">Uso de consumidores de eventos permanentes</span><span class="sxs-lookup"><span data-stu-id="f9b0f-118">Using Permanent Event Consumers</span></span>](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a><span data-ttu-id="f9b0f-119">Usar consumidores de eventos temporales</span><span class="sxs-lookup"><span data-stu-id="f9b0f-119">Using Temporary Event Consumers</span></span>

<span data-ttu-id="f9b0f-120">Los consumidores de eventos temporales son scripts o aplicaciones que devuelven los eventos que coinciden con una consulta o un filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-120">Temporary event consumers are scripts or applications that return the events that match an event query or filter.</span></span> <span data-ttu-id="f9b0f-121">Normalmente, las consultas de eventos temporales utilizan [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en aplicaciones de C++ o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) en scripts y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-121">Temporary event queries usually use either [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ applications or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in scripts and Visual Basic.</span></span>

<span data-ttu-id="f9b0f-122">Una consulta de eventos solicita instancias de una clase de eventos que especifica un tipo determinado de evento, como [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) o [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-122">An event query requests instances of an event class that specifies a certain type of event, such as [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="f9b0f-123">El siguiente ejemplo de código de VBScript solicita la notificación cuando se crea una instancia de [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="f9b0f-123">The following VBScript code example requests notification when an instance of [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) is created.</span></span> <span data-ttu-id="f9b0f-124">Se genera una instancia de esta clase cuando se inicia o se detiene un proceso.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-124">An instance of this class is generated when a process is started or stopped.</span></span>

<span data-ttu-id="f9b0f-125">Para ejecutar el script, cópielo en un archivo denominado event.vbs y use la siguiente línea de comandos: **cscript event.vbs**.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-125">To execute the script, copy it to a file named event.vbs and use the following command line: **cscript event.vbs**.</span></span> <span data-ttu-id="f9b0f-126">Puede ver la salida del script iniciando Notepad.exe o cualquier otro proceso.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-126">You can see output from the script by starting Notepad.exe or any other process.</span></span> <span data-ttu-id="f9b0f-127">El script se detiene una vez que se han iniciado o detenido cinco procesos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-127">The script stops after five processes have started or stopped.</span></span>

<span data-ttu-id="f9b0f-128">Este script llama a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), que es la versión [*semisincrónica*](gloss-s.md) del método.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-128">This script calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), which is the [*semisynchronous*](gloss-s.md) version of the method.</span></span> <span data-ttu-id="f9b0f-129">Vea el siguiente script para obtener un ejemplo de configuración de una suscripción de eventos temporal asincrónica mediante una llamada a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-129">See the next script for an example of setting up an asynchronous temporary event subscription by calling [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span> <span data-ttu-id="f9b0f-130">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-130">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="f9b0f-131">El script llama a [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para obtener y procesar cada evento a medida que llega.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-131">The script calls [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to obtain and process each event as it arrives.</span></span> <span data-ttu-id="f9b0f-132">Guarde el script en un archivo con la extensión. vbs y ejecute el script en una línea de comandos con CScript: **cscript file.vbs**.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-132">Save the script in a file with a .vbs extension and run the script on a command line using CScript: **cscript file.vbs**.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



Los consumidores de eventos temporales deben iniciarse manualmente y no deben conservarse entre los reinicios de WMI o los reinicios del sistema operativo. <span data-ttu-id="f9b0f-134">Un consumidor de eventos temporal solo puede procesar eventos mientras se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-134">A temporary event consumer can process events only while it is running.</span></span>

<span data-ttu-id="f9b0f-135">En el procedimiento siguiente se describe cómo crear un consumidor de eventos temporal.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-135">The following procedure describes how to create a temporary event consumer.</span></span>

<span data-ttu-id="f9b0f-136">**Para crear un consumidor de eventos temporal**</span><span class="sxs-lookup"><span data-stu-id="f9b0f-136">**To create a temporary event consumer**</span></span>

1.  <span data-ttu-id="f9b0f-137">Decida el lenguaje de programación que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-137">Decide which programming language to use.</span></span>

    <span data-ttu-id="f9b0f-138">El lenguaje de programación determina la API que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-138">The programming language determines the API to use.</span></span>

    -   <span data-ttu-id="f9b0f-139">Para el lenguaje de programación C++, utilice la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-139">For the C++ programming language, use the [COM API for WMI](com-api-for-wmi.md).</span></span>
    -   <span data-ttu-id="f9b0f-140">En el caso de Visual Basic o lenguajes de scripting, utilice la [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-140">For Visual Basic or scripting languages, use the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="f9b0f-141">Empiece a codificar una aplicación de consumidor de eventos temporal del mismo modo que inicia una aplicación WMI.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-141">Start coding a temporary event consumer application the same way that you start a WMI application.</span></span>

    <span data-ttu-id="f9b0f-142">Los primeros pasos de la codificación dependen del lenguaje de programación.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-142">The first steps of coding depend on the programming language.</span></span> <span data-ttu-id="f9b0f-143">Normalmente, se inicia sesión en WMI y se establece la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-143">Typically, you log onto WMI and set up the security settings.</span></span> <span data-ttu-id="f9b0f-144">Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-144">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

3.  <span data-ttu-id="f9b0f-145">Defina la consulta de eventos que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-145">Define the event query that you want to use.</span></span>

    <span data-ttu-id="f9b0f-146">Para obtener algunos tipos de datos de rendimiento, puede que necesite usar clases proporcionadas por proveedores de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-146">To obtain some types of performance data, you may need to use classes provided by high-performance providers.</span></span> <span data-ttu-id="f9b0f-147">Para obtener más información, vea [supervisar datos de rendimiento](monitoring-performance-data.md), [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md)y [realizar consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-147">For more information, see [Monitoring Performance Data](monitoring-performance-data.md), [Determining the Type of Event To Receive](determining-the-type-of-event-to-receive.md), and [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="f9b0f-148">Decida realizar una llamada asincrónica o una llamada semisincrónica y elija el método de la API.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-148">Decide to make either an asynchronous call or an semisynchronous call, and choose the API method.</span></span>

    <span data-ttu-id="f9b0f-149">Las llamadas asincrónicas le permiten evitar la sobrecarga que supone el sondeo de los datos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-149">Asynchronous calls allow you to avoid the overhead of polling for data.</span></span> <span data-ttu-id="f9b0f-150">Sin embargo, las llamadas sincrónicas proporcionan un rendimiento similar con mayor seguridad.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-150">However, semisynchronous calls provide similar performance with greater security.</span></span> <span data-ttu-id="f9b0f-151">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

5.  <span data-ttu-id="f9b0f-152">Realice la llamada al método asincrónico o semisincrónico e incluya una consulta de evento como el parámetro *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="f9b0f-152">Make the asynchronous or semisynchronous method call and include an event query as the *strQuery* parameter.</span></span>

    <span data-ttu-id="f9b0f-153">Para las aplicaciones de C++, llame a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9b0f-153">For C++ applications, call the following methods:</span></span>

    -   [<span data-ttu-id="f9b0f-154">**IWbemServices:: ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="f9b0f-154">**IWbemServices::ExecNotificationQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [<span data-ttu-id="f9b0f-155">**IWbemServices:: ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="f9b0f-155">**IWbemServices::ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    <span data-ttu-id="f9b0f-156">Para los scripts, llame a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9b0f-156">For scripts, call the following methods:</span></span>

    -   [<span data-ttu-id="f9b0f-157">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="f9b0f-157">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
    -   [<span data-ttu-id="f9b0f-158">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="f9b0f-158">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)

6.  <span data-ttu-id="f9b0f-159">Escriba el código para procesar el objeto de evento devuelto.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-159">Write the code to process the returned event object.</span></span>

    <span data-ttu-id="f9b0f-160">En el caso de las consultas de eventos asincrónicos, coloque el código en los distintos métodos o eventos del receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-160">For asynchronous event queries, put the code in the various methods or events of the object sink.</span></span> <span data-ttu-id="f9b0f-161">En el caso de las consultas de eventos semisincrónicas, cada objeto se devuelve a medida que WMI lo obtiene, por lo que el código debe estar en el bucle que controla cada objeto.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-161">For semisynchronous event queries, each object is returned as WMI obtains it, so the code should be in the loop that handles each object.</span></span>

<span data-ttu-id="f9b0f-162">El siguiente ejemplo de código de script es una versión asincrónica del [**script \_ ProcessTrace de Win32**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="f9b0f-162">The following script code example is an asynchronous version of the [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) script.</span></span> <span data-ttu-id="f9b0f-163">Dado que las operaciones asincrónicas se devuelven inmediatamente, un cuadro de diálogo mantiene el script activo mientras espera eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-163">Because asynchronous operations return immediately, a dialog box keeps the script active while it is waiting for events.</span></span>

<span data-ttu-id="f9b0f-164">En lugar de llamar a [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para recibir cada evento, el script tiene un controlador de eventos para el evento [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b0f-164">Rather than call [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to receive each event, the script has an event handler for the [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) event.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> <span data-ttu-id="f9b0f-165">Una devolución de llamada asincrónica, como una devolución de llamada administrada por la `SINK_OnObjectReady` subrutina, permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-165">An asynchronous callback such as a callback handled by the `SINK_OnObjectReady` subroutine, allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="f9b0f-166">Para mejorar la seguridad, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-166">For better security, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="f9b0f-167">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9b0f-167">For more information, see the following topics:</span></span>
>
> -   [<span data-ttu-id="f9b0f-168">Realización de una llamada semisincrónica con C++</span><span class="sxs-lookup"><span data-stu-id="f9b0f-168">Making a Semisynchronous Call with C++</span></span>](making-a-semisynchronous-call-with-c--.md)
> -   [<span data-ttu-id="f9b0f-169">Realización de una llamada semisincrónica con VBScript</span><span class="sxs-lookup"><span data-stu-id="f9b0f-169">Making a Semisynchronous Call with VBScript</span></span>](making-a-semisynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="f9b0f-170">Realización de una llamada asincrónica con C++</span><span class="sxs-lookup"><span data-stu-id="f9b0f-170">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
> -   [<span data-ttu-id="f9b0f-171">Realización de una llamada asincrónica con VBScript</span><span class="sxs-lookup"><span data-stu-id="f9b0f-171">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="f9b0f-172">Establecer la seguridad en una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="f9b0f-172">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
> -   [<span data-ttu-id="f9b0f-173">Protección de los clientes de scripting</span><span class="sxs-lookup"><span data-stu-id="f9b0f-173">Securing Scripting Clients</span></span>](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a><span data-ttu-id="f9b0f-174">Uso de consumidores de eventos permanentes</span><span class="sxs-lookup"><span data-stu-id="f9b0f-174">Using Permanent Event Consumers</span></span>

<span data-ttu-id="f9b0f-175">Un consumidor de eventos permanente se ejecuta hasta que su registro se cancela explícitamente y, a continuación, se inicia cuando WMI o el sistema se reinicia.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-175">A permanent event consumer runs until its registration is explicitly canceled, and then starts up when WMI or the system restarts.</span></span>

<span data-ttu-id="f9b0f-176">Un consumidor de eventos permanente es una combinación de clases de WMI, filtros y objetos COM de un sistema.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-176">A permanent event consumer is a combination of WMI classes, filters, and COM objects on a system.</span></span>

<span data-ttu-id="f9b0f-177">En la lista siguiente se identifican los elementos necesarios para crear un consumidor de eventos permanente:</span><span class="sxs-lookup"><span data-stu-id="f9b0f-177">The following list identifies the parts required to create a permanent event consumer:</span></span>

-   <span data-ttu-id="f9b0f-178">Objeto COM que contiene el código que implementa el consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-178">A COM object containing the code that implements the permanent consumer.</span></span>
-   <span data-ttu-id="f9b0f-179">Nueva clase de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-179">A new permanent consumer class.</span></span>
-   <span data-ttu-id="f9b0f-180">Instancia de la clase de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-180">An instance of the permanent consumer class.</span></span>
-   <span data-ttu-id="f9b0f-181">Filtro que contiene la consulta de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-181">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="f9b0f-182">Un vínculo entre el consumidor y el filtro.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-182">A link between the consumer and the filter.</span></span>

<span data-ttu-id="f9b0f-183">Para obtener más información, consulte [recibir eventos en todo momento](--filtertoconsumerbinding.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-183">For more information, see [Receiving Events At All Times](--filtertoconsumerbinding.md).</span></span>

<span data-ttu-id="f9b0f-184">WMI proporciona varios consumidores permanentes.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-184">WMI supplies several permanent consumers.</span></span> <span data-ttu-id="f9b0f-185">Las clases de consumidor y el objeto COM que contiene el código están preinstalados.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-185">The consumer classes and COM object containing the code are preinstalled.</span></span> <span data-ttu-id="f9b0f-186">Por ejemplo, puede crear y configurar una instancia de la clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para ejecutar un script cuando se produce un evento.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-186">For example, you can create and configure an instance of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to run a script when an event occurs.</span></span> <span data-ttu-id="f9b0f-187">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-187">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="f9b0f-188">Para obtener un ejemplo del uso de **ActiveScriptEventConsumer**, vea [ejecutar un script basado en un evento](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-188">For an example of using **ActiveScriptEventConsumer**, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>

<span data-ttu-id="f9b0f-189">En el procedimiento siguiente se describe cómo crear un consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-189">The following procedure describes how to create a permanent event consumer.</span></span>

<span data-ttu-id="f9b0f-190">**Para crear un consumidor de eventos permanente**</span><span class="sxs-lookup"><span data-stu-id="f9b0f-190">**To create a permanent event consumer**</span></span>

1.  <span data-ttu-id="f9b0f-191">[Registre el proveedor de eventos](registering-a-provider.md) con el espacio de nombres que está usando.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-191">[Register the event provider](registering-a-provider.md) with the namespace that you are using.</span></span>

    <span data-ttu-id="f9b0f-192">Algunos proveedores de eventos solo pueden usar un espacio de nombres específico.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-192">Some event providers can only use a specific namespace.</span></span> <span data-ttu-id="f9b0f-193">Por ejemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) es un evento intrínseco que es compatible con el [proveedor de Win32](/windows/desktop/CIMWin32Prov/win32-provider) y se registra de forma predeterminada con el \\ espacio de \\ nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-193">For example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md) is an intrinsic event that is supported by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider) and is registered by default with the \\root\\cimv2 namespace.</span></span>

    > [!Note]  
    > <span data-ttu-id="f9b0f-194">Puede usar la propiedad **EventNamespace** de [**\_ \_ EventFilter**](--eventfilter.md) que se usa en el registro para crear una suscripción entre espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-194">You can use the **EventNamespace** property of the [**\_\_EventFilter**](--eventfilter.md) used in the registration to create a cross-namespace subscription.</span></span> <span data-ttu-id="f9b0f-195">Para obtener más información, consulte [implementación de suscripciones de eventos permanentes entre espacios de nombres](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-195">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

     

2.  <span data-ttu-id="f9b0f-196">[Registre el proveedor del consumidor de eventos](registering-an-event-consumer-provider.md) con el espacio de nombres donde se encuentran las clases de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-196">[Register the event consumer provider](registering-an-event-consumer-provider.md) with the namespace where event classes are located.</span></span>

    <span data-ttu-id="f9b0f-197">WMI usa un proveedor de consumidor de eventos para buscar un consumidor de eventos que sea permanente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-197">WMI uses an event consumer provider to find an event consumer that is permanent.</span></span> <span data-ttu-id="f9b0f-198">El consumidor de eventos permanente es la aplicación que WMI inicia cuando se recibe un evento.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-198">The permanent event consumer is the application that WMI starts when an event is received.</span></span> <span data-ttu-id="f9b0f-199">Para registrar el consumidor de eventos, los proveedores crean instancias de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-199">To register event consumer, providers create instances of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span>

3.  <span data-ttu-id="f9b0f-200">Cree una instancia de la clase que represente el consumidor de eventos permanente que desee usar.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-200">Create an instance of the class that represents the permanent event consumer you want to use.</span></span>

    <span data-ttu-id="f9b0f-201">Las clases de consumidor de eventos se derivan de la clase [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-201">Event consumer classes are derived from the class [**\_\_EventConsumer**](--eventconsumer.md).</span></span> <span data-ttu-id="f9b0f-202">Establezca las propiedades que requiere la instancia del consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-202">Set the properties that the event consumer instance requires.</span></span>

4.  <span data-ttu-id="f9b0f-203">Registre el consumidor con COM mediante la utilidad **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="f9b0f-203">Register the consumer with COM by using the **regsvr32** utility.</span></span>
5.  <span data-ttu-id="f9b0f-204">Cree una instancia de la clase de filtro de eventos [**\_ \_ EventFilter**](--eventfilter.md).</span><span class="sxs-lookup"><span data-stu-id="f9b0f-204">Create an instance of the event filter class [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="f9b0f-205">Establezca los campos obligatorios para la instancia de filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-205">Set the required fields for the event filter instance.</span></span> <span data-ttu-id="f9b0f-206">Los campos obligatorios para [**\_ \_ EventFilter**](--eventfilter.md) son **nombre**, **QueryLanguage** y **consulta**.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-206">The required fields for [**\_\_EventFilter**](--eventfilter.md) are **Name**, **QueryLanguage**, and **Query**.</span></span> <span data-ttu-id="f9b0f-207">La propiedad **Name** puede ser cualquier nombre único de una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-207">The **Name** property can be any unique name for an instance of this class.</span></span> <span data-ttu-id="f9b0f-208">La propiedad **QueryLanguage** siempre se establece en "WQL".</span><span class="sxs-lookup"><span data-stu-id="f9b0f-208">The **QueryLanguage** property is always set to "WQL".</span></span> <span data-ttu-id="f9b0f-209">La propiedad de **consulta** es una cadena que contiene una consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-209">The **Query** property is a string that contains an event query.</span></span> <span data-ttu-id="f9b0f-210">Se genera un evento cuando se produce un error en la consulta del consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-210">An event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="f9b0f-211">El origen del evento es WinMgmt, el ID. de evento es 10 y el tipo de evento es error.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-211">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="f9b0f-212">Cree una instancia de la clase [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar un consumidor de eventos lógicos a un filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-212">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class to associate a logical event consumer with an event filter.</span></span>

    <span data-ttu-id="f9b0f-213">WMI utiliza una asociación para buscar el consumidor de eventos asociado al evento que coincide con los criterios especificados en el filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-213">WMI uses an association to find the event consumer associated with the event that matches the criteria specified in the event filter.</span></span> <span data-ttu-id="f9b0f-214">WMI utiliza el proveedor de consumidor de eventos para encontrar la aplicación de consumidor de eventos permanente que se va a iniciar.</span><span class="sxs-lookup"><span data-stu-id="f9b0f-214">WMI uses the event consumer provider to find the permanent event consumer application to start.</span></span>

 

 
