---
description: Tareas de WMI para el hardware del equipo obtenga información sobre la presencia, el estado o las propiedades de los componentes de hardware.
ms.assetid: eb4c2c38-4853-4486-b889-93a843d88edb
ms.tgt_platform: multiple
title: 'Tareas WMI: hardware del equipo'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5589c634a5a7bf11b95bc2d90ebeab038eb8af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715823"
---
# <a name="wmi-tasks-computer-hardware"></a><span data-ttu-id="647e4-103">Tareas WMI: hardware del equipo</span><span class="sxs-lookup"><span data-stu-id="647e4-103">WMI Tasks: Computer Hardware</span></span>

<span data-ttu-id="647e4-104">Tareas de WMI para el hardware del equipo obtenga información sobre la presencia, el estado o las propiedades de los componentes de hardware.</span><span class="sxs-lookup"><span data-stu-id="647e4-104">WMI tasks for computer hardware obtain information about the presence, state, or properties of hardware components.</span></span> <span data-ttu-id="647e4-105">Por ejemplo, puede determinar si un equipo es un equipo de escritorio o portátil.</span><span class="sxs-lookup"><span data-stu-id="647e4-105">For example, you can determine whether a computer is a desktop or laptop.</span></span> <span data-ttu-id="647e4-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="647e4-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="647e4-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="647e4-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="647e4-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="647e4-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="647e4-109">Para ejecutar un script</span><span class="sxs-lookup"><span data-stu-id="647e4-109">To run a script</span></span>

<span data-ttu-id="647e4-110">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="647e4-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="647e4-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="647e4-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="647e4-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="647e4-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="647e4-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="647e4-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="647e4-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="647e4-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="647e4-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="647e4-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="647e4-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="647e4-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="647e4-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="647e4-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="647e4-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="647e4-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="647e4-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="647e4-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="647e4-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="647e4-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="647e4-121">How do I...</span></span></th>
<th><span data-ttu-id="647e4-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="647e4-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="647e4-123">... determinar la cantidad de memoria libre que tiene un equipo</span><span class="sxs-lookup"><span data-stu-id="647e4-123">...determine how much free memory a computer has?</span></span></td>
<td><span data-ttu-id="647e4-124">Use la <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> de clase y la propiedad <strong>FreePhysicalMemory</strong> .</span><span class="sxs-lookup"><span data-stu-id="647e4-124">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> and the <strong>FreePhysicalMemory</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-125">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colSettings 
    Wscript.Echo &quot;Available Physical Memory: &quot; & objOperatingSystem.FreePhysicalMemory
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
<th><span data-ttu-id="647e4-126">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-126">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_OperatingSystem
&quot;System : {0}&quot; -f $mem.csname
&quot;Free Memory: {0}&quot; -f $mem.FreePhysicalMemory</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="647e4-127">... determinar si un equipo tiene una unidad de DVD</span><span class="sxs-lookup"><span data-stu-id="647e4-127">...determine whether a computer has a DVD drive?</span></span></td>
<td><p><span data-ttu-id="647e4-128">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> y busque el acrónimo DVD en la propiedad <strong>Name</strong> o <strong>DeviceID</strong> .</span><span class="sxs-lookup"><span data-stu-id="647e4-128">Use the <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> class and check for the acronym DVD in the <strong>Name</strong> or <strong>DeviceID</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-129">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-129">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Name: &quot; & objItem.Name 
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
<th><span data-ttu-id="647e4-130">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-130">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$drives = Get-WmiObject -Class Win32_CDROMDrives
$drives | Format-Table DeviceID, Description, Name -autosize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="647e4-131">... ¿determinar cuánta RAM está instalada en un equipo?</span><span class="sxs-lookup"><span data-stu-id="647e4-131">...determine how much RAM is installed in a computer?</span></span></td>
<td><p><span data-ttu-id="647e4-132">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> y compruebe el valor de la propiedad <strong>TotalPhysicalMemory</strong> .</span><span class="sxs-lookup"><span data-stu-id="647e4-132">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>TotalPhysicalMemory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-133">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-133">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Total Physical Memory: &quot; & objComputer.TotalPhysicalMemory
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
<th><span data-ttu-id="647e4-134">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-134">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_ComputerSystem</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="647e4-135">... determinar si un equipo tiene más de un procesador</span><span class="sxs-lookup"><span data-stu-id="647e4-135">...determine if a computer has more than one processor?</span></span></td>
<td><p><span data-ttu-id="647e4-136">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> y la propiedad <strong>NumberOfProcessors</strong>.</span><span class="sxs-lookup"><span data-stu-id="647e4-136">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the property <strong>NumberOfProcessors</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-137">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-137">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Number of Processors: &quot; & objComputer.NumberOfProcessors
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
<th><span data-ttu-id="647e4-138">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-138">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&quot;System Name : {0}&quot; -f $system.Name
&quot;Number of Processors: {0}&quot; -f $system.NumberOfProcessors</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="647e4-139">... determinar si un equipo tiene una ranura PCMCIA</span><span class="sxs-lookup"><span data-stu-id="647e4-139">...determine whether a computer has a PCMCIA slot?</span></span></td>
<td><p><span data-ttu-id="647e4-140">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> y compruebe el valor de la propiedad <strong>Count</strong> .</span><span class="sxs-lookup"><span data-stu-id="647e4-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> class and check the value of the <strong>Count</strong> property.</span></span> <span data-ttu-id="647e4-141">Si el valor de <strong>Count</strong> es 0, el equipo no tiene ninguna ranura PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="647e4-141">If <strong>Count</strong> is 0, then the computer has no PCMCIA slots.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-142">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PCMCIAController&quot;)
Wscript.Echo &quot;Number of PCMCIA slots: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="647e4-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Pcmcia = Get-WmiObject -Class Win32_PCMCIAController

if (!$pcmcia.count) {
    &quot;Number of PCMCIA Slots: {0}&quot; -f 1
}else {
    &quot;Number of PCMCIA Slots: {0}&quot; -f $pcmcia.count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="647e4-144">... identificar los dispositivos que no funcionan (los marcados con un icono de signo de exclamación en <strong>Administrador de dispositivos</strong>)?</span><span class="sxs-lookup"><span data-stu-id="647e4-144">...identify devices that are not working (those marked with an exclamation point icon in <strong>Device Manager</strong>)?</span></span></td>
<td><p><span data-ttu-id="647e4-145">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> y use la siguiente cláusula en la consulta <a href="querying-with-wql.md">WQL</a> .</span><span class="sxs-lookup"><span data-stu-id="647e4-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> class and use the following clause in your <a href="querying-with-wql.md">WQL</a> query.</span></span> <span data-ttu-id="647e4-146"><strong>Donde ConfigManagerErrorCode <> 0</strong> Tenga en cuenta que es posible que este código no detecte los dispositivos USB que faltan.</span><span class="sxs-lookup"><span data-stu-id="647e4-146"><strong>WHERE ConfigManagerErrorCode <> 0</strong> Note that this code may not detect USB devices that are missing drivers.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-147">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PnPEntity WHERE ConfigManagerErrorCode <> 0&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Class GUID: &quot; & objItem.ClassGuid
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Service: &quot; & objItem.Service
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
<th><span data-ttu-id="647e4-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$baddevices = Get-WmiObject Win32_PNPEntity | where {$_.ConfigManagerErrorcode -ne 0}
&quot; Total Bad devices: {0}&quot; -f $baddevices.count
foreach ($device in $baddevices) {
    &quot;Name : {0}&quot; -f $device.name
    &quot;Class Guid : {0}&quot; -f $device.Classguid
    &quot;Description : {0}&quot; -f $device.Description
    &quot;Device ID : {0}&quot; -f $device.deviceid
    &quot;Manufacturer : {0}&quot; -f $device.manufactuer
    &quot;PNP Devcice Id : {0}&quot; -f $device.PNPDeviceID
    &quot;Service Name : {0}&quot; -f $device.service
    &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="647e4-149">... ¿determinar las propiedades del mouse que se usan en el equipo?</span><span class="sxs-lookup"><span data-stu-id="647e4-149">...determine the properties of the mouse used on computer?</span></span></td>
<td><p><span data-ttu-id="647e4-150">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="647e4-150">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> class.</span></span> <span data-ttu-id="647e4-151">Esto devuelve las propiedades de todos los dispositivos señaladores, no solo de los dispositivos de mouse.</span><span class="sxs-lookup"><span data-stu-id="647e4-151">This returns the properties of all pointing devices, not just mouse devices.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-152">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PointingDevice&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Device Interface: &quot; & objItem.DeviceInterface
    Wscript.Echo &quot;Double Speed Threshold: &quot; & objItem.DoubleSpeedThreshold
    Wscript.Echo &quot;Handedness: &quot; & objItem.Handedness
    Wscript.Echo &quot;Hardware Type: &quot; & objItem.HardwareType
    Wscript.Echo &quot;INF File Name: &quot; & objItem.InfFileName
    Wscript.Echo &quot;INF Section: &quot; & objItem.InfSection
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Number Of Buttons: &quot; & objItem.NumberOfButtons
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Pointing Type: &quot; & objItem.PointingType
    Wscript.Echo &quot;Quad Speed Threshold: &quot; & objItem.QuadSpeedThreshold
    Wscript.Echo &quot;Resolution: &quot; & objItem.Resolution
    Wscript.Echo &quot;Sample Rate: &quot; & objItem.SampleRate
    Wscript.Echo &quot;Synch: &quot; & objItem.Synch
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
<th><span data-ttu-id="647e4-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Get Mouse information

$mouse = Get-WmiObject -Class Win32_PointingDevice

<# Decode detalis #>

function Deviceinterface {
    param ($value)
    switch ($value) {
        0 {&quot;Other&quot;}
        1 {&quot;Unknown&quot;}
        3 {&quot;Serial&quot;}
        4 {&quot;PS/2&quot;}
        5 {&quot;Infrared&quot;}
        6 {&quot;HP-HIL&quot;}
        7 {&quot;Bus Mouse&quot;}
        8 {&quot;ADP (Apple Desktop Bus)&quot;}
        160 {&quot;Bus Mouse DB-9&quot;}
        161 {&quot;Bus Mouse Micro-DIN&quot;}
        162 {&quot;USB&quot;}
    }
}

function Handedness {
    param ($value)
    switch ($value) {
        0 {&quot;Unknown&quot;}
        1 {&quot;Not Applicable&quot;}
        2 {&quot;Right-Handed Operation&quot;}
        3 {&quot;Left-Handed Operation&quot;}
    }
}

function Pointingtype {

param ($value)
    switch ($value) {
        1 {&quot;Other&quot;}
        2 {&quot;Unknown&quot;}
        3 {&quot;Mouse&quot;}
        4 {&quot;Track Ball&quot;}
        5 {&quot;Track Point&quot;}
        6 {&quot;Glide Point&quot;}
        7 {&quot;Touch Pad&quot;}
        8 {&quot;Touch Screen&quot;}
        9 {&quot;Mouse - Optical Sensor&quot;}
    }
}

<# Display details #>

&quot;Mouse Information on System: {0}&quot; -f $mouse.systemname
&quot;Description : {0}&quot; -f $mouse.Description
&quot;Device ID : {0}&quot; -f $mouse.DeviceID
&quot;Device Interface : {0}&quot; -f (Deviceinterface($mouse.DeviceInterface))
&quot;Double Speed Threshold : {0}&quot; -f $mouse.DoubleSpeedThreshold
&quot;Handedness : {0}&quot; -f (Handedness($mouse.handedness))
&quot;Hardware Type : {0}&quot; -f $mouse.Hardwaretype
&quot;INF FIle Name : {0}&quot; -f $mouse.InfFileName
&quot;Inf Section : {0}&quot; -f $mouse.InfSection
&quot;Manufacturer : {0}&quot; -f $mouse.Manufacturer
&quot;Name : {0}&quot; -f $mouse.Name
&quot;Number of buttons : {0}&quot; -f $mouse.NumberOfButtons
&quot;PNP Device ID : {0}&quot; -f $mouse.PNPDeviceID
&quot;Pointing Type : {0}&quot; -f (Pointingtype ($mouse.PointingType))
&quot;Quad Speed Threshold : {0}&quot; -f $mouse.QuadSpeedThreshold
&quot;Resolution : {0}&quot; -f $mouse.Resolution
&quot;Sample Rate : {0}&quot; -f $mouse.SampleRate
&quot;Synch : {0}&quot; -f $mouse.Synch</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="647e4-154">... ¿determinar la velocidad de un procesador instalado en un equipo?</span><span class="sxs-lookup"><span data-stu-id="647e4-154">...determine the speed of a processor installed in a computer?</span></span></td>
<td><p><span data-ttu-id="647e4-155">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> y compruebe el valor de la propiedad <strong>MaxClockSpeed</strong> .</span><span class="sxs-lookup"><span data-stu-id="647e4-155">Use the <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> class and check the value of the <strong>MaxClockSpeed</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-156">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-156">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Processor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Processor Id: &quot; & objItem.ProcessorId
    Wscript.Echo &quot;Maximum Clock Speed: &quot; & objItem.MaxClockSpeed
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="647e4-157">... determinar si un equipo es una torre, una minitorre, un portátil, etc.</span><span class="sxs-lookup"><span data-stu-id="647e4-157">...determine whether a computer is a tower, a mini-tower, a laptop, and so on?</span></span></td>
<td><p><span data-ttu-id="647e4-158">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> y compruebe el valor de la propiedad <strong>ChassisType</strong> .</span><span class="sxs-lookup"><span data-stu-id="647e4-158">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class and check the value of the <strong>ChassisType</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-159">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-159">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colChassis = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objChassis in colChassis
    For Each objItem in objChassis.ChassisTypes
        Wscript.Echo &quot;Chassis Type: &quot; & objItem
    Next
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
<th><span data-ttu-id="647e4-160">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-160">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$processors = Get-WmiObject -Class Win32_Processor
foreach ($proc in $processors)
{
    &quot;Processor ID: &quot; + $proc.ProcessorID
    &quot;Maximum Clock Speed: &quot; + $proc.MaxClockSpeed
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="647e4-161">... ¿obtener el número de serie y la etiqueta de activo de un equipo?</span><span class="sxs-lookup"><span data-stu-id="647e4-161">...get the serial number and asset tag of a computer?</span></span></td>
<td><p><span data-ttu-id="647e4-162">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> y las propiedades <strong>SerialNumber</strong> y <strong>SMBIOSAssetTag</strong>.</span><span class="sxs-lookup"><span data-stu-id="647e4-162">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class, and the properties <strong>SerialNumber</strong> and <strong>SMBIOSAssetTag</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-163">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-163">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSMBIOS = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objSMBIOS in colSMBIOS
    Wscript.Echo &quot;Part Number: &quot; & objSMBIOS.PartNumber
    Wscript.Echo &quot;Serial Number: &quot; & objSMBIOS.SerialNumber
    Wscript.Echo &quot;Asset Tag: &quot; & objSMBIOS.SMBIOSAssetTag
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
<th><span data-ttu-id="647e4-164">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-164">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSMBIOS = Get-WmiObject -Class Win32_SystemEnclosure

foreach ($objSMBIOS in $colSMBIOS)
{
    &quot;Part Number: &quot; + $objSMBIOS.PartNumber
    &quot;Serial Number: &quot; + $objSMBIOS.SerialNumber
    &quot;Asset Tag: &quot; + $objSMBIOS.SMBIOSAssetTag
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="647e4-165">... ¿determinar qué tipo de dispositivo está conectado a un puerto USB?</span><span class="sxs-lookup"><span data-stu-id="647e4-165">...determine what kind of device is plugged into a USB port?</span></span></td>
<td><p><span data-ttu-id="647e4-166">Use la clase <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> y Compruebe la propiedad <strong>Description</strong> .</span><span class="sxs-lookup"><span data-stu-id="647e4-166">Use the <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> class and check the <strong>Description</strong> property.</span></span> <span data-ttu-id="647e4-167">Esta propiedad puede tener un valor como &quot; dispositivo de almacenamiento masivo &quot; o &quot; soporte de impresión &quot; .</span><span class="sxs-lookup"><span data-stu-id="647e4-167">This property may have a value such as &quot;Mass Storage Device&quot; or &quot;Printing Support&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-168">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-168">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_USBHub&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo
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
<th><span data-ttu-id="647e4-169">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-169">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_USBHub

foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;PNP Device ID: &quot; + $objItem.PNPDeviceID
    &quot;Description: &quot; + $objItem.Description
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="647e4-170">... ¿determinar cuántas unidades de cinta hay instaladas en un equipo?</span><span class="sxs-lookup"><span data-stu-id="647e4-170">...determine how many tape drives are installed on a computer?</span></span></td>
<td><p><span data-ttu-id="647e4-171">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> clase y, a continuación, use el método <a href="swbemobjectset-count.md"><strong>SWbemObjectSet. Count</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="647e4-171">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> class and then use the <a href="swbemobjectset-count.md"><strong>SWbemObjectSet.Count</strong></a> method.</span></span> <span data-ttu-id="647e4-172">Si Count = 0, no hay unidades de cinta instaladas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="647e4-172">If Count = 0, then no tape drives are installed on the computer.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647e4-173">VB</span><span class="sxs-lookup"><span data-stu-id="647e4-173">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TapeDrive&quot;)
Wscript.Echo &quot;Number of tape drives: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="647e4-174">PowerShell</span><span class="sxs-lookup"><span data-stu-id="647e4-174">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_TapeDrive

foreach ($objItem in $colItems)
{
    &quot;Number of Drives: &quot; + $colItems.Count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="647e4-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="647e4-175">Examples</span></span>

<span data-ttu-id="647e4-176">En el siguiente [código de ejemplo](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) de la galería de TechNet se describe cómo mostrar el espacio libre de todas las unidades de varias máquinas.</span><span class="sxs-lookup"><span data-stu-id="647e4-176">The following TechNet Gallery [example code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) describes how to list the free space of all drives for several machines.</span></span>

<span data-ttu-id="647e4-177">En el ejemplo de PowerShell [Get-ComputerInfo-Query Computer info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) en la galería de TechNet, se usan varias llamadas a hardware y software para mostrar información acerca de un sistema local o remoto.</span><span class="sxs-lookup"><span data-stu-id="647e4-177">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software to display information about a local or remote system.</span></span>

<span data-ttu-id="647e4-178">El ejemplo de [recopilación de recursos del sistema multiproceso con](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell de PowerShell en TechNetGallery recopila una gran cantidad de información útil del sistema a través de WMI y multithreading con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="647e4-178">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell sample on TechNetGallery gathers a plethora of useful system information via WMI and multithreading with powershell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="647e4-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="647e4-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="647e4-180">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="647e4-180">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="647e4-181">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="647e4-181">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="647e4-182">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="647e4-182">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

