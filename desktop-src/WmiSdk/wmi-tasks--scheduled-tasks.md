---
description: Tareas programadas de WMI crea y obtiene información acerca de las tareas programadas. Para ver otros ejemplos, vea el ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Tareas de WMI: tareas programadas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4051df4348ee47710b5d2d1f5dcc3f59f607d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659869"
---
# <a name="wmi-tasks-scheduled-tasks"></a><span data-ttu-id="de983-104">Tareas de WMI: tareas programadas</span><span class="sxs-lookup"><span data-stu-id="de983-104">WMI Tasks: Scheduled Tasks</span></span>

<span data-ttu-id="de983-105">Tareas programadas de WMI crea y obtiene información acerca de las tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="de983-105">WMI scheduled tasks create and get information about scheduled tasks.</span></span> <span data-ttu-id="de983-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="de983-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="de983-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="de983-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="de983-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="de983-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="de983-109">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="de983-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="de983-110">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="de983-110">**To run a script**</span></span>

1.  <span data-ttu-id="de983-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="de983-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="de983-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="de983-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="de983-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="de983-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="de983-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="de983-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="de983-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="de983-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="de983-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="de983-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="de983-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="de983-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="de983-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="de983-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="de983-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="de983-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="de983-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="de983-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de983-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="de983-121">How do I...</span></span></th>
<th><span data-ttu-id="de983-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="de983-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de983-123">... ¿crear tareas programadas mediante scripts?</span><span class="sxs-lookup"><span data-stu-id="de983-123">...create scheduled tasks using scripts?</span></span></td>
<td><span data-ttu-id="de983-124">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="de983-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method.</span></span> <span data-ttu-id="de983-125">Si tiene dificultades para que esta tarea funcione en Windows 7 o versiones posteriores, consulte la sección <strong>Win32_ScheduledJob</strong> comentarios; lo más probable es que la configuración impida utilizar la clase.</span><span class="sxs-lookup"><span data-stu-id="de983-125">If you are having difficulty making this task work on Windows 7 or later, see the <strong>Win32_ScheduledJob</strong> Remarks section; likely your settings are preventing you from using the class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de983-126">VB</span><span class="sxs-lookup"><span data-stu-id="de983-126">VB</span></span></th>
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

<p><span data-ttu-id="de983-127">En la cadena \* \* \* \* \* \* \* \* &quot; 143000.000000-420 &quot; (usada en el valor del parámetro <em>startTime</em> del método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> ), \* \* \* \* \* \* \* \* &quot; 143000,000000 &quot; especifica que la tarea comienza en 14,30 (2:30 P.M.) y &quot; -420 &quot; especifica la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="de983-127">In the string &quot;\*\*\*\*\*\*\*\*143000.000000-420&quot; (used in the <em>StartTime</em> parameter value of the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method), &quot;\*\*\*\*\*\*\*\*143000.000000&quot; specifies that the task starts at 14.30 (2:30 P.M.) and &quot;-420&quot; specifies the time zone.</span></span> <span data-ttu-id="de983-128">El número de zona horaria es la diferencia actual de la conversión de hora local.</span><span class="sxs-lookup"><span data-stu-id="de983-128">The time zone number is the current bias of the local time translation.</span></span> <span data-ttu-id="de983-129">La diferencia es la diferencia entre la hora UTC y la hora local.</span><span class="sxs-lookup"><span data-stu-id="de983-129">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="de983-130">Para calcular la diferencia de la zona horaria, multiplique el número de horas que la zona horaria está por encima o por detrás de la hora del meridiano de Greenwich (GMT) en 60 (use un número positivo para el número de horas si la zona horaria está por detrás de GMT y un número negativo si la zona horaria está tras la hora GMT).</span><span class="sxs-lookup"><span data-stu-id="de983-130">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="de983-131">Agregue un 60 adicional al cálculo si la zona horaria usa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="de983-131">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="de983-132">Por ejemplo, la zona horaria estándar del Pacífico es de ocho horas tras la hora GMT, por lo que la diferencia es igual a-420 (-8 \* 60 + 60) cuando el horario de verano está en uso y-480 (-8 \* 60) cuando el horario de verano no está en uso.</span><span class="sxs-lookup"><span data-stu-id="de983-132">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="de983-133">También puede determinar el valor de la diferencia consultando la propiedad bias de la clase <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="de983-133">You can also determine the value of the bias by querying the bias property of the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de983-134">... ¿se devuelve una lista de todas las tareas programadas en un equipo?</span><span class="sxs-lookup"><span data-stu-id="de983-134">...return a list of all the scheduled tasks on a computer?</span></span></td>
<td><p><span data-ttu-id="de983-135">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="de983-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class.</span></span> <span data-ttu-id="de983-136">Tenga en cuenta que esta clase solo puede devolver trabajos que se crean mediante un script o un AT.exe.</span><span class="sxs-lookup"><span data-stu-id="de983-136">Note that this class can only return jobs that are created using either a script or AT.exe.</span></span> <span data-ttu-id="de983-137">No puede devolver información acerca de los trabajos creados o modificados por el Asistente para tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="de983-137">It cannot return information about jobs that are either created by or modified by the Scheduled Task wizard.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de983-138">VB</span><span class="sxs-lookup"><span data-stu-id="de983-138">VB</span></span></th>
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



 

## <a name="related-topics"></a><span data-ttu-id="de983-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de983-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de983-140">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="de983-140">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="de983-141">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="de983-141">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="de983-142">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="de983-142">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

