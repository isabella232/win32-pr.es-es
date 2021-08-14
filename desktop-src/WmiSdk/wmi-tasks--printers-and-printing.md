---
description: Las tareas WMI para impresoras e impresión administran y obtienen datos sobre impresoras, como buscar o establecer la impresora predeterminada. Para obtener otros ejemplos, vea ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: 56aa8043-08cc-42c9-82b0-f1328cd52ff8
ms.tgt_platform: multiple
title: 'Tareas wmi: impresoras e impresión'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcc7315f32ee1c00928b1feefe7d7d9dbebaf9fd169cd741440ad53ce4343c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311999"
---
# <a name="wmi-tasks-printers-and-printing"></a>Tareas wmi: impresoras e impresión

Las tareas WMI para impresoras e impresión administran y obtienen datos sobre impresoras, como buscar o establecer la impresora predeterminada. Para obtener otros ejemplos, vea ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

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
<td>... ¿Agregar una nueva conexión de impresora a un equipo remoto?</td>
<td>Use la <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y el <a href="/windows/desktop/CIMWin32Prov/addprinterconnection-method-in-class-win32-printer"><strong>método AddPrinterConnection.</strong></a><br/> <span data-codelanguage="VisualBasic"></span>
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
<td>... establecer la impresora predeterminada?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y el <a href="/windows/desktop/CIMWin32Prov/setdefaultprinter-method-in-class-win32-printer"><strong>método SetDefaultPrinter.</strong></a></p>
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
<th>PowerShell</th>
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
<td>... ¿Cancelar trabajos de impresión mediante WMI?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y el <a href="/windows/desktop/CIMWin32Prov/cancelalljobs-method-in-class-win32-printer"><strong>método CancelAllJobs.</strong></a></p>
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
<th>PowerShell</th>
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
<td>... determinar la impresora predeterminada de un equipo?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> y compruebe si la <strong>propiedad Default</strong> es <strong>True.</strong></p>
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
<th>PowerShell</th>
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



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas wmi para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Ejemplos de aplicaciones wmi de C++](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

