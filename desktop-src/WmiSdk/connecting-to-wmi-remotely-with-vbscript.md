---
description: Puede crear una conexión remota a WMI con VBScript mediante la creación de un objeto de conexión. Este objeto contiene el nombre del equipo, el espacio de nombres WMI al que desea conectarse, así como las credenciales y los niveles de autenticación pertinentes.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Conexión a WMI de forma remota con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569381"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Conexión a WMI de forma remota con VBScript

Puede crear una conexión remota a WMI con VBScript mediante la creación de un objeto de conexión. Este objeto contiene el nombre del equipo, el espacio de nombres WMI al que desea conectarse, así como las credenciales y los niveles de autenticación pertinentes.

**Para conectarse a un sistema remoto mediante VBScript**

1.  Especifique la información de conexión, como el nombre del equipo remoto, las credenciales y el nivel de autenticación de la conexión.

    Si se conecta a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con las que ha iniciado sesión, puede especificar la información de conexión en un [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), como se describe en el ejemplo de código siguiente.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    Por lo general, debe especificar el espacio de nombres WMI al que conectarse en el equipo remoto. Esto se debe a que es posible que el espacio de nombres predeterminado no sea el mismo en equipos diferentes. La especificación del espacio de nombres garantiza que se conecte al mismo espacio de nombres en todos los equipos.

    Para obtener más información sobre las constantes de VBScript y las cadenas de scripting para usar la conexión de moniker, vea Establecer el nivel de seguridad de proceso [predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md).

2.  Si se conecta a un equipo remoto en un dominio diferente o con un nombre de usuario y una contraseña diferentes, debe usar el [**método SWbemLocator.ConnectServer.**](swbemlocator-connectserver.md)

    Al igual que con un moniker, use **ConnectServer** para especificar las credenciales, el nivel de autenticación y el espacio de nombres para la conexión remota. En el ejemplo de código siguiente se describe el uso de ConnectServer para acceder a un equipo remoto mediante una cuenta de administrador y una contraseña.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  Al usar la [**función ConnectServer**](swbemlocator-connectserver.md) para conexiones remotas, establezca la suplantación y la autenticación en el objeto de seguridad obtenido por una llamada a [**SWbemServices.Security**](swbemservices-security-.md). Puede usar la enumeración [WbemImpersonationLevelEnum para](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) especificar el nivel de suplantación.

    En el ejemplo de código siguiente se establece el nivel de suplantación para el ejemplo de código de VBScript anterior.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Tenga en cuenta que algunas conexiones requieren un nivel de autenticación específico. Para obtener más información, vea [Establecer la seguridad del proceso de aplicación cliente](setting-client-application-process-security.md) y Proteger clientes de [scripting.](securing-scripting-clients.md)

    En concreto, debe establecer el nivel de autenticación en **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** o 6 si el espacio de nombres al que se conecta en el equipo remoto requiere una conexión cifrada antes de que devuelva datos. También puede usar este nivel de autenticación, incluso si el espacio de nombres no lo requiere. Esto garantiza que los datos se cifran a medida que cruzan la red. Si intenta establecer un nivel de autenticación inferior al permitido, se devolverá un mensaje de acceso denegado. Para obtener más información, vea [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

Una vez que haya realizado la conexión, puede seguir accediendo a los datos wmi. Para obtener más información, vea [Tareas de WMI para scripts y aplicaciones.](wmi-tasks-for-scripts-and-applications.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de VBScript mayor, vea la sección Ejemplos de la página de referencia [**SWbemLocator.ConnectServer.**](swbemlocator-connectserver.md)

En el ejemplo de código de VBScript siguiente se conecta a un grupo de equipos remotos del mismo dominio mediante la creación de una matriz de nombres de equipo remoto y, a continuación, se muestran los nombres de los dispositivos Plug and Play (instancias de [**Win32 \_ PnPEntity)**](/windows/desktop/CIMWin32Prov/win32-pnpentity)en cada equipo. Para ejecutar el script siguiente, debe ser administrador en los equipos remotos. Tenga en cuenta que " " necesario antes de que el nombre del equipo remoto se agrega mediante el script después de la \\ \\ configuración de nivel de suplantación. Para obtener más información sobre las rutas de acceso WMI, vea [Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



El siguiente ejemplo de código de VBScript le permite conectarse a un equipo remoto con credenciales diferentes. Por ejemplo, un equipo remoto en un dominio diferente o conectarse a un equipo remoto que requiera un nombre de usuario y una contraseña diferentes. En este caso, use la [**conexión SWbemServices.ConnectServer.**](swbemlocator-connectserver.md)


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
