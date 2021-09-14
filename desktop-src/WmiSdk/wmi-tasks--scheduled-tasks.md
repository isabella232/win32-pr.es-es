---
description: Las tareas programadas de WMI crean y obtienen información sobre las tareas programadas. Para obtener otros ejemplos, vea ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Tareas wmi: tareas programadas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37a1d44a07feea7beb07984c383620fd2f166cdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172533"
---
# <a name="wmi-tasks-scheduled-tasks"></a>Tareas wmi: tareas programadas

Las tareas programadas de WMI crean y obtienen información sobre las tareas programadas. Para obtener otros ejemplos, vea ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Los ejemplos de script que se muestran en este tema obtienen datos solo del equipo local. Para obtener más información sobre cómo usar el script para obtener datos de equipos remotos, vea [Conectarse a WMI en un equipo remoto.](connecting-to-wmi-on-a-remote-computer.md)


En el procedimiento siguiente se describe cómo ejecutar un script.

**Para ejecutar un script**

1.  Copie el código y guárdelo en un archivo con una extensión .vbs, como *filename.vbs*. Asegúrese de que el editor de texto no agrega .txt extensión al archivo.
2.  Abra una ventana del símbolo del sistema y vaya al directorio donde guardó el archivo.
3.  Escriba **cscript filename.vbs** en el símbolo del sistema.
4.  Si no puede acceder a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados. Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).

> [!Note]  
> De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema. Dado que los scripts WMI pueden generar grandes cantidades de salida, es posible que desee redirigir la salida a un archivo. Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del *script* filename.vbsa *outfile.txt*.

 

En la tabla siguiente se enumeran ejemplos de script que se pueden usar para obtener varios tipos de datos del equipo local.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Cómo...</th>
<th>Clases o métodos WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... ¿Crear tareas programadas mediante scripts?</td>
<td>Use la <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> y el <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>método Create.</strong></a> Si tiene dificultades para que esta tarea funcione en Windows 7 o posterior, consulte la <strong>sección Win32_ScheduledJob</strong> Comentarios. es probable que la configuración le impida usar la clase .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p>En la cadena &quot; **",*143000.000000-420 (que se usa en el valor del parámetro &quot; <em>StartTime</em> del <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>método Create),</strong></a> &quot; **-143000.0000000 especifica que la tarea comienza a las &quot; 14:30 (2:30 p. m.) y &quot; -420 especifica la zona &quot; horaria. El número de zona horaria es el sesgo actual de la traducción de hora local. El sesgo es la diferencia entre la hora UTC y la hora local. Para calcular el sesgo de la zona horaria, multiplique el número de horas que la zona horaria está por delante o por detrás de la hora media de Greenwich (GMT) por 60 (use un número positivo para el número de horas si la zona horaria está por delante de GMT y un número negativo si la zona horaria está detrás de GMT). Agregue 60 adicionales al cálculo si la zona horaria usa el horario de verano. Por ejemplo, la zona horaria estándar del Pacífico está ocho horas por detrás de GMT, por lo que el sesgo es igual a -420 (-8 * 60 + 60) cuando el horario de verano está en uso y -480 (-8 * 60) cuando el horario de verano no está en uso. También puede determinar el valor del sesgo consultando la propiedad bias de la <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>clase Win32_TimeZone</strong></a> sesgo.</p></td>
</tr>
<tr class="even">
<td>... devuelve una lista de todas las tareas programadas en un equipo.</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> clase . Tenga en cuenta que esta clase solo puede devolver trabajos creados mediante un script o AT.exe. No puede devolver información sobre los trabajos creados por o modificados por el Asistente para tareas programadas.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
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

 

