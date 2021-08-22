---
description: Describe cómo los scripts, las aplicaciones y los proveedores pueden establecer conexiones a WMI en equipos remotos para obtener datos o controlar hardware y software.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Conexión a WMI en un equipo remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd8c4b592353c10836e8dd5516d9c4f729aed5d968ef4c0e551a05a17c8a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819721"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a>Conexión a WMI en un equipo remoto

WMI se puede usar para administrar y acceder a datos WMI en equipos remotos. Las conexiones remotas en WMI se ven afectadas por la [configuración Windows Firewall y](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) DCOM. [El Control de cuentas de usuario (UAC)](/previous-versions/aa905108(v=msdn.10)) también puede requerir cambios en algunas configuraciones. Sin embargo, una vez que la configuración sea correcta, la llamada a un sistema remoto es muy similar a una llamada WMI local. Sin embargo, puede optar por hacerlo más complejo mediante credenciales diferentes, protocolos de autenticación alternativos y otras características de seguridad.

## <a name="configuring-a-computer-for-a-remote-connection"></a>Configuración de un equipo para una conexión remota

Para poder acceder a un sistema remoto con WMI, es posible que tenga que comprobar alguna configuración de seguridad para confirmar que tiene acceso. En concreto:

-   Windows contiene una serie de características de seguridad que pueden bloquear el acceso a scripts en sistemas remotos. Por lo tanto, es posible que deba modificar la configuración del firewall de Active Directory y Windows antes de realizar una llamada WMI. Para obtener más información, vea [Configurar una conexión WMI remota](connecting-to-wmi-remotely-starting-with-vista.md) y Solucionar problemas de una conexión WMI [remota.](troubleshooting-a-remote-wmi-connection.md)

-   La configuración correcta de DCOM debe estar habilitada para que funcione una conexión remota. Cambiar la configuración de DCOM puede permitir que los usuarios con pocos derechos accedan a un equipo para una conexión remota. Para obtener más información, [vea Proteger una conexión WMI remota.](securing-a-remote-wmi-connection.md)

Además, puede haber algunas circunstancias en las que puede que desee ejecutar WMI a través de un puerto fijo. Para ello, también tendrá que cambiar la configuración. Para obtener más información, vea [Configurar un puerto fijo para WMI.](setting-up-a-fixed-port-for-wmi.md)

## <a name="connecting-to-a-remote-computer"></a>Connecting to a Remote Computer

En su núcleo, la conexión a un sistema remoto con WMI consiste en asegurarse de que tiene los permisos adecuados para acceder al sistema y de que la conexión está configurada correctamente. Una vez que tenga esos dos elementos, la propia conexión es relativamente sencilla. Por ejemplo, si usa sus credenciales de seguridad predeterminadas, puede acceder a WMI en un sistema remoto mediante el código siguiente:

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Conexión a WMI de forma remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

Use el *parámetro -ComputerName* común a la mayoría de los cmdlets WMI, como [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Conexión a WMI de forma remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

Use un moniker que contenga el nombre del sistema remoto en la llamada a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conexión a WMI de forma remota con C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Para la versión actual de la interfaz administrada de WMI[(Microsoft.Management.Infrastructure),](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))use el objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) para representar una conexión a un host remoto.


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conexión a WMI de forma remota con C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Para la versión v1 de la interfaz administrada de WMI[(System.Management),](/dotnet/api/system.management)use el objeto [ManagementScope](/dotnet/api/system.management.managementscope) para representar una conexión a un host remoto.


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Ejemplo: Obtener datos WMI de un equipo remoto (C++)](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

Use el [**método IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para especificar el nombre del equipo remoto en el *parámetro strNetworkResource.*


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

Los ejemplos de código anteriores son posiblemente la conexión remota más básica que puede realizar con WMI. En concreto, en los ejemplos se da por hecho lo siguiente:

-   Es administrador en el equipo remoto. Debido al [control de cuentas de](/previous-versions/aa905108(v=msdn.10))usuario , la cuenta del sistema remoto debe ser una cuenta de dominio en el grupo Administradores. Para obtener más información, vea Control de cuentas de usuario y WMI.
-   La contraseña del equipo local actual no está en blanco. Se trata básicamente de un Windows de seguridad que debe haber iniciado sesión en el sistema con una contraseña.
-   Los equipos locales y remotos están dentro del mismo dominio. Si necesita traspasar los límites del dominio, deberá proporcionar información adicional o usar un modelo de programación ligeramente diferente.
-   Está usando su propia cuenta para acceder a la máquina remota. Si estaba intentando acceder a otra cuenta, tendría que proporcionar credenciales adicionales. (Tenga en cuenta que no se permite intentar acceder a WMI localmente con credenciales distintas de la cuenta actual).
-   Ambos equipos ejecutan IPv6. WMI admite conexiones a equipos que ejecutan IPv6. Sin embargo, tanto la máquina local como el "Equipo \_ B" deben ejecutar IPv6. Cualquier equipo también puede ejecutar IPv4. Para obtener más información, [vea Compatibilidad con IPv6 e IPv4 en WMI.](ipv6-and-ipv4-support-in-wmi.md)
-   El script no necesita delegar; es decir, no necesita acceder a equipos remotos adicionales a través del equipo remoto de destino. Para obtener más información, vea [Delegación con WMI.](connecting-to-a-3rd-computer-delegation.md)
-   Está intentando realizar una llamada específica, en lugar de crear un proceso remoto. Para obtener más información, vea [Crear procesos de forma remota mediante WMI.](creating-processes-remotely.md)

Con estas restricciones en mente, una llamada WMI remota es muy similar a una llamada WMI local; la única diferencia es que debe especificar el nombre del sistema remoto. Sin embargo, puede optar por cambiar muchas de esas características: usar credenciales diferentes, enrutar la llamada a través de un equipo de terceros o acceder a un dominio diferente.

 

 
