---
title: Método Update de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Actualiza la Directiva de autorización de conexión Escritorio remoto actual (RD \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Método Update Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Servicios de Escritorio remoto de clase Win32_TSGatewayConnectionAuthorizationPolicy, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079446"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método Update de la \_ clase Win32 TSGatewayConnectionAuthorizationPolicy

Actualiza la Directiva de autorización de conexión Escritorio remoto actual (CAP de RD).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Nombre de la CAP de RD. El nombre debe tener 64 caracteres o menos, único (se omite el caso) y no puede contener los siguientes caracteres reservados:

<> :; " / \\ \| ? \*\[Pestaña\]

</dd> <dt>

*UserGroupNames* \[ de\]
</dt> <dd>

Lista de nombres de grupos de usuarios separados por punto y coma. Los nombres tienen el formato *dominio \\ UserGroupName*. Si el usuario pertenece a uno de estos grupos de usuarios, se le permitirá el acceso al servidor de puerta de enlace de escritorio remoto.

</dd> <dt>

*ComputerGroupNames* \[ de\]
</dt> <dd>

Lista de nombres de grupos de máquinas separados por punto y coma. Este valor puede estar vacío. Los nombres tienen el formato *dominio \\ ComputerGroupName*. Si se especifica un valor, el equipo cliente debe pertenecer a uno de estos grupos de equipos para que el usuario tenga acceso al servidor de puerta de enlace de escritorio remoto.

</dd> <dt>

*Tarjeta inteligente* \[ de\]
</dt> <dd>

Especifica si las tarjetas inteligentes se pueden usar para autenticarse con el servidor de puerta de enlace de escritorio remoto.

</dd> <dt>

*Contraseña* \[ de de\]
</dt> <dd>

Especifica si las contraseñas se pueden usar para autenticarse con el servidor de puerta de enlace de escritorio remoto.

</dd> <dt>

*SecureId* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> <dt>

*Habilitado* \[ de\]
</dt> <dd>

Especifica si esta CAP de RD está habilitada.

</dd> <dt>

*DeviceRedirectionType* \[ de\]
</dt> <dd>

Especifica los tipos de dispositivos que se redirigirán.

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

Los dispositivos especificados no se redirigirán. Los parámetros *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* y *PlugAndPlayDevicesDisabled* controlan qué dispositivos no se redirigirán.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ de\]
</dt> <dd>

Especifica si se va a deshabilitar la redirección de la unidad de disco si el parámetro *DeviceRedirectionType* es "2".

</dd> <dt>

*PrintersDisabled* \[ de\]
</dt> <dd>

Especifica si se va a deshabilitar la redirección de impresora si el parámetro *DeviceRedirectionType* es "2".

</dd> <dt>

*SerialPortsDisabled* \[ de\]
</dt> <dd>

Especifica si se va a deshabilitar la redirección de puertos serie si el parámetro *DeviceRedirectionType* es "2".

</dd> <dt>

*ClipboardDisabled* \[ de\]
</dt> <dd>

Especifica si se va a deshabilitar la redirección del portapapeles si el parámetro *DeviceRedirectionType* es "2".

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ de\]
</dt> <dd>

Especifica si se va a deshabilitar la redirección de dispositivos Plug and Play si el parámetro *DeviceRedirectionType* es "2".

</dd> <dt>

*IdleTimeout* \[ de\]
</dt> <dd>

Valor de tiempo de espera de inactividad en minutos

</dd> <dt>

*SessionTimeout* \[ de\]
</dt> <dd>

Valor de tiempo de espera de sesión en minutos

</dd> <dt>

*SessionTimeoutAction* \[ de\]
</dt> <dd>

Acción de tiempo de espera de sesión en minutos

</dd> <dt>

*AllowOnlySDRServers* \[ de\]
</dt> <dd>

Si las conexiones solo se permiten a los servidores SDR TS

</dd> <dt>

*CookieAuthentication* \[ de\]
</dt> <dd>

Indica si se puede usar la autenticación de cookies para conectarse al servidor de puerta de enlace de TS

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

