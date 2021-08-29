---
title: Establecer el nivel de seguridad del proceso predeterminado con VBScript
description: Un script puede usar la autenticación WMI predeterminada y la configuración de suplantación. Sin embargo, el script puede necesitar una conexión con más seguridad o puede conectarse a un espacio de nombres que requiera una conexión cifrada.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7def50c94a044a521b32b75d8e04175ebe3c37ee741f5c22663924c774be1806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050283"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a>Establecer el nivel de seguridad del proceso predeterminado con VBScript

Un script puede usar la autenticación WMI predeterminada y la configuración de suplantación. Sin embargo, el script puede necesitar una conexión con más seguridad o puede conectarse a un espacio de nombres que requiera una conexión cifrada. Para obtener más información, vea Establecer descriptores de seguridad [namepace](setting-namespace-security-descriptors.md) y [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

En el caso más sencillo, un script puede usar la configuración predeterminada de autenticación y suplantación. WMI normalmente se ejecuta en un host de servicio compartido y comparte la misma autenticación que otros procesos del host. Si desea ejecutar el proceso WMI con un nivel de autenticación diferente, ejecute WMI con el comando [**winmgmt**](winmgmt.md) con el modificador **/standalonehost** y establezca el nivel de autenticación para WMI en general. Para obtener más información, vea [Mantenimiento de la seguridad WMI.](maintaining-wmi-security.md)

El script siguiente usa la configuración predeterminada para los niveles de suplantación y autenticación.


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



También puede usar un [moniker en](constructing-a-moniker-string.md) una llamada a [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)y establecer la configuración de seguridad predeterminada, como en el ejemplo siguiente.


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Para obtener más información sobre cómo establecer diferentes niveles de suplantación o autenticación en un script, o para establecer los valores predeterminados de un equipo, vea los temas siguientes:

-   [Cambiar las credenciales de autenticación predeterminadas mediante VBScript](#changing-the-default-authentication-credentials-using-vbscript)
-   [Cambiar el valor predeterminado de suplantación Configuración usar VBScript](#changing-the-default-impersonation-levels-using-vbscript)
-   [Establecer el nivel de suplantación predeterminado mediante el Registro](#setting-the-default-impersonation-level-using-the-registry)
-   [Acceso al objeto SWbemSecurity en VBScript](#accessing-the-swbemsecurity-object-in-vbscript)
-   [**SWbemSecurity**](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a>Cambiar las credenciales de autenticación predeterminadas mediante VBScript

Puede cambiar el nivel de autenticación en un script mediante una cadena [de moniker](constructing-a-moniker-string.md) y los objetos [**SWbemLocator**](swbemlocator.md) [**y SWbemSecurity.**](swbemsecurity.md)

El nivel de autenticación debe establecerse según los requisitos del sistema operativo de destino al que se conecta. Para obtener más información, vea [Conectarse entre diferentes sistemas operativos.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)

En el ejemplo de código de VBScript siguiente se muestra cómo cambiar el nivel de autenticación en un script que obtiene los datos de espacio libre de un equipo remoto denominado "Server1".


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



En las conexiones de moniker de script a WMI, use el nombre corto que se muestra en la columna "Nombre/descripción de Moniker" de la tabla siguiente. Por ejemplo, en el siguiente script, el nivel de autenticación se establece en **WbemAuthenticationLevelPktIntegrity**.


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



En la tabla siguiente se enumeran los niveles de autenticación que puede establecer. Estos niveles se definen en Wbemdisp.tlb en la [enumeración WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).



| Nombre o valor                                                      | Descripción                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WbemAuthenticationLevelDefault**<br/> 0<br/>      | Moniker: valor predeterminado<br/> WMI usa la configuración predeterminada Windows autenticación. Esta es la configuración recomendada que permite a WMI negociar hasta el nivel requerido por el servidor que devuelve datos. Sin embargo, si el espacio de nombres requiere cifrado, use **WbemAuthenticationLevelPktPrivacy**.<br/> |
| **WbemAuthenticationLevelNone**<br/> 1<br/>         | Moniker: None<br/> No usa ninguna autenticación.<br/>                                                                                                                                                                                                                                            |
| **WbemAuthenticationLevelConnect**<br/> 2<br/>      | Moniker: Conectar<br/> Autentica las credenciales del cliente solo cuando el cliente establece una relación con el servidor.<br/>                                                                                                                                                    |
| **WbemAuthenticationLevelCall**<br/> 3<br/>         | Call<br/> Solo se autentica al principio de cada llamada cuando el servidor recibe la solicitud.<br/>                                                                                                                                                                                      |
| **WbemAuthenticationLevelPkt**<br/> 4<br/>          | Moniker: Pkt<br/> Autentica que todos los datos recibidos son del cliente esperado.<br/>                                                                                                                                                                                                   |
| **WbemAuthenticationLevelPktIntegrity**<br/> 5<br/> | Moniker: PktIntegrity<br/> Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.<br/>                                                                                                                                                  |
| **WbemAuthenticationLevelPktPrivacy**<br/> 6<br/>   | Moniker: PktPrivacy<br/> Autentica todos los niveles de suplantación anteriores y cifra el valor del argumento de cada llamada a procedimiento remoto. Use esta configuración si el espacio de nombres al que se conecta requiere una conexión cifrada.<br/>                                               |



 

Para determinar una llamada correcta, compruebe el valor devuelto después de cambiar el nivel de autenticación.

Por ejemplo, dado que las conexiones locales siempre tienen un nivel de autenticación **de wbemAuthenticationLevelPktPrivacy**, en el ejemplo siguiente no se puede establecer el nivel de autenticación porque se conecta al equipo local.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



Un proveedor puede establecer la seguridad en un espacio de nombres para que no se devuelva ningún dato a menos que use la privacidad de paquetes (PktPrivacy) en la conexión a ese espacio de nombres. Esto garantiza que los datos se cifran a medida que cruzan la red. Si intenta establecer un nivel de autenticación inferior, recibirá un mensaje de acceso denegado. Para obtener más información, vea [Securing WMI Namespaces](securing-wmi-namespaces.md).

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a>Cambiar los niveles de suplantación predeterminados mediante VBScript

Al realizar llamadas a scripting API para WMI, se recomienda usar los valores predeterminados que WMI proporciona para el nivel de suplantación. Las llamadas remotas y algunos proveedores con más de un salto de red requieren un nivel de suplantación mayor que el que usa WMI. Si el nivel de suplantación no es suficiente, un proveedor podría rechazar una solicitud o proporcionar información incompleta.

Si no establece el nivel de suplantación en un moniker o estableciendo [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) en un objeto protegible, establezca el nivel de suplantación DCOM predeterminado para el sistema operativo. El nivel de suplantación debe establecerse según los requisitos del sistema operativo de destino al que se conecta. Para obtener más información, vea [Conectarse entre diferentes sistemas operativos.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)

En el ejemplo de código de VBScript siguiente se muestra cómo cambiar el nivel de suplantación en el mismo script mostrado anteriormente.


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



En la tabla siguiente se enumeran los niveles de [autenticación de WbemImpersonationLevelEnum que](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) se usan.



| Nombre o valor                                                    | Descripción                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wbemImpersonationLevelAnonymous**<br/> 1<br/>   | Moniker: Anónimo<br/> Oculta las credenciales de la persona que llama. Las llamadas a WMI pueden dar error con este nivel de suplantación.<br/>                                                                                                  |
| **wbemImpersonationLevelIdentify**<br/> 2<br/>    | Moniker: Identificación<br/> permite que los objetos consulten las credenciales de la persona que llama. Las llamadas a WMI pueden dar error con este nivel de suplantación.<br/>                                                                                 |
| **wbemImpersonationLevelImpersonate**<br/> 3<br/> | Moniker: Suplantar<br/> permite que los objetos usen las credenciales de la persona que llama. Este es el nivel de suplantación recomendado para Scripting API para llamadas WMI.<br/>                                                        |
| **wbemImpersonationLevelDelegate**<br/> 4<br/>    | Moniker: Delegado<br/> Permite que los objetos dejen que otros objetos usen las credenciales de la persona que llama. Esta suplantación funcionará con scripting API para llamadas WMI, pero puede suponer un riesgo de seguridad innecesario.<br/> |



 

En el ejemplo siguiente se muestra cómo establecer la suplantación en una cadena de moniker al obtener una instancia específica de [**Proceso de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process).


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



Para obtener más información, vea [Crear una aplicación WMI o script](creating-a-wmi-application-or-script.md).

## <a name="setting-the-default-impersonation-level-using-the-registry"></a>Establecer el nivel de suplantación predeterminado mediante el Registro

Si tiene acceso al Registro, también puede establecer la clave del Registro de nivel de suplantación predeterminada. Esta clave especifica qué nivel de suplantación usa scripting API para WMI, a menos que se especifique lo contrario. La ruta de acceso siguiente identifica la ruta de acceso del Registro.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Default Impersonation Level**

De forma predeterminada, la clave del Registro se establece en 3, especificando el nivel suplantar suplantación. Algunos proveedores pueden requerir un mayor nivel de suplantación.

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a>Acceso al objeto SWbemSecurity en VBScript

La otra manera de establecer el nivel de suplantación es desde el objeto de seguridad [**SWbemSecurity,**](swbemsecurity.md) que aparece como la propiedad [**Security \_**](swbemservices-security-.md) de los objetos [**SWbemServices,**](swbemservices.md) [**SWbemObject,**](swbemobject.md) [**SWbemObjectSet,**](swbemobjectset.md) [**SWbemEventSource,**](swbemeventsource.md) [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator.**](swbemlocator.md)

WMI pasa la configuración de seguridad de un objeto primario a los descendientes del objeto original. Por lo tanto, puede establecer el nivel de suplantación de un objeto [**SWbemServices**](swbemservices.md) después de iniciar sesión en llamadas WMI y API mediante este objeto u objetos creados a partir de él, como objetos de tipo [**SWbemObject**](swbemobject.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Protección de clientes de scripting](securing-scripting-clients.md)
</dt> </dl>

 

