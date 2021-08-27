---
title: Método Update de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Actualiza la directiva de autorización Escritorio remoto conexión actual (Escritorio remoto \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Actualización del método Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , Update
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
ms.openlocfilehash: 2ec7c3d1802f4faa3da8e382d00aa14fc8b3e091baef9659ad45322ec2a909c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850890"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método Update de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Actualiza la directiva de autorización Escritorio remoto de conexión (CAP de Escritorio remoto) actual.

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

*Nombre* \[ En\]
</dt> <dd>

Nombre del CAP de Escritorio remoto. El nombre debe tener 64 caracteres o menos, ser único (se omite case) y no puede contener los siguientes caracteres reservados:

<> : ; " / \\ \| ? \*\[TAB\]

</dd> <dt>

*UserGroupNames* \[ En\]
</dt> <dd>

Lista de nombres de grupos de usuarios separados por punto y coma. Los nombres tienen el formato *Dominio \\ UserGroupName*. Si el usuario pertenece a cualquiera de estos grupos de usuarios, se le permitirá el acceso al servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

*ComputerGroupNames* \[ En\]
</dt> <dd>

Lista de nombres de grupos de máquinas separados por punto y coma. Este valor puede estar vacío. Los nombres tienen el formato *Domain \\ ComputerGroupName*. Si se especifica un valor, el equipo cliente debe pertenecer a uno de estos grupos de equipos para que el usuario acceda al servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

*Tarjeta inteligente* \[ En\]
</dt> <dd>

Especifica si se pueden usar tarjetas inteligentes para autenticarse con el servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

*Contraseña* \[ En\]
</dt> <dd>

Especifica si se pueden usar contraseñas para autenticarse con el servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

*SecureId* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> <dt>

*Habilitado* \[ En\]
</dt> <dd>

Especifica si este CAP de Escritorio remoto está habilitado.

</dd> <dt>

*DeviceRedirectionType* \[ En\]
</dt> <dd>

Especifica qué tipos de dispositivo se redirigirán.

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

Los dispositivos especificados no se redirigirán. Los parámetros *DiskDrivesDisabled,* *PrintersDisabled,* *SerialPortsDisabled,* *ClipboardDisabled* y *PlugAndPlayDevicesDisabled* controlan qué dispositivos no se redirigirán.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ En\]
</dt> <dd>

Especifica si se debe deshabilitar el redireccionamiento de unidades de disco si el *parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*ImpresorasDisabled* \[ En\]
</dt> <dd>

Especifica si se debe deshabilitar el redireccionamiento de impresora si el *parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*SerialPortsDisabled* \[ En\]
</dt> <dd>

Especifica si se debe deshabilitar el redireccionamiento del puerto serie si el *parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*ClipboardDisabled* \[ En\]
</dt> <dd>

Especifica si se debe deshabilitar el redireccionamiento del Portapapeles si el *parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ En\]
</dt> <dd>

Especifica si se debe deshabilitar la redirección de Plug and Play dispositivos si el *parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*IdleTimeout* \[ En\]
</dt> <dd>

Valor de tiempo de espera de inactividad en minutos

</dd> <dt>

*SessionTimeout* \[ En\]
</dt> <dd>

Valor de tiempo de espera de sesión en minutos

</dd> <dt>

*SessionTimeoutAction* \[ En\]
</dt> <dd>

Acción de tiempo de espera de sesión en minutos

</dd> <dt>

*AllowOnlySDRServers* \[ En\]
</dt> <dd>

Si las conexiones solo se permiten a servidores TS de SDR

</dd> <dt>

*CookieAuthentication* \[ En\]
</dt> <dd>

Indica si se puede usar la autenticación de cookies para conectarse al servidor de puerta de enlace de TS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy de Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

