---
description: Utilice las clases WMI que obtienen datos de contadores de rendimiento para obtener acceso y actualizar datos sobre el rendimiento del equipo.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Tareas WMI: supervisión del rendimiento'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105660103"
---
# <a name="wmi-tasks-performance-monitoring"></a><span data-ttu-id="685e1-103">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="685e1-103">WMI Tasks: Performance Monitoring</span></span>

<span data-ttu-id="685e1-104">Utilice las clases WMI que obtienen datos de contadores de rendimiento para obtener acceso y actualizar datos sobre el rendimiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="685e1-104">Use the WMI classes that obtain data from performance counters to access and refresh data about computer performance.</span></span> <span data-ttu-id="685e1-105">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="685e1-105">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span> <span data-ttu-id="685e1-106">Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md) y [supervisión de datos de rendimiento](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="685e1-106">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

<span data-ttu-id="685e1-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="685e1-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="685e1-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="685e1-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="685e1-109">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="685e1-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="685e1-110">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="685e1-110">**To run a script**</span></span>

1.  <span data-ttu-id="685e1-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="685e1-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="685e1-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="685e1-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="685e1-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="685e1-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="685e1-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="685e1-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="685e1-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="685e1-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="685e1-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="685e1-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="685e1-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="685e1-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="685e1-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="685e1-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="685e1-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="685e1-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="685e1-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="685e1-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="685e1-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="685e1-121">How do I...</span></span></th>
<th><span data-ttu-id="685e1-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="685e1-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="685e1-123">... obtener los datos del contador de rendimiento que se pueden ver en la utilidad Perfmon en un script</span><span class="sxs-lookup"><span data-stu-id="685e1-123">...obtain the performance counter data that I can see in the Perfmon utility in a script?</span></span></td>
<td><span data-ttu-id="685e1-124">Utilice clases que tengan nombres que comiencen por &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , por ejemplo <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="685e1-124">Use classes that have names that begin with &quot;<a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>&quot;, for example <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="685e1-125">Las propiedades con nombres como <strong>PageFileBytes</strong> se corresponden con los contadores de rendimiento que se ven en Perfmon.</span><span class="sxs-lookup"><span data-stu-id="685e1-125">Properties with names like <strong>PageFileBytes</strong> correspond to performance counters you see in Perfmon.</span></span> <span data-ttu-id="685e1-126">Las &quot; clases de Win32_PerfFormattedData &quot; calculan los valores finales de los contadores.</span><span class="sxs-lookup"><span data-stu-id="685e1-126">The &quot;Win32_PerfFormattedData&quot; classes calculate the final values of counters for you.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685e1-127">... obtener datos de rendimiento en curso para un único proceso, unidad de disco y otros datos</span><span class="sxs-lookup"><span data-stu-id="685e1-127">...get on-going performance data for a single process, disk drive, and other data?</span></span></td>
<td><span data-ttu-id="685e1-128">Use el <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> o la clase de <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">contador de rendimiento</a> con formato adecuada y el método <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="685e1-128">Use the <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> or the appropriate formatted <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Performance Counter Class</a> and the <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> method.</span></span> <span data-ttu-id="685e1-129">Para obtener más información, consulte <a href="scripting-with-swbemobject.md">scripting con SWbemObject</a>.</span><span class="sxs-lookup"><span data-stu-id="685e1-129">For more information, see <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span></span><br/> <span data-ttu-id="685e1-130">En C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher:: AddObjectByPath</strong></a> y <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher:: Refresh</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="685e1-130">In C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> and <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>.</span></span> <span data-ttu-id="685e1-131">Para obtener más información, vea <a href="monitoring-performance-data.md">supervisar datos de rendimiento</a>.</span><span class="sxs-lookup"><span data-stu-id="685e1-131">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span><br/> <span data-ttu-id="685e1-132">El siguiente script se ejecuta hasta que se reinicia el equipo, se detiene WMI o se detiene el script.</span><span class="sxs-lookup"><span data-stu-id="685e1-132">The following script runs until the computer is restarted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="685e1-133">Para detener el script manualmente, use el administrador de tareas para detener el proceso.</span><span class="sxs-lookup"><span data-stu-id="685e1-133">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="685e1-134">Para detenerlo mediante programación, use el método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> en la clase <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="685e1-134">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="685e1-135">VB</span><span class="sxs-lookup"><span data-stu-id="685e1-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="685e1-136">... obtener datos de rendimiento en curso para todos los procesos sin sondeos repetidos</span><span class="sxs-lookup"><span data-stu-id="685e1-136">...get on-going performance data for all processes without repeated polling?</span></span></td>
<td><p><span data-ttu-id="685e1-137">Utilice clases que tengan nombres que comiencen por &quot; Win32_PerfFormattedData &quot; y un objeto <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="685e1-137">Use classes that have names that begin with &quot;Win32_PerfFormattedData&quot; and an <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> object.</span></span> <span data-ttu-id="685e1-138">El actualizador contiene los objetos, por lo que no es necesario obtener la colección repetidamente.</span><span class="sxs-lookup"><span data-stu-id="685e1-138">The refresher holds the objects so you do not need to get the collection repeatedly.</span></span> <span data-ttu-id="685e1-139">Se necesita un mínimo de dos valores para calcular los datos de rendimiento, ya que la mayoría de los contadores son de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="685e1-139">A minimum of two values are needed to calculate performance data because most counters are rate counters.</span></span> <span data-ttu-id="685e1-140">La primera vez que se muestran los datos del actualizador están vacíos.</span><span class="sxs-lookup"><span data-stu-id="685e1-140">The first time you display the refresher data it is empty.</span></span></p>
<p><span data-ttu-id="685e1-141">El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script.</span><span class="sxs-lookup"><span data-stu-id="685e1-141">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="685e1-142">Para detener el script manualmente, use el administrador de tareas para detener el proceso.</span><span class="sxs-lookup"><span data-stu-id="685e1-142">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="685e1-143">Para detenerlo mediante programación, use el método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> en la clase <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="685e1-143">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="685e1-144">VB</span><span class="sxs-lookup"><span data-stu-id="685e1-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="685e1-145">... obtener y calcular los datos de rendimiento de los procesos en Windows 2000</span><span class="sxs-lookup"><span data-stu-id="685e1-145">...get and calculate performance data for processes on Windows 2000?</span></span></td>
<td><p><span data-ttu-id="685e1-146">Utilice las &quot; clases de Win32_PerfRawData &quot; , como <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="685e1-146">Use the &quot;Win32_PerfRawData&quot; classes, such as <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="685e1-147">Obtenga los datos de la propiedad, como <strong>PercentProcessorTime</strong>, dos veces para un proceso específico.</span><span class="sxs-lookup"><span data-stu-id="685e1-147">Get the property data, such as <strong>PercentProcessorTime</strong>, twice for a specific process.</span></span> <span data-ttu-id="685e1-148">Busque la fórmula especificada en el calificador de <a href="countertype-qualifier.md"><strong>tipo</strong></a> de la propiedad y calcule.</span><span class="sxs-lookup"><span data-stu-id="685e1-148">Look up the formula specified in the <a href="countertype-qualifier.md"><strong>CounterType</strong></a> qualifier for the property and calculate.</span></span> <span data-ttu-id="685e1-149">El tipo de PERTYPE en el ejemplo es <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span><span class="sxs-lookup"><span data-stu-id="685e1-149">The CounterType in the example is <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span></span> <span data-ttu-id="685e1-150">Para obtener más información, vea <a href="monitoring-performance-data.md">supervisar datos de rendimiento</a>.</span><span class="sxs-lookup"><span data-stu-id="685e1-150">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span></p>
<p><span data-ttu-id="685e1-151">El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script.</span><span class="sxs-lookup"><span data-stu-id="685e1-151">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="685e1-152">Para detener el script manualmente, use el administrador de tareas para detener el proceso.</span><span class="sxs-lookup"><span data-stu-id="685e1-152">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="685e1-153">Para detenerlo mediante programación, use el método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> en la clase <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="685e1-153">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="685e1-154">VB</span><span class="sxs-lookup"><span data-stu-id="685e1-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="685e1-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="685e1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="685e1-156">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="685e1-156">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="685e1-157">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="685e1-157">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="685e1-158">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="685e1-158">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
