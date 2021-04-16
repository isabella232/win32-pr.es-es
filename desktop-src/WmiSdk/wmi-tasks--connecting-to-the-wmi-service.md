---
description: Para obtener datos de WMI, en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un espacio de nombres específico.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'Tareas WMI: conectarse al servicio WMI'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706149"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>Tareas WMI: conectarse al servicio WMI

Para obtener datos de WMI, en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un [*espacio de nombres*](gloss-n.md)específico. En la mayoría de los casos, puede usar la conexión de [moniker](creating-a-wmi-script.md) abreviada o la conexión del [**localizador**](swbemlocator-connectserver.md) . Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Las conexiones remotas requieren una configuración adecuada para el Firewall de Windows y DCOM. Para obtener más información, vea [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) y [conectarse a través de Firewall de Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). A partir de Windows Vista, el control de cuentas de usuario (UAC) puede afectar al acceso a WMI. Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).

Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local. Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).


En el procedimiento siguiente se describe cómo ejecutar un script.

**Para ejecutar un script**

1.  Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*. Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.
2.  Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.
3.  Escriba **cscript filename.vbs** en el símbolo del sistema.
4.  Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados. Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).

> [!Note]  
> De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema. Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo. Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.

 

En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.



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
<td>... ¿conectarse a un equipo remoto mediante WMI?</td>
<td>Especifique una de las siguientes como parte de la cadena de conexión de <a href="constructing-a-moniker-string.md">moniker</a> :<br/>
<ul>
<li>Un nombre de equipo NetBIOS, como &quot; ATL-DC-01&quot;</li>
<li>Un nombre de dominio completo, como &quot; ATL-DC-01.fabrikam.com&quot;</li>
<li>Una dirección IPv4, como &quot; 192.168.1.1&quot;</li>
<li>A partir de Windows Vista, puede especificar una dirección IPv6 si el equipo de destino y el equipo desde el que está realizando la conexión ejecutan IPv6.<br/></li>
</ul>
Para obtener más información, vea <a href="connecting-to-wmi-on-a-remote-computer.md">conectarse a WMI en un equipo remoto</a> y <a href="ipv6-and-ipv4-support-in-wmi.md">compatibilidad con IPv6 e IPv4 en WMI</a>.<br/> <span data-codelanguage="VisualBasic"></span>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... ¿ejecutar un script de WMI en credenciales alternativas?</td>
<td><p>Use el método <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> o <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator:: ConnectServer</strong></a> en C++ e incluya el nombre de usuario y la contraseña adecuados. No se pueden cambiar las credenciales al conectarse al equipo local. Para obtener más información, vea <a href="creating-a-wmi-script.md">crear un script WMI</a> y <a href="connecting-to-wmi-on-a-remote-computer.md">conectarse a WMI en un equipo remoto</a>.</p>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Ejemplos de aplicaciones de C++ de WMI](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter de TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
