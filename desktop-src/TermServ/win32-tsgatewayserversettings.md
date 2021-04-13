---
title: Win32_TSGatewayServerSettings (clase)
description: Proporciona métodos y propiedades para ver y configurar la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayServerSettings de clase, se describe
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
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492706"
---
# <a name="win32_tsgatewayserversettings-class"></a>\_Clase Win32 TSGatewayServerSettings

Proporciona métodos y propiedades para ver y configurar la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). Un administrador puede utilizar esta clase para configurar un conjunto de protocolos, el conjunto de eventos que se escribirán en el registro de eventos y el número máximo de conexiones a través de la puerta de enlace de escritorio remoto.

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

La clase **Win32 \_ TSGatewayServerSettings** tiene estos métodos.



| Método                                                                                                                                             | Descripción                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configuración**](configure-win32-tsgatewayserversettings.md)                                                                                       | Configura los valores de IIS y RPC requeridos por el servicio de puerta de enlace de escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                               |
| [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Habilita o deshabilita la propiedad **CentralCAPEnabled** , que controla si se usan los servidores de la Directiva de autorización de conexión (Cap) central escritorio remoto para controlar las directivas de autorización de conexión para este servidor.<br/>                    |
| [**EnableLogEvent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Habilita o deshabilita el registro del tipo de evento especificado.<br/>                                                                                                                                                                                              |
| [**EnableOnlyConsentCapableClients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Establece la propiedad **OnlyConsentCapableClients** .<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                                      |
| [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Este método no se admite a partir de Windows Server 2016.<br/> **Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 y Windows server 2008:** Habilita o deshabilita las solicitudes de un informe de mantenimiento (SoH).<br/> <br/> |
| [**EnableTransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Habilita o deshabilita el transporte especificado.<br/> **Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                                                  |
| [**EnumAuthenticationPlugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Enumera todos los complementos de autenticación registrados.<br/> **Windows Server 2008:** Este método no está disponible.<br/>                                                                                                                                  |
| [**EnumAuthorizationPlugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Enumera todos los complementos de autorización registrados.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                                     |
| [**GetIPAndPort**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.<br/> **Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                 |
| [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Devuelve el nombre del evento de registro para el índice de eventos de registro especificado.<br/>                                                                                                                                                                                         |
| [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Devuelve el nombre de protocolo para el índice de protocolo especificado.<br/>                                                                                                                                                                                           |
| [**IsLogEventEnabled**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Indica si el tipo de registro de eventos especificado está habilitado.<br/>                                                                                                                                                                                            |
| [**IsTransportEnabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Determina si el transporte especificado está habilitado.<br/> **Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                                        |
| [**QueryCertContext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Indica si el certificado especificado está instalado.<br/>                                                                                                                                                                                             |
| [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Recicla los grupos de aplicaciones RPC en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                                            |
| [**RefreshCertContext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Actualiza el certificado usado por el servidor de puerta de enlace de escritorio remoto.<br/>                                                                                                                                                                                      |
| [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Establece el complemento de autenticación actual para el servidor de puerta de enlace de escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                    |
| [**SetAuthenticationPluginAndRecycleRpcApplicationPools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Establece el complemento de autenticación actual para el servidor de puerta de enlace de escritorio remoto y recicla los grupos de aplicaciones RPC en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                      |
| [**SetAuthorizationPlugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Establece el complemento de autorización actual para el servidor de puerta de enlace de escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                     |
| [**SetCertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Establece el hash del certificado para el enlace HTTPS en el puerto 443 en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                       |
| [**SetCertificateACL**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Establece las listas de control de acceso (ACL) del certificado para este servidor.<br/>                                                                                                                                                                                     |
| [**SetDefaultPluginsAndRecycleRpcApplicationPools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Establece los complementos de autenticación y autorización actuales para el servidor de puerta de enlace de escritorio remoto y recicla los grupos de aplicaciones RPC en IIS.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                   |
| [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Establece la propiedad **EnforceChannelBinding** .<br/> **Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                                                  |
| [**SetIPAndPort**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Establece la dirección IP de escucha y el número de puerto para el transporte especificado.<br/> **Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.<br/>                                                    |
| [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Establece el número máximo de conexiones permitidas a través de la puerta de enlace de escritorio remoto. Este método cambia las propiedades **MaxConnections** y **UnlimitedConnections** .<br/>                                                                                                |
| [**SetSslBridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Establece el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de escritorio remoto.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                    |
| [**TSGRemoveAdminMsg**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Quita el mensaje administrativo del servidor de puerta de enlace.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGRemoveConsentMsg**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Quita el mensaje administrativo del servidor de puerta de enlace.<br/> **Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.<br/>                                                                                            |
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

La hora de finalización del mensaje administrativo.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**adminMessageStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora de inicio del mensaje administrativo.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**adminMessageText**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El texto del mensaje administrativo.

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

La descripción del complemento de autenticación actual.

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

La descripción del complemento de autorización actual.

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

Especifica si se usan los servidores de CAP de RD central para controlar este servidor. Esta propiedad se puede cambiar llamando al método [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) .

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el hash del certificado para el enlace HTTPS en el puerto 443 en IIS.

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

Indica si se aplica el enlace de canal para el transporte HTTP. Este valor de propiedad se puede cambiar mediante el método [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .

**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible antes de Windows Server 2012.

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la configuración de IIS y RPC requerida por el servicio de puerta de enlace de escritorio remoto está configurada.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Devuelve el número máximo de conexiones permitidas a través de la puerta de enlace de escritorio remoto. Esta propiedad se puede establecer mediante el método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .

</dd> <dt>

**MaximumAllowedConnectionsBySku**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de conexiones que permite la unidad de almacén (SKU).

</dd> <dt>

**MaxLogEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Devuelve el número máximo de eventos de registro.

</dd> <dt>

**MaxProtocols**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de protocolos admitidos por la puerta de enlace de escritorio remoto.

</dd> <dt>

**OnlyConsentCapableClients**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si solo se permite que los clientes con capacidad de consentimiento se conecten a la puerta de enlace de escritorio remoto.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

<dt>

distinto
</dt> <dd>

Solo los clientes compatibles con mensajes de consentimiento pueden conectarse.

</dd> <dt>

cero
</dt> <dd>

Los clientes que no son compatibles con los mensajes de consentimiento también pueden conectarse.

</dd> </dl>

</dd> <dt>

**RequestSOH**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad no se admite a partir de Windows Server 2016.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: * *

Especifica si el servidor debe solicitar un informe de mantenimiento (SoH) del cliente. Esta propiedad se puede cambiar mediante el método [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) .

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

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de escritorio remoto. Puede ser uno de los valores siguientes.

**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.

<dt>

0
</dt> <dd>

Sin puentes SSL.

</dd> <dt>

1
</dt> <dd>

Puente de HTTPS a HTTP.

</dd> <dt>

2
</dt> <dd>

Puente de HTTPS a HTTPS.

</dd> </dl>

</dd> <dt>

**UnlimitedConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se permite un número ilimitado de conexiones a través de la puerta de enlace de escritorio remoto. Esta propiedad se puede establecer mediante el método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

