---
description: Tareas de WMI para impresoras e impresión administrar y obtener datos acerca de las impresoras, como buscar o establecer la impresora predeterminada. Para ver otros ejemplos, vea el ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: 56aa8043-08cc-42c9-82b0-f1328cd52ff8
ms.tgt_platform: multiple
title: 'Tareas de WMI: impresoras e impresión'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d6a2ec1693a62b16e7b147cbbdf362eadb6dd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361371"
---
# <a name="wmi-tasks-printers-and-printing"></a><span data-ttu-id="352a1-104">Tareas de WMI: impresoras e impresión</span><span class="sxs-lookup"><span data-stu-id="352a1-104">WMI Tasks: Printers and Printing</span></span>

<span data-ttu-id="352a1-105">Tareas de WMI para impresoras e impresión administrar y obtener datos acerca de las impresoras, como buscar o establecer la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="352a1-105">WMI tasks for printers and printing manage and obtain data about printers, such as finding or setting the default printer.</span></span> <span data-ttu-id="352a1-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="352a1-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="352a1-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="352a1-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="352a1-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="352a1-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="352a1-109">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="352a1-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="352a1-110">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="352a1-110">**To run a script**</span></span>

1.  <span data-ttu-id="352a1-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="352a1-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="352a1-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="352a1-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="352a1-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="352a1-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="352a1-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="352a1-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="352a1-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="352a1-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="352a1-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="352a1-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="352a1-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="352a1-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="352a1-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="352a1-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="352a1-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="352a1-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="352a1-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="352a1-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="352a1-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="352a1-121">How do I...</span></span></th>
<th><span data-ttu-id="352a1-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="352a1-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="352a1-123">... ¿desea agregar una nueva conexión de impresora a un equipo remoto?</span><span class="sxs-lookup"><span data-stu-id="352a1-123">...add a new printer connection to a remote computer?</span></span></td>
<td><span data-ttu-id="352a1-124">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/addprinterconnection-method-in-class-win32-printer"><strong>AddPrinterConnection</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="352a1-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/addprinterconnection-method-in-class-win32-printer"><strong>AddPrinterConnection</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="352a1-125">VB</span><span class="sxs-lookup"><span data-stu-id="352a1-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-ws-01&quot;
Set objWMIService = GetObject( &quot;winmgmts:{impersonationLevel=Impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objPrinter = objWMIService.Get(&quot;Win32_Printer&quot;)
errReturn = objPrinter.AddPrinterConnection (&quot;\\PrintServer1\ArtDepartmentPrinter&quot;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="352a1-126">... ¿establecer la impresora predeterminada?</span><span class="sxs-lookup"><span data-stu-id="352a1-126">...set the default printer?</span></span></td>
<td><p><span data-ttu-id="352a1-127">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/setdefaultprinter-method-in-class-win32-printer"><strong>SetDefaultPrinter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="352a1-127">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/setdefaultprinter-method-in-class-win32-printer"><strong>SetDefaultPrinter</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="352a1-128">VB</span><span class="sxs-lookup"><span data-stu-id="352a1-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colInstalledPrinters =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer Where Name = &#39;ScriptedPrinter&#39;&quot;)
For Each objPrinter in colInstalledPrinters
    objPrinter.SetDefaultPrinter()
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
<th><span data-ttu-id="352a1-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="352a1-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$printerName = &quot;\\ServerName\ShareName&quot;
$printer = get-wmiObject -class win32_printer -Namespace $namespace | Where-Object { $_.Name -eq $printerName }
[void]$printer.setDefaultPrinter()</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="352a1-130">... ¿cancelar los trabajos de impresión mediante WMI?</span><span class="sxs-lookup"><span data-stu-id="352a1-130">...cancel print jobs using WMI?</span></span></td>
<td><p><span data-ttu-id="352a1-131">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/cancelalljobs-method-in-class-win32-printer"><strong>CancelAllJobs</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="352a1-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class, and the <a href="/windows/desktop/CIMWin32Prov/cancelalljobs-method-in-class-win32-printer"><strong>CancelAllJobs</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="352a1-132">VB</span><span class="sxs-lookup"><span data-stu-id="352a1-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colPrintJobs =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer&quot;)
For Each objPrintJob in colPrintJobs 
    objPrintJob.CancelAllJobs
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
<th><span data-ttu-id="352a1-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="352a1-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$result = (get-wmiObject -class win32_printer -Namespace &quot;root\cimv2&quot;).CancelAllJobs()</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="352a1-134">... ¿determinar la impresora predeterminada de un equipo?</span><span class="sxs-lookup"><span data-stu-id="352a1-134">...determine the default printer for a computer?</span></span></td>
<td><p><span data-ttu-id="352a1-135">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y compruebe si la propiedad <strong>predeterminada</strong> es <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="352a1-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class, and check whether the <strong>Default</strong> property is <strong>True</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="352a1-136">VB</span><span class="sxs-lookup"><span data-stu-id="352a1-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colInstalledPrinters =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer Where Default = True&quot;)
For Each objPrinter in colInstalledPrinters
    Wscript.Echo objPrinter.Name
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
<th><span data-ttu-id="352a1-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="352a1-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>get-wmiObject -class win32_printer -Namespace &quot;root\cimv2&quot; | where-object { $_.Default -eq &#39;True&#39; }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="352a1-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="352a1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="352a1-139">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="352a1-139">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="352a1-140">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="352a1-140">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="352a1-141">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="352a1-141">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

