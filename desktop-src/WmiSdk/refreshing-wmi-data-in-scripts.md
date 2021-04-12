---
description: En los scripts de supervisión, puede evitar las llamadas sucesivas a GetObject mediante el uso de un objeto SWbemRefresher. El objeto SWbemRefresher es un contenedor que puede contener varios objetos WMI cuyos datos se pueden actualizar en una llamada.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Actualizar datos WMI en scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277700"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Actualizar datos WMI en scripts

En los scripts de supervisión, puede evitar las llamadas sucesivas a **GetObject** mediante el uso de un objeto [**SWbemRefresher**](swbemrefresher.md) . El objeto **SWbemRefresher** es un contenedor que puede contener varios objetos WMI cuyos datos se pueden actualizar en una llamada.

El uso de un objeto [**SWbemRefresher**](swbemrefresher.md) es necesario para obtener datos precisos de las clases de rendimiento de WMI, como [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) u otras clases preinstaladas derivadas de [**\_ rendimiento de Win32**](/windows/desktop/CIMWin32Prov/win32-perf).

En el procedimiento siguiente se describe cómo actualizar los datos de los scripts.

**Para actualizar datos en scripts**

1.  Llame a **CreateObject** para crear un objeto de actualizador de [**SWbemRefresher**](swbemrefresher.md) .

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Conéctese al espacio de nombres WMI. Para usar las clases de [**\_ rendimiento de Win32**](/windows/desktop/CIMWin32Prov/win32-perf) preinstaladas, conéctese a la **raíz \\ cimv2**.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Agregue un solo objeto (llame a [**SWbemRefresher. Add**](swbemrefresher-add.md)) o una colección (llame a [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) al actualizador.

    Utilice las clases de datos precalculadas derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), por ejemplo, [**Win32 \_ PerfFormattedData \_ Perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) en lugar de [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md). De lo contrario, debe calcular los valores de todas las propiedades que no sean contadores simples.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Actualice los datos una vez para obtener los datos de rendimiento iniciales.

    Llame al método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) o al método genérico [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) .

    ```VB
    objRefresher.Refresh
    ```

    

5.  Si está supervisando el rendimiento y tiene una colección en el objeto actualizador, recorra en bucle los objetos de la colección.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Borre los elementos del actualizador llamando a [**SWbemRefresher. deleteAll**](swbemrefresher-deleteall.md) o quite elementos específicos llamando a [**SWbemRefresher. Remove**](swbemrefresher-remove.md).

En el ejemplo de código de VBScript siguiente se muestra cómo actualizar un solo objeto en el equipo local. El script crea un contenedor actualizado y agrega una instancia de un enumerador para las instancias de [**\_ proceso de PerfFormattedData \_ PerfProc \_ de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) . La llamada de [**actualización**](swbemrefresher-refresh.md) se realiza tres veces para mostrar los cambios en la propiedad **PercentProcessorTime** para los procesos que usan más de un porcentaje de tiempo de procesador.


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



La propiedad [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelta representa el índice del objeto en la colección del actualizador. Puede llamar a la propiedad [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) para determinar si un elemento de un actualizador es un elemento único o una colección. Para tener acceso a un único elemento, use la propiedad [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) . Si no realiza la llamada a **SWbemRefreshableItem. Object**, el script generará un error cuando intente obtener acceso al objeto. Para tener acceso a una colección, use la propiedad [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Obtener acceso a los datos de rendimiento del script](accessing-performance-data-in-script.md)
</dt> <dt>

[Tareas WMI: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
