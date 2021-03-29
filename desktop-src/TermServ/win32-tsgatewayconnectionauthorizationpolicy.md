---
title: Win32_TSGatewayConnectionAuthorizationPolicy (clase)
description: Describe una Escritorio remoto Directiva de autorización de conexión (RD \ 160; CAP). RD \ 160; Los Cap se usan para determinar si un usuario puede conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayConnectionAuthorizationPolicy de clase, se describe
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
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905188"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>\_Clase Win32 TSGatewayConnectionAuthorizationPolicy

Describe una Escritorio remoto Directiva de autorización de conexión (CAP de RD). Las Cap de RD se usan para determinar si un usuario puede conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

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

La clase **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tiene estos métodos.



| Método                                                                                                                | Descripción                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Agrega los nombres de grupo de equipos especificados a la propiedad **ComputerGroupNames** .<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Agrega los nombres de grupos de usuarios especificados a la propiedad **UserGroupNames** .<br/>                                                                                              |
| [**A**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Crea una CAP de RD.<br/>                                                                                                                                                   |
| [**Elimínelos**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Elimina la CAP de RD actual.<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Establece la propiedad **ClipboardDisabled** .<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Establece la propiedad **DiskDrivesDisabled** .<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Establece la propiedad **PlugAndPlayDevicesDisabled** .<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Establece la propiedad **PrintersDisabled** .<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Establece la propiedad **SerialPortsDisabled** .<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Se usa para alternar la propiedad **AllowOnlySDRServers**<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                  |
| [**Bajar**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Mueve la CAP de RD actual una posición hacia abajo en la lista.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Mueve la CAP de RD actual una posición hacia arriba en la lista.<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Quita los nombres de grupo de equipos especificados de la propiedad **ComputerGroupNames** .<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Quita los nombres de grupos de usuarios especificados de la propiedad **UserGroupNames** .<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Establece la propiedad **ComputerGroupNames** .<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Establece la propiedad **CookieAuthenticationAllowed** .<br/> **Windows Server 2008:** Este método no está disponible.<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Establece la propiedad **DeviceRedirectionType** .<br/>                                                                                                                         |
| [**SetEnabled**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Habilita o deshabilita la CAP de RD actual.<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Establece la propiedad **IdleTimeout** .<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Establece un nuevo nombre para esta CAP de RD. Este método garantiza que los nombres serán únicos.<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Establece la propiedad **PasswordAllowed** .<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Establece la propiedad **SecureIdAllowed** .<br/> **Windows Server 2008:** Este método se reserva para uso futuro.<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Establece las propiedades **SessionTimeout** y **SessionTimeoutAction** .<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Establece la propiedad **SmartcardAllowed** .<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Establece la propiedad **UserGroupNames** .<br/>                                                                                                                                |
| [**Update**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Actualiza la CAP de RD actual.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayConnectionAuthorizationPolicy de Win32** tiene estas propiedades.

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si las conexiones solo se permiten para los servidores RDS de redirección de dispositivos (SDR). Esta propiedad se puede establecer mediante el método [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**ClipboardDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará la redirección del portapapeles. Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de nombres de grupos de equipos separados por punto y coma. Este valor puede estar vacío. Los nombres tienen el formato *dominio \\ ComputerGroupName*. Si se especifica un valor, el equipo cliente debe pertenecer a uno de estos grupos de equipos para que el usuario tenga acceso al servidor de puerta de enlace de escritorio remoto.

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar la autenticación de cookies para conectarse al servidor de puerta de enlace de escritorio remoto. Esta propiedad se puede establecer mediante el método [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica los dispositivos que se redirigirán.

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

Los dispositivos especificados no se redirigirán. Las propiedades **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** y **PlugAndPlayDevicesDisabled** controlan qué dispositivos no se redirigirán.

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará la redirección de la unidad de disco. Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se usará esta CAP de RD para evaluar la autorización de un usuario.

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la CAP de RD usa atributos de protección de acceso a redes (NAP).

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de tiempo de espera de inactividad, en minutos. Un valor de 0 significa que no hay tiempo de espera. Esta propiedad se puede establecer mediante el método [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre de la CAP de RD.

</dd> <dt>

**Pedido**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Orden de evaluación de la CAP de RD. La primera CAP de RD evaluada tiene un valor de "1". La propiedad **Order** se puede cambiar cuando se llama a los métodos [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**moveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)o [**moveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar una contraseña para conectarse al servidor de puerta de enlace de escritorio remoto. Esta propiedad se puede cambiar mediante el método [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará la redirección de Plug and Play dispositivos. Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**PrintersDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará la redirección de la impresora. Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar un identificador seguro para conectarse al servidor de puerta de enlace de escritorio remoto.

**Windows Server 2008:** Esta propiedad no se utiliza.

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se deshabilitará la redirección de puertos serie. Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El valor de tiempo de espera de la sesión, en minutos. Un valor de 0 significa que no hay tiempo de espera. Esta propiedad se puede establecer mediante el método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Esta propiedad no está disponible.

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la acción que se va a realizar en caso de que se agote el tiempo de espera de una sesión. Esta propiedad se puede establecer mediante el método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

Puede ser uno de los valores siguientes.

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

**SmartcardAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede usar una tarjeta inteligente para conectarse al servidor de puerta de enlace de escritorio remoto. Esta propiedad se puede cambiar mediante el método [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de nombres de grupos de usuarios separados por punto y coma. Los nombres tienen el formato *dominio \\ UserGroupName*. Si el usuario pertenece a alguno de estos grupos de usuarios, se le permitirá el acceso al servidor de puerta de enlace de escritorio remoto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar esta clase, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
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

 

