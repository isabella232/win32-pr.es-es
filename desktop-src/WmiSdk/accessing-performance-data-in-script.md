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
# <a name="accessing-performance-data-in-script"></a><span data-ttu-id="04bf3-103">Obtener acceso a los datos de rendimiento del script</span><span class="sxs-lookup"><span data-stu-id="04bf3-103">Accessing Performance Data in Script</span></span>

<span data-ttu-id="04bf3-104">Los scripts de WMI pueden tener acceso a las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes)de WMI preinstaladas, ya sea en el equipo local o de forma remota.</span><span class="sxs-lookup"><span data-stu-id="04bf3-104">WMI scripts can access the preinstalled WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes), either on the local computer or remotely.</span></span> <span data-ttu-id="04bf3-105">Mientras que los scripts pueden obtener datos de clases no calculadas, como la memoria de rendimiento de PerfRawData de Win32, o clases con formato, la [**memoria de \_ PerfFormattedData de \_ rendimiento \_ de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), las clases de datos con formato pueden ser más fáciles de usar. [**\_ \_ \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)</span><span class="sxs-lookup"><span data-stu-id="04bf3-105">While scripts can obtain data from uncalculated classes, such as [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), or formatted classes, [**Win32\_PerfFormattedData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), the formatted data classes can be easier to use.</span></span>

<span data-ttu-id="04bf3-106">La supervisión de los datos de rendimiento con las clases de contador de rendimiento requiere el uso de un [*actualizador*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="04bf3-106">Monitoring performance data with the performance counter classes requires the use of a [*refresher*](gloss-r.md).</span></span> <span data-ttu-id="04bf3-107">Use el objeto [**SWbemRefresher**](swbemrefresher.md) para almacenar uno o más objetos de rendimiento para actualizar o actualizar un solo objeto mediante la llamada a [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="04bf3-107">Use the [**SWbemRefresher**](swbemrefresher.md) object to store one or more performance objects for refresh or refresh a single object by the [**SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md) call.</span></span> <span data-ttu-id="04bf3-108">Para obtener más información, vea [actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="04bf3-108">For more information, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="04bf3-109">Al establecer la propiedad [**SWbemRefresher. reconexión automática**](swbemrefresher-autoreconnect.md) en **true**, WMI se vuelve a conectar automáticamente a un proveedor remoto si se interrumpe la conexión para que no sea necesario comprobar el estado de la conexión.</span><span class="sxs-lookup"><span data-stu-id="04bf3-109">By setting the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **TRUE**, WMI automatically reconnects to a remote provider if the connection is broken so that you do not need to check for connection status.</span></span>

<span data-ttu-id="04bf3-110">Como se muestra en el siguiente script de ejemplo de código de script, debe realizar una llamada de actualización inicial para obtener un valor inicial para el objeto que está actualizando.</span><span class="sxs-lookup"><span data-stu-id="04bf3-110">As shown in the following script code example script, you must make an initial refresh call to get a starting value for the object you are refreshing.</span></span> <span data-ttu-id="04bf3-111">Las llamadas posteriores a la actualización contienen datos.</span><span class="sxs-lookup"><span data-stu-id="04bf3-111">Subsequent refresh calls then contain data.</span></span>

> [!Note]  
> <span data-ttu-id="04bf3-112">Cuando un script tiene acceso a los datos del contador de rendimiento de WMI desde un equipo remoto, el script solo se puede ejecutar en la cuenta de usuario que ha iniciado la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="04bf3-112">When a script is accessing WMI performance counter data from a remote computer, the script can only run under the current logged-on user account.</span></span> <span data-ttu-id="04bf3-113">WMI no admite una llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) que pase otras credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="04bf3-113">WMI does not support an [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) call that passes in different user credentials.</span></span> <span data-ttu-id="04bf3-114">Por lo tanto, la cuenta que llama al equipo remoto ya debe tener los privilegios adecuados en dicho equipo.</span><span class="sxs-lookup"><span data-stu-id="04bf3-114">Therefore, the account calling the remote computer must already have the appropriate privileges on that computer.</span></span>

 

<span data-ttu-id="04bf3-115">En el ejemplo de código de script siguiente se muestra cómo usar un objeto [**SWbemRefresher**](swbemrefresher.md) para actualizar los datos de los objetos de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="04bf3-115">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="04bf3-116">Para obtener más información sobre el uso de contadores de rendimiento en WMI, consulte [acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="04bf3-116">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


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



## <a name="example"></a><span data-ttu-id="04bf3-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04bf3-117">Example</span></span>

<span data-ttu-id="04bf3-118">En el ejemplo de código de script siguiente se muestra que debe realizar una llamada de actualización inicial para obtener un valor de inicio para el objeto actualizado.</span><span class="sxs-lookup"><span data-stu-id="04bf3-118">The following script code example shows that you must make an initial refresh call to get a starting value for the refreshed object.</span></span> <span data-ttu-id="04bf3-119">Las llamadas posteriores a la actualización contienen datos.</span><span class="sxs-lookup"><span data-stu-id="04bf3-119">Subsequent refresh calls then contain data.</span></span>

<span data-ttu-id="04bf3-120">En el ejemplo de código de script siguiente se muestra cómo usar un objeto [**SWbemRefresher**](swbemrefresher.md) para actualizar los datos de los objetos de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="04bf3-120">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="04bf3-121">Para obtener más información sobre el uso de contadores de rendimiento en WMI, consulte [acceso a las clases de rendimiento preinstaladas de WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="04bf3-121">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="04bf3-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04bf3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04bf3-123">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="04bf3-123">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="04bf3-124">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="04bf3-124">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="04bf3-125">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="04bf3-125">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
