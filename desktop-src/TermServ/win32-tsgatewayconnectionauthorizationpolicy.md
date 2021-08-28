---
title: Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Describe una directiva de Escritorio remoto de autorización de conexión (Rd\ 160; CAP). Rd \ 160; Las CAP se usan para determinar si un usuario puede conectarse al servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfaefb0a3062db27622afe90023928507c6d127c64edb60041347f73c1b261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349250"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>Clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Describe una directiva de Escritorio remoto de autorización de conexión (CAP de Escritorio remoto). Las CAP de Escritorio remoto se usan para determinar si un usuario puede conectarse al servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGatewayConnectionAuthorizationPolicy de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSGatewayConnectionAuthorizationPolicy de Win32** tiene estos métodos.



| Método                                                                                                                | Descripción                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Agrega los nombres de grupo de equipos especificados a **la propiedad ComputerGroupNames.**<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Agrega los nombres de grupo de usuarios especificados a **la propiedad UserGroupNames.**<br/>                                                                                              |
| [**Creación**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Crea un CAP de Escritorio remoto.<br/>                                                                                                                                                   |
| [**Eliminar**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Elimina el CAP de Escritorio remoto actual.<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Establece la **propiedad ClipboardDisabled.**<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Establece la **propiedad DiskDrivesDisabled.**<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Establece la **propiedad PlugAndPlayDevicesDisabled.**<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Establece la **propiedad PrintersDisabled.**<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Establece la **propiedad SerialPortsDisabled.**<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Se usa para alternar **la propiedad AllowOnlySDRServers.**<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                  |
| [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Mueve el CAP de Escritorio remoto actual una posición hacia abajo en la lista.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Mueve el CAP de Escritorio remoto actual una posición hacia arriba en la lista.<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Quita los nombres de grupo de equipos especificados de la **propiedad ComputerGroupNames.**<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Quita los nombres de grupo de usuarios especificados de **la propiedad UserGroupNames.**<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Establece la **propiedad ComputerGroupNames.**<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Establece la **propiedad CookieAuthenticationAllowed.**<br/> **Windows Server 2008:** Este método no está disponible.<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Establece la **propiedad DeviceRedirectionType.**<br/>                                                                                                                         |
| [**SetEnabled**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Habilita o deshabilita el CAP de Escritorio remoto actual.<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Establece la **propiedad IdleTimeout.**<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Establece un nuevo nombre para este CAP de Escritorio remoto. Este método garantiza que los nombres sean únicos.<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Establece la **propiedad PasswordAllowed.**<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Establece la **propiedad SecureIdAllowed.**<br/> **Windows Server 2008:** Este método está reservado para su uso futuro.<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Establece las **propiedades SessionTimeout** **y SessionTimeoutAction.**<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Establece la **propiedad SmartcardAllowed.**<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Establece la **propiedad UserGroupNames.**<br/>                                                                                                                                |
| [**Actualizar**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Actualiza el CAP de Escritorio remoto actual.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayConnectionAuthorizationPolicy de Win32** tiene estas propiedades.

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si las conexiones solo permiten proteger servidores RDS de redireccionamiento de dispositivos (SDR). Esta propiedad se puede establecer mediante el [**método EnableAllowOnlySDRServers.**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**ClipboardDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará el redireccionamiento del Portapapeles. Esta propiedad solo tiene efecto si la **propiedad DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de nombres de grupos de equipos separados por punto y coma. Este valor puede estar vacío. Los nombres tienen el formato *Domain \\ ComputerGroupName*. Si se especifica un valor, el equipo cliente debe pertenecer a uno de estos grupos de equipos para que el usuario acceda al servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar la autenticación de cookies para conectarse al servidor de puerta de enlace de Escritorio remoto. Esta propiedad se puede establecer mediante el [**método SetCookieAuthenticationAllowed.**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md)

**Windows Server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica qué dispositivos se redirigirán.

<dt>

0
</dt> <dd>

Se redirigirán todos los dispositivos.

</dd> <dt>

1
</dt> <dd>

No se redirigirá ningún dispositivo.

</dd> <dt>

2
</dt> <dd>

Los dispositivos especificados no se redirigirán. Las propiedades **DiskDrivesDisabled**, **PrintersDisabled,** **SerialPortsDisabled,** **ClipboardDisabled** y **PlugAndPlayDevicesDisabled** controlan qué dispositivos no se redirigirán.

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará el redireccionamiento de la unidad de disco. Esta propiedad solo tiene efecto si la **propiedad DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**Habilitado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si este CAP de Escritorio remoto se usará para evaluar la autorización de un usuario.

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el CAP de Escritorio remoto usa atributos de Protección de acceso a redes (NAP).

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de tiempo de espera de inactividad, en minutos. Un valor de 0 significa que no hay tiempo de espera. Esta propiedad se puede establecer mediante el [**método SetIdleTimeout.**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)

**Windows Server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del CAP de Escritorio remoto.

</dd> <dt>

**Pedido**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Orden de evaluación del CAP de Escritorio remoto. El primer CAP de Escritorio remoto evaluado tiene un valor de "1". La **propiedad Order** se puede cambiar cuando se llama a los métodos [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete,**](delete-win32-tsgatewayconnectionauthorizationpolicy.md) [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)o [**MoveDown.**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar una contraseña para conectarse al servidor de puerta de enlace de Escritorio remoto. Esta propiedad se puede cambiar mediante el [**método SetPasswordAllowed.**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el redireccionamiento de Plug and Play dispositivos se deshabilitará. Esta propiedad solo tiene efecto si la **propiedad DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**ImpresorasDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará el redireccionamiento de impresoras. Esta propiedad solo tiene efecto si la **propiedad DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar un identificador seguro para conectarse al servidor de puerta de enlace de Escritorio remoto.

**Windows Server 2008:** Esta propiedad no se utiliza.

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará el redireccionamiento del puerto serie. Esta propiedad solo tiene efecto si la **propiedad DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El valor de tiempo de espera de la sesión, en minutos. Un valor de 0 significa que no hay tiempo de espera. Esta propiedad se puede establecer mediante el [**método SetSessionTimeout.**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)

**Windows Server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la acción que se debe realizar en el caso de que se agote el tiempo de espera de la sesión. Esta propiedad se puede establecer mediante el [**método SetSessionTimeout.**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)

Puede ser uno de los siguientes valores.

**Windows Server 2008:** Esta propiedad no está disponible.

<dt>

0
</dt> <dd>

Desconecte la sesión.

</dd> <dt>

1
</dt> <dd>

Intente volver a autorizar la sesión.

</dd> </dl>

</dd> <dt>

**Tarjeta inteligenteAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar una tarjeta inteligente para conectarse al servidor de puerta de enlace de Escritorio remoto. Esta propiedad se puede cambiar mediante el [**método SetSmartcardAllowed.**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de nombres de grupos de usuarios separados por punto y coma. Los nombres tienen el formato *Dominio \\ UserGroupName*. Si el usuario pertenece a cualquiera de estos grupos de usuarios, se le permitirá el acceso al servidor de puerta de enlace de Escritorio remoto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

