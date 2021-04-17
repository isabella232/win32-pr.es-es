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
# <a name="wmi-tasks-performance-monitoring"></a>Tareas WMI: supervisión del rendimiento

Utilice las clases WMI que obtienen datos de contadores de rendimiento para obtener acceso y actualizar datos sobre el rendimiento del equipo. Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Para obtener más información, consulte [bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md) y [supervisión de datos de rendimiento](monitoring-performance-data.md).

Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local. Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).


En el procedimiento siguiente se describe cómo ejecutar un script.

**Para ejecutar un script**

1.  Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*. Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.
2.  Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.
3.  Escriba **cscript filename.vbs** en el símbolo del sistema.
4.  Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados. Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).

> [!Note]  
> De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema. Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo. Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.

 

En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Cómo...</th>
<th>Clases o métodos WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... obtener los datos del contador de rendimiento que se pueden ver en la utilidad Perfmon en un script</td>
<td>Utilice clases que tengan nombres que comiencen por &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , por ejemplo <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>. Las propiedades con nombres como <strong>PageFileBytes</strong> se corresponden con los contadores de rendimiento que se ven en Perfmon. Las &quot; clases de Win32_PerfFormattedData &quot; calculan los valores finales de los contadores.<br/></td>
</tr>
<tr class="even">
<td>... obtener datos de rendimiento en curso para un único proceso, unidad de disco y otros datos</td>
<td>Use el <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> o la clase de <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">contador de rendimiento</a> con formato adecuada y el método <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> . Para obtener más información, consulte <a href="scripting-with-swbemobject.md">scripting con SWbemObject</a>.<br/> En C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher:: AddObjectByPath</strong></a> y <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher:: Refresh</strong></a>. Para obtener más información, vea <a href="monitoring-performance-data.md">supervisar datos de rendimiento</a>.<br/> El siguiente script se ejecuta hasta que se reinicia el equipo, se detiene WMI o se detiene el script. Para detener el script manualmente, use el administrador de tareas para detener el proceso. Para detenerlo mediante programación, use el método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> en la clase <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... obtener datos de rendimiento en curso para todos los procesos sin sondeos repetidos</td>
<td><p>Utilice clases que tengan nombres que comiencen por &quot; Win32_PerfFormattedData &quot; y un objeto <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> . El actualizador contiene los objetos, por lo que no es necesario obtener la colección repetidamente. Se necesita un mínimo de dos valores para calcular los datos de rendimiento, ya que la mayoría de los contadores son de frecuencia. La primera vez que se muestran los datos del actualizador están vacíos.</p>
<p>El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script. Para detener el script manualmente, use el administrador de tareas para detener el proceso. Para detenerlo mediante programación, use el método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> en la clase <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... obtener y calcular los datos de rendimiento de los procesos en Windows 2000</td>
<td><p>Utilice las &quot; clases de Win32_PerfRawData &quot; , como <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>. Obtenga los datos de la propiedad, como <strong>PercentProcessorTime</strong>, dos veces para un proceso específico. Busque la fórmula especificada en el calificador de <a href="countertype-qualifier.md"><strong>tipo</strong></a> de la propiedad y calcule. El tipo de PERTYPE en el ejemplo es <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Para obtener más información, vea <a href="monitoring-performance-data.md">supervisar datos de rendimiento</a>.</p>
<p>El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script. Para detener el script manualmente, use el administrador de tareas para detener el proceso. Para detenerlo mediante programación, use el método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> en la clase <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Ejemplos de aplicaciones de C++ de WMI](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter de TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
