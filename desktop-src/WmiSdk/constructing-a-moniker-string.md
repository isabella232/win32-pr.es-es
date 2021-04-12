---
description: El formato de cadena de moniker es similar al de una ruta de acceso de objeto WMI estándar. Para obtener más información, vea requisitos de ruta de acceso de objeto WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Construir una cadena de moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360586"
---
# <a name="constructing-a-moniker-string"></a>Construir una cadena de moniker

El formato de cadena de moniker es similar al de una ruta de acceso de objeto WMI estándar. Para obtener más información, vea [requisitos de ruta de acceso de objeto WMI](wmi-object-path-requirements.md).

Un moniker tiene las siguientes partes:

-   El prefijo WinMgmts: (obligatorio). El prefijo indica a Windows Script Host (WSH) que el siguiente código utilizará los [objetos de API de scripting](scripting-api-objects.md).
-   Un componente de configuración de seguridad (opcional)
-   Un componente de ruta de acceso de objeto WMI (opcional)

No se puede especificar una contraseña en una cadena de moniker de WMI. Si debe cambiar la contraseña (parámetro *strPassword* ) o el tipo de autenticación (parámetro *strAuthority* ) al conectarse a WMI, llame a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Tenga en cuenta que solo puede especificar la contraseña y la autoridad en las conexiones a equipos remotos. Si intenta establecerlos en un script que se esté ejecutando en el equipo local, se producirá un error. Para obtener más información sobre cuándo se utilizan la configuración de seguridad y los componentes de la ruta de acceso del objeto, vea [configuración de seguridad de WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).

El moniker siguiente especifica el objeto [**SWbemServices**](swbemservices.md) que representa el valor predeterminado de la raíz del espacio de nombres \\ , con suplantación en y el privilegio wbemPrivilegeDebug (SeDebugPrivilege) habilitado, y el privilegio wbemPrivilegeSecurity (SeSecurityPrivilege) deshabilitado.


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> Todos los literales de cadena no distinguen mayúsculas de minúsculas.
>
> El prefijo "!" de un privilegio indica que se va a deshabilitar el privilegio; la omisión de este prefijo implica que se va a habilitar el privilegio.
>
> El prefijo "!" se usa en el nombre de equipo o espacio de nombres cuando la configuración de seguridad se especifica entre corchetes antes del nombre o espacio de nombres del equipo.

 

Se permiten las siguientes asignaciones predeterminadas al especificar la ruta de acceso del objeto:

-   El nombre del equipo se puede omitir en la ruta de acceso del objeto, en cuyo caso se presupone el nombre del equipo local.
-   El espacio de nombres se puede omitir en la ruta de acceso del objeto, en cuyo caso se supone que se trata del espacio de nombres predeterminado.

    Esto viene determinado por el valor de la clave del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **scripting** \\ **default namespace**, el valor predeterminado es "root \\ CIMv2".

-   También se puede especificar una clase o una instancia, en cuyo caso el objeto devuelto es un objeto WMI en lugar de un objeto de servicios.

> [!Note]  
> Si se especifica una clase o instancia, no se puede omitir el espacio de nombres al especificar el nombre del equipo.

 

Para obtener una referencia de las constantes de privilegio usadas en la cadena de moniker de WMI, vea [constantes de privilegios](privilege-constants.md)y los descriptores "nombre corto de scripting".

## <a name="valid-moniker-strings"></a>Cadenas de moniker válidas

En los ejemplos siguientes se muestran cadenas de moniker válidas.

El moniker siguiente identifica el espacio de nombres predeterminado en el equipo local. Se devuelve un objeto [**SWbemServices**](swbemservices.md) .


```VB
WinMgmts:
```



El moniker siguiente identifica el espacio de nombres predeterminado en el equipo Server. Se devuelve un objeto [**SWbemServices**](swbemservices.md) .


```VB
"WinMgmts://myServer"
```



El moniker siguiente identifica el \\ espacio de nombres root cimv2 en el equipo de servidor. Se devuelve un objeto [**SWbemServices**](swbemservices.md) .


```VB
"WinMgmts://myServer/root/cimv2"
```



El moniker siguiente identifica el \\ espacio de nombres root cimv2 en el servidor local. Se devuelve un objeto [**SWbemServices**](swbemservices.md) .


```VB
"WinMgmts:root/cimv2"
```



El moniker siguiente identifica la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de nombres root cimv2 en el servidor de servidor. Se devuelve un objeto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



El moniker siguiente identifica la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de nombres root cimv2 en el servidor local. Se devuelve un objeto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



El moniker siguiente identifica la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el espacio de nombres predeterminado en el servidor local. Se devuelve un objeto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres de scripting predeterminado en el servidor local. Se devuelve un objeto [**SWbemObject**](swbemobject.md) . El espacio de nombres predeterminado para scripting viene determinado por el valor predeterminado de configuración del espacio de nombres, tal y como se especifica en el control WMI. Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el \\ espacio de nombres root cimv2 en el servidor de servidor. Se devuelve un objeto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el \\ espacio de nombres root cimv2 en el servidor local. Se devuelve un objeto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres predeterminado en el servidor local. Se devuelve un objeto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



El moniker siguiente establece el nivel de suplantación en Impersonate y establece el \_ privilegio de depuración se.


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



El moniker siguiente establece el nivel de suplantación en Impersonate y establece el \_ privilegio de depuración se. También revoca el privilegio de cierre de SE \_ .


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



El moniker siguiente recupera las descripciones localizadas en Inglés de Estados Unidos de la clase **MyClass** del \\ espacio de nombres WMI raíz.


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



El moniker siguiente solicita la autenticación Kerberos mediante el \\ servidor dominio principal.


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



El moniker siguiente solicita la autenticación NTLM mediante el dominio midominio.


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



En el ejemplo de código de VBScript siguiente se muestra cómo combinar parámetros de configuración regional y seguridad en un moniker.


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
> Aunque los monikers proporcionan un acceso directo a los objetos, en determinadas circunstancias, el uso repetido de monikers puede ser menos eficaz que el código equivalente que se conecta explícitamente a WMI. Si el rendimiento de la aplicación es una consideración, considere la posibilidad de usar los mecanismos alternativos.
>
> No es posible usar la función **GetObject** proporcionada por VBScript para actualizar o establecer los datos al ejecutar scripts incrustados en una página HTML, ya que Microsoft Internet Explorer deniega el uso de esta llamada por motivos de seguridad.

 

 

 
