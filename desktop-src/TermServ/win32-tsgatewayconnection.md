---
title: Win32_TSGatewayConnection clase
description: Representa una conexión desde un equipo cliente a un servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnection clase Servicios de Escritorio remoto
- Win32_TSGatewayConnection clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a805882866a46a3ccba5a7620dad68e453408c13fada4897c5e0b2154d21e230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118847909"
---
# <a name="win32_tsgatewayconnection-class"></a>Clase \_ TSGatewayConnection de Win32

Representa una conexión desde un equipo cliente a un servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGatewayConnection de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSGatewayConnection de Win32** tiene estos métodos.



| Método                                                                     | Descripción                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**CheckStatus**](checkstatus-win32-tsgatewayconnection.md)               | Comprueba el estado de una conexión de servidor de puerta de enlace de Escritorio remoto y si el servidor de destino está configurado para el equilibrio de carga.<br/> |
| [**Desconectar**](disconnect-win32-tsgatewayconnection.md)                 | Finaliza la conexión.<br/>                                                                                                  |
| [**DisconnectProtocol**](disconnectprotocol-win32-tsgatewayconnection.md) | Finaliza todas las conexiones que usan el protocolo especificado.<br/>                                                                 |
| [**DisconnectUser**](disconnectuser-win32-tsgatewayconnection.md)         | Finaliza todas las conexiones del usuario especificado.<br/>                                                                           |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayConnection de Win32** tiene estas propiedades.

<dl> <dt>

**ChannelId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de canal.

</dd> <dt>

**ClientAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección IP del cliente.

</dd> <dt>

**ConnectedPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Puerto en el recurso conectado al que está conectado el usuario.

</dd> <dt>

**ConnectedResource**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo (o clúster) al que está conectado el cliente.

</dd> <dt>

**ConnectedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo para cuando se estableció la conexión. Esta vez se restablece cuando se restablece la conexión, incluso si se vuelve a conectar automáticamente.

</dd> <dt>

**ConnectionDuration**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo transcurrido desde la hora de conexión.

</dd> <dt>

**ConnectionKey**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador de conexión con el formato "tunnelId:channelID".

</dd> <dt>

**FullUserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de usuario completo del usuario conectado.

</dd> <dt>

**Tiempo de inactividad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo de inactividad de la conexión.

</dd> <dt>

**NumberOfKilobytesReceived**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de kilobytes recibidos del equipo cliente por el servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

**NumberOfKilobytesSent**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de kilobytes enviados al equipo cliente por el servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

**ProtocolName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo que se usa para conectarse al servidor de puerta de enlace de Escritorio remoto.

<dt>

"RDP"
</dt> <dd>

Protocolo para el servidor de puerta de enlace de Escritorio remoto.

</dd> </dl>

</dd> <dt>

**TransportProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de transporte para la conexión. Debe ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

RPC sobre transporte HTTP.

</dd> <dt>

1
</dt> <dd>

Transporte HTTP.

</dd> <dt>

2
</dt> <dd>

Transporte UDP.

</dd> </dl>

</dd> <dt>

**TunnelId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tunnel identificador.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de usuario conectado al servidor de puerta de enlace de Escritorio remoto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy de Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**TSGatewayRADIUSServer de Win32 \_**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy de Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**TSGatewayResourceGroup de Win32 \_**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

