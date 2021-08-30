---
description: Las tareas WMI para redes administran y obtienen información sobre las conexiones y las direcciones IP o MAC. Para ver otros ejemplos, consulte ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: 25da32c3-34bf-4c88-9b09-ff371f2cf8db
ms.tgt_platform: multiple
title: 'Tareas WMI: Redes'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2a0555d63ccc01086983789dae5226492e8aa41
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625601"
---
# <a name="wmi-tasks-networking"></a>Tareas WMI: Redes

Las tareas WMI para redes administran y obtienen información sobre las conexiones y las direcciones IP o MAC. Para ver otros ejemplos, consulte ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Los ejemplos de script que se muestran en este tema obtienen datos solo del equipo local. Para obtener más información sobre cómo usar el script para obtener datos de equipos remotos, vea [Conectarse a WMI en un equipo remoto.](connecting-to-wmi-on-a-remote-computer.md)


En el procedimiento siguiente se describe cómo ejecutar un script.

**Para ejecutar un script**

1.  Copie el código y guárdelo en un archivo con una extensión .vbs, *comofilename.vbs*. Asegúrese de que el editor de texto no agrega .txt extensión al archivo.
2.  Abra una ventana del símbolo del sistema y vaya al directorio donde guardó el archivo.
3.  Escriba **cscript filename.vbs** en el símbolo del sistema.
4.  Si no puede acceder a un registro de eventos, compruebe si se ejecuta desde un símbolo del sistema con privilegios elevados. Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).

> [!Note]  
> De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema. Dado que los scripts WMI pueden generar grandes cantidades de salida, es posible que desee redirigir la salida a un archivo. Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script *filename.vbs* a *outfile.txt*.

 

En la tabla siguiente se muestran ejemplos de script que se pueden usar para obtener varios tipos de datos del equipo local.



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
<td>... deshabilitar una conexión de red mediante WMI?</td>
<td>Si usa DHCP, use los métodos <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>y ReleaseDHCPLease</strong></a> para liberar la dirección IP. Si no usa DHCP, no puede usar WMI para deshabilitar una conexión de red. Para volver a habilitar la conexión de red, use <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard.RenewDHCPLease</strong></a>. También puede publicar o renovar todas las concesiones DHCP mediante los métodos <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> y <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll.</strong></a><br/> <span data-codelanguage="VisualBasic"></span>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetCards = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration &quot; _
        & &quot;Where IPEnabled = True&quot;)
For Each objNetCard in colNetCards
    objNetCard.ReleaseDHCPLease()
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
<td><pre><code>$Computer = &quot;.&quot;
$net = Get-WMIObject -class Win32_NetworkAdapterConfiguration -ComputerName $computer
$netenabled = $net | where {$_.IPenabled}
foreach ($NetCard in $netenabled) {
    &quot;Releasing lease on: {0}&quot; -f $netcard.caption
 $netcard.ReleaseDHCPLease()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... ¿Deshabilitar o habilitar una NIC?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>clase Win32_NetworkAdapter</strong></a> y los <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>métodos Disable</strong></a> o <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>Enable.</strong></a></p></td>
</tr>
<tr class="odd">
<td>... determinar qué dirección IP se ha asignado a una conexión de red determinada?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> y la <strong>propiedad NetConnectionID</strong> para determinar la dirección MAC de la conexión de red. A continuación, <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>use Win32_NetworkAdapterConfiguration</strong></a> clase para buscar la dirección IP asociada a la dirección MAC.</p>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection 2&#39;&quot;)

For Each objItem in colItems
    strMACAddress = objItem.MACAddress
Next

Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration&quot;)

For Each objItem in colItems
    If objItem.MACAddress = strMACAddress Then
        For Each strIPAddress in objItem.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNics = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection&#39;&quot;)
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      (&quot;ASSOCIATORS OF &quot; _
          & &quot;{Win32_NetworkAdapter.DeviceID=&#39;&quot; & _
      objNic.DeviceID & &quot;&#39;}&quot; & _
      &quot; WHERE AssocClass=Win32_NetworkAdapterSetting&quot;)
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... determinar la dirección MAC de un adaptador de red?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> clase y compruebe el valor de la <strong>propiedad MACAddress.</strong></p></td>
</tr>
<tr class="odd">
<td>... determinar la dirección IP de un equipo?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> clase y compruebe el valor de la <strong>propiedad IPAddress.</strong> Esto se devuelve como una matriz, por lo que use un bucle For-Each para obtener el valor.</p>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration &quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
            to UBound(IPConfig.IPAddress)
                WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
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
<td><pre><code>$Computer = &quot;.&quot;
$IPconfigset = Get-WmiObject Win32_NetworkAdapterConfiguration
  
# Iterate and get IP address
$count = 0
foreach ($IPConfig in $IPConfigSet) {
   if ($Ipconfig.IPaddress) {
      foreach ($addr in $Ipconfig.Ipaddress) {
   &quot;IP Address   : {0}&quot; -f  $addr;
   $count++ 
   }
   }
}
if ($count -eq 0) {&quot;No IP addresses found&quot;}
else {&quot;$Count IP addresses found on this system&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>...configun equipo para empezar a obtener su dirección IP a través de DHCP?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> y el <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>método EnableDHCP.</strong></a></p>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
 
For Each objNetAdapter In colNetAdapters
    errEnable = objNetAdapter.EnableDHCP()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... ¿Asignar una dirección IP estática a un equipo?</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> y el <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>método EnableStatic.</strong></a></p>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
strIPAddress = Array(&quot;192.168.1.141&quot;)
strSubnetMask = Array(&quot;255.255.255.0&quot;)
strGateway = Array(&quot;192.168.1.100&quot;)
strGatewayMetric = Array(1)
 
For Each objNetAdapter in colNetAdapters
    errEnable = objNetAdapter.EnableStatic( _
        strIPAddress, strSubnetMask)
    errGateways = objNetAdapter.SetGateways(_
        strGateway, strGatewaymetric)
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... obtener información sobre los adaptadores de red sin recuperar también información sobre aspectos como las conexiones RAS y VPN.</td>
<td><p>Use la <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> clase . En la <a href="querying-with-wql.md">consulta WQL,</a> use esta cláusula: Where <strong>IPEnabled</strong>  =  <strong>True</strong>.</p>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration&quot; _
        & &quot; where IPEnabled=TRUE&quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
        to UBound(IPConfig.IPAddress)
            WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... hacer ping a un equipo sin usar Ping.exe?</td>
<td><p>Use la <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> clase .</p>
<p><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> pueden devolver datos para equipos que tienen direcciones IPv4 e IPv6.</p>
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
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colPings = objWMIService.ExecQuery _
    (&quot;Select * From Win32_PingStatus where Address = &#39;192.168.1.1&#39;&quot;)

For Each objStatus in colPings
    If IsNull(objStatus.StatusCode) _
        or objStatus.StatusCode<>0 Then 
        WScript.Echo &quot;Computer did not respond.&quot; 
    Else
        Wscript.Echo &quot;Computer responded.&quot;
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
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
<td><pre><code>strComputer = &quot;client1&quot;
Set objShell = CreateObject(&quot;WScript.Shell&quot;)
Set objScriptExec = objShell.Exec( _
    &quot;ping -n 2 -w 1000 &quot; & strComputer)
strPingResults = LCase(objScriptExec.StdOut.ReadAll)
If InStr(strPingResults, &quot;reply from&quot;) Then
    If InStr(strPingResults, &quot;destination net unreachable&quot;) Then
        WScript.Echo strComputer & &quot;did not respond to ping.&quot;
    Else
        WScript.Echo strComputer & &quot; responded to ping.&quot;
    End If 
Else
    WScript.Echo strComputer & &quot; did not respond to ping.&quot;
End If
  </code></pre></td>
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

[Ejemplos de aplicación C++ de WMI](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

