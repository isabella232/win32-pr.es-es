---
description: En los scripts de supervisión, puede evitar llamadas sucesivas a GetObject mediante un objeto SWbemRefresher. El objeto SWbemRefresher es un contenedor que puede contener varios objetos WMI cuyos datos se pueden actualizar en una llamada.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Actualizar datos WMI en scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969a97c6300ac256e08c79e4f4aaeaa8d05bda072a2c310812ce3b2061c791fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050453"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Actualizar datos WMI en scripts

En los scripts de supervisión, puede evitar llamadas sucesivas a **GetObject** mediante un [**objeto SWbemRefresher.**](swbemrefresher.md) El **objeto SWbemRefresher** es un contenedor que puede contener varios objetos WMI cuyos datos se pueden actualizar en una llamada.

El uso de un objeto [**SWbemRefresher**](swbemrefresher.md) es necesario para obtener datos precisos de clases de rendimiento WMI, como [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) u otras clases preinstaladas derivadas de [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf).

En el procedimiento siguiente se describe cómo actualizar datos en scripts.

**Para actualizar datos en scripts**

1.  Llame **a CreateObject** para crear un [**objeto de actualizador SWbemRefresher.**](swbemrefresher.md)

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Conectar al espacio de nombres WMI. Para usar clases de rendimiento de [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf) preinstaladas, conéctese a **la raíz \\ cimv2**.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Agregue un único objeto (llamar a [**SWbemRefresher.Add)**](swbemrefresher-add.md)o una colección (llame a [**SWbemRefresher.AddEnum)**](swbemrefresher-addenum.md)al actualizador.

    Use las clases de datos precalculadas derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), por ejemplo, [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) en lugar de [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md). De lo contrario, debe calcular los valores de todas las propiedades que no son contadores simples.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Actualice los datos una vez para obtener los datos de rendimiento iniciales.

    Llame al [**método SWbemRefresher.Refresh**](swbemrefresher-refresh.md) o al método [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md) genérico.

    ```VB
    objRefresher.Refresh
    ```

    

5.  Si está supervisando el rendimiento y tiene una colección en el objeto de actualizador, recorre en bucle los objetos de colección.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Borre los elementos del actualizador llamando a [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) o quite elementos específicos llamando a [**SwbemRefresher.Remove**](swbemrefresher-remove.md).

En el ejemplo de código de VBScript siguiente se muestra cómo actualizar un único objeto en el equipo local. El script crea un contenedor de actualizador y agrega una instancia de un enumerador para las instancias de [**Proceso de PerfProc de Win32 \_ \_ \_ PerfFormattedData.**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) La [**llamada Refresh**](swbemrefresher-refresh.md) se realiza tres veces para mostrar los cambios en la propiedad **PercentProcessorTime** para los procesos que usan más del uno por ciento del tiempo de procesador.


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



La [**propiedad Index**](swbemrefreshableitem-index.md) del objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelto representa el índice del objeto en la colección del actualizador. Puede llamar a la propiedad [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) para determinar si un elemento de un actualizador es o no un elemento único o una colección. Para acceder a un único elemento, use la [**propiedad SWbemRefreshableItem.Object.**](swbemrefreshableitem-object.md) Si no realiza la llamada a **SWbemRefreshableItem.Object**, se produce un error en el script al intentar acceder al objeto . Para acceder a una colección, use [**la propiedad SWbemRefreshableItem.ObjectSet.**](swbemrefreshableitem-objectset.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Acceso a datos de rendimiento en script](accessing-performance-data-in-script.md)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
