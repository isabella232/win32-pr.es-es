---
description: Las tareas de WMI para archivos y carpetas cambian las propiedades de archivo o carpeta a través de WMI, incluida la creación de un recurso compartido o el cambio de nombre de un archivo.
ms.assetid: 91281fe1-0461-48da-ac5c-cab7e8e1b285
ms.tgt_platform: multiple
title: 'Tareas de WMI: archivos y carpetas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b24d5f7708b88507cd08b73c0b08a83c94f6bb28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716983"
---
# <a name="wmi-tasks-files-and-folders"></a><span data-ttu-id="c278f-103">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="c278f-103">WMI Tasks: Files and Folders</span></span>

<span data-ttu-id="c278f-104">Las tareas de WMI para archivos y carpetas cambian las propiedades de archivo o carpeta a través de WMI, incluida la creación de un recurso compartido o el cambio de nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="c278f-104">WMI tasks for files and folders change file or folder properties through WMI, including creating a share or renaming a file.</span></span> <span data-ttu-id="c278f-105">Si desea copiar un archivo o leer y escribir un archivo, la manera más fácil es usar el [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) de Windows Script Host en lugar de WMI.</span><span class="sxs-lookup"><span data-stu-id="c278f-105">If you want to copy a file or read and write a file, the easiest way is to use the Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) rather than WMI.</span></span> <span data-ttu-id="c278f-106">Para ver otros ejemplos, vea la sección de [archivos y carpetas](/previous-versions/tn-archive/ee176985(v=technet.10)) de [technet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span><span class="sxs-lookup"><span data-stu-id="c278f-106">For other examples, see the [Files and Folders](/previous-versions/tn-archive/ee176985(v=technet.10)) section of the [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span></span>

<span data-ttu-id="c278f-107">[**CIM \_ El archivo de archivos**](/windows/desktop/CIMWin32Prov/cim-datafile) es una de las [clases CIM](cimclas.md) en WMI que se implementa.</span><span class="sxs-lookup"><span data-stu-id="c278f-107">[**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) is one of the few [CIM classes](cimclas.md) in WMI that is implemented.</span></span> <span data-ttu-id="c278f-108">Evite la enumeración o consulta de todas las instancias **del \_ archivo** de datos CIM en un equipo, ya que es probable que el volumen de datos afecte al rendimiento o que el equipo deje de responder.</span><span class="sxs-lookup"><span data-stu-id="c278f-108">Avoid enumerating or querying for all instances of **CIM\_DataFile** on a computer because the volume of data is likely to either affect performance or cause the computer to stop responding.</span></span>

<span data-ttu-id="c278f-109">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="c278f-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="c278f-110">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c278f-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="c278f-111">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="c278f-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="c278f-112">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="c278f-112">**To run a script**</span></span>

1.  <span data-ttu-id="c278f-113">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="c278f-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="c278f-114">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="c278f-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="c278f-115">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="c278f-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="c278f-116">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c278f-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="c278f-117">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="c278f-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="c278f-118">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="c278f-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="c278f-119">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c278f-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="c278f-120">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="c278f-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="c278f-121">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="c278f-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="c278f-122">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="c278f-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c278f-123">Cómo...</span><span class="sxs-lookup"><span data-stu-id="c278f-123">How do I...</span></span></th>
<th><span data-ttu-id="c278f-124">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="c278f-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c278f-125">... ¿cambiar el nombre de un archivo sin recibir un mensaje de error?</span><span class="sxs-lookup"><span data-stu-id="c278f-125">...rename a file without getting an error message?</span></span></td>
<td><span data-ttu-id="c278f-126">Utilice la clase <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c278f-126">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class.</span></span> <span data-ttu-id="c278f-127">Asegúrese de pasar el nombre completo de la ruta de acceso al llamar al método <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> , por ejemplo, &quot;C:\Scripts\Test.txt&quot; en lugar de &quot;Text.txt&quot; .</span><span class="sxs-lookup"><span data-stu-id="c278f-127">Ensure that you pass the entire path name when calling the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> method, for example, &quot;C:\Scripts\Test.txt&quot; instead of &quot;Text.txt&quot;.</span></span> <span data-ttu-id="c278f-128">Para PowerShell, el uso de <strong>CIM_DataFile</strong> puede ser ineficaz.</span><span class="sxs-lookup"><span data-stu-id="c278f-128">For PowerShell, using <strong>CIM_DataFile</strong> may be inefficient.</span></span> <span data-ttu-id="c278f-129">Por lo tanto, puede usar simplemente el cmdlet Rename-Item.</span><span class="sxs-lookup"><span data-stu-id="c278f-129">As such, you may simply use the Rename-Item cmdlet.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c278f-130">VB</span><span class="sxs-lookup"><span data-stu-id="c278f-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery (&quot;Select * from CIM_DataFile where Name = &quot; & &quot;&#39;c:\\scripts\\toggle_service.vbs&#39;&quot;)
For Each objFile in colFiles
    errResult = objFile.Rename(&quot;c:\scripts\toggle_service.old&quot;)
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
<th><span data-ttu-id="c278f-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c278f-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>rename-item c:\scripts\toggle_service.vbs toggle_service.old</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c278f-132">... Determine si los usuarios tienen. Archivos MP3 almacenados en su equipo</span><span class="sxs-lookup"><span data-stu-id="c278f-132">...determine whether users have .MP3 files stored on their computer?</span></span></td>
<td><p><span data-ttu-id="c278f-133">Use la clase <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> y seleccione archivos con la siguiente cláusula <strong>Where</strong> de <a href="querying-with-wql.md">WQL</a> : Where Extension = &quot; mp3 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c278f-133">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class and select files using the following <a href="querying-with-wql.md">WQL</a> <strong>WHERE</strong> clause: Where Extension = &quot;MP3&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c278f-134">VB</span><span class="sxs-lookup"><span data-stu-id="c278f-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery(&quot;Select * from CIM_DataFile where Extension = &#39;mp3&#39;&quot;)
For Each objFile in colFiles
    Wscript.Echo &quot;File Name: &quot; & objFile.Name & &quot;.&quot; & objFile.Extension
    Wscript.Echo &quot;Path: &quot; & objFile.Path
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
<th><span data-ttu-id="c278f-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c278f-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class CIM_DataFile -namespace &quot;root\cimv2&quot; -Filter &quot;Extension = &#39;mp3&#39;&quot; | `
   format-list Name, Extension, Path</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c278f-136">... ¿crear carpetas compartidas en un equipo?</span><span class="sxs-lookup"><span data-stu-id="c278f-136">...create shared folders on a computer?</span></span></td>
<td><p><span data-ttu-id="c278f-137">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c278f-137">Use the <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c278f-138">VB</span><span class="sxs-lookup"><span data-stu-id="c278f-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 25
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objNewShare = objWMIService.Get(&quot;Win32_Share&quot;)
errReturn = objNewShare.Create(&quot;C:\Finance&quot;, &quot;FinanceShare&quot;, FILE_SHARE, MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;)</code></pre></td>
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
<th><span data-ttu-id="c278f-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c278f-139">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$FILE_SHARE = 0
$MAXIMUM_CONNECTIONS = 25

$NewDir = new-item C:\Finance -type directory 
$Shares= [WMICLASS]&quot;Win32_Share&quot;
[void]$Shares.Create(&quot;C:\Finance&quot;,&quot;FinanceShare&quot;, $FILE_SHARE, $MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;) </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c278f-140">... ¿copiar una carpeta?</span><span class="sxs-lookup"><span data-stu-id="c278f-140">...copy a folder?</span></span></td>
<td><p><span data-ttu-id="c278f-141">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c278f-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> method.</span></span> <span data-ttu-id="c278f-142">Para PowerShell, simplemente puede usar el cmdlet Copy-Item.</span><span class="sxs-lookup"><span data-stu-id="c278f-142">For PowerShell, you can simply use the Copy-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c278f-143">VB</span><span class="sxs-lookup"><span data-stu-id="c278f-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery(&quot;Select * from Win32_Directory where Name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy(&quot;D:\Archive&quot;) 
Next </code></pre></td>
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
<th><span data-ttu-id="c278f-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c278f-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Copy-Item C:\Scripts -Destination D:\Archive -Recurse</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c278f-145">... ¿mueve una carpeta?</span><span class="sxs-lookup"><span data-stu-id="c278f-145">...move a folder?</span></span></td>
<td><p><span data-ttu-id="c278f-146">Use la clase <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> y el método <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c278f-146">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> method.</span></span> <span data-ttu-id="c278f-147">Para PowerShell, simplemente puede usar el cmdlet Move-Item.</span><span class="sxs-lookup"><span data-stu-id="c278f-147">For PowerShell, you can simply use the Move-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c278f-148">VB</span><span class="sxs-lookup"><span data-stu-id="c278f-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; _ 
    & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery _ 
    (&quot;Select * from Win32_Directory where name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename(&quot;C:\Admins\Documents\Archive\VBScript&quot;) 
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
<th><span data-ttu-id="c278f-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c278f-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>move-item -path C:\Scripts -destination C:\Admins\Documents\Archive\PowerShell</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c278f-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c278f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c278f-151">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c278f-151">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="c278f-152">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="c278f-152">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="c278f-153">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="c278f-153">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
