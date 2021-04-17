---
description: Hay varias clases de WMI y un objeto de scripting para analizar o convertir el formato de fecha y hora de CIM. Para ver otros ejemplos, vea el ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: dd01a732-5c88-4c24-a551-4d5452e712cc
ms.tgt_platform: multiple
title: 'Tareas de WMI: fechas y horas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8864deb4f76b8ce6b76017c0348cdb86bf38b697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716984"
---
# <a name="wmi-tasks-dates-and-times"></a><span data-ttu-id="713ea-104">Tareas de WMI: fechas y horas</span><span class="sxs-lookup"><span data-stu-id="713ea-104">WMI Tasks: Dates and Times</span></span>

<span data-ttu-id="713ea-105">Hay varias clases de WMI y un objeto de scripting para analizar o convertir el formato de [fecha y hora de CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="713ea-105">There are several WMI classes and a scripting object to parse or convert the [CIM datetime](date-and-time-format.md) format.</span></span> <span data-ttu-id="713ea-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="713ea-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="713ea-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="713ea-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="713ea-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="713ea-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="713ea-109">Para ejecutar un script</span><span class="sxs-lookup"><span data-stu-id="713ea-109">To run a script</span></span>

<span data-ttu-id="713ea-110">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="713ea-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="713ea-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="713ea-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="713ea-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="713ea-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="713ea-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="713ea-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="713ea-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="713ea-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="713ea-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="713ea-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="713ea-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="713ea-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="713ea-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="713ea-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="713ea-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="713ea-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="713ea-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="713ea-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="713ea-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="713ea-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="713ea-121">How do I...</span></span></th>
<th><span data-ttu-id="713ea-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="713ea-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="713ea-123">... ¿desea convertir las fechas de WMI en fechas y horas estándar?</span><span class="sxs-lookup"><span data-stu-id="713ea-123">...convert WMI dates to standard dates and times?</span></span><br/></td>
<td><span data-ttu-id="713ea-124">Use el objeto <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> para convertirlos en fechas y horas normales.</span><span class="sxs-lookup"><span data-stu-id="713ea-124">Use the <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> object to convert these to regular dates and times.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-125">VB</span><span class="sxs-lookup"><span data-stu-id="713ea-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Set dtmInstallDate = CreateObject(&quot;WbemScripting.SWbemDateTime&quot;)
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objOS = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each strOS in objOS
    dtmInstallDate.Value = strOS.InstallDate
    Wscript.Echo dtmInstallDate.GetVarDate
Next</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="713ea-126">O hacer que el código Realice la tarea manualmente.</span><span class="sxs-lookup"><span data-stu-id="713ea-126">Or have your code do the task manually.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-127">VB</span><span class="sxs-lookup"><span data-stu-id="713ea-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Function WMIDateStringToDate(dtmInstallDate) 
    WMIDateStringToDate = CDate(Mid(dtmInstallDate, 5, 2) & &quot;/&quot; & Mid(dtmInstallDate, 7, 2) _
                        & &quot;/&quot; & Left(dtmInstallDate, 4) & &quot; &quot; & Mid (dtmInstallDate, 9, 2) & &quot;:&quot; _
                        & Mid(dtmInstallDate, 11, 2) & &quot;:&quot; & Mid(dtmInstallDate,13, 2)) 
End Function </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="713ea-128">... ¿determinar la hora configurada actualmente en un equipo?</span><span class="sxs-lookup"><span data-stu-id="713ea-128">...determine the time currently configured on a computer?</span></span></p></td>
<td><p><span data-ttu-id="713ea-129">Utilice la clase <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="713ea-129">Use the <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-130">VB</span><span class="sxs-lookup"><span data-stu-id="713ea-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_LocalTime&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Day:           &quot; & objItem.Day & VBNewLine _
               & &quot;Day Of Week:   &quot; & objItem.DayOfWeek & VBNewLine _
               & &quot;Hour:          &quot; & objItem.Hour & VBNewLine _
               & &quot;Minute:        &quot; & objItem.Minute & VBNewLine _
               & &quot;Month:         &quot; & objItem.Month & VBNewLine _
               & &quot;Quarter:       &quot; & objItem.Quarter & VBNewLine _
               & &quot;Second:        &quot; & objItem.Second & VBNewLine _
               & &quot;Week In Month: &quot; & objItem.WeekInMonth & VBNewLine _
               & &quot;Year:          &quot; & objItem.Year 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="713ea-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Specify computer and get Local Time
$Computer = &quot;.&quot;
$times = Get-WmiObject Win32_LocalTime -computer $computer

<# Now display the result #>

Foreach ($time in $times) {
    &quot;Day : {0}&quot; -f $Time.Day
    &quot;Day Of Week : {0}&quot; -f $Time.DayOfWeek
    &quot;Hour : {0}&quot; -f $Time.Hour
    &quot;Minute : {0}&quot; -f $Time.Minute
    &quot;Month : {0}&quot; -f $Time.Month
    &quot;Quarter : {0}&quot; -f $Time.Quarter
    &quot;Second : {0}&quot; -f $time.Second 
    &quot;Week In Month: {0}&quot; -f $Time.WeekInMonth 
    &quot;Year : {0}&quot; -f $Time.Year 
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="713ea-132">... ¿determinar el nombre de la zona horaria en la que se ejecuta un equipo?</span><span class="sxs-lookup"><span data-stu-id="713ea-132">...determine the name of the time zone in which a computer is running?</span></span></p></td>
<td><p><span data-ttu-id="713ea-133">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> y compruebe el valor de la propiedad <strong>Description</strong> .</span><span class="sxs-lookup"><span data-stu-id="713ea-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class and check the value of the <strong>Description</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-134">VB</span><span class="sxs-lookup"><span data-stu-id="713ea-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TimeZone&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description:   &quot; & objItem.Description
    Wscript.Echo &quot;Daylight Name: &quot; & objItem.DaylightName
    Wscript.Echo &quot;Standard Name: &quot; & objItem.StandardName
    Wscript.Echo
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="713ea-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;  
$timezone = Get-WMIObject -class Win32_TimeZone -ComputerName $computer  
  
<# Display details  #>
if ($computer -eq &quot;.&quot;) {$computer = Hostname}  
&quot;Time zone information on computer `&quot;{0}`&quot;&quot; -f $computer  
&quot;Time Zone Description   : {0}&quot; -f $timezone.Description  
&quot;Daylight Name           : {0}&quot; -f $timezone.DaylightName  
&quot;Standard Name           : {0}&quot; -f $timezone.StandardName  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="713ea-136">... Asegúrese de que &quot; 10/02/2000 &quot; se interpreta como Oct. 2, 2000, no &quot; 10 Feb, 2000 &quot; ?</span><span class="sxs-lookup"><span data-stu-id="713ea-136">...ensure that &quot;10/02/2000&quot; is interpreted as Oct. 2, 2000, not &quot;10 Feb, 2000&quot;?</span></span></p></td>
<td><p><span data-ttu-id="713ea-137">Administrar fechas en formato de <a href="datetime.md">fecha y hora</a> de <a href="gloss-c.md"><em>CIM</em></a> y usar métodos de <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> , como <a href="swbemdatetime-getvardate.md"><strong>getvardate (</strong></a> para convertirlos en formatos <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a> o <strong>VT_Date</strong> .</span><span class="sxs-lookup"><span data-stu-id="713ea-137">Manage dates in <a href="gloss-c.md"><em>CIM</em></a> <a href="datetime.md">DATETIME</a> format and use <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> methods, such as <a href="swbemdatetime-getvardate.md"><strong>GetVarDate</strong></a> to convert to them to and from either <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a> or <strong>VT_Date</strong> formats.</span></span> <span data-ttu-id="713ea-138">Dado que el formato de fecha y hora es independiente de la configuración regional, puede escribir un script que se ejecute en cualquier equipo.</span><span class="sxs-lookup"><span data-stu-id="713ea-138">Because DATETIME format is locale-independent, you can write a script that runs on any machine.</span></span> <span data-ttu-id="713ea-139">Use el objeto <strong>SWbemDateTime</strong> para convertirlos en fechas y horas normales.</span><span class="sxs-lookup"><span data-stu-id="713ea-139">Use the <strong>SWbemDateTime</strong> object to convert these to regular dates and times.</span></span> <span data-ttu-id="713ea-140">Consulte <a href="date-and-time-format.md">formato de fecha y hora</a> para obtener más información sobre la conversión de fechas y horas.</span><span class="sxs-lookup"><span data-stu-id="713ea-140">See <a href="date-and-time-format.md">Date and Time Format</a> for more information on converting dates and times.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="713ea-141">... ¿convertir una fecha y hora de WMI a un valor DateTime de .NET?</span><span class="sxs-lookup"><span data-stu-id="713ea-141">...convert a WMI datetime to a .NET DateTime value?</span></span></p></td>
<td><p><span data-ttu-id="713ea-142">Analice la cadena manualmente y, a continuación, coloque los valores recuperados en un objeto <a href="/dotnet/api/system.datetime">DateTime</a> .</span><span class="sxs-lookup"><span data-stu-id="713ea-142">Manually parse the string, then put the retrieved values into a <a href="/dotnet/api/system.datetime">DateTime</a> object.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="713ea-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="713ea-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDateTime( [String] $strWmiDate ) 
{ 
    $strWmiDate.Trim() > $null 
    $iYear   = [Int32]::Parse($strWmiDate.SubString( 0, 4)) 
    $iMonth  = [Int32]::Parse($strWmiDate.SubString( 4, 2)) 
    $iDay    = [Int32]::Parse($strWmiDate.SubString( 6, 2)) 
    $iHour   = [Int32]::Parse($strWmiDate.SubString( 8, 2)) 
    $iMinute = [Int32]::Parse($strWmiDate.SubString(10, 2)) 
    $iSecond = [Int32]::Parse($strWmiDate.SubString(12, 2)) 
<# decimal point is at $strWmiDate.Substring(14, 1) #> 
    $iMicroseconds = [Int32]::Parse($strWmiDate.Substring(15, 6)) 
    $iMilliseconds = $iMicroseconds / 1000 
    $iUtcOffsetMinutes = [Int32]::Parse($strWmiDate.Substring(21, 4)) 
    if ( $iUtcOffsetMinutes -ne 0 ) 
    { 
        $dtkind = [DateTimeKind]::Local 
    } 
    else 
    { 
        $dtkind = [DateTimeKind]::Utc 
    } 
    return New-Object -TypeName DateTime ` 
                      -ArgumentList $iYear, $iMonth, $iDay, ` 
                                    $iHour, $iMinute, $iSecond, ` 
                                    $iMilliseconds, $dtkind 
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="713ea-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="713ea-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="713ea-145">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="713ea-145">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="713ea-146">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="713ea-146">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="713ea-147">Formato de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="713ea-147">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="713ea-148">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="713ea-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
