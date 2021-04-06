---
title: Obtención de datos de un equipo remoto
description: Puede obtener datos o administrar recursos en equipos remotos, así como en el equipo local. La conexión a un equipo remoto en un script Administración remota de Windows es muy similar a establecer una conexión local.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904616"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Obtención de datos de un equipo remoto

Puede obtener datos o administrar recursos en equipos remotos, así como en el equipo local. La conexión a un equipo remoto en un script Administración remota de Windows es muy similar a establecer una conexión local. Los datos de la instancia de WMI están disponibles y, si el equipo remoto tiene hardware de BMC que se puede comunicar mediante el protocolo WS-Management, también están disponibles los datos de la [interfaz de administración de plataforma inteligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) . Para obtener más información, consulte [administración remota de Windows y WMI](windows-remote-management-and-wmi.md) y [administración remota de hardware](remote-hardware-management.md).

Es posible que tenga que crear un objeto [**ConnectionOptions**](connectionoptions.md) para especificar información sobre el tipo de autenticación solicitado para el inicio de sesión.

Si la cuenta del equipo remoto tiene el mismo nombre de usuario y contraseña de inicio de sesión, la única información adicional que necesita es el transporte, el nombre de dominio y el nombre del equipo. Debido a un [control de cuentas de usuario (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), la cuenta remota debe ser una cuenta de dominio y un miembro del grupo administradores del equipo remoto. Si la cuenta es miembro del equipo local del grupo administradores, UAC no permite el acceso al servicio WinRM. Para tener acceso a un servicio WinRM remoto en un grupo de trabajo, el filtrado de UAC para cuentas locales debe estar deshabilitado mediante la creación de la siguiente entrada de registro DWORD y el establecimiento de su valor en 1: **\[ HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.

**Para conectarse a un equipo remoto con el nombre de usuario y la contraseña de inicio de sesión**

1.  Especifique el equipo de destino con un nombre de dominio completo o una dirección IP y asígnelo a una constante. Si se especifica una dirección IPv6, la dirección debe ir entre corchetes.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Cree un objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Cree la sesión, especificando el transporte, HTTP o HTTPS, y concatene con la constante que representa el equipo de destino.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

En el siguiente ejemplo de código VBScript se muestra el script completo. El script incluye una subrutina para transformar los datos de XML sin formato al formato legible para el usuario. Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



**Para conectarse a un equipo remoto con una cuenta diferente**

1.  Especifique el equipo de destino con un nombre de dominio completo o una dirección IP y asígnelo a una constante. Si se especifica una dirección IPv6, la dirección debe ir entre corchetes.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Cree un objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Llame al método [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) para crear un objeto [**ConnectionOptions**](connectionoptions.md) . La cuenta del equipo remoto debe ser miembro del grupo administradores del equipo local.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  En la llamada [**WSman. createSession**](wsman-createsession.md) , especifique las marcas de conexión de sesión adecuadas en el parámetro *Flags* . Para obtener más información, vea [constantes de sesión](session-constants.md). Especifique el equipo de destino con un nombre de equipo completo o una dirección IP y el transporte (http o https). Este script solicita la autenticación [*Kerberos*](windows-remote-management-glossary.md) desde el servicio WinRM remoto.

    A diferencia de los scripts de WMI, puede utilizar varios métodos de autenticación en los scripts de WinRM. Para obtener más información, consulte [autenticación para conexiones remotas](authentication-for-remote-connections.md).

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  Una vez que el objeto de sesión esté disponible, puede llamar a cualquiera de los métodos del objeto de [**sesión**](session.md) para obtener datos de un recurso. Puede obtener datos de cualquier recurso que esté disponible en el equipo en el que se ejecuta la sesión. Para obtener más información, consulte [obtener datos del equipo local](obtaining-data-from-the-local-computer.md).

En el siguiente ejemplo de código VBScript se muestra el script completo. El script incluye una subrutina para transformar los datos de XML sin formato al formato legible para el usuario. Para obtener más información, vea [Mostrar la salida XML de los scripts de WinRM](displaying-xml-output-from-winrm-scripts.md). El script especifica la autenticación Kerberos, pero si el equipo remoto se encuentra en un grupo de trabajo y no en un dominio, la especificación de Kerberos genera un error.


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 