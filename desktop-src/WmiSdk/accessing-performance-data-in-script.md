---
description: Los scripts WMI pueden acceder a las clases de contador de rendimiento WMI preinstaladas, ya sea en el equipo local o de forma remota.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Acceso a datos de rendimiento en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 42fe1ecdbaf5cdc5cbafc53117ad7c8f370dae2b4e1a3adcee3a4fcf719c995a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320448"
---
# <a name="accessing-performance-data-in-script"></a>Acceso a datos de rendimiento en script

Los scripts WMI pueden acceder a las clases de contador de rendimiento [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes)preinstaladas, ya sea en el equipo local o de forma remota. Aunque los scripts pueden obtener datos de clases nocalculadas, como [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)o clases con formato, [**\_ Win32 PerfFormattedData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), las clases de datos con formato pueden ser más fáciles de usar.

La supervisión de los datos de rendimiento con las clases de contador de rendimiento requiere el uso de [*un actualizador*](gloss-r.md). Use el [**objeto SWbemRefresher**](swbemrefresher.md) para almacenar uno o varios objetos de rendimiento para actualizar o actualizar un único objeto mediante la llamada [**SWbemObjectEx.Refresh.**](swbemobjectex-refresh-.md) Para obtener más información, vea [Actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md).

Al establecer la propiedad [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) en **TRUE,** WMI se vuelve a conectar automáticamente a un proveedor remoto si la conexión está rota, por lo que no es necesario comprobar el estado de la conexión.

Como se muestra en el siguiente script de ejemplo de código de script, debe realizar una llamada de actualización inicial para obtener un valor inicial para el objeto que está actualizando. Las llamadas de actualización posteriores contienen datos.

> [!Note]  
> Cuando un script accede a los datos del contador de rendimiento wmi desde un equipo remoto, el script solo se puede ejecutar en la cuenta de usuario que inició sesión actualmente. WMI no admite una [**llamada SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) que pase credenciales de usuario diferentes. Por lo tanto, la cuenta que llama al equipo remoto ya debe tener los privilegios adecuados en ese equipo.

 

En el siguiente ejemplo de código de script se muestra cómo usar un [**objeto SWbemRefresher**](swbemrefresher.md) para actualizar los datos en objetos de contador de rendimiento. Para obtener más información sobre el uso de contadores de rendimiento en WMI, vea [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).


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

En el siguiente ejemplo de código de script se muestra que debe realizar una llamada de actualización inicial para obtener un valor inicial para el objeto actualizado. Las llamadas de actualización posteriores contienen datos.

En el siguiente ejemplo de código de script se muestra cómo usar un [**objeto SWbemRefresher**](swbemrefresher.md) para actualizar los datos en objetos de contador de rendimiento. Para obtener más información sobre el uso de contadores de rendimiento en WMI, vea [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).


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

[Tareas wmi: supervisión del rendimiento](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

 
