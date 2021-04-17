---
description: Use SWbemServices.ExecQuery para solicitar todos los eventos existentes.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Recibir notificaciones de eventos sincrónicos y semisincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697364"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a><span data-ttu-id="6d417-103">Recibir notificaciones de eventos sincrónicos y semisincrónicos</span><span class="sxs-lookup"><span data-stu-id="6d417-103">Receiving Synchronous and Semisynchronous Event Notifications</span></span>

<span data-ttu-id="6d417-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) para solicitar todos los eventos existentes.</span><span class="sxs-lookup"><span data-stu-id="6d417-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to request all existing events.</span></span>

<span data-ttu-id="6d417-105">En el ejemplo de código siguiente se muestra cómo consultar los eventos en un registro.</span><span class="sxs-lookup"><span data-stu-id="6d417-105">The following code example shows how to query for the events in a log.</span></span>

`Select * from Win32_NTLogEvent`

<span data-ttu-id="6d417-106">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md), [recibir notificaciones de eventos](receiving-event-notifications.md)y [WQL (SQL para WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-106">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md), [Receiving Event Notifications](receiving-event-notifications.md), and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="6d417-107">La llamada predeterminada a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) utiliza la comunicación semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="6d417-107">The default call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) uses semisynchronous communication.</span></span> <span data-ttu-id="6d417-108">El parámetro *iflags* tiene los marcadores **wbemFlagForwardOnly** y **wbemFlagReturnImmediately** establecidos de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6d417-108">The *iflags* parameter has the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags set by default.</span></span> <span data-ttu-id="6d417-109">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6d417-110">En el procedimiento siguiente se describe cómo recibir una notificación de eventos semisincrónica mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="6d417-110">The following procedure describes how to receive semisynchronous event notification using VBScript.</span></span>

<span data-ttu-id="6d417-111">**Para recibir la notificación de eventos semisincrónicos en VBScript**</span><span class="sxs-lookup"><span data-stu-id="6d417-111">**To receive semisynchronous event notification in VBScript**</span></span>

1.  <span data-ttu-id="6d417-112">Cree una consulta para el tipo de evento que desea recibir.</span><span class="sxs-lookup"><span data-stu-id="6d417-112">Create a query for the type of event that you want to receive.</span></span> <span data-ttu-id="6d417-113">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-113">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="6d417-114">Si solicita un tipo de instancia de evento como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indique en la consulta un tipo de instancia de destino, por ejemplo, [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="6d417-114">If you request an instance type of event such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), indicate in the query a type of target instance, for example, [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>

3.  <span data-ttu-id="6d417-115">Si es necesario, especifique una instancia, por ejemplo, el nombre de un espacio de nombres al solicitar futuras instancias de [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) para un espacio de nombres concreto.</span><span class="sxs-lookup"><span data-stu-id="6d417-115">If necessary, specify an instance, for example, the name of a namespace when requesting future [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) instances for a specific namespace.</span></span>

4.  <span data-ttu-id="6d417-116">Especifique un intervalo de sondeo para Instrumental de administración de Windows (WMI) en una consulta, como "dentro de 10", para sondear cada 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="6d417-116">Specify a polling interval for Windows Management Instrumentation (WMI) in a query, such as "WITHIN 10"—to poll every 10 seconds.</span></span> <span data-ttu-id="6d417-117">Para obtener más información, vea [dentro de la cláusula](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-117">For more information, see [WITHIN Clause](within-clause.md).</span></span>

5.  <span data-ttu-id="6d417-118">Llame a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) con la consulta.</span><span class="sxs-lookup"><span data-stu-id="6d417-118">Call [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) using the query.</span></span>

6.  <span data-ttu-id="6d417-119">Recorra en bucle la colección que recibe.</span><span class="sxs-lookup"><span data-stu-id="6d417-119">Loop through the collection you receive.</span></span>

<span data-ttu-id="6d417-120">En el ejemplo siguiente se muestra cómo supervisar la inserción y la eliminación de discos desde una unidad de disquete en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="6d417-120">The following example shows how to monitor insertion and removal of disks from a floppy disk drive on a local machine.</span></span> <span data-ttu-id="6d417-121">El script solicita \_ instancias de [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) para la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de la unidad de disquete y sondea cada 10 segundos para las nuevas instancias.</span><span class="sxs-lookup"><span data-stu-id="6d417-121">The script requests \_[**\_\_InstanceModificationEvent**](--instancemodificationevent.md) instances for the floppy drive [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance and polls every 10 seconds for new instances.</span></span> <span data-ttu-id="6d417-122">Este script es un ejemplo de consumidor de eventos temporal y continúa ejecutándose hasta que se detiene en el administrador de tareas o cuando se reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="6d417-122">This script is an example of a temporary event consumer, and continues running until it is stopped in Task Manager or the system is rebooted.</span></span> <span data-ttu-id="6d417-123">Para obtener más información, consulte [recepción de eventos para la duración de la aplicación](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-123">For more information, see [Receiving Events for the Duration of your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



<span data-ttu-id="6d417-124">En el procedimiento siguiente se describe cómo recibir una notificación de eventos semisincrónica mediante C++.</span><span class="sxs-lookup"><span data-stu-id="6d417-124">The following procedure describes how to receive semisynchronous event notification using C++.</span></span>

<span data-ttu-id="6d417-125">**Para recibir la notificación de eventos semisincrónicos en C++**</span><span class="sxs-lookup"><span data-stu-id="6d417-125">**To receive semisynchronous event notification in C++**</span></span>

1.  <span data-ttu-id="6d417-126">Configure la aplicación con llamadas a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="6d417-126">Set up the application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="6d417-127">Dado que WMI está basado en COM, llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) es un paso necesario para una aplicación WMI.</span><span class="sxs-lookup"><span data-stu-id="6d417-127">Because WMI is COM based, calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a required step for a WMI application.</span></span> <span data-ttu-id="6d417-128">Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-128">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

2.  <span data-ttu-id="6d417-129">Determine el tipo de eventos que desea recibir.</span><span class="sxs-lookup"><span data-stu-id="6d417-129">Determine the kind of events that you want to receive.</span></span>

    <span data-ttu-id="6d417-130">WMI admite eventos intrínsecos y extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="6d417-130">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="6d417-131">Un evento intrínseco es un evento predefinido por WMI.</span><span class="sxs-lookup"><span data-stu-id="6d417-131">An intrinsic event is an event predefined by WMI.</span></span> <span data-ttu-id="6d417-132">Un evento extrínseco es un evento definido por un proveedor de terceros.</span><span class="sxs-lookup"><span data-stu-id="6d417-132">An extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="6d417-133">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-133">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

3.  <span data-ttu-id="6d417-134">Regístrese para recibir una clase específica de eventos con una llamada al método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="6d417-134">Register to receive a specific class of events with a call to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) method.</span></span>

    <span data-ttu-id="6d417-135">Haga que cada consulta sea muy específica.</span><span class="sxs-lookup"><span data-stu-id="6d417-135">Make each query very specific.</span></span> <span data-ttu-id="6d417-136">El objetivo del registro es registrarse para recibir solo las notificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="6d417-136">The goal of registration is to register to receive only the required notifications.</span></span> <span data-ttu-id="6d417-137">Notificaciones que no son necesarias para el procesamiento de residuos y el tiempo de entrega.</span><span class="sxs-lookup"><span data-stu-id="6d417-137">Notifications that are not required waste processing and delivery time.</span></span>

    <span data-ttu-id="6d417-138">Puede diseñar un consumidor de eventos para recibir varios eventos.</span><span class="sxs-lookup"><span data-stu-id="6d417-138">You can design an event consumer to receive multiple events.</span></span> <span data-ttu-id="6d417-139">Por ejemplo, un consumidor podría requerir la notificación de eventos de modificación de instancia para una clase específica de eventos de dispositivo y de infracción de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6d417-139">For example, a consumer might require notification of instance modification events for a specific class of device and security violation events.</span></span> <span data-ttu-id="6d417-140">En este caso, las tareas que realiza un consumidor al recibir un evento de modificación de instancia son diferentes para los dos eventos.</span><span class="sxs-lookup"><span data-stu-id="6d417-140">In this case, the tasks a consumer performs when receiving an instance modification event are different for the two events.</span></span> <span data-ttu-id="6d417-141">Por lo tanto, el consumidor debe realizar una llamada a [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) para registrar los eventos de modificación de instancias y otra llamada a **ExecNotificationQuery** para registrar los eventos de infracción de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6d417-141">Thus, the consumer should make one call to [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) to register for instance modification events, and another call to **ExecNotificationQuery** to register for security violation events.</span></span>

    <span data-ttu-id="6d417-142">En la llamada a [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), establezca el parámetro *lFlags* en **la \_ marca WBEM \_ Return \_ inmediatamente** y **WBEM \_ Flag \_ Forward \_ Only**.</span><span class="sxs-lookup"><span data-stu-id="6d417-142">In the call to [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), set the *lFlags* parameter to **WBEM\_FLAG\_RETURN\_IMMEDIATELY** and **WBEM\_FLAG\_FORWARD\_ONLY**.</span></span> <span data-ttu-id="6d417-143">La **\_ marca WBEM \_ devolverá \_ inmediatamente** el procesamiento semisincrónico de las solicitudes y el marcador **WBEM \_ Flag \_ Forward \_ Only** solicita un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="6d417-143">The **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag requests semisynchronous processing, and the **WBEM\_FLAG\_FORWARD\_ONLY** flag requests a forward-only enumerator.</span></span> <span data-ttu-id="6d417-144">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6d417-144">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="6d417-145">La función **ExecNotificationQuery** devuelve un puntero a una interfaz [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="6d417-145">The **ExecNotificationQuery** function returns a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface.</span></span>

4.  <span data-ttu-id="6d417-146">Sondear las notificaciones de eventos registradas realizando llamadas repetidas al método [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="6d417-146">Poll for registered event notifications by making repeated calls to the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span>
5.  <span data-ttu-id="6d417-147">Cuando termine, libere el enumerador que señala al objeto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="6d417-147">When finished, release the enumerator that points to the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object.</span></span>

    <span data-ttu-id="6d417-148">Puede liberar el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) asociado al registro.</span><span class="sxs-lookup"><span data-stu-id="6d417-148">You can release the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer associated with the registration.</span></span> <span data-ttu-id="6d417-149">Al liberar el puntero **IWbemServices** , WMI deja de entregar eventos a todos los consumidores temporales asociados.</span><span class="sxs-lookup"><span data-stu-id="6d417-149">Releasing the **IWbemServices** pointer causes WMI to stop delivering events to all associated temporary consumers.</span></span>

 

 
