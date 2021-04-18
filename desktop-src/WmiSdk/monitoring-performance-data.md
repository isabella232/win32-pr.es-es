---
description: Mediante WMI, puede tener acceso mediante programación a los datos del contador del sistema desde los objetos de las bibliotecas de rendimiento.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Supervisión de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cee18ba88a8aff920c2d14b5709a0fd913e2ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649247"
---
# <a name="monitoring-performance-data"></a><span data-ttu-id="09be7-103">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="09be7-103">Monitoring Performance Data</span></span>

<span data-ttu-id="09be7-104">Mediante WMI, puede tener acceso mediante programación a los datos del contador del sistema desde los objetos de las bibliotecas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="09be7-104">Using WMI, you can access system counter data programmatically from objects in the performance libraries.</span></span> <span data-ttu-id="09be7-105">Se trata de los mismos datos de rendimiento que aparecen en el monitor de sistema en la utilidad Perfmon.</span><span class="sxs-lookup"><span data-stu-id="09be7-105">This is the same performance data that appears in the System Monitor in the Perfmon utility.</span></span> <span data-ttu-id="09be7-106">Utilice las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) preinstaladas para obtener datos de rendimiento en scripts o aplicaciones de C++.</span><span class="sxs-lookup"><span data-stu-id="09be7-106">Use the preinstalled [performance counter classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) to obtain performance data in scripts or C++ applications.</span></span>

<span data-ttu-id="09be7-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="09be7-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="09be7-108">Clases de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="09be7-108">WMI Performance Classes</span></span>](#wmi-performance-classes)
-   [<span data-ttu-id="09be7-109">Proveedores de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="09be7-109">Performance Data Providers</span></span>](#performance-data-providers)
-   [<span data-ttu-id="09be7-110">Usar clases de datos de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="09be7-110">Using Formatted Performance Data Classes</span></span>](#using-formatted-performance-data-classes)
-   [<span data-ttu-id="09be7-111">Usar clases de datos de rendimiento sin procesar</span><span class="sxs-lookup"><span data-stu-id="09be7-111">Using Raw Performance Data Classes</span></span>](#using-raw-performance-data-classes)
-   [<span data-ttu-id="09be7-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09be7-112">Related topics</span></span>](#related-topics)

## <a name="wmi-performance-classes"></a><span data-ttu-id="09be7-113">Clases de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="09be7-113">WMI Performance Classes</span></span>

<span data-ttu-id="09be7-114">Por ejemplo, el objeto "interfaz cluster", en el monitor de sistema, se representa en WMI mediante la clase [**\_ interfaz Cluster de PerfRawData \_ TCPIP \_ de Win32**](./retrieving-raw-and-formatted-performance-data.md) para los datos sin procesar y la clase [**\_ \_ \_ interfaz Cluster de TCP PerfFormattedData TCPIP**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para los datos con formato precalculado o.</span><span class="sxs-lookup"><span data-stu-id="09be7-114">As an example, the "NetworkInterface" object, in System Monitor, is represented in WMI by the [**Win32\_PerfRawData\_Tcpip\_NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) class for raw data and the [**Win32\_PerfFormattedData\_Tcpip\_NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class for precalculated, or formatted data.</span></span> <span data-ttu-id="09be7-115">Las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) deben usarse con un objeto [*actualizador*](gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="09be7-115">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) must be used with a [*refresher*](gloss-r.md) object.</span></span> <span data-ttu-id="09be7-116">En las clases de datos sin procesar, la aplicación o el script de C++ deben realizar cálculos para obtener el mismo resultado que Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="09be7-116">On raw data classes, your C++ application or script must perform calculations to obtain the same output as Perfmon.exe.</span></span> <span data-ttu-id="09be7-117">Las clases de datos con formato proporcionan datos precalculados.</span><span class="sxs-lookup"><span data-stu-id="09be7-117">Formatted data classes supply precalculated data.</span></span> <span data-ttu-id="09be7-118">Para obtener más información sobre cómo obtener datos en aplicaciones de C++, vea [obtener acceso a los datos de rendimiento en c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="09be7-118">For more information about obtaining data in C++ applications, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="09be7-119">Para el scripting, consulte [acceso a los datos de rendimiento en script](accessing-performance-data-in-script.md) y [actualización de los datos WMI en scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="09be7-119">For scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="09be7-120">En el siguiente ejemplo de código de VBScript se usa el [**proceso de Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para obtener los datos de rendimiento del proceso inactivo.</span><span class="sxs-lookup"><span data-stu-id="09be7-120">The following VBScript code example uses [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) to obtain performance data for the Idle process.</span></span> <span data-ttu-id="09be7-121">El script muestra los mismos datos que aparecen en Perfmon para el contador% de tiempo de procesador del objeto de proceso.</span><span class="sxs-lookup"><span data-stu-id="09be7-121">The script displays the same data that appears in Perfmon for the % Processor Time counter of the Process object.</span></span> <span data-ttu-id="09be7-122">La llamada a [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) realiza la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="09be7-122">The call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) performs the refresh operation.</span></span> <span data-ttu-id="09be7-123">Tenga en cuenta que los datos se deben actualizar, una vez a la concesión, para obtener una línea base.</span><span class="sxs-lookup"><span data-stu-id="09be7-123">Be aware that the data must be refreshed, at lease once, to obtain a baseline.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")
set PerfProcess = objWMIService.Get(_
    "Win32_PerfFormattedData_PerfProc_Process.Name='Idle'")

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend
```



<span data-ttu-id="09be7-124">Las clases de contador de rendimiento también pueden proporcionar datos estadísticos.</span><span class="sxs-lookup"><span data-stu-id="09be7-124">Performance counter classes can also provide statistical data.</span></span> <span data-ttu-id="09be7-125">Para obtener más información, consulte [obtención de datos de rendimiento estadísticos](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="09be7-125">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="performance-data-providers"></a><span data-ttu-id="09be7-126">Proveedores de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="09be7-126">Performance Data Providers</span></span>

<span data-ttu-id="09be7-127">WMI tiene proveedores preinstalados que supervisan el rendimiento del sistema en el sistema local y de forma remota.</span><span class="sxs-lookup"><span data-stu-id="09be7-127">WMI has preinstalled providers that monitor system performance on both the local system and remotely.</span></span> <span data-ttu-id="09be7-128">El proveedor [WmiPerfClass](wmiperfclass-provider.md) crea las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="09be7-128">The [WmiPerfClass](wmiperfclass-provider.md) provider creates the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="09be7-129">El proveedor [WmiPerfInst](wmiperfinst-provider.md) proporciona datos dinámicamente a las clases sin formato y con formato.</span><span class="sxs-lookup"><span data-stu-id="09be7-129">The [WmiPerfInst](wmiperfinst-provider.md) provider supplies data dynamically to both raw and formatted classes.</span></span>

## <a name="using-formatted-performance-data-classes"></a><span data-ttu-id="09be7-130">Usar clases de datos de rendimiento con formato</span><span class="sxs-lookup"><span data-stu-id="09be7-130">Using Formatted Performance Data Classes</span></span>

<span data-ttu-id="09be7-131">El siguiente ejemplo de código de VBScript obtiene datos de rendimiento acerca de la memoria, las particiones de disco y las colas de trabajo del servidor.</span><span class="sxs-lookup"><span data-stu-id="09be7-131">The following VBScript code example obtains performance data about memory, disk partitions, and server work queues.</span></span> <span data-ttu-id="09be7-132">Después, el script determina si los valores están dentro de un intervalo aceptable.</span><span class="sxs-lookup"><span data-stu-id="09be7-132">The script then determines if the values are within an acceptable range.</span></span>

<span data-ttu-id="09be7-133">El script usa los siguientes objetos de proveedor WMI y objetos de scripting:</span><span class="sxs-lookup"><span data-stu-id="09be7-133">The script uses the following WMI provider objects and scripting objects:</span></span>

-   <span data-ttu-id="09be7-134">Clases de contador de rendimiento de WMI preinstaladas.</span><span class="sxs-lookup"><span data-stu-id="09be7-134">Preinstalled WMI performance counter classes.</span></span>
-   <span data-ttu-id="09be7-135">El objeto actualizador, [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="09be7-135">The refresher object, [**SWbemRefresher**](swbemrefresher.md).</span></span>
-   <span data-ttu-id="09be7-136">Elementos que se van a agregar al contenedor del actualizador, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)</span><span class="sxs-lookup"><span data-stu-id="09be7-136">Items to add to the refresher container, [**SWbemRefreshableItem**](swbemrefreshableitem.md)</span></span>


```VB
Set objCimv2 = GetObject("winmgmts:root\cimv2")
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add items to the SWbemRefresher
' Without the SWbemRefreshableItem.ObjectSet call,
' the script will fail
Set objMemory = objRefresher.AddEnum _
    (objCimv2, _ 
    "Win32_PerfFormattedData_PerfOS_Memory").ObjectSet
Set objDiskQueue = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfDisk_LogicalDisk").ObjectSet
Set objQueueLength = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfNet_ServerWorkQueues").ObjectSet

' Initial refresh needed to get baseline values
objRefresher.Refresh
intTotalHealth = 0
' Do three refreshes to get data
For i = 1 to 3
    WScript.Echo "Refresh " & i
    For each intAvailableBytes in objMemory
        WScript.Echo "Available megabytes of memory: " _
            & intAvailableBytes.AvailableMBytes
        If intAvailableBytes.AvailableMBytes < 4 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intDiskQueue in objDiskQueue
        WScript.Echo "Current disk queue length " & "Name: " _
            & intDiskQueue.Name & ":" _
            & intDiskQueue.CurrentDiskQueueLength
        If intDiskQueue.CurrentDiskQueueLength > 2 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intServerQueueLength in objQueueLength
        WScript.Echo "Server work queue length: " _
            & intServerQueueLength.QueueLength
        If intServerQueueLength.QueueLength > 4 Then
            intTotalHealth = intTotalHealth + 1                       
        End If
    Wscript.Echo "  "
    Next
    If intTotalHealth > 0 Then
        Wscript.Echo "Unhealthy."
    Else
        Wscript.Echo "Healthy."
    End If
    intTotalHealth = 0
    Wscript.Sleep 5000
' Refresh data for all objects in the collection
    objRefresher.Refresh
Next
```



## <a name="using-raw-performance-data-classes"></a><span data-ttu-id="09be7-137">Usar clases de datos de rendimiento sin procesar</span><span class="sxs-lookup"><span data-stu-id="09be7-137">Using Raw Performance Data Classes</span></span>

<span data-ttu-id="09be7-138">El siguiente ejemplo de código de VBScript obtiene el porcentaje de tiempo de procesador actual y sin procesar en el equipo local y lo convierte en un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="09be7-138">The following VBScript code example obtains raw, current percent processor time on the local computer and converts it to a percentage.</span></span> <span data-ttu-id="09be7-139">En el ejemplo se muestra cómo obtener datos de rendimiento sin procesar de la propiedad **PercentProcessorTime** de la clase de [**\_ \_ \_ procesador PerfRawData de rendimiento de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="09be7-139">The example shows you how to obtain raw performance data from the **PercentProcessorTime** property of the [**Win32\_PerfRawData\_PerfOS\_Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class.</span></span>

<span data-ttu-id="09be7-140">Para calcular el valor de porcentaje de tiempo de procesador, debe buscar la fórmula.</span><span class="sxs-lookup"><span data-stu-id="09be7-140">To calculate the percent processor time value, you must locate the formula.</span></span> <span data-ttu-id="09be7-141">Busque el valor en el calificador de **tipo** para la propiedad **PercentProcessorTime** de la tabla de [**calificador de tipo unitype**](countertype-qualifier.md) para obtener el nombre de la constante.</span><span class="sxs-lookup"><span data-stu-id="09be7-141">Look up the value in the **CounterType** qualifier for the **PercentProcessorTime** property in the [**CounterType Qualifier**](countertype-qualifier.md) table to get the constant name.</span></span> <span data-ttu-id="09be7-142">Busque el nombre de la constante en [tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) para obtener la fórmula.</span><span class="sxs-lookup"><span data-stu-id="09be7-142">Locate the constant name in [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) to obtain the formula.</span></span>


```VB
Set objService = GetObject( _
    "Winmgmts:{impersonationlevel=impersonate}!\Root\Cimv2")

For i = 1 to 8
    Set objInstance1 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N1 = objInstance1.PercentProcessorTime
    D1 = objInstance1.TimeStamp_Sys100NS

'Sleep for two seconds = 2000 ms
    WScript.Sleep(2000)

    Set perf_instance2 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N2 = perf_instance2.PercentProcessorTime
    D2 = perf_instance2.TimeStamp_Sys100NS
' Look up the CounterType qualifier for the PercentProcessorTime 
' and obtain the formula to calculate the meaningful data. 
' CounterType - PERF_100NSEC_TIMER_INV
' Formula - (1- ((N2 - N1) / (D2 - D1))) x 100

    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    WScript.Echo "% Processor Time=" , Round(PercentProcessorTime,2)
Next
```



## <a name="related-topics"></a><span data-ttu-id="09be7-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09be7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09be7-144">Usar WMI</span><span class="sxs-lookup"><span data-stu-id="09be7-144">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
