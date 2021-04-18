---
description: Para recibir notificaciones del proveedor del registro del sistema, una aplicación de administración debe registrarse como consumidor de eventos temporal.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrar eventos del registro del sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707276"
---
# <a name="registering-for-system-registry-events"></a><span data-ttu-id="23552-103">Registrar eventos del registro del sistema</span><span class="sxs-lookup"><span data-stu-id="23552-103">Registering for System Registry Events</span></span>

<span data-ttu-id="23552-104">Para recibir notificaciones del proveedor [del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , una aplicación de administración debe registrarse como consumidor de eventos temporal.</span><span class="sxs-lookup"><span data-stu-id="23552-104">To receive notifications from the [System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider) provider, a management application must register as a temporary event consumer.</span></span> <span data-ttu-id="23552-105">La mayoría de los requisitos para registrarse en el proveedor del registro del sistema son los mismos que cualquier otro registro de eventos, salvo que también debe realizar el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="23552-105">Most of the requirements to register for the System Registry provider are the same as any other event registration, except you must also perform the following procedure.</span></span>

<span data-ttu-id="23552-106">El proveedor del registro proporciona clases de eventos para los eventos en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="23552-106">The registry provider supplies event classes for events in the system registry.</span></span> <span data-ttu-id="23552-107">Para obtener más información sobre el registro de eventos generales, consulte [recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="23552-107">For more information about general event registration, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="23552-108">En el procedimiento siguiente se describe cómo registrar eventos del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="23552-108">The following procedure describes how to register for system registry events.</span></span>

<span data-ttu-id="23552-109">**Para registrar eventos del registro del sistema**</span><span class="sxs-lookup"><span data-stu-id="23552-109">**To register for system registry events**</span></span>

1.  <span data-ttu-id="23552-110">Llamar a un método de consulta de notificación.</span><span class="sxs-lookup"><span data-stu-id="23552-110">Call a notification query method.</span></span>

    <span data-ttu-id="23552-111">En script o C++, use una consulta de notificación como [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span><span class="sxs-lookup"><span data-stu-id="23552-111">In either script or C++, use a notification query such as [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span></span> <span data-ttu-id="23552-112">Cree una cadena de consulta para el parámetro *bstrQuery* de **IWbemServices:: ExecNotificationQueryAsync** o *strQuery* en el script.</span><span class="sxs-lookup"><span data-stu-id="23552-112">Create a query string for the *bstrQuery* parameter of **IWbemServices::ExecNotificationQueryAsync** or the *strQuery* in script.</span></span>

2.  <span data-ttu-id="23552-113">Determine el tipo de evento que desea recibir y cree la consulta.</span><span class="sxs-lookup"><span data-stu-id="23552-113">Determine which type of event you want to receive and create the query.</span></span>

    <span data-ttu-id="23552-114">En la tabla siguiente se enumeran las clases de eventos del registro que se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="23552-114">The following table lists the registry event classes that you can use.</span></span>

    

    | <span data-ttu-id="23552-115">Clase de evento</span><span class="sxs-lookup"><span data-stu-id="23552-115">Event class</span></span>                                                      | <span data-ttu-id="23552-116">Ubicación de Hive</span><span class="sxs-lookup"><span data-stu-id="23552-116">Hive location</span></span>        | <span data-ttu-id="23552-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="23552-117">Description</span></span>                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [<span data-ttu-id="23552-118">**RegistryEvent**</span><span class="sxs-lookup"><span data-stu-id="23552-118">**RegistryEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryevent)                       | <span data-ttu-id="23552-119">N/D</span><span class="sxs-lookup"><span data-stu-id="23552-119">N/A</span></span><br/>       | <span data-ttu-id="23552-120">Clase base abstracta para los cambios en el registro.</span><span class="sxs-lookup"><span data-stu-id="23552-120">Abstract base class for changes in the registry.</span></span><br/> |
    | [<span data-ttu-id="23552-121">**RegistryTreeChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="23552-121">**RegistryTreeChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | <span data-ttu-id="23552-122">RootPath</span><span class="sxs-lookup"><span data-stu-id="23552-122">RootPath</span></span><br/>  | <span data-ttu-id="23552-123">Supervisa los cambios en una jerarquía de claves.</span><span class="sxs-lookup"><span data-stu-id="23552-123">Monitors changes to a hierarchy of keys.</span></span><br/>         |
    | [<span data-ttu-id="23552-124">**RegistryKeyChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="23552-124">**RegistryKeyChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | <span data-ttu-id="23552-125">Rutas</span><span class="sxs-lookup"><span data-stu-id="23552-125">KeyPath</span></span><br/>   | <span data-ttu-id="23552-126">Supervisa los cambios en una sola clave.</span><span class="sxs-lookup"><span data-stu-id="23552-126">Monitors changes to a single key.</span></span><br/>                |
    | [<span data-ttu-id="23552-127">**RegistryValueChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="23552-127">**RegistryValueChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | <span data-ttu-id="23552-128">ValueName</span><span class="sxs-lookup"><span data-stu-id="23552-128">ValueName</span></span><br/> | <span data-ttu-id="23552-129">Supervisa los cambios en un único valor.</span><span class="sxs-lookup"><span data-stu-id="23552-129">Monitors changes to a single value.</span></span><br/>              |

    

     

    <span data-ttu-id="23552-130">Estas clases tienen una propiedad denominada **Hive** que identifica la jerarquía de claves que se va a supervisar para el cambio, como **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="23552-130">These classes have a property called **Hive** that identifies the hierarchy of keys to be monitored for change, such as **HKEY\_LOCAL\_MACHINE**.</span></span>

    <span data-ttu-id="23552-131">Los cambios en **las \_ clases HKEY \_ root** y **HKEY del \_ \_ usuario actual** no son compatibles con [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ni con las clases derivadas de él, como [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span><span class="sxs-lookup"><span data-stu-id="23552-131">Changes to the **HKEY\_CLASSES\_ROOT** and **HKEY\_CURRENT\_USER** hives are not supported by [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) or classes derived from it, such as [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span></span>

3.  <span data-ttu-id="23552-132">Cree la cláusula WHERE para el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="23552-132">Create the WHERE clause for your event registration.</span></span>

    <span data-ttu-id="23552-133">El proveedor del registro del sistema tiene reglas específicas para las cláusulas WHERE.</span><span class="sxs-lookup"><span data-stu-id="23552-133">The System Registry provider has specific rules for WHERE clauses.</span></span> <span data-ttu-id="23552-134">Para obtener más información, vea [crear una cláusula WHERE adecuada para el proveedor del registro](creating-a-proper-where-clause-for-the-registry-provider.md).</span><span class="sxs-lookup"><span data-stu-id="23552-134">For more information, see [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md).</span></span> <span data-ttu-id="23552-135">Para obtener más información general sobre la creación de una cláusula WHERE, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="23552-135">For more general information about creating a WHERE clause, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="23552-136">Determine si el consumidor está recibiendo eventos.</span><span class="sxs-lookup"><span data-stu-id="23552-136">Determine whether your consumer is receiving events.</span></span>

    <span data-ttu-id="23552-137">El proveedor del registro del sistema no garantiza que se entreguen todos los eventos enviados.</span><span class="sxs-lookup"><span data-stu-id="23552-137">The System Registry provider does not guarantee that all sent events are delivered.</span></span> <span data-ttu-id="23552-138">Para obtener más información, consulte [recibir eventos del registro](receiving-registry-events.md).</span><span class="sxs-lookup"><span data-stu-id="23552-138">For more information, see [Receiving Registry Events](receiving-registry-events.md).</span></span>

<span data-ttu-id="23552-139">En el ejemplo de código de VBScript siguiente se muestra cómo detectar un cambio en el registro en el software del **\_ \_ equipo local HKEY** \\  \\ **Microsoft** Hive o subárbol.</span><span class="sxs-lookup"><span data-stu-id="23552-139">The following VBScript code example shows how to detect a registry change in the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft** hive or subtree.</span></span> <span data-ttu-id="23552-140">Se trata de un script de supervisión que, para fines de demostración, se ejecuta en un proceso denominado Wscript.exe hasta que se termina en el **Administrador de tareas**, se detiene WMI o se reinicia el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="23552-140">This is a monitoring script that, for demonstration purposes, runs in a process named Wscript.exe until it is terminated in **Task Manager**, WMI is stopped, or the operating system is rebooted.</span></span> <span data-ttu-id="23552-141">El script usa una llamada [*semisincrónica*](gloss-s.md) a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="23552-141">The script uses a [*semisynchronous*](gloss-s.md) call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="23552-142">Para obtener más información sobre las llamadas semisincrónicas, vea [realizar una llamada semisincrónica con VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="23552-142">For more information about semisynchronous calls, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



En el ejemplo de código de VBScript siguiente se muestra cómo supervisar el cambio en los valores de una clave registrando el tipo de evento [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)del proveedor del registro. El script llama a un método asincrónico, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). <span data-ttu-id="23552-145">Para obtener más información sobre las llamadas asincrónicas y la seguridad, vea [realizar una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="23552-145">For more information about asynchronous calls and security, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="23552-146">El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script.</span><span class="sxs-lookup"><span data-stu-id="23552-146">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="23552-147">Para detener el script manualmente, use el administrador de tareas para detener el proceso.</span><span class="sxs-lookup"><span data-stu-id="23552-147">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="23552-148">Para detenerlo mediante programación, use el método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) en la clase de proceso de Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="23552-148">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

