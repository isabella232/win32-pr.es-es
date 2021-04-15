---
description: La notificación de eventos asincrónicos es una técnica que permite a una aplicación supervisar constantemente eventos sin monopolizar los recursos del sistema.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Recibir notificaciones de eventos asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648498"
---
# <a name="receiving-asynchronous-event-notifications"></a><span data-ttu-id="270fe-103">Recibir notificaciones de eventos asincrónicas</span><span class="sxs-lookup"><span data-stu-id="270fe-103">Receiving Asynchronous Event Notifications</span></span>

<span data-ttu-id="270fe-104">La notificación de eventos asincrónicos es una técnica que permite a una aplicación supervisar constantemente eventos sin monopolizar los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="270fe-104">Asynchronous event notification is a technique that allows an application to constantly monitor events without monopolizing system resources.</span></span> <span data-ttu-id="270fe-105">Las notificaciones de eventos asincrónicos tienen las mismas limitaciones de seguridad que otras llamadas asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="270fe-105">Asynchronous event notifications have the same security limitations that other asynchronous calls have.</span></span> <span data-ttu-id="270fe-106">En su lugar, puede realizar llamadas semisincrónicas.</span><span class="sxs-lookup"><span data-stu-id="270fe-106">You can make semisynchronous calls instead.</span></span> <span data-ttu-id="270fe-107">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="270fe-108">La cola de eventos asincrónicos enrutados a un cliente tiene la posibilidad de crecer excepcionalmente grande.</span><span class="sxs-lookup"><span data-stu-id="270fe-108">The queue of asynchronous events routed to a client has the potential to grow exceptionally large.</span></span> <span data-ttu-id="270fe-109">Por lo tanto, WMI implementa una directiva de todo el sistema para evitar quedarse sin memoria.</span><span class="sxs-lookup"><span data-stu-id="270fe-109">Therefore, WMI implements a system-wide policy to avoid running out of memory.</span></span> <span data-ttu-id="270fe-110">WMI ralentiza eventos o comienza a quitar eventos de la cola cuando la cola crece más allá de un tamaño determinado.</span><span class="sxs-lookup"><span data-stu-id="270fe-110">WMI either slows down events, or starts dropping events from the queue when the queue grows past a certain size.</span></span>

<span data-ttu-id="270fe-111">WMI utiliza las propiedades [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) y [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) de la clase [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para establecer límites en la prevención de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="270fe-111">WMI uses the [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) and [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) properties of the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) class to set limits on out-of-memory avoidance.</span></span> <span data-ttu-id="270fe-112">El valor mínimo indica cuándo WMI debería empezar a ralentizar la notificación de eventos y el valor máximo indica cuándo se debe iniciar la eliminación de eventos.</span><span class="sxs-lookup"><span data-stu-id="270fe-112">The minimum value indicates when WMI should start slowing event notification, and the maximum value indicates when to start dropping events.</span></span> <span data-ttu-id="270fe-113">Los valores predeterminados para los umbrales inferior y superior son 1 millón (10 MB) y 2 millones (20 MB).</span><span class="sxs-lookup"><span data-stu-id="270fe-113">The default values for the low and high thresholds are 1000000 (10 MB) and 2000000 (20 MB).</span></span> <span data-ttu-id="270fe-114">Además, puede establecer la propiedad [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para describir la cantidad de tiempo que WMI debe esperar antes de quitar los eventos.</span><span class="sxs-lookup"><span data-stu-id="270fe-114">In addition, you can set the [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property to describe the amount of time WMI should wait before dropping events.</span></span> <span data-ttu-id="270fe-115">El valor predeterminado de **MaxWaitOnEvents** es 2000 o 2 segundos.</span><span class="sxs-lookup"><span data-stu-id="270fe-115">The default value for **MaxWaitOnEvents** is 2000, or 2 seconds.</span></span>

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a><span data-ttu-id="270fe-116">Recibir notificaciones de eventos asincrónicas en VBScript</span><span class="sxs-lookup"><span data-stu-id="270fe-116">Receiving Asynchronous Event Notifications in VBScript</span></span>

<span data-ttu-id="270fe-117">Las llamadas de scripting para recibir notificaciones de eventos son esencialmente las mismas que todas las llamadas asincrónicas con los mismos problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="270fe-117">The scripting calls to receive event notifications are essentially the same as all asynchronous calls with the same security issues.</span></span> <span data-ttu-id="270fe-118">Para obtener más información, vea [crear una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-118">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="270fe-119">**Para recibir notificaciones de eventos asincrónicos en VBScript**</span><span class="sxs-lookup"><span data-stu-id="270fe-119">**To receive asynchronous event notifications in VBScript**</span></span>

1.  <span data-ttu-id="270fe-120">Cree un objeto de receptor llamando a [Wscript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) y especificando el ProgID de "WbemScripting" y el tipo de objeto de [**SWbemSink**](swbemsink.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-120">Create a sink object by calling [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and specifying the progid of "WbemScripting" and the object type of [**SWbemSink**](swbemsink.md).</span></span> <span data-ttu-id="270fe-121">El objeto receptor recibe las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="270fe-121">The sink object receives the notifications.</span></span>
2.  <span data-ttu-id="270fe-122">Escriba una subrutina para cada evento que desee controlar.</span><span class="sxs-lookup"><span data-stu-id="270fe-122">Write a subroutine for each event you want to handle.</span></span> <span data-ttu-id="270fe-123">En la tabla siguiente se enumeran los eventos de [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="270fe-123">The following table lists the [**SWbemSink**](swbemsink.md) events.</span></span>

    

    | <span data-ttu-id="270fe-124">Evento</span><span class="sxs-lookup"><span data-stu-id="270fe-124">Event</span></span>                                            | <span data-ttu-id="270fe-125">Significado</span><span class="sxs-lookup"><span data-stu-id="270fe-125">Meaning</span></span>                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="270fe-126">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="270fe-126">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="270fe-127">Notifica las devoluciones de un objeto al receptor.</span><span class="sxs-lookup"><span data-stu-id="270fe-127">Reports the returns of an object to the sink.</span></span> <span data-ttu-id="270fe-128">El uso de esta llamada devuelve un objeto cada vez hasta que se completa la operación.</span><span class="sxs-lookup"><span data-stu-id="270fe-128">Using this call returns one object each time until the operation is complete.</span></span>     |
    | [<span data-ttu-id="270fe-129">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="270fe-129">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="270fe-130">Informa cuando se completa una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="270fe-130">Reports when an asynchronous call is complete.</span></span> <span data-ttu-id="270fe-131">Este evento nunca se produce si la operación es indefinida.</span><span class="sxs-lookup"><span data-stu-id="270fe-131">This event never occurs if the operation is indefinite.</span></span>                          |
    | [<span data-ttu-id="270fe-132">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="270fe-132">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="270fe-133">Informa de la finalización de una operación PUT asincrónica.</span><span class="sxs-lookup"><span data-stu-id="270fe-133">Reports the completion of an asynchronous put operation.</span></span> <span data-ttu-id="270fe-134">Este evento devuelve la ruta de acceso del objeto de la instancia o la clase guardada.</span><span class="sxs-lookup"><span data-stu-id="270fe-134">This event returns the object path of the instance or the saved class.</span></span> |
    | [<span data-ttu-id="270fe-135">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="270fe-135">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="270fe-136">Informa del estado de una llamada asincrónica que está en curso.</span><span class="sxs-lookup"><span data-stu-id="270fe-136">Reports the status of an asynchronous call that is in progress.</span></span> <span data-ttu-id="270fe-137">No todos los proveedores admiten informes de progreso provisional.</span><span class="sxs-lookup"><span data-stu-id="270fe-137">Not all providers support interim progress reports.</span></span>             |
    | [<span data-ttu-id="270fe-138">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="270fe-138">**Cancel**</span></span>](swbemsink-cancel.md)               | <span data-ttu-id="270fe-139">Cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="270fe-139">Cancels all of the outstanding asynchronous operations associated with this object sink.</span></span>                                        |

    

     

<span data-ttu-id="270fe-140">En el siguiente ejemplo de código de VBScript se notifica la eliminación de procesos con un intervalo de sondeo de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="270fe-140">The following VBScript code example notifies the deletion of processes with a 10 second polling interval.</span></span> <span data-ttu-id="270fe-141">En este script, el receptor de subrutinas \_ OnObjectReady controla la repetición del evento.</span><span class="sxs-lookup"><span data-stu-id="270fe-141">In this script, the subroutine SINK\_OnObjectReady handles the event occurrence.</span></span> <span data-ttu-id="270fe-142">En el ejemplo, el objeto receptor se denomina "Sink"; sin embargo, puede asignar un nombre a este objeto como elija.</span><span class="sxs-lookup"><span data-stu-id="270fe-142">In the example, the sink object is named "Sink", however you can name this object as you choose.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a><span data-ttu-id="270fe-143">Recibir notificaciones de eventos asincrónicas en C++</span><span class="sxs-lookup"><span data-stu-id="270fe-143">Receiving Asynchronous Event Notifications in C++</span></span>

<span data-ttu-id="270fe-144">Para realizar una notificación asincrónica, se crea un subproceso independiente únicamente para supervisar y recibir eventos de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="270fe-144">To perform asynchronous notification, you create a separate thread solely to monitor and receive events from Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="270fe-145">Cuando ese subproceso recibe un mensaje, el subproceso notifica a la aplicación principal.</span><span class="sxs-lookup"><span data-stu-id="270fe-145">When that thread receives a message, the thread notifies your main application.</span></span>

<span data-ttu-id="270fe-146">Al dedicar un subproceso independiente, permite que el proceso principal realice otras actividades mientras espera que llegue un evento.</span><span class="sxs-lookup"><span data-stu-id="270fe-146">By dedicating a separate thread, you permit your main process to perform other activities while waiting for an event to arrive.</span></span> <span data-ttu-id="270fe-147">La entrega asincrónica de notificaciones mejora el rendimiento, pero puede proporcionar menos seguridad de lo que se desee.</span><span class="sxs-lookup"><span data-stu-id="270fe-147">Asynchronous delivery of notifications improves performance but may provide less security than you want.</span></span> <span data-ttu-id="270fe-148">En C++, tiene la opción de usar la interfaz [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) o realizar comprobaciones de acceso en descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="270fe-148">In C++, you have the option of using the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface or performing access checks on security descriptors.</span></span> <span data-ttu-id="270fe-149">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-149">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="270fe-150">**Para configurar notificaciones de eventos asincrónicos**</span><span class="sxs-lookup"><span data-stu-id="270fe-150">**To set up asynchronous event notifications**</span></span>

1.  <span data-ttu-id="270fe-151">Antes de inicializar las notificaciones asincrónicas, asegúrese de que los parámetros de prevención de memoria insuficiente están configurados correctamente en [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span><span class="sxs-lookup"><span data-stu-id="270fe-151">Before initializing any asynchronous notifications, ensure your out-of-memory avoidance parameters are set correctly in [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span></span>

2.  <span data-ttu-id="270fe-152">Determine qué tipo de eventos desea recibir.</span><span class="sxs-lookup"><span data-stu-id="270fe-152">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="270fe-153">WMI admite eventos intrínsecos y extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="270fe-153">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="270fe-154">Un evento intrínseco es un evento predefinido por WMI, mientras que un evento extrínseco es un evento definido por un proveedor de terceros.</span><span class="sxs-lookup"><span data-stu-id="270fe-154">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="270fe-155">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="270fe-156">En el procedimiento siguiente se describe cómo recibir notificaciones de eventos asincrónicas en C++.</span><span class="sxs-lookup"><span data-stu-id="270fe-156">The following procedure describes how to receive asynchronous event notifications in C++.</span></span>

<span data-ttu-id="270fe-157">**Para recibir notificaciones de eventos asincrónicos en C++**</span><span class="sxs-lookup"><span data-stu-id="270fe-157">**To receive asynchronous event notifications in C++**</span></span>

1.  <span data-ttu-id="270fe-158">Configure la aplicación con llamadas a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="270fe-158">Set up your application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="270fe-159">La llamada a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) inicializa com, mientras que [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) concede a WMI el permiso para llamar al proceso del consumidor.</span><span class="sxs-lookup"><span data-stu-id="270fe-159">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) initializes COM, while [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) grants WMI the permission to call into the process of the consumer.</span></span> <span data-ttu-id="270fe-160">La función **CoInitializeEx** también le concede la capacidad de programar una aplicación multiproceso, que es necesaria para la notificación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="270fe-160">The **CoInitializeEx** function also grants you the ability to program a multithreaded application, which is necessary for asynchronous notification.</span></span> <span data-ttu-id="270fe-161">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-161">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="270fe-162">El código de este tema requiere las siguientes referencias e \# incluir instrucciones para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="270fe-162">The code in this topic requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    <span data-ttu-id="270fe-163">En el ejemplo de código siguiente se describe cómo configurar el consumidor de eventos temporal con llamadas a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="270fe-163">The following code example describes how to set up the temporary event consumer with calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  <span data-ttu-id="270fe-164">Cree un objeto de receptor a través de la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="270fe-164">Create a sink object through the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="270fe-165">WMI usa [**IWbemObjectSink**](iwbemobjectsink.md) para enviar notificaciones de eventos y para notificar el estado de una operación asincrónica o una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="270fe-165">WMI uses [**IWbemObjectSink**](iwbemobjectsink.md) to send event notifications and to report status on an asynchronous operation or event notification.</span></span>

3.  <span data-ttu-id="270fe-166">Registre el consumidor de eventos con una llamada al método [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="270fe-166">Register your event consumer with a call to the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span>

    <span data-ttu-id="270fe-167">Asegúrese de que el parámetro *pResponseHandler* apunta al objeto receptor creado en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="270fe-167">Make sure that the *pResponseHandler* parameter points to the sink object created in the preceding step.</span></span>

    <span data-ttu-id="270fe-168">El propósito del registro es recibir solo las notificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="270fe-168">The purpose of registration is to receive only the required notifications.</span></span> <span data-ttu-id="270fe-169">Recibir notificaciones superfluas desperdicia el procesamiento y el tiempo de entrega; y no utiliza la capacidad de filtrado de WMI para obtener el máximo potencial.</span><span class="sxs-lookup"><span data-stu-id="270fe-169">Receiving superfluous notifications wastes processing and delivery time; and does not use the filtering ability of WMI to the fullest potential.</span></span>

    <span data-ttu-id="270fe-170">Sin embargo, un consumidor temporal puede recibir más de un tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="270fe-170">However, a temporary consumer can receive more than one type of event.</span></span> <span data-ttu-id="270fe-171">En este caso, un consumidor temporal debe realizar llamadas independientes a [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) para cada tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="270fe-171">In this case, a temporary consumer must make separate calls to [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) for each event type.</span></span> <span data-ttu-id="270fe-172">Por ejemplo, un consumidor podría requerir una notificación cuando se creen nuevos procesos (un evento de creación de instancia o [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) y para los cambios en ciertas claves del registro (un evento del registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span><span class="sxs-lookup"><span data-stu-id="270fe-172">For example, a consumer might require notification when new processes are created (an instance creation event or [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) and for changes to certain registry keys (a registry event such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span></span> <span data-ttu-id="270fe-173">Por consiguiente, el consumidor realiza una llamada a [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) para registrar los eventos de creación de instancia y otra llamada a **ExecNotificationQueryAsync** para registrar los eventos del registro.</span><span class="sxs-lookup"><span data-stu-id="270fe-173">Therefore, the consumer makes one call to [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) to register for instance creation events and another call to **ExecNotificationQueryAsync** to register for registry events.</span></span>

    <span data-ttu-id="270fe-174">Si decide crear un consumidor de eventos que se registre para varios eventos, debe evitar el registro de varias clases con el mismo receptor.</span><span class="sxs-lookup"><span data-stu-id="270fe-174">If you choose to create an event consumer that registers for multiple events, you should avoid registering multiple classes with the same sink.</span></span> <span data-ttu-id="270fe-175">En su lugar, utilice un receptor independiente para cada clase de evento registrado.</span><span class="sxs-lookup"><span data-stu-id="270fe-175">Instead, use a separate sink for each class of registered event.</span></span> <span data-ttu-id="270fe-176">Tener un receptor dedicado simplifica el procesamiento y la ayuda en el mantenimiento, lo que le permite cancelar un registro sin que afecte a los demás.</span><span class="sxs-lookup"><span data-stu-id="270fe-176">Having a dedicated sink simplifies processing and aids in maintenance, allowing you to cancel one registration without affecting the others.</span></span>

4.  <span data-ttu-id="270fe-177">Realice las actividades necesarias en el consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="270fe-177">Perform any necessary activities in your event consumer.</span></span>

    <span data-ttu-id="270fe-178">Este paso debe contener la mayor parte del código e incluir actividades como la visualización de eventos en una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="270fe-178">This step should contain most of your code and include such activities as displaying events to a user interface.</span></span>

5.  <span data-ttu-id="270fe-179">Cuando termine, anule el registro del consumidor de eventos temporal con una llamada al evento [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="270fe-179">When finished, unregister the temporary event consumer with a call to the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) event.</span></span>

    <span data-ttu-id="270fe-180">Independientemente de si la llamada a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) se realiza correctamente o se produce un error, no elimine el objeto de receptor hasta que el recuento de referencias de objeto llegue a cero.</span><span class="sxs-lookup"><span data-stu-id="270fe-180">Regardless of whether the call to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) succeeds or fails, do not delete the sink object until the object reference count reaches zero.</span></span> <span data-ttu-id="270fe-181">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-181">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 
