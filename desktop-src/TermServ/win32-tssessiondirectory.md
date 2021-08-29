---
title: Win32_TSSessionDirectory clase
description: Define los Conexión a Escritorio remoto de configuración de Broker (Agente de conexión a Escritorio remoto) para la clase \_ TSSessionDirectorySetting de Win32.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748eb3a84650a3188b55e90a6f13bb282fadbac285cdbc56722197d6d88a354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137588"
---
# <a name="win32_tssessiondirectory-class"></a>Clase TSSessionDirectory de Win32 \_

Define la configuración Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto) para la [**clase \_ TSSessionDirectorySetting de Win32.**](win32-tssessiondirectorysetting.md)

> [!Note]  
> En Windows Server 2008 R2, el nombre del Agente de sesión de Terminal Services (TS Session Broker) se cambió a Agente de conexión a Escritorio remoto. Estas propiedades se aplican a todos los sistemas operativos compatibles, a menos que se indique lo contrario.

 

La sintaxis siguiente se simplifica a partir del código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético. Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSSessionDirectory de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSSessionDirectory de Win32** tiene estos métodos.



| Método                                                                                                  | Descripción                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [**CreateUserDiskTemplate**](createuserdisktemplate-win32-tssessiondirectory.md)                       | Crea una plantilla de disco de usuario.<br/>                                                                     |
| [**DisableUserVhd**](disableuservhd-win32-tssessiondirectory.md)                                       | Deshabilita un VHD de perfil de usuario.<br/>                                                                      |
| [**EnableUserVhd**](enableuservhd-win32-tssessiondirectory.md)                                         | Habilita un VHD de perfil de usuario en un servidor RDSH.<br/>                                                     |
| [**GetCurrentRedirectableAddresses**](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Obtiene la lista configurada actualmente de direcciones aptas para DNS y el tipo de redirección.<br/>        |
| [**GetRedirectableAddresses**](getredirectableaddresses-win32-tssessiondirectory.md)                   | Obtiene la lista completa de direcciones aptas para DNS.<br/>                                                |
| [**PingSessionDirectory**](pingsessiondirectory-win32-tssessiondirectory.md)                           | Comprueba si el servidor del Agente de conexión a Escritorio remoto está disponible.<br/>                                      |
| [**SetCurrentRedirectableAddresses**](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Establece la lista configurada de direcciones DNS aptas y el tipo de redirección.<br/>                     |
| [**SetLoadBalancingState**](setloadbalancingstate-win32-tssessiondirectory.md)                         | Establece el valor para indicar si el servidor participará en el equilibrio de carga del Agente de conexión a Escritorio remoto.<br/> |
| [**SetServerWeight**](setserverweight-win32-tssessiondirectory.md)                                     | Establece el valor de peso del servidor para el equilibrio de carga del Agente de conexión a Escritorio remoto.<br/>                             |
| [**SetSessionDirectoryActive**](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | Deshabilita y habilita el Agente de conexión a Escritorio remoto.<br/>                                                    |
| [**SetSessionDirectoryExposeServerIP**](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | Establece la **propiedad SessionDirectoryExposeServerIP.**<br/>                                             |
| [**SetSessionDirectoryProperty**](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | Establece la **propiedad SessionDirectoryLocation** o **la propiedad SessionDirectoryClusterName.**<br/>   |
| [**SetTSRedirectorMode**](settsredirectormode-win32-tssessiondirectory.md)                             | Este método no está disponible.<br/>                                                                     |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSSessionDirectory de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descripción breve (cadena de una línea) del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**GetLoadBalancingState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor está configurado para participar en el equilibrio de carga del Agente de conexión a Escritorio remoto.

<dt>

0
</dt> <dd>

El servidor no está configurado para participar en el equilibrio de carga del Agente de conexión a Escritorio remoto.

</dd> <dt>

1
</dt> <dd>

El servidor está configurado para participar en el equilibrio de carga del Agente de conexión a Escritorio remoto.

</dd> </dl>

</dd> <dt>

**GetServerWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Recupera el valor de peso del servidor que se usa en el equilibrio de carga del Agente de conexión a Escritorio remoto.

</dd> <dt>

**GetTSRedirectorMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor está configurado para actuar como Servicios de Escritorio remoto redirector.

<dt>

0
</dt> <dd>

El servidor está configurado para actuar como Servicios de Escritorio remoto redirector.

</dd> <dt>

1
</dt> <dd>

El servidor no está configurado para actuar como un Servicios de Escritorio remoto de acceso.

</dd> </dl>

**Windows Server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PolicySourceLoadBalancing**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor o la directiva de grupo configuran la propiedad **GetLoadBalancingState.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryActive**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor o la directiva de grupo configuran la propiedad **SessionDirectoryActive.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor o la directiva de grupo configuran la propiedad **SessionDirectoryClusterName.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor o la directiva de grupo configuran la propiedad **SessionDirectoryExposeServerIP.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryLocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor o la directiva de grupo configuran la propiedad **SessionDirectoryLocation.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceTSRedirectorMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad no está disponible.

**Windows Server 2008 R2:** Indica si el servidor o la directiva de grupo configuran la propiedad **GetTSRedirectorMode.**

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**SessionDirectoryActive**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Especifica si Servicios de Escritorio remoto participa en el Agente de conexión a Escritorio remoto.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Servicios de Escritorio remoto participación en el Agente de conexión a Escritorio remoto está deshabilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Servicios de Escritorio remoto está habilitada la participación en el Agente de conexión a Escritorio remoto.

</dd> </dl>

</dd> <dt>

**SessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección IP virtual del clúster al que pertenece el servidor host de sesión de Escritorio remoto.

</dd> <dt>

**SessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se permite la recuperación de la dirección IP del Agente de conexión a Escritorio remoto.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Se deniega la recuperación.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Se permite la recuperación.

</dd> </dl>

</dd> <dt>

**SessionDirectoryIPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Dirección IP del adaptador laN usado por el directorio de sesión.

</dd> <dt>

**SessionDirectoryLocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre DNS de red o dirección IP del servidor donde se ejecuta el servicio agente de conexión a Escritorio remoto.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Entre los estados no operativo se incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los otros estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("Ok")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Error previo")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Deteniendo")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para conectarse al espacio \\ \\ de nombres Raíz de \\ \\ TerminalServices CIMV2, el nivel de autenticación debe incluir privacidad de paquetes. Para las llamadas de C/C++, se trata de un nivel de autenticación de **RPC \_ C \_ AUTHN LEVEL \_ \_ PKT \_ PRIVACY**. Para Visual Basic y llamadas de scripting, se trata de un nivel de autenticación **de WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de seis.

En el ejemplo Visual Basic Scripting Edition (VBScript) siguiente se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



En Windows Server 2008, el nombre de la característica Directorio de sesión de Terminal Services se cambió a Agente de sesión de Terminal Services.

En Windows Server 2008 R2, el nombre de la característica Agente de sesión de Terminal Services se cambió a Conexión a Escritorio remoto Broker.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

