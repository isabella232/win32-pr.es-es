---
title: Método Create de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Crea una directiva Escritorio remoto de autorización de conexión (Rd\ 160; CAP) mediante los valores especificados. El nuevo escritorio remoto \ 160; CAP se insertará en la parte superior del escritorio remoto \ 160; Orden de evaluación cap, con un valor de propiedad Order de \ 0034;1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create method Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy class
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto , Create (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16bf9dadb2a76a46d607a6cf2554192e3658686b58a089c19c3604c0c510bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871865"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método Create de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Crea una Escritorio remoto de autorización de conexión (CAP de Escritorio remoto) mediante los valores especificados. El nuevo CAP de Escritorio remoto se insertará en la parte superior del orden de evaluación del CAP de Escritorio remoto, con un valor de propiedad **Order** de "1".

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
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

Lista de nombres de grupo de usuarios, separados por punto y coma, para el nuevo CAP de Escritorio remoto.

</dd> <dt>

*ComputerGroupNames* \[ En\]
</dt> <dd>

Lista de nombres de grupo de equipos, separados por punto y coma, para el nuevo CAP de Escritorio remoto.

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

Los dispositivos especificados no se redirigirán. Los parámetros *DiskDrivesDisabled*, *PrintersDisabled,* *SerialPortsDisabled,* *ClipboardDisabled* y *PlugAndPlayDevicesDisabled* controlan qué dispositivos no se redirigirán.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ En\]
</dt> <dd>

Especifica si se deshabilita el redireccionamiento de la unidad de disco si el *parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*ImpresorasDisabled* \[ En\]
</dt> <dd>

Especifica si se deshabilita el redireccionamiento de impresora si *el parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*SerialPortsDisabled* \[ En\]
</dt> <dd>

Especifica si se debe deshabilitar la redirección de puertos serie si el *parámetro DeviceRedirectionType* es "2".

</dd> <dt>

*ClipboardDisabled* \[ En\]
</dt> <dd>

Especifica si se debe deshabilitar la redirección del Portapapeles si el *parámetro DeviceRedirectionType* es "2".

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

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

