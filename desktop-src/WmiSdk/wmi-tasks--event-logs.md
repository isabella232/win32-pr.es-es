---
description: Las tareas WMI para los registros de eventos obtienen datos de eventos de los archivos de registro de eventos y realizan operaciones como la copia de seguridad o el borrado de archivos de registro. Para ver otros ejemplos, vea el ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: f6d4e68e-d757-44aa-be74-3b26168626b8
ms.tgt_platform: multiple
title: 'Tareas de WMI: Registros de eventos '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fdcfe3f547e58fa60e552abad9867f8556fc8b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715822"
---
# <a name="wmi-tasks-event-logs"></a><span data-ttu-id="343f8-104">Tareas de WMI: Registros de eventos </span><span class="sxs-lookup"><span data-stu-id="343f8-104">WMI Tasks: Event Logs</span></span>

<span data-ttu-id="343f8-105">Las tareas WMI para los registros de eventos obtienen datos de eventos de los archivos de registro de eventos y realizan operaciones como la copia de seguridad o el borrado de archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="343f8-105">WMI tasks for event logs obtain event data from event log files and perform operations like backing up or clearing log files.</span></span> <span data-ttu-id="343f8-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="343f8-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="343f8-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="343f8-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="343f8-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="343f8-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="343f8-109">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="343f8-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="343f8-110">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="343f8-110">**To run a script**</span></span>

1.  <span data-ttu-id="343f8-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="343f8-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="343f8-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="343f8-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="343f8-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="343f8-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="343f8-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="343f8-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="343f8-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="343f8-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="343f8-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="343f8-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="343f8-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="343f8-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="343f8-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="343f8-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="343f8-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="343f8-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="343f8-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="343f8-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="343f8-121">How do I...</span></span></th>
<th><span data-ttu-id="343f8-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="343f8-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="343f8-123">... ¿recuperar información acerca del registro de eventos de seguridad?</span><span class="sxs-lookup"><span data-stu-id="343f8-123">...retrieve information about the Security event log?</span></span></td>
<td><span data-ttu-id="343f8-124">Incluya el privilegio de <a href="privilege-constants.md">seguridad</a> al conectarse a la clase <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="343f8-124">Include the <a href="privilege-constants.md">Security</a> privilege when connecting to the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class.</span></span> <span data-ttu-id="343f8-125">Para obtener más información, vea <a href="executing-privileged-operations-using-vbscript.md">ejecutar operaciones con privilegios mediante VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="343f8-125">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-126">VB</span><span class="sxs-lookup"><span data-stu-id="343f8-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate,(Security)}!\\&quot; & _
        strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTEventLogFile &quot; _
        & &quot;Where LogFileName=&#39;Security&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
    Wscript.Echo &quot;Maximum Size: &quot; _
    &  objLogfile.MaxFileSize 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="343f8-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;security&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    &quot;Record Number: &quot; + $objLogFile.NumberOfRecords
    &quot;Maximum Size: &quot; + $objLogFile.MaxFileSize
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="343f8-128">... ¿realizar una copia de seguridad de un registro de eventos?</span><span class="sxs-lookup"><span data-stu-id="343f8-128">...back up an event log?</span></span></td>
<td><p><span data-ttu-id="343f8-129">Use la clase <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> y el método <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="343f8-129">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="343f8-130">Es posible que tenga que incluir el privilegio de <a href="privilege-constants.md">copia de seguridad</a> al conectarse a WMI.</span><span class="sxs-lookup"><span data-stu-id="343f8-130">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="343f8-131">Para obtener más información, vea <a href="executing-privileged-operations-using-vbscript.md">ejecutar operaciones con privilegios mediante VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="343f8-131">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-132">VB</span><span class="sxs-lookup"><span data-stu-id="343f8-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    errBackupLog = objLogFile.BackupEventLog(&quot;c:\scripts\application.evt&quot;)
    WScript.Echo &quot;File saved as c:\scripts\applications.evt&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="343f8-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.BackupEventlog(&quot;c:\scripts\applications.evt&quot;)
    &quot;File saved as c:\scripts\applications.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="343f8-134">... ¿desea hacer una copia de seguridad de un registro de eventos más de una vez?</span><span class="sxs-lookup"><span data-stu-id="343f8-134">...back up an event log more than once?</span></span></td>
<td><p><span data-ttu-id="343f8-135">Asegúrese de que el archivo de copia de seguridad tiene un nombre único antes de usar los <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> y el método <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="343f8-135">Ensure that the backup file has a unique name before using the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="343f8-136">El sistema operativo no permite sobrescribir un archivo de copia de seguridad existente; debe trasladar el archivo de copia de seguridad o cambiarle el nombre para poder volver a ejecutar el script.</span><span class="sxs-lookup"><span data-stu-id="343f8-136">The operating system does not allow you to overwrite an existing backup file; you must either move the backup file or rename it before you can run the script again.</span></span> <span data-ttu-id="343f8-137">Es posible que tenga que incluir el privilegio de <a href="privilege-constants.md">copia de seguridad</a> al conectarse a WMI.</span><span class="sxs-lookup"><span data-stu-id="343f8-137">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="343f8-138">Para obtener más información, vea <a href="executing-privileged-operations-using-vbscript.md">ejecutar operaciones con privilegios mediante VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="343f8-138">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-139">VB</span><span class="sxs-lookup"><span data-stu-id="343f8-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>dtmThisDay = Day(Date)
dtmThisMonth = Month(Date)
dtmThisYear = Year(Date)
strBackupName = dtmThisYear & &quot;_&quot; & dtmThisMonth & &quot;_&quot; & dtmThisDay
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.BackupEventLog(&quot;c:\scripts\&quot; & strBackupName & &quot;_application.evt&quot;)
    objLogFile.ClearEventLog()
    WScript.Echo &quot;File saved: &quot; & strBackupName & &quot;_application.evt&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="343f8-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$CurDate = Get-Date
$strBackupName = $curDate.Year.ToString() + &quot;_&quot; + $curDate.Month.ToString() + &quot;_&quot; + $CurDate.Day.ToString()

$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    $BackupFile = $objLogFile.BackupEventlog(&quot;c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;)
    &quot;File saved: c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="343f8-141">... ¿determinar el número de registros en un registro de eventos?</span><span class="sxs-lookup"><span data-stu-id="343f8-141">...determine the number of records in an event log?</span></span></td>
<td><p><span data-ttu-id="343f8-142">Use la clase <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> y compruebe el valor de la propiedad <strong>NumberOfRecords</strong> .</span><span class="sxs-lookup"><span data-stu-id="343f8-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and check the value of the <strong>NumberOfRecords</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-143">VB</span><span class="sxs-lookup"><span data-stu-id="343f8-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;System&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="343f8-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    $objLogFile.NumberOfRecords
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="343f8-145">... ¿borrar mis registros de eventos?</span><span class="sxs-lookup"><span data-stu-id="343f8-145">...clear my event logs?</span></span></td>
<td><p><span data-ttu-id="343f8-146">Use la clase <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> y el método <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="343f8-146">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-147">VB</span><span class="sxs-lookup"><span data-stu-id="343f8-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup, Security)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.ClearEventLog()
    WScript.Echo &quot;Cleared application event log file&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="343f8-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.ClearEventlog()
    &quot;Cleared application event log file&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="343f8-149">... ¿leer eventos de los registros de eventos?</span><span class="sxs-lookup"><span data-stu-id="343f8-149">...read events from the event logs?</span></span></td>
<td><p><span data-ttu-id="343f8-150">Utilice la clase <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="343f8-150">Use the <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-151">VB</span><span class="sxs-lookup"><span data-stu-id="343f8-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colLoggedEvents = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTLogEvent &quot; _
        & &quot;Where Logfile = &#39;System&#39;&quot;)
For Each objEvent in colLoggedEvents
    Wscript.Echo &quot;Category: &quot; & objEvent.Category & VBNewLine _
    & &quot;Computer Name: &quot; & objEvent.ComputerName & VBNewLine _
    & &quot;Event Code: &quot; & objEvent.EventCode & VBNewLine _
    & &quot;Message: &quot; & objEvent.Message & VBNewLine _
    & &quot;Record Number: &quot; & objEvent.RecordNumber & VBNewLine _
    & &quot;Source Name: &quot; & objEvent.SourceName & VBNewLine _
    & &quot;Time Written: &quot; & objEvent.TimeWritten & VBNewLine _
    & &quot;Event Type: &quot; & objEvent.Type & VBNewLine _
    & &quot;User: &quot; & objEvent.User
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343f8-152">PowerShell</span><span class="sxs-lookup"><span data-stu-id="343f8-152">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTLogEvent -ComputerName $strComputer | Where-Object {$_.LogFile -eq &#39;System&#39;}

foreach ($objEvent in $colLoggedEvents) 
{ 
    &quot;Category: &quot; + $objEvent.Category
    &quot;Computer Name: &quot; + $objEvent.ComputerName
    &quot;Event Code: &quot; + $objEvent.EventCode
    &quot;Message: &quot; + $objEvent.Message
    &quot;Record Number: &quot; + $objEvent.RecordNumber
    &quot;Source Name: &quot; + $objEvent.SourceName
    &quot;Time Written: &quot; + $objEvent.TimeWritten
    &quot;Event Type: &quot; + $objEvent.Type
    &quot;User: &quot; + $objEvent.Use
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="343f8-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="343f8-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343f8-154">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="343f8-154">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="343f8-155">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="343f8-155">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="343f8-156">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="343f8-156">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

