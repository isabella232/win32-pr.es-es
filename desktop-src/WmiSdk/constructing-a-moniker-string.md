---
description: El formato de cadena del moniker es similar al de una ruta de acceso de objeto WMI estándar. Para obtener más información, vea Wmi Object Path Requirements.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Construcción de una cadena de Moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170518"
---
# <a name="constructing-a-moniker-string"></a>Construcción de una cadena de Moniker

El formato de cadena del moniker es similar al de una ruta de acceso de objeto WMI estándar. Para obtener más información, vea [Wmi Object Path Requirements](wmi-object-path-requirements.md).

Un moniker tiene las siguientes partes:

-   Prefijo WinMgmts: (obligatorio). El prefijo indica al Windows host de script (WSH) que el código siguiente va a usar los objetos [de la API de scripting](scripting-api-objects.md).
-   Un componente de configuración de seguridad (opcional)
-   Componente de ruta de acceso de objeto WMI (opcional)

No se puede especificar una contraseña en una cadena de moniker WMI. Si debe cambiar la contraseña (parámetro *strPassword)* o el tipo de autenticación (parámetro *strAuthority)* al conectarse a WMI, llame a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md). Tenga en cuenta que solo puede especificar la contraseña y la autoridad en las conexiones a equipos remotos. Si se intenta establecer en un script que se ejecuta en el equipo local, se produce un error. Para obtener más información sobre cuándo se usan la configuración de seguridad y los componentes de ruta de acceso de [objeto,](/previous-versions/tn-archive/ee156574(v=technet.10))vea Wmi Security Configuración .

El moniker siguiente especifica el objeto [**SWbemServices**](swbemservices.md) que representa el valor predeterminado de la raíz del espacio de nombres, con la suplantación activada y el privilegio \\ wbemPrivilegeDebug (SeDebugPrivilege) habilitado y el privilegio wbemPrivilegeSecurity (SeSecurityPrivilege) deshabilitado.


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> Todos los literales de cadena no tienen en cuenta las mayúsculas y minúsculas.
>
> El prefijo "!" de un privilegio indica que el privilegio se va a deshabilitar; La omisión de este prefijo implica que el privilegio se va a habilitar.
>
> El prefijo "!" se usa en el nombre o espacio de nombres del equipo cuando la configuración de seguridad se especifica entre corchetes antes del nombre o espacio de nombres del equipo.

 

Se permiten las siguientes asignaciones predeterminadas al especificar la ruta de acceso del objeto:

-   El nombre del equipo se puede omitir en la ruta de acceso del objeto, en cuyo caso se supone que el nombre de la máquina local.
-   El espacio de nombres se puede omitir en la ruta de acceso del objeto, en cuyo caso se asume el espacio de nombres predeterminado.

    Esto viene determinado por el valor de la clave del Registro **HKEY \_ LOCAL \_ MACHINE** Software Microsoft WBEM Scripting Default Namespace , el valor predeterminado \\  \\  \\  \\  \\ es \\ "ROOT CIMv2".

-   También se puede especificar una clase o instancia, en cuyo caso el objeto devuelto es un objeto WMI en lugar de un objeto de servicios.

> [!Note]  
> Si se especifica una clase o instancia, no se puede omitir el espacio de nombres al especificar el nombre del equipo.

 

Para obtener una referencia de las constantes de privilegio usadas en la cadena de moniker WMI, vea Constantes de [privilegios](privilege-constants.md)y descriptores de "Nombre corto de scripting".

## <a name="valid-moniker-strings"></a>Cadenas de moniker válidas

En los ejemplos siguientes se muestran cadenas de moniker válidas.

El moniker siguiente identifica el espacio de nombres predeterminado en el equipo local. Se devuelve un objeto [**SWbemServices.**](swbemservices.md)


```VB
WinMgmts:
```



El moniker siguiente identifica el espacio de nombres predeterminado en el equipo myServer. Se devuelve un objeto [**SWbemServices.**](swbemservices.md)


```VB
"WinMgmts://myServer"
```



El moniker siguiente identifica el espacio de nombres \\ cimv2 raíz en el equipo myServer. Se devuelve un objeto [**SWbemServices.**](swbemservices.md)


```VB
"WinMgmts://myServer/root/cimv2"
```



El moniker siguiente identifica el espacio de \\ nombres cimv2 raíz en el servidor local. Se devuelve un objeto [**SWbemServices.**](swbemservices.md)


```VB
"WinMgmts:root/cimv2"
```



El moniker siguiente identifica la clase [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el espacio de nombres \\ raíz cimv2 en el servidor myServer. Se devuelve un objeto [**SWbemObject.**](swbemobject.md)


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



El moniker siguiente identifica la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el espacio de nombres \\ raíz cimv2 del servidor local. Se devuelve un objeto [**SWbemObject.**](swbemobject.md)


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



El moniker siguiente identifica la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el espacio de nombres predeterminado en el servidor local. Se devuelve un objeto [**SWbemObject.**](swbemobject.md)


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



El moniker siguiente identifica la instancia de [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres de scripting predeterminado en el servidor local. Se devuelve un objeto [**SWbemObject.**](swbemobject.md) El espacio de nombres predeterminado para scripting viene determinado por la configuración predeterminada del espacio de nombres, tal como se especifica en el control WMI. Para obtener más información, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



El moniker siguiente identifica la instancia de [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres \\ raíz cimv2 en el servidor myServer. Se devuelve un objeto [**SWbemObject.**](swbemobject.md)


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres \\ cimv2 raíz del servidor local. Se devuelve un objeto [**SWbemObject.**](swbemobject.md)


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



El moniker siguiente identifica la instancia de [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres predeterminado en el servidor local. Se devuelve un objeto [**SWbemObject.**](swbemobject.md)


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



El moniker siguiente establece el nivel de suplantación para suplantar y establece el SE \_ debug.


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



El moniker siguiente establece el nivel de suplantación para suplantar y establece el SE \_ debug. También revoca el SE \_ shutdown.


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



El moniker siguiente recupera las descripciones localizadas en inglés de Estados Unidos para la **clase myclass** del espacio de \\ nombres wmi raíz.


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



El moniker siguiente solicita la autenticación Kerberos mediante el servidor mydomain \\ principal.


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



El moniker siguiente solicita la autenticación NTLM mediante el dominio mydomain.


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



En el ejemplo de código de VBScript siguiente se muestra cómo combinar parámetros de seguridad y configuración regional en un moniker.


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Aunque los monikers proporcionan un acceso más directo a los objetos, en determinadas circunstancias, el uso repetido de monikers puede ser menos eficaz que el código equivalente que se conecta explícitamente a WMI. Si el rendimiento de la aplicación es una consideración, considere la posibilidad de usar los mecanismos alternativos.
>
> No es posible usar la función **GetObject** proporcionada por VBScript para actualizar o establecer datos al ejecutar scripts insertados en una página HTML, ya que Microsoft Internet Explorer deniega el uso de esta llamada por motivos de seguridad.

 

 

 
