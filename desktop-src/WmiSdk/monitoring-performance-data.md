---
description: Con WMI, puede acceder a los datos del contador del sistema mediante programación desde objetos de las bibliotecas de rendimiento.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Supervisión de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4f3ddd5024fb27d83f08225fa65faaa2e7d02cdd28189c86fc979175861453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317109"
---
# <a name="monitoring-performance-data"></a>Supervisión de datos de rendimiento

Con WMI, puede acceder a los datos del contador del sistema mediante programación desde objetos de las bibliotecas de rendimiento. Se trata de los mismos datos de rendimiento que aparecen en el Monitor de sistema en la utilidad Perfmon. Use las clases de contador de [rendimiento preinstaladas para](/windows/desktop/CIMWin32Prov/performance-counter-classes) obtener datos de rendimiento en scripts o aplicaciones de C++.

En este tema se de abordan las secciones siguientes:

-   [Clases de rendimiento wmi](#wmi-performance-classes)
-   [Proveedores de datos de rendimiento](#performance-data-providers)
-   [Usar clases de datos de rendimiento con formato](#using-formatted-performance-data-classes)
-   [Usar clases de datos de rendimiento sin procesar](#using-raw-performance-data-classes)
-   [Temas relacionados](#related-topics)

## <a name="wmi-performance-classes"></a>Clases de rendimiento wmi

Por ejemplo, el objeto "NetworkInterface", en el Monitor de sistema, se representa en WMI mediante la clase [**\_ Win32 PerfRawData \_ Tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) para datos sin procesar y la clase [**\_ Win32 PerfFormattedData \_ Tcpip \_ NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para datos precalculados o con formato. Las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**de Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) deben usarse con un [*objeto refresher.*](gloss-r.md) En las clases de datos sin procesar, la aplicación o script de C++ debe realizar cálculos para obtener la misma salida que Perfmon.exe. Las clases de datos con formato suministran datos precalculados. Para obtener más información sobre cómo obtener datos en aplicaciones de C++, vea Acceso a [datos de rendimiento en C++.](accessing-performance-data-in-c--.md) Para scripting, vea [Acceso a datos de rendimiento en script y](accessing-performance-data-in-script.md) Actualización de datos WMI en [scripts](refreshing-wmi-data-in-scripts.md).

En el ejemplo de código de VBScript siguiente se usa [**el proceso \_ \_ PerfProc PerfProc \_ de Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para obtener datos de rendimiento para el proceso inactivo. El script muestra los mismos datos que aparecen en Perfmon para el contador % processor time del objeto Process. La llamada a [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md) realiza la operación de actualización. Tenga en cuenta que los datos deben actualizarse, en concesión una vez, para obtener una línea base.


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



Las clases de contadores de rendimiento también pueden proporcionar datos estadísticos. Para obtener más información, vea [Obtener datos estadísticos de rendimiento.](obtaining-statistical-performance-data.md)

## <a name="performance-data-providers"></a>Proveedores de datos de rendimiento

WMI tiene proveedores preinstalados que supervisan el rendimiento del sistema en el sistema local y de forma remota. El [proveedor WmiPerfClass](wmiperfclass-provider.md) crea las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**de Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). El [proveedor WmiPerfInst](wmiperfinst-provider.md) proporciona datos dinámicamente a las clases sin formato y con formato.

## <a name="using-formatted-performance-data-classes"></a>Usar clases de datos de rendimiento con formato

En el ejemplo de código de VBScript siguiente se obtienen datos de rendimiento sobre la memoria, las particiones de disco y las colas de trabajo del servidor. A continuación, el script determina si los valores están dentro de un intervalo aceptable.

El script usa los siguientes objetos de proveedor WMI y objetos de scripting:

-   Clases de contadores de rendimiento WMI preinstaladas.
-   El objeto refresher, [**SWbemRefresher.**](swbemrefresher.md)
-   Elementos que se agregarán al contenedor del actualizador, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


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

El siguiente ejemplo de código VBScript obtiene el tiempo de procesador de porcentaje actual sin procesar en el equipo local y lo convierte en un porcentaje. En el ejemplo se muestra cómo obtener datos de rendimiento sin procesar de la propiedad **PercentProcessorTime** de la clase [**\_ PerfRawData \_ PerfOS \_ Processor de Win32.**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)

Para calcular el valor de tiempo de procesador de porcentaje, debe buscar la fórmula. Busque el valor en el **calificador CounterType** para la propiedad **PercentProcessorTime** de la tabla [**CounterType Qualifier**](countertype-qualifier.md) para obtener el nombre de constante. Busque el nombre de constante en [Tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) para obtener la fórmula.


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

[Uso de WMI](using-wmi.md)
</dt> </dl>

 

 
