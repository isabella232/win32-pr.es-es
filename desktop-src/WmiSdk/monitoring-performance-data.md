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
# <a name="monitoring-performance-data"></a>Supervisión de datos de rendimiento

Mediante WMI, puede tener acceso mediante programación a los datos del contador del sistema desde los objetos de las bibliotecas de rendimiento. Se trata de los mismos datos de rendimiento que aparecen en el monitor de sistema en la utilidad Perfmon. Utilice las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) preinstaladas para obtener datos de rendimiento en scripts o aplicaciones de C++.

En este tema se describen las siguientes secciones:

-   [Clases de rendimiento de WMI](#wmi-performance-classes)
-   [Proveedores de datos de rendimiento](#performance-data-providers)
-   [Usar clases de datos de rendimiento con formato](#using-formatted-performance-data-classes)
-   [Usar clases de datos de rendimiento sin procesar](#using-raw-performance-data-classes)
-   [Temas relacionados](#related-topics)

## <a name="wmi-performance-classes"></a>Clases de rendimiento de WMI

Por ejemplo, el objeto "interfaz cluster", en el monitor de sistema, se representa en WMI mediante la clase [**\_ interfaz Cluster de PerfRawData \_ TCPIP \_ de Win32**](./retrieving-raw-and-formatted-performance-data.md) para los datos sin procesar y la clase [**\_ \_ \_ interfaz Cluster de TCP PerfFormattedData TCPIP**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para los datos con formato precalculado o. Las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) deben usarse con un objeto [*actualizador*](gloss-r.md) . En las clases de datos sin procesar, la aplicación o el script de C++ deben realizar cálculos para obtener el mismo resultado que Perfmon.exe. Las clases de datos con formato proporcionan datos precalculados. Para obtener más información sobre cómo obtener datos en aplicaciones de C++, vea [obtener acceso a los datos de rendimiento en c++](accessing-performance-data-in-c--.md). Para el scripting, consulte [acceso a los datos de rendimiento en script](accessing-performance-data-in-script.md) y [actualización de los datos WMI en scripts](refreshing-wmi-data-in-scripts.md).

En el siguiente ejemplo de código de VBScript se usa el [**proceso de Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para obtener los datos de rendimiento del proceso inactivo. El script muestra los mismos datos que aparecen en Perfmon para el contador% de tiempo de procesador del objeto de proceso. La llamada a [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) realiza la operación de actualización. Tenga en cuenta que los datos se deben actualizar, una vez a la concesión, para obtener una línea base.


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



Las clases de contador de rendimiento también pueden proporcionar datos estadísticos. Para obtener más información, consulte [obtención de datos de rendimiento estadísticos](obtaining-statistical-performance-data.md).

## <a name="performance-data-providers"></a>Proveedores de datos de rendimiento

WMI tiene proveedores preinstalados que supervisan el rendimiento del sistema en el sistema local y de forma remota. El proveedor [WmiPerfClass](wmiperfclass-provider.md) crea las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). El proveedor [WmiPerfInst](wmiperfinst-provider.md) proporciona datos dinámicamente a las clases sin formato y con formato.

## <a name="using-formatted-performance-data-classes"></a>Usar clases de datos de rendimiento con formato

El siguiente ejemplo de código de VBScript obtiene datos de rendimiento acerca de la memoria, las particiones de disco y las colas de trabajo del servidor. Después, el script determina si los valores están dentro de un intervalo aceptable.

El script usa los siguientes objetos de proveedor WMI y objetos de scripting:

-   Clases de contador de rendimiento de WMI preinstaladas.
-   El objeto actualizador, [**SWbemRefresher**](swbemrefresher.md).
-   Elementos que se van a agregar al contenedor del actualizador, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>Usar clases de datos de rendimiento sin procesar

El siguiente ejemplo de código de VBScript obtiene el porcentaje de tiempo de procesador actual y sin procesar en el equipo local y lo convierte en un porcentaje. En el ejemplo se muestra cómo obtener datos de rendimiento sin procesar de la propiedad **PercentProcessorTime** de la clase de [**\_ \_ \_ procesador PerfRawData de rendimiento de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .

Para calcular el valor de porcentaje de tiempo de procesador, debe buscar la fórmula. Busque el valor en el calificador de **tipo** para la propiedad **PercentProcessorTime** de la tabla de [**calificador de tipo unitype**](countertype-qualifier.md) para obtener el nombre de la constante. Busque el nombre de la constante en [tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) para obtener la fórmula.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar WMI](using-wmi.md)
</dt> </dl>

 

 
