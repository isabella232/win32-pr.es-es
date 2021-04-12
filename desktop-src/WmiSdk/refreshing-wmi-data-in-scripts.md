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
# <a name="refreshing-wmi-data-in-scripts"></a><span data-ttu-id="a8280-104">Actualizar datos WMI en scripts</span><span class="sxs-lookup"><span data-stu-id="a8280-104">Refreshing WMI Data in Scripts</span></span>

<span data-ttu-id="a8280-105">En los scripts de supervisión, puede evitar las llamadas sucesivas a **GetObject** mediante el uso de un objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="a8280-105">In monitoring scripts, you can avoid successive calls to **GetObject** by using an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="a8280-106">El objeto **SWbemRefresher** es un contenedor que puede contener varios objetos WMI cuyos datos se pueden actualizar en una llamada.</span><span class="sxs-lookup"><span data-stu-id="a8280-106">The **SWbemRefresher** object is a container that can hold several WMI objects whose data can be refreshed in one call.</span></span>

<span data-ttu-id="a8280-107">El uso de un objeto [**SWbemRefresher**](swbemrefresher.md) es necesario para obtener datos precisos de las clases de rendimiento de WMI, como [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) u otras clases preinstaladas derivadas de [**\_ rendimiento de Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="a8280-107">Using an [**SWbemRefresher**](swbemrefresher.md) object is required to get accurate data from WMI performance classes, such as [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) or other preinstalled classes derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span>

<span data-ttu-id="a8280-108">En el procedimiento siguiente se describe cómo actualizar los datos de los scripts.</span><span class="sxs-lookup"><span data-stu-id="a8280-108">The following procedure describes how to refresh data in scripts.</span></span>

<span data-ttu-id="a8280-109">**Para actualizar datos en scripts**</span><span class="sxs-lookup"><span data-stu-id="a8280-109">**To refresh data in scripts**</span></span>

1.  <span data-ttu-id="a8280-110">Llame a **CreateObject** para crear un objeto de actualizador de [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="a8280-110">Call **CreateObject** to create an [**SWbemRefresher**](swbemrefresher.md) refresher object.</span></span>

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  <span data-ttu-id="a8280-111">Conéctese al espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="a8280-111">Connect to the WMI namespace.</span></span> <span data-ttu-id="a8280-112">Para usar las clases de [**\_ rendimiento de Win32**](/windows/desktop/CIMWin32Prov/win32-perf) preinstaladas, conéctese a la **raíz \\ cimv2**.</span><span class="sxs-lookup"><span data-stu-id="a8280-112">To use preinstalled [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) performances classes, connect to **root\\cimv2**.</span></span>

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  <span data-ttu-id="a8280-113">Agregue un solo objeto (llame a [**SWbemRefresher. Add**](swbemrefresher-add.md)) o una colección (llame a [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) al actualizador.</span><span class="sxs-lookup"><span data-stu-id="a8280-113">Add a single object (call [**SWbemRefresher.Add**](swbemrefresher-add.md)) or a collection (call [**SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)) to the refresher.</span></span>

    <span data-ttu-id="a8280-114">Utilice las clases de datos precalculadas derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), por ejemplo, [**Win32 \_ PerfFormattedData \_ Perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) en lugar de [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="a8280-114">Use the precalculated data classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), for example, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) instead of [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="a8280-115">De lo contrario, debe calcular los valores de todas las propiedades que no sean contadores simples.</span><span class="sxs-lookup"><span data-stu-id="a8280-115">Otherwise, you must calculate the values for all of the properties other than simple counters.</span></span>

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  <span data-ttu-id="a8280-116">Actualice los datos una vez para obtener los datos de rendimiento iniciales.</span><span class="sxs-lookup"><span data-stu-id="a8280-116">Refresh the data one time to get the initial performance data.</span></span>

    <span data-ttu-id="a8280-117">Llame al método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) o al método genérico [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="a8280-117">Call either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the generic [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

    ```VB
    objRefresher.Refresh
    ```

    

5.  <span data-ttu-id="a8280-118">Si está supervisando el rendimiento y tiene una colección en el objeto actualizador, recorra en bucle los objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="a8280-118">If you are monitoring performance and have a collection in the refresher object, loop through the collection objects.</span></span>

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  <span data-ttu-id="a8280-119">Borre los elementos del actualizador llamando a [**SWbemRefresher. deleteAll**](swbemrefresher-deleteall.md) o quite elementos específicos llamando a [**SWbemRefresher. Remove**](swbemrefresher-remove.md).</span><span class="sxs-lookup"><span data-stu-id="a8280-119">Clear the items from the refresher by calling [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) or remove specific items by calling [**SwbemRefresher.Remove**](swbemrefresher-remove.md).</span></span>

<span data-ttu-id="a8280-120">En el ejemplo de código de VBScript siguiente se muestra cómo actualizar un solo objeto en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="a8280-120">The following VBScript code example shows how to refresh a single object on the local computer.</span></span> <span data-ttu-id="a8280-121">El script crea un contenedor actualizado y agrega una instancia de un enumerador para las instancias de [**\_ proceso de PerfFormattedData \_ PerfProc \_ de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="a8280-121">The script creates a refresher container and adds an instance of an enumerator for [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instances.</span></span> <span data-ttu-id="a8280-122">La llamada de [**actualización**](swbemrefresher-refresh.md) se realiza tres veces para mostrar los cambios en la propiedad **PercentProcessorTime** para los procesos que usan más de un porcentaje de tiempo de procesador.</span><span class="sxs-lookup"><span data-stu-id="a8280-122">The [**Refresh**](swbemrefresher-refresh.md) call is made three times to demonstrate the changes in the **PercentProcessorTime** property for processes using more than one percent of the processor time.</span></span>


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



<span data-ttu-id="a8280-123">La propiedad [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelta representa el índice del objeto en la colección del actualizador.</span><span class="sxs-lookup"><span data-stu-id="a8280-123">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span> <span data-ttu-id="a8280-124">Puede llamar a la propiedad [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) para determinar si un elemento de un actualizador es un elemento único o una colección.</span><span class="sxs-lookup"><span data-stu-id="a8280-124">You can call [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) property to determine whether or not an item in a refresher is a single item or a collection.</span></span> <span data-ttu-id="a8280-125">Para tener acceso a un único elemento, use la propiedad [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="a8280-125">To access a single item, use the [**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) property.</span></span> <span data-ttu-id="a8280-126">Si no realiza la llamada a **SWbemRefreshableItem. Object**, el script generará un error cuando intente obtener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="a8280-126">If you do not make the call to **SWbemRefreshableItem.Object**, then the script fails when you try to access the object.</span></span> <span data-ttu-id="a8280-127">Para tener acceso a una colección, use la propiedad [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .</span><span class="sxs-lookup"><span data-stu-id="a8280-127">To access a collection, use the [**SWbemRefreshableItem.ObjectSet**](swbemrefreshableitem-objectset.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8280-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8280-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8280-129">Clases de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8280-129">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="a8280-130">Obtener acceso a los datos de rendimiento del script</span><span class="sxs-lookup"><span data-stu-id="a8280-130">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="a8280-131">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8280-131">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="a8280-132">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="a8280-132">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
