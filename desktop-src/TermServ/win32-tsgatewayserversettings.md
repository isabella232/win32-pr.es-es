---
title: Win32_TSGatewayServerSettings clase
description: Proporciona métodos y propiedades para ver y configurar las opciones Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c199b4b8e98832dcc8dbe65b8fc2ef636df71c8bd6e3c096670e6333f83a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008534"
---
# <a name="win32_tsgatewayserversettings-class"></a>Clase \_ TSGatewayServerSettings de Win32

Proporciona métodos y propiedades para ver y configurar las opciones Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto). Un administrador puede usar esta clase para configurar un conjunto de protocolos, el conjunto de eventos que se escribirán en el registro de eventos y el número máximo de conexiones a través de puerta de enlace de Escritorio remoto.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGatewayServerSettings de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSGatewayServerSettings de Win32** tiene estos métodos.



| Método                                                                                                                                             | Descripción                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](configure-win32-tsgatewayserversettings.md)                                                                                       | Configura los valores de IIS y RPC requeridos por el servicio puerta de enlace de Escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                               |
| [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Habilita o deshabilita la propiedad **CentralCAPEnabled,** que controla si los servidores centrales de la directiva de autorización de conexión Escritorio remoto (CAP de Escritorio remoto) se usan para controlar las directivas de autorización de conexión para este servidor.<br/>                    |
| [**EnableLogEvent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Habilita o deshabilita el registro del tipo de evento especificado.<br/>                                                                                                                                                                                              |
| [**EnableOnlyConsentCapableClients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Establece la **propiedad OnlyConsentCapableClients.**<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                                      |
| [**EnableRequestS ENABLE**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Este método no se admite a partir de Windows Server 2016.<br/> **Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008:** Habilita o deshabilita las solicitudes de una instrucción de mantenimiento (SoH).<br/> <br/> |
| [**EnableTransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Habilita o deshabilita el transporte especificado.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                                                  |
| [**EnumAuthenticationPlugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Enumera todos los complementos de autenticación registrados.<br/> **Windows Server 2008:** Este método no está disponible.<br/>                                                                                                                                  |
| [**EnumAuthorizationPlugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Enumera todos los complementos de autorización registrados.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                                     |
| [**GetIPAndPort**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                 |
| [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Devuelve el nombre del evento de registro para el índice de eventos de registro especificado.<br/>                                                                                                                                                                                         |
| [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Devuelve el nombre del protocolo para el índice de protocolo especificado.<br/>                                                                                                                                                                                           |
| [**IsLogEventEnabled**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Indica si el tipo de registro de eventos especificado está habilitado.<br/>                                                                                                                                                                                            |
| [**IsTransportEnabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Determina si el transporte especificado está habilitado.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                                        |
| [**QueryCertContext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Indica si el certificado especificado está instalado.<br/>                                                                                                                                                                                             |
| [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Recicla los grupos de aplicaciones RPC en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                                            |
| [**RefreshCertContext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Actualiza el certificado que usa el servidor de puerta de enlace de Escritorio remoto.<br/>                                                                                                                                                                                      |
| [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Establece el complemento de autenticación actual para el servidor de puerta de enlace de Escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                    |
| [**SetAuthenticationPluginAndRecycleRpcApplicationPools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Establece el complemento de autenticación actual para el servidor de puerta de enlace de Escritorio remoto y recicla los grupos de aplicaciones RPC en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                      |
| [**SetAuthorizationPlugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Establece el complemento de autorización actual para el servidor de puerta de enlace de Escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                     |
| [**SetCertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Establece el hash de certificado para el enlace HTTPS en el puerto 443 en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                       |
| [**SetCertificateACL**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Establece las listas de control de acceso (ACL) de certificado para este servidor.<br/>                                                                                                                                                                                     |
| [**SetDefaultPluginsAndRecycleRpcApplicationPools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Establece los complementos de autenticación y autorización actuales para el servidor de puerta de enlace de Escritorio remoto y recicla los grupos de aplicaciones RPC en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                   |
| [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Establece la **propiedad EnforceChannelBinding.**<br/> **Windows Server 2008 R2 y Windows Server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                                                  |
| [**SetIPAndPort**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Establece la dirección IP de escucha y el número de puerto para el transporte especificado.<br/> **Windows Server 2008 R2 y Windows Server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                    |
| [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Establece el número máximo de conexiones permitidas a través de puerta de enlace de Escritorio remoto. Este método cambia las **propiedades MaxConnections** **y UnlimitedConnections.**<br/>                                                                                                |
| [**SetSslBridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Establece el tipo de puente SSL que usará el servidor de puerta de enlace de Escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                    |
| [**TSGRemoveAdminMsg**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Quita el mensaje administrativo para el servidor de puerta de enlace.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGRemoveConsentMsg**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Quita el mensaje administrativo para el servidor de puerta de enlace.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreAdminMsg**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | Actualiza el mensaje administrativo para el servidor de puerta de enlace.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreConsentMsg**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | Actualiza el mensaje de consentimiento para el servidor de puerta de enlace.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                                   |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayServerSettings de Win32** tiene estas propiedades.

<dl> <dt>

**adminMessageEndTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora de finalización del mensaje administrativo.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**adminMessageStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora de inicio del mensaje administrativo.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**adminMessageText**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Texto del mensaje administrativo.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginCLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

CLSID del complemento de autenticación actual.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del complemento de autenticación actual.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del complemento de autenticación actual.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginCLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

CLSID del complemento de autorización actual.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del complemento de autorización actual.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del complemento de autorización actual.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**CentralCAPEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se usan servidores CAP de Escritorio remoto centrales para controlar este servidor. Esta propiedad se puede cambiar llamando al [**método EnableCentralCAP.**](enablecentralcap-win32-tsgatewayserversettings.md)

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el hash de certificado para el enlace HTTPS en el puerto 443 en IIS.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**consentMessageText**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Texto del mensaje de consentimiento.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**EnforceChannelBinding**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se aplica el enlace de canal para el transporte HTTP. Este valor de propiedad se puede cambiar mediante el [**método SetEnforceChannelBinding.**](setenforcechannelbinding-win32-tsgatewayserversettings.md)

**Windows Server 2008 R2 y Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2012.

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se configuran los valores de IIS y RPC requeridos por el servicio puerta de enlace de Escritorio remoto.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Devuelve el número máximo de conexiones que se permiten a través de puerta de enlace de Escritorio remoto. Esta propiedad se puede establecer mediante el [**método SetMaxConnections.**](setmaxconnections-win32-tsgatewayserversettings.md)

</dd> <dt>

**MaximumAllowedConnectionsBySku**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de conexiones que permite la unidad de almacén (SKU).

</dd> <dt>

**MaxLogEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Devuelve el número máximo de eventos de registro.

</dd> <dt>

**MaxProtocols**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de protocolos admitidos por puerta de enlace de Escritorio remoto.

</dd> <dt>

**OnlyConsentCapableClients**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si solo los clientes que pueden recibir mensajes de consentimiento pueden conectarse a la puerta de enlace de Escritorio remoto.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

<dt>

Distinto
</dt> <dd>

Solo los clientes compatibles con mensajes de consentimiento pueden conectarse.

</dd> <dt>

cero
</dt> <dd>

Los clientes que no son compatibles con mensajes de consentimiento también pueden conectarse.

</dd> </dl>

</dd> <dt>

**RequestSHH**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad no se admite a partir de Windows Server 2016.

**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: **

Especifica si el servidor debe solicitar una instrucción de estado (SoH) al cliente. Esta propiedad se puede cambiar mediante el [**método EnableRequestS EXECUTE.**](win32-tsgatewayserversettings-enablerequestsoh.md)

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la SKU.

</dd> <dt>

**SslBridging**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica qué tipo de puente SSL va a usar el servidor de puerta de enlace de Escritorio remoto. Puede ser uno de los siguientes valores.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

<dt>

0
</dt> <dd>

Sin protocolo de puente SSL.

</dd> <dt>

1
</dt> <dd>

Protocolo de puente HTTPS a HTTP.

</dd> <dt>

2
</dt> <dd>

Protocolo de puente https a HTTPS.

</dd> </dl>

</dd> <dt>

**UnlimitedConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se permite un número ilimitado de conexiones a través de puerta de enlace de Escritorio remoto. Esta propiedad se puede establecer mediante el [**método SetMaxConnections.**](setmaxconnections-win32-tsgatewayserversettings.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para usar esta clase.

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

[**TSGatewayConnection de Win32 \_**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy de Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**TSGatewayRADIUSServer de Win32 \_**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy de Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**TSGatewayResourceGroup de Win32 \_**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

