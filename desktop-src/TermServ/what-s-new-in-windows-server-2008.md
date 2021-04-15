---
title: Novedades de Windows Server 2008
description: Windows Server 2008 presenta los siguientes elementos de programación nuevos para Terminal Services.
ms.assetid: a2299b03-5e06-4984-a33f-b44c7cded513
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab74f22c41fa88147a1ef30a8f55f158e34990c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104421515"
---
# <a name="whats-new-in-windows-server-2008"></a>Novedades de Windows Server 2008

Windows Server 2008 presenta los siguientes elementos de programación nuevos para Terminal Services.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento de programación</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Referencia de canales virtuales dinámicos<br/></td>
<td>Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Terminal Services, conocidas como API de canal virtual estático (SVC).<br/>
<ul>
<li><a href="dynamic-virtual-channels.md">Canales virtuales dinámicos</a></li>
<li><a href="dynamic-virtual-channels-reference.md">Referencia de canales virtuales dinámicos</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Referencia de Conexión web a Escritorio remoto<br/></td>
<td>Se han agregado las siguientes interfaces (y sus métodos y propiedades asociados) a <a href="remote-desktop-web-connection-reference.md">conexión web a escritorio remoto referencia</a>:<br/>
<ul>
<li><a href="imsrdpclient5.md"><strong>Interfaz IMsRdpClient5</strong></a></li>
<li><a href="imsrdpclient6.md"><strong>Interfaz IMsRdpClient6</strong></a></li>
<li><a href="imsrdpclientadvancedsettings5.md"><strong>Interfaz IMsRdpClientAdvancedSettings5</strong></a></li>
<li><a href="imsrdpclientadvancedsettings6.md"><strong>Interfaz IMsRdpClientAdvancedSettings6</strong></a></li>
<li><a href="imsrdpclientnonscriptable3.md"><strong>Interfaz IMsRdpClientNonScriptable3</strong></a></li>
<li><a href="imsrdpclientshell.md"><strong>Interfaz IMsRdpClientShell</strong></a></li>
<li><a href="imsrdpclienttransportsettings.md"><strong>Interfaz IMsRdpClientTransportSettings</strong></a></li>
<li><a href="imsrdpclienttransportsettings2.md"><strong>Interfaz IMsRdpClientTransportSettings2</strong></a></li>
<li><a href="imsrdpdevice.md"><strong>Interfaz IMsRdpDevice</strong></a></li>
<li><a href="imsrdpdevicecollection.md"><strong>Interfaz IMsRdpDeviceCollection</strong></a></li>
<li><a href="imsrdpdrive.md"><strong>Interfaz IMsRdpDrive</strong></a></li>
<li><a href="imsrdpdrivecollection.md"><strong>Interfaz IMsRdpDriveCollection</strong></a></li>
<li><a href="itsremoteprogram.md"><strong>Interfaz ITSRemoteProgram</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Referencia de API de Terminal Services<br/></td>
<td>Se han agregado las siguientes funciones a <a href="terminal-services-api-reference.md">Terminal Services referencia de API</a>:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>WTSConnectSession función)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>WTSRegisterSessionNotificationEx función)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>WTSStartRemoteControlSession función)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>WTSStopRemoteControlSession función)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>WTSUnRegisterSessionNotificationEx función)</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>WTSVirtualChannelOpenEx función)</strong></a></li>
</ul>
Se han agregado las siguientes estructuras:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>Estructura WTSCLIENT</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>Estructura WTSINFO</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Terminal Services proveedor WMI<br/></td>
<td>Se han agregado las clases y los métodos siguientes a la <a href="terminal-services-wmi-provider.md">Terminal Services proveedor WMI</a>.<br/>
<ul>
<li><a href="terminal-services-gateway-classes.md">Clases de puerta de enlace de Terminal Services (y métodos asociados)</a></li>
<li><a href="terminal-services-license-server-classes.md">Clases del servidor de licencias Terminal Services (y métodos asociados)</a></li>
<li><a href="terminal-services-remoteapp-classes.md">Clases RemoteApp (y métodos asociados)</a></li>
<li><a href="win32-tsdiscoveredlicenseserver.md"><strong>Win32_TSDiscoveredLicenseServer (clase)</strong></a></li>
<li><a href="create-win32-terminal.md"><strong>Método Create de la clase Win32_Terminal</strong></a></li>
<li><a href="delete-win32-terminal.md"><strong>Método Delete de la clase Win32_Terminal</strong></a></li>
<li><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>Método CanAccessLicenseServer de la clase Win32_TerminalServiceSetting</strong></a></li>
<li><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>Método FindLicenseServers de la clase Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getdomain-win32-terminalservicesetting.md"><strong>Método GetDomain de la clase Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>Método GetGracePeriodDays de la clase Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>Método GetWinstationDriverNames de la clase Win32_TerminalServiceSetting</strong></a></li>
<li><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>Método PingLicenseServer de la clase Win32_TerminalServiceSetting</strong></a></li>
<li><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>Método UpdateDirectConnectLicenseServer de la clase Win32_TerminalServiceSetting</strong></a></li>
<li><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>Método SetUserAuthenticationRequired de la clase Win32_TSGeneralSetting</strong></a></li>
<li><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Método GetCurrentRedirectableAddresses de la clase Win32_TSSessionDirectory</strong></a></li>
<li><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Método SetCurrentRedirectableAddresses de la clase Win32_TSSessionDirectory</strong></a></li>
<li><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>Método GetRedirectableAddresses de la clase Win32_TSSessionDirectory</strong></a></li>
<li><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>Método PingSessionDirectory de la clase Win32_TSSessionDirectory</strong></a></li>
<li><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>Método SetLoadBalancingState de la clase Win32_TSSessionDirectory</strong></a></li>
<li><a href="setserverweight-win32-tssessiondirectory.md"><strong>Método SetServerWeight de la clase Win32_TSSessionDirectory</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Referencia del complemento de agente de sesiones de Terminal Services<br/></td>
<td>El complemento agente de sesiones de Terminal Services (agente de sesiones de TS) se usa para ampliar las capacidades del agente de sesiones de TS.<br/>
<ul>
<li><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Referencia del complemento de agente de sesiones de Terminal Services</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

