---
title: Método Create de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Crea una directiva de autorización de conexión Escritorio remoto (RD \ 160; CAP) usando los valores especificados. El nuevo RD \ 160; El límite se insertará en la parte superior de la RD \ 160; Orden de evaluación CAP, con un valor de propiedad order de \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_TSGatewayConnectionAuthorizationPolicy (clase)
- Win32_TSGatewayConnectionAuthorizationPolicy Servicios de Escritorio remoto de clase, Create (método)
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
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079037"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método Create de la \_ clase Win32 TSGatewayConnectionAuthorizationPolicy

Crea una directiva de autorización de conexión Escritorio remoto (CAP de RD) mediante los valores especificados. La nueva CAP de RD se insertará en la parte superior del orden de evaluación de CAP de RD, con un valor de propiedad **Order** de "1".

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

*Nombre* \[ de de\]
</dt> <dd>

Nombre de la CAP de RD. El nombre debe tener 64 caracteres o menos, único (se omite el caso) y no puede contener los siguientes caracteres reservados:

<> :; " / \\ \| ? \*\[Pestaña\]

</dd> <dt>

*UserGroupNames* \[ de\]
</dt> <dd>

Lista de nombres de grupos de usuarios, separados por punto y coma, para la nueva CAP de RD.

</dd> <dt>

*ComputerGroupNames* \[ de\]
</dt> <dd>

Lista de nombres de grupos de equipos, separados por punto y coma, para la nueva CAP de RD.

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

 

