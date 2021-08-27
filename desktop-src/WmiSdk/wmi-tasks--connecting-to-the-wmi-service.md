---
description: Para obtener datos de WMI, ya sea en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un espacio de nombres específico.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'Tareas wmi: conectarse al servicio WMI'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da816b45709f6140efb7e6e0460e27d9f9ed00f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627721"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>Tareas wmi: conectarse al servicio WMI

Para obtener datos de WMI, ya sea en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un espacio de nombres [*específico.*](gloss-n.md) En la mayoría de los casos, use la conexión de [moniker](creating-a-wmi-script.md) abreviada o la [**conexión de localizador.**](swbemlocator-connectserver.md) Para obtener otros ejemplos, vea ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Las conexiones remotas requieren una configuración adecuada para Windows Firewall y DCOM. Para obtener más información, vea [Conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) y [Conectarse](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)a través de Windows Firewall . A partir Windows Vista, el control de cuentas de usuario (UAC) puede afectar al acceso WMI. Para obtener más información, vea [Control de cuentas de usuario y WMI.](user-account-control-and-wmi.md)

Los ejemplos de script que se muestran en este tema obtienen datos solo del equipo local. Para obtener más información sobre cómo usar el script para obtener datos de equipos remotos, vea [Conectarse a WMI en un equipo remoto.](connecting-to-wmi-on-a-remote-computer.md)


En el procedimiento siguiente se describe cómo ejecutar un script.

**Para ejecutar un script**

1.  Copie el código y guárdelo en un archivo con una extensión .vbs, como *filename.vbs*. Asegúrese de que el editor de texto no agrega una .txt extensión al archivo.
2.  Abra una ventana del símbolo del sistema y vaya al directorio donde guardó el archivo.
3.  Escriba **cscript filename.vbs** en el símbolo del sistema.
4.  Si no puede acceder a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados. Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).

> [!Note]  
> De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema. Dado que los scripts WMI pueden generar grandes cantidades de salida, es posible que desee redirigir la salida a un archivo. Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script *filename.vbs* a *outfile.txt*.

 

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
<td>... ¿Conectarse a un equipo remoto mediante WMI?</td>
<td>Especifique uno de los siguientes elementos como parte de la cadena de <a href="constructing-a-moniker-string.md">conexión del moniker:</a><br/>
<ul>
<li>Un nombre de equipo NetBIOS, como &quot; atl-dc-01&quot;</li>
<li>Un nombre de dominio completo, como &quot; atl-dc-01.fabrikam.com&quot;</li>
<li>Una dirección IPv4, como &quot; 192.168.1.1&quot;</li>
<li>A partir Windows Vista, puede especificar una dirección IPv6 si el equipo de destino y el equipo desde el que realiza la conexión ejecutan IPv6.<br/></li>
</ul>
Para obtener más información, vea <a href="connecting-to-wmi-on-a-remote-computer.md">Conectarse a WMI en un equipo</a> remoto y Compatibilidad con <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 e IPv4 en WMI.</a><br/> <span data-codelanguage="VisualBasic"></span>
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
<col  />
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
<td>... ¿Ejecutar un script WMI con credenciales alternativas?</td>
<td><p>Use el <a href="swbemlocator-connectserver.md"><strong>método SWbemLocator.ConnectServer</strong></a> o <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> en C++, e incluya el nombre de usuario y la contraseña adecuados. No puede cambiar las credenciales al conectarse al equipo local. Para obtener más información, vea <a href="creating-a-wmi-script.md">Crear un script WMI y</a> <a href="connecting-to-wmi-on-a-remote-computer.md">Conectarse a WMI en un equipo remoto.</a></p>
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
<col  />
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

[Tareas wmi para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Ejemplos de aplicaciones wmi de C++](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
