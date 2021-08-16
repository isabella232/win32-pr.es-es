---
description: Use las clases WMI que obtienen datos de los contadores de rendimiento para acceder a los datos sobre el rendimiento del equipo y actualizarlo.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Tareas wmi: supervisión del rendimiento'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91302b0d6c6e13f86f275d755c5f4b6150de6a59dd400e47ed877d01f3fe876e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312061"
---
# <a name="wmi-tasks-performance-monitoring"></a>Tareas wmi: supervisión del rendimiento

Use las clases WMI que obtienen datos de los contadores de rendimiento para acceder a los datos sobre el rendimiento del equipo y actualizarlo. Para obtener otros ejemplos, vea ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Para obtener más información, vea [Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md) y Supervisión de datos de [rendimiento](monitoring-performance-data.md).

Los ejemplos de script que se muestran en este tema obtienen datos solo del equipo local. Para obtener más información sobre cómo usar el script para obtener datos de equipos remotos, vea [Conectarse a WMI en un equipo remoto.](connecting-to-wmi-on-a-remote-computer.md)


En el procedimiento siguiente se describe cómo ejecutar un script.

**Para ejecutar un script**

1.  Copie el código y guárdelo en un archivo con una extensión .vbs, como *filename.vbs*. Asegúrese de que el editor de texto no agrega una .txt extensión al archivo.
2.  Abra una ventana del símbolo del sistema y vaya al directorio donde guardó el archivo.
3.  Escriba **cscript filename.vbs** en el símbolo del sistema.
4.  Si no puede acceder a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados. Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).

> [!Note]  
> De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema. Dado que los scripts WMI pueden generar grandes cantidades de salida, es posible que desee redirigir la salida a un archivo. Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del *script* filename.vbsa *outfile.txt*.

 

En la tabla siguiente se enumeran ejemplos de script que se pueden usar para obtener varios tipos de datos del equipo local.



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
<td>... obtener los datos del contador de rendimiento que puedo ver en la utilidad Perfmon en un script.</td>
<td>Use clases que tengan nombres que comiencen &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">por Win32_PerfFormattedData</a> &quot; , por <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>ejemplo, Win32_PerfFormattedData_PerfProc_Process</strong></a>. Las propiedades con nombres <strong>como PageFileBytes corresponden</strong> a los contadores de rendimiento que se ven en Perfmon. Las &quot; Win32_PerfFormattedData &quot; calculan automáticamente los valores finales de los contadores.<br/></td>
</tr>
<tr class="even">
<td>... obtener datos de rendimiento en marcha para un único proceso, unidad de disco y otros datos.</td>
<td>Use el <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> o la clase de contador de rendimiento con formato <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">adecuada</a> y <a href="swbemobjectex-refresh-.md"><strong>el SWbemObjectEx.Refresh_</strong></a> método. Para obtener más información, vea <a href="scripting-with-swbemobject.md">Scripting con SWbemObject</a>.<br/> En C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> e <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>. Para obtener más información, vea <a href="monitoring-performance-data.md">Supervisión de datos de rendimiento.</a><br/> El siguiente script se ejecuta hasta que se reinicia el equipo, WMI se detiene o se detiene el script. Para detener el script manualmente, use Administrador de tareas para detener el proceso. Para detenerla mediante programación, use el <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>método Terminate</strong></a> de la <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> clase .<br/> <span data-codelanguage="VisualBasic"></span>
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
<td>... obtener datos de rendimiento en marcha para todos los procesos sin sondeo repetido?</td>
<td><p>Use clases que tengan nombres que comiencen &quot; por Win32_PerfFormattedData y un objeto &quot; <a href="swbemrefresher.md"><strong>SWbemRefresher.</strong></a> El actualizador contiene los objetos, por lo que no es necesario obtener la colección varias veces. Se necesitan dos valores como mínimo para calcular los datos de rendimiento, ya que la mayoría de los contadores son contadores de velocidad. La primera vez que muestre los datos del actualizador, está vacío.</p>
<p>El siguiente script se ejecuta indefinidamente hasta que se reinicia el equipo, WMI se detiene o se detiene el script. Para detener el script manualmente, use Administrador de tareas para detener el proceso. Para detenerla mediante programación, use el <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>método Terminate</strong></a> de la <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> clase .</p>
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
<td>... ¿Obtener y calcular los datos de rendimiento de los procesos Windows 2000?</td>
<td><p>Use las &quot; &quot; Win32_PerfRawData, como <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>. Obtenga los datos de propiedad, como <strong>PercentProcessorTime,</strong>dos veces para un proceso específico. Busque la fórmula especificada en el <a href="countertype-qualifier.md"><strong>calificador CounterType</strong></a> para la propiedad y calcule. CounterType en el ejemplo es <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Para obtener más información, vea <a href="monitoring-performance-data.md">Supervisión de datos de rendimiento.</a></p>
<p>El siguiente script se ejecuta indefinidamente hasta que se reinicia el equipo, WMI se detiene o se detiene el script. Para detener el script manualmente, use Administrador de tareas para detener el proceso. Para detenerla mediante programación, use el <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>método Terminate</strong></a> de la <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> clase .</p>
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

[Tareas wmi para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Ejemplos de aplicaciones wmi de C++](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
