---
description: Los scripts de WMI pueden tener acceso a las clases de contador de rendimiento de WMI preinstaladas, ya sea en el equipo local o de forma remota.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Obtener acceso a los datos de rendimiento del script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697846"
---
# <a name="accessing-performance-data-in-script"></a>Obtener acceso a los datos de rendimiento del script

Los scripts de WMI pueden tener acceso a las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)de WMI preinstaladas, ya sea en el equipo local o de forma remota. Mientras que los scripts pueden obtener datos de clases no calculadas, como la memoria de rendimiento de PerfRawData de Win32, o clases con formato, la [**memoria de \_ PerfFormattedData de \_ rendimiento \_ de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), las clases de datos con formato pueden ser más fáciles de usar. [**\_ \_ \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)

La supervisión de los datos de rendimiento con las clases de contador de rendimiento requiere el uso de un [*actualizador*](gloss-r.md). Use el objeto [**SWbemRefresher**](swbemrefresher.md) para almacenar uno o más objetos de rendimiento para actualizar o actualizar un solo objeto mediante la llamada a [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) . Para obtener más información, vea [actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md).

Al establecer la propiedad [**SWbemRefresher. reconexión automática**](swbemrefresher-autoreconnect.md) en **true**, WMI se vuelve a conectar automáticamente a un proveedor remoto si se interrumpe la conexión para que no sea necesario comprobar el estado de la conexión.

Como se muestra en el siguiente script de ejemplo de código de script, debe realizar una llamada de actualización inicial para obtener un valor inicial para el objeto que está actualizando. Las llamadas posteriores a la actualización contienen datos.

> [!Note]  
> Cuando un script tiene acceso a los datos del contador de rendimiento de WMI desde un equipo remoto, el script solo se puede ejecutar en la cuenta de usuario que ha iniciado la sesión actual. WMI no admite una llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) que pase otras credenciales de usuario. Por lo tanto, la cuenta que llama al equipo remoto ya debe tener los privilegios adecuados en dicho equipo.

 

En el ejemplo de código de script siguiente se muestra cómo usar un objeto [**SWbemRefresher**](swbemrefresher.md) para actualizar los datos de los objetos de contador de rendimiento. Para obtener más información sobre el uso de contadores de rendimiento en WMI, consulte [acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a>Ejemplo

En el ejemplo de código de script siguiente se muestra que debe realizar una llamada de actualización inicial para obtener un valor de inicio para el objeto actualizado. Las llamadas posteriores a la actualización contienen datos.

En el ejemplo de código de script siguiente se muestra cómo usar un objeto [**SWbemRefresher**](swbemrefresher.md) para actualizar los datos de los objetos de contador de rendimiento. Para obtener más información sobre el uso de contadores de rendimiento en WMI, consulte [acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Tareas WMI: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
