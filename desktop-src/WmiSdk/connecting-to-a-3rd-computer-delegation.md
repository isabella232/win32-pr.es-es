---
description: Al ejecutar un script en un sistema local que obtiene datos de un sistema remoto, WMI proporciona sus credenciales al proveedor de los datos en el sistema remoto.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delegación con WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424135"
---
# <a name="delegating-with-wmi"></a>Delegación con WMI

Al ejecutar un script en un sistema local que obtiene datos de un sistema remoto, WMI proporciona sus credenciales al proveedor de los datos en el sistema remoto. Esto requiere solo un nivel de suplantación de **Suplantar**, porque solo se requiere un salto de red. Sin embargo, si el script se conecta a WMI en el sistema remoto e intenta abrir un archivo de registro en un sistema remoto adicional, el script producirá un error a menos que el nivel de suplantación sea **Delegate**. El nivel de suplantación de **delegado** es necesario para cualquier operación que implique más de un salto de red. Para obtener más información sobre la seguridad de DCOM en WMI, vea establecer la seguridad del proceso de la [aplicación cliente](setting-client-application-process-security.md). Para obtener más información acerca de la conexión de un salto de red entre dos equipos, consulte [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).

**Para usar la delegación para conectarse a un equipo a través de otro equipo**

1.  Habilite la delegación en Active Directory (**Active Directory usuarios y equipos** en el **Panel de control** **tareas administrativas**) en el controlador de dominio. La cuenta del sistema remoto debe estar marcada como **de confianza para la delegación** y la cuenta del sistema local no debe estar marcada como la **cuenta es importante y no se puede delegar**. el sistema local, el sistema remoto y el controlador de dominio deben ser miembros del mismo dominio o de dominios de confianza.

    **Nota:**  El uso de la delegación supone un riesgo para la seguridad, ya que proporciona a los procesos que están fuera de su control directo la capacidad de usar las credenciales.

2.  Modifique el código de la siguiente manera para indicar que desea usar la delegación.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell
    </dt> <dd>

    Establezca el parámetro *-Impersonation* en el CMDLET de WMI en **Delegate**.

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript
    </dt> <dd>

    Establezca el parámetro *impersonationLevel* en **Delegate** en la llamada a [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) o **Delegate** en la cadena de [moniker](constructing-a-moniker-string.md) . También puede establecer la suplantación en un objeto [**SWbemSecurity**](swbemsecurity.md).

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Establezca el parámetro de nivel de suplantación en el **\_ \_ \_ \_ delegado de nivel Imp de RPC C** en la llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Para obtener más información acerca de cuándo realizar estas llamadas, consulte [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).

    Para pasar la identidad del cliente a los servidores COM remotos en C++, establezca Cloaking en la llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Para obtener más información, consulte [Cloaking](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra una cadena de moniker que establece la suplantación en **Delegate**. Tenga en cuenta que la autoridad debe establecerse en Kerberos.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



En el ejemplo de código siguiente se muestra cómo establecer la suplantación en **Delegate** (un valor de 4) mediante [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protección de una conexión WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Crear procesos de forma remota con WMI](creating-processes-remotely.md)
</dt> </dl>

 

 
