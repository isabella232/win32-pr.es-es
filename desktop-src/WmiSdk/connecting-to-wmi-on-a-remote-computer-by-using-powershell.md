---
description: Conexión a WMI de forma remota con PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Conexión a WMI de forma remota con PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d499c59ee6774b1e972e192dfc2c0d1228469196c66e8f3feb80d1c9d6339c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679884"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Conexión a WMI de forma remota con PowerShell

Windows PowerShell proporciona un mecanismo sencillo para conectarse a Windows Management Instrumentation (WMI) en un equipo remoto. Las conexiones remotas en WMI se ven afectadas por el [firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))de Windows, la configuración de DCOM y el control de cuentas de usuario [(UAC).](/previous-versions/aa905108(v=msdn.10)) Para obtener más información sobre cómo configurar conexiones remotas, vea [Conectarse](connecting-to-wmi-remotely-starting-with-vista.md)a WMI de forma remota a partir Windows Vista .

Los ejemplos de este tema se basan en los VBScript de [Conectarse a WMI en un equipo remoto.](connecting-to-wmi-on-a-remote-computer.md) Todos los ejemplos de este tema usan el cmdlet [Get-WmiObject.](/previous-versions//dd315295(v=technet.10)) Para obtener más información, [vea Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

## <a name="windows-powershell-examples"></a>Windows PowerShell ejemplos

Al crear una conexión a un equipo remoto, un usuario puede especificar la información de conexión, como el nombre del equipo remoto, las credenciales y el nivel de autenticación de la conexión. En los ejemplos siguientes se muestra cómo conectarse a un equipo remoto mediante diferentes conjuntos de credenciales y cómo acceder a la información de WMI.

En el ejemplo Windows PowerShell siguiente se muestra cómo establecer el nivel de suplantación:


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



En el ejemplo anterior, el usuario se conecta a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con las que inició sesión. El usuario también solicitó usar la suplantación. A diferencia del ejemplo de VBScript original, no se necesita una cadena de moniker porque la propiedad "Impersonation" establece el nivel de suplantación. De forma predeterminada, el nivel de suplantación se establece en 3 (Suplantar).

En el ejemplo se enumeran todas las instancias de la [**clase \_ Win32 Process**](/windows/desktop/CIMWin32Prov/win32-process) que se ejecutan en el equipo remoto.

> [!Note]  
> Debe especificar el espacio de nombres WMI al que conectarse en el equipo remoto porque es posible que el espacio de nombres predeterminado no sea el mismo en equipos diferentes.

 

En el Windows PowerShell ejemplo siguiente se muestra cómo conectarse a un equipo remoto con credenciales diferentes y establecer el nivel de suplantación en 3, que es Suplantar:


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



En el ejemplo anterior, el nombre del equipo se asignó a $Computer variable. El usuario se conecta a un equipo remoto mediante credenciales específicas (dominio y nombre de usuario) y solicita suplantación para el nivel de autenticación.

> [!Note]  
> El carácter de acento grave ( \` ) se usa para indicar un salto de línea. Es equivalente al carácter de subrayado ( \_ ) en VBScript.

 

En el ejemplo Windows PowerShell siguiente se conecta a un grupo de equipos remotos en el mismo dominio mediante la creación de una matriz de nombres de equipo remoto y, a continuación, se muestran los nombres de los dispositivos Plug and Play (instancias de [**Win32 \_ PnPEntity)**](/windows/desktop/CIMWin32Prov/win32-pnpentity)en cada equipo:


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> Para ejecutar el script Windows PowerShell anterior, debe ser administrador en los equipos remotos. Además, en relación con el ejemplo anterior, tenga en cuenta lo siguiente:

 

-   Los nombres de equipo de la matriz deben ir entre comillas porque son cadenas.
-   Los objetos devueltos por [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) se asignan a $ColItems variable.
-   El operador range \[ \] limitó la lista de Plug and Play dispositivos a 48 instancias. Para obtener más información, vea [About \_ Operators](/previous-versions//dd347588(v=technet.10)).
-   " " \| es el carácter de canalización. El objeto devuelto por ColItems se envía al cmdlet [Format-List.]( /previous-versions//dd347700(v=technet.10))

El siguiente Windows PowerShell ejemplo le permite conectarse a un equipo remoto en un dominio diferente. En este ejemplo también se muestran los nombres de proceso de las instancias de [**Proceso win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) en el equipo remoto.


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> Para ejecutar el script Windows PowerShell anterior, debe ser administrador en el equipo remoto.

 

En el ejemplo anterior, el usuario se conecta a un equipo remoto en un dominio diferente y especifica una configuración regional preferida. El [comando Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita las credenciales del usuario y las asigna a un objeto . En el ejemplo también se enumeran los nombres de las instancias de la clase Process de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) que se ejecutan en el equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
