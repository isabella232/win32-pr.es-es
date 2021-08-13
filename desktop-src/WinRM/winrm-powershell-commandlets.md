---
title: Referencia administrada para las clases de comandos de Windows PowerShell para WinRM
description: Windows Administración remota 2.0 (WinRM) puede usar cmdlets Windows PowerShell para la administración del sistema. Windows PowerShell cmdlets permiten a un administrador configurar WinRM y obtener datos o administrar recursos.
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- ConnectWSManCommand
- DisableWSManCredSSPCommand
- DisconnectWSManCommand
- EnableWSManCredSSPCommand
- GetWSManCredSSPCommand
- GetWSManInstanceCommand
- InvokeWSManActionCommand
- NewWSManInstanceCommand
- NewWSManSessionOptionCommand
- RemoveWSManInstanceCommand
- SetWSManInstanceCommand
- SetWSManQuickConfigCommand
- TestWSManCommand
- SessionOption
- AuthenticationMechanism
- ProxyAccessType
- ProxyAuthentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d20a7615be5180350153596502386c9eac7c0c6820442284a717161ee1283e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412455"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>Referencia administrada para las clases de comandos de Windows PowerShell para WinRM

Windows Administración remota 2.0 (WinRM) puede usar cmdlets Windows PowerShell para la administración del sistema. Windows PowerShell cmdlets permiten a un administrador configurar WinRM y obtener datos o administrar recursos.

Windows PowerShell cmdlets para WinRM proporcionan la misma funcionalidad que la utilidad de línea de comandos winrm. Sin embargo, Windows PowerShell también hace lo siguiente:

-   Automatiza las tareas de WinRM en un lenguaje de scripting extensible y orientado a la administración.
-   Proporciona una única herramienta para todas las tareas de administración.

Consulte [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) para obtener más información.

## <a name="ws-management-windows-powershell-classes"></a>WS-Management Windows PowerShell clases

**Espacio de** nombres : Microsoft.WsMan.Management

**Ensamblado:** System.Management.Automation

Las siguientes clases de comandos de WinRM se implementan mediante Windows PowerShell. Estas clases se incluyen en este kit de desarrollo de software (SDK) solo para integridad. Los miembros de estas clases no se pueden usar directamente ni deben usarse para derivar otras clases.



| Clase                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConnectWSManCommand          | Se conecta al servicio WinRM en un equipo remoto. <br/> Consulte el [cmdlet Conectar-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                              |
| DisableWSManCredSSPCommand   | Deshabilita la autenticación CredSSP en un cliente.<br/> Consulte el cmdlet [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                                                                                                                                                                                                                                                                                                                                           |
| DisconnectWSManCommand       | Se desconecta del servicio WinRM en un equipo remoto. <br/> Consulte el cmdlet [Disconnect-WSMan](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                      |
| EnableWSManCredSSPCommand    | Habilita la autenticación CredSSP en el cliente.<br/> Consulte el cmdlet [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                               |
| GetWSManCredSSPCommand       | Obtiene la configuración relacionada con CredSSP para el cliente.<br/> Consulte el cmdlet [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                         |
| GetWSManInstanceCommand      | Muestra información de administración de una instancia de recurso especificada por un URI de recurso.<br/> Consulte el cmdlet [Get-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                          |
| InvokeWSManActionCommand     | Invoca una acción en el objeto de destino especificado por el URI de recurso y los selectores. <br/> Consulte el cmdlet [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                         |
| NewWSManInstanceCommand      | Crea una nueva instancia de un recurso de administración. <br/> Consulte el cmdlet [New-WSManInstance](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                             |
| NewWSManSessionOptionCommand | Crea una tabla hash de opciones de sesión winRM para usarla como parámetros de entrada para los siguientes cmdlets de WSMan: [Get-WSManInstance,](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) [Set-WSManInstance,](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) [y Conectar-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true). <br/> Consulte [New-WSManSessionOption para](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) obtener ejemplos e información detallada sobre los parámetros.<br/> |
| RemoveWSManInstanceCommand   | Elimina una instancia de recurso de administración. <br/> Consulte el cmdlet [Remove-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| SetWSManInstanceCommand      | Modifica la información de administración relacionada con un recurso. <br/> Consulte el cmdlet [Set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                       |
| SetWSManQuickConfigCommand   | Configura el equipo local para la administración remota. <br/> Consulte el cmdlet [Set-WSManQuickConfig](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                                      |
| TestWSManCommand             | Comprueba si el servicio WinRM se ejecuta en un equipo local o remoto. <br/> Consulte el cmdlet [Test-WSMan]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true) para obtener ejemplos e información detallada sobre los parámetros.<br/>                                                                                                                                                                                                                                                                                                                        |
| SessionOption                | Define un conjunto de opciones ampliadas para la sesión de WS-Management.<br/> Consulte el [cmdlet Conectar-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los valores posibles.<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>WS-Management Windows PowerShell enumeraciones

Las enumeraciones siguientes se implementan mediante Windows PowerShell. Estas enumeraciones se incluyen en este kit de desarrollo de software (SDK) solo para su integridad.



| Enumeración             | Descripción                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AuthenticationMechanism | Especifica el mecanismo de autenticación que se va a usar en el servidor. <br/> Consulte el [cmdlet Conectar-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los valores posibles.<br/>      |
| ProxyAccessType         | Especifica el mecanismo por el que se encuentra el servidor proxy.<br/> Consulte el cmdlet [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los valores posibles.<br/> |
| ProxyAuthentication     | Especifica el método de autenticación que se va a usar en el proxy.<br/> Consulte el cmdlet [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) para obtener ejemplos e información detallada sobre los valores posibles.<br/>      |



 

 

