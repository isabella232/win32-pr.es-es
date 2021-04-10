---
description: WMI contiene una infraestructura de eventos que genera notificaciones sobre los cambios en los datos y servicios de WMI. Las clases de eventos WMI proporcionan una notificación cuando se producen eventos específicos.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Recibir un evento de WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155861"
---
# <a name="receiving-a-wmi-event"></a><span data-ttu-id="4bf7c-104">Recibir un evento de WMI</span><span class="sxs-lookup"><span data-stu-id="4bf7c-104">Receiving a WMI Event</span></span>

<span data-ttu-id="4bf7c-105">WMI contiene una infraestructura de eventos que genera notificaciones sobre los cambios en los datos y servicios de WMI.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-105">WMI contains an event infrastructure that produces notifications about changes in WMI data and services.</span></span> <span data-ttu-id="4bf7c-106">[*Las clases de eventos*](gloss-e.md) WMI proporcionan una notificación cuando se producen eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-106">WMI [*event classes*](gloss-e.md) provide notification when specific events occur.</span></span>

<span data-ttu-id="4bf7c-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="4bf7c-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="4bf7c-108">Consultas de eventos</span><span class="sxs-lookup"><span data-stu-id="4bf7c-108">Event Queries</span></span>](#event-queries)
-   [<span data-ttu-id="4bf7c-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bf7c-109">Example</span></span>](#example)
-   [<span data-ttu-id="4bf7c-110">Consumidores de eventos</span><span class="sxs-lookup"><span data-stu-id="4bf7c-110">Event Consumers</span></span>](#event-consumers)
-   [<span data-ttu-id="4bf7c-111">Proporcionar eventos</span><span class="sxs-lookup"><span data-stu-id="4bf7c-111">Providing Events</span></span>](#providing-events)
-   [<span data-ttu-id="4bf7c-112">Cuotas de suscripción</span><span class="sxs-lookup"><span data-stu-id="4bf7c-112">Subscription Quotas</span></span>](#subscription-quotas)
-   [<span data-ttu-id="4bf7c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bf7c-113">Related topics</span></span>](#related-topics)

## <a name="event-queries"></a><span data-ttu-id="4bf7c-114">Consultas de eventos</span><span class="sxs-lookup"><span data-stu-id="4bf7c-114">Event Queries</span></span>

<span data-ttu-id="4bf7c-115">Puede crear una consulta [semisincrónica](receiving-synchronous-and-semisynchronous-event-notifications.md) o [**asincrónica**](receiving-asynchronous-event-notifications.md) para supervisar los cambios en los registros de eventos, la creación de procesos, el estado del servicio, la disponibilidad del equipo o el espacio libre en la unidad de disco, y otras entidades o eventos.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-115">You can create a [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) or [**asynchronous**](receiving-asynchronous-event-notifications.md) query to monitor changes to event logs, process creation, service status, computer availability or disk drive free space, and other entities or events.</span></span> <span data-ttu-id="4bf7c-116">En scripting, el método [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) se usa para suscribirse a eventos.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-116">In scripting, the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method is used to subscribe to events.</span></span> <span data-ttu-id="4bf7c-117">En C++, se utiliza [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="4bf7c-117">In C++, [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) is used.</span></span> <span data-ttu-id="4bf7c-118">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-118">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4bf7c-119">La notificación de un cambio en el modelo de datos WMI estándar se denomina [*evento intrínseco*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-119">Notification of a change in the standard WMI data model is called an [*intrinsic event*](gloss-i.md).</span></span> <span data-ttu-id="4bf7c-120">[**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) o [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) son ejemplos de eventos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-120">[**\_\_InstanceCreationEvent**](--instancecreationevent.md) or [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md) are examples of intrinsic events.</span></span> <span data-ttu-id="4bf7c-121">La notificación de un cambio que realiza un proveedor para definir un evento de proveedor se denomina [*evento extrínseco*](gloss-e.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-121">Notification of a change that a provider makes to define a provider event is called an [*extrinsic event*](gloss-e.md).</span></span> <span data-ttu-id="4bf7c-122">Por ejemplo, el proveedor de [registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), el [proveedor de eventos de administración de energía](/windows/desktop/CIMWin32Prov/power-management-event-provider)y el proveedor de [Win32](/windows/desktop/CIMWin32Prov/win32-provider) definen sus propios eventos.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-122">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), [Power Management Event Provider](/windows/desktop/CIMWin32Prov/power-management-event-provider), and [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) define their own events.</span></span> <span data-ttu-id="4bf7c-123">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-123">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

## <a name="example"></a><span data-ttu-id="4bf7c-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bf7c-124">Example</span></span>

<span data-ttu-id="4bf7c-125">El siguiente ejemplo de código de script es una consulta para el [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrínseco de la clase de evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-125">The following script code example is a query for the intrinsic [**\_\_InstanceCreationEvent**](--instancecreationevent.md) of the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="4bf7c-126">Puede ejecutar este programa en segundo plano y, cuando se produce un evento, aparece un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-126">You can run this program in the background and when there is an event, a message appears.</span></span> <span data-ttu-id="4bf7c-127">Si cierra el cuadro **de diálogo esperando eventos** , el programa deja de esperar los eventos.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-127">If you close the **Waiting for events** dialog box, the program stops waiting for events.</span></span> <span data-ttu-id="4bf7c-128">Tenga en cuenta que **SeSecurityPrivilege** debe estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-128">Be aware that the **SeSecurityPrivilege** must be enabled.</span></span>


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





<span data-ttu-id="4bf7c-129">En el ejemplo de código de VBScript siguiente se muestra el evento extrínseco [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) que define el proveedor del registro.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-129">The following VBScript code example shows the extrinsic event [\_\_RegistryValueChangeEvent](registering-for-system-registry-events.md) that the registry provider defines.</span></span> <span data-ttu-id="4bf7c-130">El script crea un consumidor temporal mediante la llamada a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)y solo recibe eventos cuando se ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-130">The script creates a temporary consumer by using the call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md), and only receives events when the script is running.</span></span> <span data-ttu-id="4bf7c-131">El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-131">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="4bf7c-132">Para detener el script manualmente, use el administrador de tareas para detener el proceso.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-132">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="4bf7c-133">Para detenerlo mediante programación, use el método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) en la clase de proceso de Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="4bf7c-133">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span> <span data-ttu-id="4bf7c-134">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-134">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a><span data-ttu-id="4bf7c-135">Consumidores de eventos</span><span class="sxs-lookup"><span data-stu-id="4bf7c-135">Event Consumers</span></span>

<span data-ttu-id="4bf7c-136">Puede supervisar o consumir eventos mediante los siguientes consumidores mientras se ejecuta un script o una aplicación:</span><span class="sxs-lookup"><span data-stu-id="4bf7c-136">You can monitor or consume events using the following consumers while a script or application is running:</span></span>

-   <span data-ttu-id="4bf7c-137">Consumidores de eventos temporales</span><span class="sxs-lookup"><span data-stu-id="4bf7c-137">Temporary event consumers</span></span>

    <span data-ttu-id="4bf7c-138">Un [*consumidor temporal*](gloss-t.md) es una aplicación cliente de WMI que recibe un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-138">A [*temporary consumer*](gloss-t.md) is a WMI client application that receives a WMI event.</span></span> <span data-ttu-id="4bf7c-139">WMI incluye una interfaz única que se utiliza para especificar los eventos que WMI envía a una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-139">WMI includes a unique interface that use to specify the events for WMI to send to a client application.</span></span> <span data-ttu-id="4bf7c-140">Un consumidor de eventos temporal se considera temporal porque solo funciona cuando lo carga específicamente un usuario.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-140">A temporary event consumer is considered temporary because it only works when specifically loaded by a user.</span></span> <span data-ttu-id="4bf7c-141">Para obtener más información, consulte [recepción de eventos para la duración de la aplicación](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-141">For more information, see [Receiving Events for the Duration of Your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>

-   <span data-ttu-id="4bf7c-142">Consumidores de eventos permanentes</span><span class="sxs-lookup"><span data-stu-id="4bf7c-142">Permanent event consumers</span></span>

    <span data-ttu-id="4bf7c-143">Un [*consumidor permanente*](gloss-p.md) es un objeto com que puede recibir un evento WMI en todo momento.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-143">A [*permanent consumer*](gloss-p.md) is a COM object that can receive a WMI event at all times.</span></span> <span data-ttu-id="4bf7c-144">Un consumidor de eventos permanente utiliza un conjunto de objetos y filtros persistentes para capturar un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-144">A permanent event consumer uses a set of persistent objects and filters to capture a WMI event.</span></span> <span data-ttu-id="4bf7c-145">Al igual que un consumidor de eventos temporal, se configura una serie de objetos y filtros WMI que capturan un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-145">Like a temporary event consumer, you set up a series of WMI objects and filters that capture a WMI event.</span></span> <span data-ttu-id="4bf7c-146">Cuando se produce un evento que coincide con un filtro, WMI carga el consumidor de eventos permanente y lo notifica sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-146">When an event occurs that matches a filter, WMI loads the permanent event consumer and notifies it about the event.</span></span> <span data-ttu-id="4bf7c-147">Dado que un consumidor permanente está implementado en el repositorio WMI y es un archivo ejecutable que se registra en WMI, el consumidor de eventos permanente opera y recibe los eventos una vez creado, e incluso después de reiniciar el sistema operativo, siempre y cuando WMI se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-147">Because a permanent consumer is implemented in the WMI repository and is an executable file that is registered in WMI, the permanent event consumer operates and receives events after it is created and even after a reboot of the operating system as long as WMI is running.</span></span> <span data-ttu-id="4bf7c-148">Para obtener más información, consulte [recibir eventos en todo momento](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-148">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

<span data-ttu-id="4bf7c-149">Los scripts o las aplicaciones que reciben eventos tienen consideraciones de seguridad especiales.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-149">Scripts or applications that receive events have special security considerations.</span></span> <span data-ttu-id="4bf7c-150">Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-150">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="4bf7c-151">Una aplicación o un script puede usar un proveedor de eventos WMI integrado que proporciona [clases de consumidor estándar](standard-consumer-classes.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-151">An application or script can use a built-in WMI event provider that supplies [standard consumer classes](standard-consumer-classes.md).</span></span> <span data-ttu-id="4bf7c-152">Cada clase de consumidor estándar responde a un evento con una acción diferente mediante el envío de un mensaje de correo electrónico o la ejecución de un script.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-152">Each standard consumer class responds to an event with a different action by sending an email message or executing a script.</span></span> <span data-ttu-id="4bf7c-153">No es necesario escribir código de proveedor para usar una clase de consumidor estándar para crear un consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-153">You do not have to write provider code to use a standard consumer class to create a permanent event consumer.</span></span> <span data-ttu-id="4bf7c-154">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-154">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="providing-events"></a><span data-ttu-id="4bf7c-155">Proporcionar eventos</span><span class="sxs-lookup"><span data-stu-id="4bf7c-155">Providing Events</span></span>

<span data-ttu-id="4bf7c-156">Un proveedor de eventos es un componente COM que envía un evento a WMI.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-156">An event provider is a COM component that sends an event to WMI.</span></span> <span data-ttu-id="4bf7c-157">Puede crear un proveedor de eventos para enviar un evento en una aplicación de C++ o C#.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-157">You can create an event provider to send an event in a C++ or C# application.</span></span> <span data-ttu-id="4bf7c-158">La mayoría de los proveedores de eventos administran un objeto para WMI, por ejemplo, una aplicación o un elemento de hardware.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-158">Most event providers manage an object for WMI, for example, an application or hardware item.</span></span> <span data-ttu-id="4bf7c-159">Para obtener más información, consulte [escribir un proveedor de eventos](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-159">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="4bf7c-160">Un evento de tiempo o repetición es un evento que se produce en un tiempo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-160">A timed or repeating event is an event that occurs at a predetermined time.</span></span>

<span data-ttu-id="4bf7c-161">WMI proporciona las siguientes formas de crear eventos de tiempo o repetición para las aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="4bf7c-161">WMI provides the following ways to create timed or repeating events for your applications:</span></span>

-   <span data-ttu-id="4bf7c-162">La infraestructura de eventos estándar de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-162">The standard Microsoft event infrastructure.</span></span>
-   <span data-ttu-id="4bf7c-163">Una clase de temporizador especializada.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-163">A specialized timer class.</span></span>

<span data-ttu-id="4bf7c-164">Para obtener más información, consulte [recibir un evento con tiempo o repetir](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-164">For more information, see [Receiving a Timed or Repeating Event](receiving-a-timed-or-repeating-event.md).</span></span> <span data-ttu-id="4bf7c-165">Al escribir un proveedor de eventos, tenga en cuenta la información de seguridad identificada en [proporcionar eventos de forma segura](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-165">When you write an event provider, consider the security information identified in [Providing Events Securely](providing-events-securely.md).</span></span>

<span data-ttu-id="4bf7c-166">Se recomienda que las suscripciones de eventos permanentes se compilen en el espacio de nombres de la \\ \\ suscripción raíz.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-166">It is recommended that permanent event subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="4bf7c-167">Para obtener más información, consulte [implementación de suscripciones de eventos permanentes entre espacios de nombres](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-167">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

## <a name="subscription-quotas"></a><span data-ttu-id="4bf7c-168">Cuotas de suscripción</span><span class="sxs-lookup"><span data-stu-id="4bf7c-168">Subscription Quotas</span></span>

<span data-ttu-id="4bf7c-169">El sondeo de eventos puede degradar el rendimiento de los proveedores que admiten consultas en conjuntos de datos de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-169">Polling for events can degrade performance for providers that support queries over huge data sets.</span></span> <span data-ttu-id="4bf7c-170">Además, cualquier usuario que tenga acceso de lectura a un espacio de nombres con proveedores dinámicos puede realizar un ataque de denegación de servicio (DoS).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-170">Additionally, any user that has read access to a namespace with dynamic providers can perform a denial of service (DoS) attack.</span></span> <span data-ttu-id="4bf7c-171">WMI mantiene cuotas para todos los usuarios combinados y para cada consumidor de eventos en la única instancia de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) que se encuentra en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-171">WMI maintains quotas for all of the users combined and for each event consumer in the single instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md) located in the \\root namespace.</span></span> <span data-ttu-id="4bf7c-172">Estas cuotas son globales en lugar de para cada espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-172">These quotas are global rather than for each namespace.</span></span> <span data-ttu-id="4bf7c-173">No se pueden cambiar las cuotas.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-173">You cannot change the quotas.</span></span>

<span data-ttu-id="4bf7c-174">WMI actualmente aplica cuotas mediante las propiedades de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-174">WMI currently enforces quotas using the properties of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="4bf7c-175">Cada cuota tiene un por usuario y una versión total que incluye todos los usuarios combinados, no por espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-175">Each quota has a per user and a total version that includes all users combined, not per namespace.</span></span> <span data-ttu-id="4bf7c-176">En la tabla siguiente se enumeran las cuotas que se aplican a las propiedades de **\_ \_ ArbitratorConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="4bf7c-176">The following table lists the quotas that apply to the **\_\_ArbitratorConfiguration** properties.</span></span>



| <span data-ttu-id="4bf7c-177">Total/perusuario</span><span class="sxs-lookup"><span data-stu-id="4bf7c-177">Total/PerUser</span></span>                                                                   | <span data-ttu-id="4bf7c-178">Quota</span><span class="sxs-lookup"><span data-stu-id="4bf7c-178">Quota</span></span>                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="4bf7c-179">TemporarySubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="4bf7c-179">TemporarySubscriptionsTotal</span></span><br/> <span data-ttu-id="4bf7c-180">TemporarySubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="4bf7c-180">TemporarySubscriptionsPerUser</span></span><br/> | <span data-ttu-id="4bf7c-181">10 000</span><span class="sxs-lookup"><span data-stu-id="4bf7c-181">10,000</span></span><br/> <span data-ttu-id="4bf7c-182">1,000</span><span class="sxs-lookup"><span data-stu-id="4bf7c-182">1,000</span></span><br/>                                          |
| <span data-ttu-id="4bf7c-183">PermanentSubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="4bf7c-183">PermanentSubscriptionsTotal</span></span><br/> <span data-ttu-id="4bf7c-184">PermanentSubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="4bf7c-184">PermanentSubscriptionsPerUser</span></span><br/> | <span data-ttu-id="4bf7c-185">10 000</span><span class="sxs-lookup"><span data-stu-id="4bf7c-185">10,000</span></span><br/> <span data-ttu-id="4bf7c-186">1,000</span><span class="sxs-lookup"><span data-stu-id="4bf7c-186">1,000</span></span><br/>                                          |
| <span data-ttu-id="4bf7c-187">PollingInstructionsTotal</span><span class="sxs-lookup"><span data-stu-id="4bf7c-187">PollingInstructionsTotal</span></span><br/> <span data-ttu-id="4bf7c-188">PollingInstructionsPerUser</span><span class="sxs-lookup"><span data-stu-id="4bf7c-188">PollingInstructionsPerUser</span></span><br/>       | <span data-ttu-id="4bf7c-189">10 000</span><span class="sxs-lookup"><span data-stu-id="4bf7c-189">10,000</span></span><br/> <span data-ttu-id="4bf7c-190">1,000</span><span class="sxs-lookup"><span data-stu-id="4bf7c-190">1,000</span></span><br/>                                          |
| <span data-ttu-id="4bf7c-191">PollingMemoryTotal</span><span class="sxs-lookup"><span data-stu-id="4bf7c-191">PollingMemoryTotal</span></span><br/> <span data-ttu-id="4bf7c-192">PollingMemoryPerUser</span><span class="sxs-lookup"><span data-stu-id="4bf7c-192">PollingMemoryPerUser</span></span><br/>                   | <span data-ttu-id="4bf7c-193">10 millones (0x989680) bytes</span><span class="sxs-lookup"><span data-stu-id="4bf7c-193">10,000,000 (0x989680) bytes</span></span><br/> <span data-ttu-id="4bf7c-194">5 millones (0x4CB40) bytes</span><span class="sxs-lookup"><span data-stu-id="4bf7c-194">5,000,000 (0x4CB40) bytes</span></span><br/> |



 

<span data-ttu-id="4bf7c-195">Un administrador o un usuario con permiso de **\_ escritura completo** en el espacio de nombres puede modificar la instancia singleton de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4bf7c-195">An administrator or a user with **FULL\_WRITE** permission in the namespace can modify the singleton instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="4bf7c-196">WMI realiza un seguimiento de la cuota por usuario.</span><span class="sxs-lookup"><span data-stu-id="4bf7c-196">WMI tracks the per-user quota.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bf7c-197">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bf7c-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf7c-198">Usar WMI</span><span class="sxs-lookup"><span data-stu-id="4bf7c-198">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

