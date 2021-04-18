---
description: Las tareas de WMI para discos y sistemas de archivos obtienen información sobre el estado de hardware de la unidad de disco y los volúmenes lógicos. Para ver otros ejemplos, vea el ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: d310e5e6-3b67-41bc-b5f2-cea33d0a7a2b
ms.tgt_platform: multiple
title: 'Tareas de WMI: Discos y sistemas de archivos '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0357a91d893120ec1bb72a7c1d54ad4a5e9a0acf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718581"
---
# <a name="wmi-tasks-disks-and-file-systems"></a><span data-ttu-id="8eafe-104">Tareas de WMI: Discos y sistemas de archivos </span><span class="sxs-lookup"><span data-stu-id="8eafe-104">WMI Tasks: Disks and File Systems</span></span>

<span data-ttu-id="8eafe-105">Las tareas de WMI para discos y sistemas de archivos obtienen información sobre el estado de hardware de la unidad de disco y los volúmenes lógicos.</span><span class="sxs-lookup"><span data-stu-id="8eafe-105">WMI tasks for disks and file systems obtain information about disk drive hardware state and logical volumes.</span></span> <span data-ttu-id="8eafe-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8eafe-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="8eafe-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="8eafe-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="8eafe-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="8eafe-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="8eafe-109">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="8eafe-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="8eafe-110">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="8eafe-110">**To run a script**</span></span>

1.  <span data-ttu-id="8eafe-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="8eafe-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="8eafe-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="8eafe-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="8eafe-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="8eafe-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="8eafe-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="8eafe-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="8eafe-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="8eafe-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="8eafe-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="8eafe-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="8eafe-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="8eafe-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="8eafe-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="8eafe-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="8eafe-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="8eafe-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="8eafe-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="8eafe-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="8eafe-121">How do I...</span></span></th>
<th><span data-ttu-id="8eafe-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="8eafe-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8eafe-123">... ¿Cuánto espacio en disco usa actualmente cada usuario en un equipo?</span><span class="sxs-lookup"><span data-stu-id="8eafe-123">...find out how much disk space each user is currently using on a computer?</span></span></td>
<td><span data-ttu-id="8eafe-124">Si utiliza cuotas de disco, use la clase <a href="/previous-versions/windows/desktop/wmipdskq/win32-diskquota"><strong>Win32_DiskQuota</strong></a> y recupere los valores de las propiedades <strong>User</strong> y <strong>DiskSpaceUsed</strong> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-124">If you are using disk quotas, then use the <a href="/previous-versions/windows/desktop/wmipdskq/win32-diskquota"><strong>Win32_DiskQuota</strong></a> class and retrieve the values of the <strong>User</strong> and <strong>DiskSpaceUsed</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-125">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuotas = objWMIService.ExecQuery (&quot;Select * from Win32_DiskQuota&quot;)
For each objQuota in colQuotas
    Wscript.Echo &quot;Volume: &quot;& vbTab &  objQuota.QuotaVolume
    Wscript.Echo &quot;User: &quot;& vbTab &  objQuota.User      
    Wscript.Echo &quot;Disk Space Used: &quot; & vbTab &  objQuota.DiskSpaceUsed
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
<th><span data-ttu-id="8eafe-126">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8eafe-126">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_DiskQuota -ComputerName $strComputer
foreach ($objQuota in $colItems) 
{ 
    &quot;Volume: &quot; + $objQuota.QuotaVolume
    &quot;User: &quot; + $objQuota.User      
    &quot;Disk Space Used: &quot; + $objQuota.DiskSpaceUsed
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eafe-127">... ¿determinar cuándo se ha agregado o quitado una unidad extraíble de un equipo?</span><span class="sxs-lookup"><span data-stu-id="8eafe-127">...determine when a removable drive has been added to or removed from a computer?</span></span></td>
<td><p><span data-ttu-id="8eafe-128">Use un script de supervisión que consulte la clase <a href="/windows/desktop/CIMWin32Prov/win32-volumechangeevent"><strong>Win32_VolumeChangeEvent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-128">Use a monitoring script that queries the <a href="/windows/desktop/CIMWin32Prov/win32-volumechangeevent"><strong>Win32_VolumeChangeEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-129">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-129">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colMonitoredEvents = objWMIService. ExecNotificationQuery( &quot;Select * from Win32_VolumeChangeEvent&quot;)
Do
    Set objLatestEvent = colMonitoredEvents.NextEvent
    Wscript.Echo objLatestEvent.DriveName
    Wscript.Echo objLatestEvent.EventType
    Wscript.Echo objLatestEvent.Time_Created
Loop</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eafe-130">... determinar si un CD está en una unidad de CD-ROM?</span><span class="sxs-lookup"><span data-stu-id="8eafe-130">...determine if a CD is in a CD-ROM drive?</span></span></td>
<td><p><span data-ttu-id="8eafe-131">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> y la propiedad <strong>MediaLoaded</strong> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> class and the <strong>MediaLoaded</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-132">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery( &quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Media Loaded: &quot; & objItem.MediaLoaded
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
<th><span data-ttu-id="8eafe-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8eafe-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_CDROMDrive -ComputerName $strComputer
foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;MediaLoaded: &quot; + $objItem.MediaLoaded
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eafe-134">... ¿determinar si un disco está en la unidad de disquete?</span><span class="sxs-lookup"><span data-stu-id="8eafe-134">...determine if a disk is in the floppy drive?</span></span></td>
<td><p><span data-ttu-id="8eafe-135">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> y Compruebe la propiedad <strong>FreeSpace</strong> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and check the <strong>FreeSpace</strong> property.</span></span> <span data-ttu-id="8eafe-136">Si el valor es null, no hay ningún disco en la unidad.</span><span class="sxs-lookup"><span data-stu-id="8eafe-136">If the value is Null, then no disk is in the drive.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-137">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-137">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery (&quot;Select * From Win32_LogicalDisk Where DeviceID = &#39;A:&#39;&quot;)

For Each objItem in colItems
    intFreeSpace = objItem.FreeSpace
    If IsNull(intFreeSpace) Then
        Wscript.Echo &quot;There is no disk in the floppy drive.&quot;
    Else
        Wscript.Echo &quot;There is a disk in the floppy drive.&quot;
    End If
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
<th><span data-ttu-id="8eafe-138">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8eafe-138">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_LogicalDisk -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
    Where-Object { $_.DeviceID -eq &quot;A:&quot; }

foreach ($objItem in $colItems)
{
    $intFreeSpace = $objItem.FreeSpace
    if ($intFreeSpace -eq $null) { &quot;There is no disk in the floppy drive.&quot; }
    else { &quot;There is a disk in the floppy drive.&quot; }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eafe-139">... ¿distinguir entre un disco duro fijo y un disco duro extraíble?</span><span class="sxs-lookup"><span data-stu-id="8eafe-139">...distinguish between a fixed hard disk and a removable hard disk?</span></span></td>
<td><p><span data-ttu-id="8eafe-140">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> y compruebe el valor de la propiedad <strong>Drivetype</strong> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and check the value of the <strong>DriveType</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-141">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery _
    (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot;& vbTab _
        &  objDisk.DeviceID       
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo &quot;No root directory. &quot; & &quot;Drive type could not be &quot; & &quot;determined.&quot;
        Case 2
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Removable drive.&quot;
        Case 3
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Local hard disk.&quot;
        Case 4
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Network disk.&quot;      
        Case 5
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Compact disk.&quot;      
        Case 6
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;RAM disk.&quot;   
        Case Else
            Wscript.Echo &quot;Drive type could not be&quot; & &quot; determined.&quot;
    End Select
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
<th><span data-ttu-id="8eafe-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8eafe-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colDisks = Get-WmiObject -Class Win32_LogicalDisk -ComputerName $strComputer 

foreach ($objDisk in $colDisks)
{
    &quot;DeviceID: &quot; + $objDisk.deviceID
    switch ($objDisk.DriveType)
    {
        &#39;1&#39; { &quot;No root directory. Drive type could not be determined.&quot; }
        &#39;2&#39; { &quot;DriveType: Removable drive.&quot; }
        &#39;3&#39; { &quot;DriveType: Local hard disk.&quot; }
        &#39;4&#39; { &quot;DriveType: Network disk.&quot; }
        &#39;5&#39; { &quot;DriveType: Compact disk.&quot; }
        &#39;6&#39; { &quot;DriveType: RAM disk.&quot; }
        default: { &quot;Drive type could not be determined.&quot; }
    }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eafe-143">... ¿determinar qué sistema de archivos se está usando en una unidad?</span><span class="sxs-lookup"><span data-stu-id="8eafe-143">...determine what file system is in use on a drive?</span></span></td>
<td><p><span data-ttu-id="8eafe-144">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> y la propiedad <strong>filesystem</strong> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and the <strong>FileSystem</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-145">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-145">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;File System: &quot; & objDisk.FileSystem
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eafe-146">... ¿Cuál es la cantidad de espacio libre disponible en una unidad?</span><span class="sxs-lookup"><span data-stu-id="8eafe-146">...determine how much free space is available on a drive?</span></span></td>
<td><p><span data-ttu-id="8eafe-147">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> y la propiedad <strong>FreeSpace</strong> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-147">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and the <strong>FreeSpace</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-148">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Free Disk Space: &quot; & objDisk.FreeSpace
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eafe-149">... ¿determinar el tamaño de una unidad?</span><span class="sxs-lookup"><span data-stu-id="8eafe-149">...determine the size of a drive?</span></span></td>
<td><p><span data-ttu-id="8eafe-150">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> y la propiedad <strong>size</strong> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-150">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class, and the <strong>Size</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-151">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Disk Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eafe-152">... ¿averiguar qué unidades están asignadas en un equipo?</span><span class="sxs-lookup"><span data-stu-id="8eafe-152">...find out what drives are mapped on a computer?</span></span></td>
<td><p><span data-ttu-id="8eafe-153">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-mappedlogicaldisk"><strong>Win32_MappedLogicalDisk</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-153">Use the <a href="/windows/desktop/CIMWin32Prov/win32-mappedlogicaldisk"><strong>Win32_MappedLogicalDisk</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-154">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService. ExecQuery(&quot;Select * from Win32_MappedLogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;Device ID: &quot; & objDisk.DeviceID
    Wscript.Echo &quot;Name: &quot; & objDisk.Name
    Wscript.Echo &quot;Free Space: &quot; & objDisk.FreeSpace
    Wscript.Echo &quot;Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eafe-155">... ¿desfragmentar un disco duro?</span><span class="sxs-lookup"><span data-stu-id="8eafe-155">...defragment a hard disk?</span></span></td>
<td><p><span data-ttu-id="8eafe-156">Use la clase <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)"><strong>Win32_Volume</strong></a> y el método <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume"><strong>Defrag</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-156">Use the <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)"><strong>Win32_Volume</strong></a> class and the <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume"><strong>Defrag</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-157">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colVolumes = objWMIService.ExecQuery (&quot;Select * from Win32_Volume Where Name = &#39;K:\\&#39;&quot;)
For Each objVolume in colVolumes
     errResult = objVolume.Defrag()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eafe-158">... ¿detectar la letra de unidad asociada a una partición de disco lógico?</span><span class="sxs-lookup"><span data-stu-id="8eafe-158">...detect which drive letter is associated with a logical disk partition?</span></span></td>
<td><ol>
<li><span data-ttu-id="8eafe-159">Comience con la clase <a href="/windows/desktop/CIMWin32Prov/win32-diskdrive"><strong>Win32_DiskDrive</strong></a> y consulte las instancias de <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition</strong></a> mediante la propiedad <strong>DeviceID</strong> y la clase de asociación <a href="/windows/desktop/CIMWin32Prov/win32-diskdrivetodiskpartition"><strong>Win32_DiskDriveToDiskPartition</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-159">Start with the <a href="/windows/desktop/CIMWin32Prov/win32-diskdrive"><strong>Win32_DiskDrive</strong></a> class and query for instances of <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition</strong></a> using the <strong>DeviceID</strong> property and the <a href="/windows/desktop/CIMWin32Prov/win32-diskdrivetodiskpartition"><strong>Win32_DiskDriveToDiskPartition</strong></a> association class.</span></span> <span data-ttu-id="8eafe-160">Ahora tiene una colección de las particiones en la unidad física.</span><span class="sxs-lookup"><span data-stu-id="8eafe-160">Now you have a collection of the partitions on the physical drive.</span></span></li>
<li><span data-ttu-id="8eafe-161">Consulte el <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> que representa la partición mediante la propiedad <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition. DeviceID</strong></a> y la clase de asociación <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisktopartition"><strong>Win32_LogicalDiskToPartition</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8eafe-161">Query for the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> that represents the partition using the <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition.DeviceID</strong></a> property and <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisktopartition"><strong>Win32_LogicalDiskToPartition</strong></a> association class.</span></span></li>
<li><span data-ttu-id="8eafe-162">Obtenga la letra de unidad del <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk. DeviceID</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8eafe-162">Get the drive letter from the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk.DeviceID</strong></a>.</span></span></li>
</ol>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eafe-163">VB</span><span class="sxs-lookup"><span data-stu-id="8eafe-163">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>ComputerName = &quot;.&quot;
Set wmiServices  = GetObject ( _
    &quot;winmgmts:{impersonationLevel=Impersonate}!//&quot; & ComputerName)
&#39; Get physical disk drive
Set wmiDiskDrives =  wmiServices.ExecQuery ( &quot;SELECT Caption, DeviceID FROM Win32_DiskDrive&quot;)

For Each wmiDiskDrive In wmiDiskDrives
    WScript.Echo &quot;Disk drive Caption: &quot; & wmiDiskDrive.Caption & VbNewLine & &quot;DeviceID: &quot; & &quot; (&quot; & wmiDiskDrive.DeviceID & &quot;)&quot;

&#39;Use the disk drive device id to
&#39; find associated partition
query = &quot;ASSOCIATORS OF {Win32_DiskDrive.DeviceID=&#39;&quot; _
        & wmiDiskDrive.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_DiskDriveToDiskPartition&quot;    
Set wmiDiskPartitions = wmiServices.ExecQuery(query)

For Each wmiDiskPartition In wmiDiskPartitions
    &#39;Use partition device id to find logical disk
    Set wmiLogicalDisks = wmiServices.ExecQuery _
        (&quot;ASSOCIATORS OF {Win32_DiskPartition.DeviceID=&#39;&quot; _
             & wmiDiskPartition.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_LogicalDiskToPartition&quot;)

For Each wmiLogicalDisk In wmiLogicalDisks
    WScript.Echo &quot;Drive letter associated&quot; _
        & &quot; with disk drive = &quot; _ 
        & wmiDiskDrive.Caption _
        & wmiDiskDrive.DeviceID _
        & VbNewLine & &quot; Partition = &quot; _
        & wmiDiskPartition.DeviceID _
        & VbNewLine & &quot; is &quot; _
        & wmiLogicalDisk.DeviceID
    Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8eafe-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8eafe-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eafe-165">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8eafe-165">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="8eafe-166">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="8eafe-166">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="8eafe-167">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="8eafe-167">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
