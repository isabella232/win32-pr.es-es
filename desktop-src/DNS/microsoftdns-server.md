---
title: MicrosoftDNS_Server (clase)
description: La \_ clase de servidor MicrosoftDNS describe un servidor DNS. Cada instancia de esta clase puede estar asociada a una instancia de la \_ caché de microsoftdns, una instancia de microsoftdns \_ RootHints y varias instancias de la \_ zona microsoftdns.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- DNS de la clase MicrosoftDNS_Server
- MicrosoftDNS_Server de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996001"
---
# <a name="microsoftdns_server-class"></a>MicrosoftDNS ( \_ clase de servidor)

La clase de **\_ servidor MicrosoftDNS** describe un servidor DNS. Cada instancia de esta clase puede estar asociada a una instancia de [**la \_ caché de microsoftdns**](microsoftdns-cache.md), una instancia de [**microsoftdns \_ RootHints**](microsoftdns-roothints.md)y varias instancias de la [**\_ zona microsoftdns**](microsoftdns-zone.md).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a>Miembros

La clase de **\_ servidor MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ servidor MicrosoftDNS** tiene estos métodos.



| Método                   | Descripción                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **GetDistinguishedName** | Recupera el nombre distintivo DNS de la zona.<br/>                        |
| **StartScavenging**      | Inicia la eliminación de registros obsoletos en las zonas sometidas a limpieza.<br/> |
| **StartService**         | Inicia el servidor DNS.<br/>                                                |
| **StopService**          | Detiene el servidor DNS.<br/>                                                 |



 

### <a name="properties"></a>Propiedades

La clase de **\_ servidor MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número máximo de registros de host devueltos en respuesta a una solicitud de dirección. Los valores entre 5 y 28 son válidos.

</dd> <dt>

**Recibe**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si el servidor DNS acepta solicitudes de actualización dinámica. Los valores válidos son los que se muestran en la tabla siguiente.



| Value                                                                                                | Significado                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | Sin restricciones.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | No permite actualizaciones dinámicas de registros SOA.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | No permite actualizaciones dinámicas de registros NS en la raíz de la zona.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | No permite actualizaciones dinámicas de registros NS que no estén en la raíz de la zona (registros NS de delegación).<br/> |



 

Sume estos valores para determinar el valor de configuración.

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS intenta actualizar sus entradas de caché con los datos de los servidores raíz. Cuando se inicia un servidor DNS, necesita una lista de "sugerencias" de servidor raíz NS y registros A para los servidores que históricamente se denominaba archivo caché. Los servidores DNS de Microsoft tienen una característica que les permite intentar volver a escribir un nuevo archivo caché en función de las respuestas de los servidores raíz.

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica qué zonas principales estándar que son autoritativas para el nombre del servidor DNS deben actualizarse cuando cambia el servidor de nombres. Los valores válidos son los siguientes:



| Value                                                                                                | Significado                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | Ninguno.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Solo los servidores que permiten actualizaciones dinámicas.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Solo los servidores que no permiten actualizaciones dinámicas.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Todos los servidores.<br/>                                    |



 

El valor predeterminado es 1.

* * Windows Server 2003: * *

El número 3 representa todos los servidores.

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Determina el formato del mensaje AXFR cuando se envía a los secundarios del servidor DNS que no son de Microsoft. Cuando se establece en TRUE, el servidor DNS envía las transferencias a las secundarias del servidor DNS que no son de Microsoft en el formato sin comprimir. Cuando es FALSE, todas las transferencias se envían en el formato rápido.

</dd> <dt>

**BootMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Método de inicialización del servidor DNS. En la siguiente tabla se muestran los valores válidos.



| Value                                                                                                | Significado                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | Sin inicializar.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Arranque desde el archivo.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Arranque desde el registro.<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Arranque desde el directorio y el registro.<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Valor predeterminado de **ScavengingInterval** establecido para todas las zonas integradas en Active Directory creadas en este servidor DNS. El valor predeterminado es cero, lo que indica que la eliminación de registros obsoletos está deshabilitada.

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Intervalo sin actualización, en horas, establecido para todas las zonas integradas en Active Directory creadas en este servidor DNS. El valor predeterminado es 168 horas (siete días).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Intervalo de actualización, en horas, establecido para todas las zonas integradas en Active Directory creadas en este servidor DNS. El valor predeterminado es 168 horas (siete días).

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS crea automáticamente zonas de búsqueda inversa estándar.

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si se puede invalidar el enlace de puerto predeterminado para un socket que se usa para enviar consultas a servidores DNS remotos.

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si hay un DS disponible en el servidor DNS.

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Intervalo, en segundos, para sondear las zonas integradas en el DS.

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Duración de los registros de desecho en zonas integradas en el servicio de directorio, expresado en segundos.

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Duración, en segundos, de la información almacenada en caché que describe la versión de EDNS compatible con otros servidores DNS.

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si la compatibilidad con las particiones de directorio de aplicaciones está habilitada en el servidor DNS.

* * Windows Server 2003: * *

Este método se denomina EnableDirectoryPartitionSupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si el servidor DNS incluye RR específicos de DNSSEC, KEY, SIG y NXT en una respuesta, según la tabla siguiente:



| Value                                                                                                | Significado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | No se incluye ningún registro DNSSEC en la respuesta a menos que la consulta solicite un conjunto de registros de recursos del tipo de registro DNSSEC.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Los registros DNSSEC se incluyen en la respuesta según RFC 2535.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Los registros DNSSEC se incluyen en una respuesta solo si la consulta de cliente original contenía el registro de recursos OPT según RFC 2671<br/> |



 

Si una consulta solicita un conjunto de registros de recursos del tipo DNSSEC, el servidor DNS siempre responde con dichos registros, si está disponible.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica el comportamiento del servidor DNS. Si es TRUE, el servidor DNS responde siempre con los registros de recursos OPT según RFC 2671, a menos que el servidor remoto haya indicado que no admite EDNS en un intercambio anterior. Si es FALSE, el servidor DNS responde a las consultas con OPC solo si se envían las OPC en la consulta original.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica qué eventos registra el servidor DNS en el registro del sistema de Visor de eventos. Se usan los valores siguientes.



| Value                                                                                                | Significado                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | Ninguno.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Solo registra errores.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Solo registra advertencias y errores.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Registra todos los eventos.<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se reenvían las consultas a zonas secundarias delegadas.

</dd> <dt>

**Reenviadores**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Enumera la lista de direcciones IP de los reenviadores a los que el servidor DNS reenvía las consultas.

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tiempo, en segundos, que un servidor DNS que reenvía una consulta esperará la resolución del [*reenviador*](f-gly.md) antes de intentar resolver la propia consulta.

Este valor no tiene sentido si el servidor de reenvío no está configurado para usar la recursividad. Para determinar esto, Compruebe la propiedad booleana IsSlave.

</dd> <dt>

**IsSlave**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

**True** si el servidor DNS no utiliza la recursividad cuando se produce un error en la resolución de nombres a través de reenviadores.

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Enumera la lista de direcciones IP en las que el servidor DNS puede recibir consultas.

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS da prioridad a la dirección de red local al devolver los registros.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tamaño del registro de depuración del servidor DNS, en bytes.

</dd> <dt>

**LogFilePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre de archivo y ruta de acceso para el registro de depuración del servidor DNS. El valor predeterminado es% system32% \\ DNS \\ DNS. log. Las rutas de acceso relativas son relativas a% systemroot% \\ system32. Se pueden usar rutas de acceso absolutas, pero no se admiten rutas de acceso UNC.

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Lista de direcciones IP utilizadas para filtrar los eventos DNS escritos en el registro de depuración.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica qué directivas se activan en el registro del sistema de Visor de eventos.

Debe establecerse en valores específicos basados en el siguiente algoritmo: cada Directiva (que se va a activar en el registro del sistema de Visor de eventos) se asigna a un valor específico.



| Value                                                                                                                  | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Misma.<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | Notificar a.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Actualizar:<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Transacciones que no son de consulta.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Preguntas.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Contesta.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Send.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Aparecen.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | Puertos.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Todos los paquetes.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | Transacción de escritura del servicio de directorio NT.<br/>  |
| <span id="131072"></span><dl> <dt>**131 072**</dt> </dl>         | Transacción de actualización del servicio de directorio NT.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Paquetes completos.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Escritura a través de.<br/>                           |



 

La suma de los valores correspondientes a todas las directivas que se van a activar se indica en esta propiedad.

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS realiza caracteres comodín sueltos. Si no está definida o es cero, el servidor sigue el comportamiento de los caracteres comodín especificados en el RFC de DNS. En este caso, se recomienda que un administrador incluya registros MX para todos los hosts que no puedan recibir correo. Si es distinto de cero, el servidor busca el nodo comodín más cercano; en este caso, un administrador debe colocar registros MX en la raíz de la zona y en un nodo comodín (' \* ') directamente debajo de la raíz de la zona. Además, los administradores deben colocar registros MX que hagan referencia a sí mismos en los hosts que reciben su propio correo.

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tiempo máximo, en segundos, que el registro de una consulta de nombres recursivos puede permanecer en la memoria caché del servidor DNS. El servidor DNS elimina los registros de la memoria caché cuando expira el valor de esta entrada, incluso si el valor del campo TTL del registro es mayor.

El valor predeterminado de esta propiedad es 86.400 segundos (1 día).

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tiempo máximo, en segundos, que el resultado de un error de nombre de una consulta recursiva puede permanecer en la memoria caché del servidor DNS. DNS elimina los registros de la memoria caché cuando este temporizador expira, incluso si el campo TTL es mayor. El valor predeterminado es 86.400 (un día).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de dominio completo (FQDN) o dirección IP del servidor DNS.

</dd> <dt>

**NameCheckFlag**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica el conjunto de caracteres válidos que se van a usar en los nombres DNS. Se usan los valores siguientes.



| Value                                                                                                | Significado                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | RFC estricto (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | No RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Multibyte (UTF8)<br/>  |



 

* * Windows Server 2003: * *

Un valor de "2" indica "any".

</dd> <dt>

**Recursividad**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS realiza búsquedas recursivas. TRUE indica que no se realizan búsquedas recursivas.

</dd> <dt>

**RecursionRetry**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Segundos transcurridos antes de volver a intentar una búsqueda recursiva. Si la propiedad no está definida o es cero, los reintentos se realizan después de tres segundos. No se recomienda a los usuarios modificar esta propiedad. Hay ciertas situaciones en las que se debe cambiar la propiedad; un ejemplo es cuando el servidor DNS se pone en contacto con los servidores remotos a través de un vínculo de baja velocidad y el servidor DNS vuelve a intentarlo antes de recibir la respuesta del DNS remoto. En este caso, sería razonable aumentar el tiempo de espera para que sea ligeramente mayor que el tiempo de respuesta observado del DNS remoto.

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Segundos transcurridos antes de que el servidor DNS proporcione una consulta recursiva. Si la propiedad no está definida o es cero, el servidor DNS se muestra después de 15 segundos. En general, el tiempo de espera de 15 segundos es suficiente para permitir que cualquier respuesta pendiente vuelva al servidor DNS.

No se recomienda a los usuarios modificar esta propiedad. Un escenario en el que se debe cambiar la propiedad es cuando el servidor DNS se pone en contacto con los servidores remotos a través de un vínculo de baja velocidad y se observa que el servidor DNS rechaza las consultas (con errores del servidor \_ ) antes de que se reciban las respuestas.

Los solucionadores de cliente también reintentan las consultas, por lo que es necesaria una investigación cuidadosa para determinar si las respuestas remotas están asociadas realmente a la consulta que agotó el tiempo de espera. En este caso, la elevación del valor de tiempo de espera para que sea ligeramente mayor que el tiempo de respuesta observado del DNS remoto sería razonable.

</dd> <dt>

**RoundRobin**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS redondea Robins varios registros A.

</dd> <dt>

**RPC**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Protocolo RPC o protocolos en los que se ejecuta RPC administrativo. El algoritmo siguiente se utiliza para asignar un valor específico:



| Value                                                                                                | Significado                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0,1**</dt> </dl> | None<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Canalizaciones con nombre<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | LPC<br/>         |



 

La suma de los valores indica los protocolos usados.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Intervalo, en horas, entre dos operaciones de eliminación de registros obsoletos consecutivas realizadas por el servidor DNS. Cero indica que la eliminación de registros obsoletos está deshabilitada. El valor predeterminado es 168 horas (siete días).

</dd> <dt>

**SecureResponses**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS guarda exclusivamente los registros de nombres en el mismo subárbol que el servidor que los proporcionó.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Puerto en el que el servidor DNS envía consultas UDP a otros servidores. De forma predeterminada, el servidor DNS envía consultas en un socket enlazado al puerto DNS.

En determinadas situaciones, no es la mejor configuración. Un caso obvio es cuando un administrador bloquea el puerto DNS con un firewall para evitar el acceso externo al servidor DNS, pero aún desea que el servidor pueda ponerse en contacto con los servidores DNS de Internet para proporcionar resolución de nombres para los clientes internos. Otro caso es cuando el servidor DNS admite redes no contiguas (la propiedad **DisjointNets** establecida en true identifica este escenario). En estos casos, el establecimiento de la propiedad **SendOnNonDnsPort** en un valor distinto de cero indica al servidor DNS que se enlace a un puerto arbitrario para enviarlo a servidores DNS remotos.

Si el valor de **SendOnNonDnsPort** es mayor que 1024, el servidor DNS se enlaza explícitamente con el valor de puerto especificado. Esta opción de configuración es útil cuando un administrador necesita corregir el puerto de consulta DNS para fines de Firewall.

* * Windows Server 2003: * *

Si se establece la propiedad puertoEnvío en un valor distinto de cero, el servidor DNS se enlaza a un puerto arbitrario para el envío a servidores DNS remotos.

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Enumera la lista de direcciones IP para el servidor DNS.

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el servidor DNS analiza estrictamente [*los archivos de zona*](z-gly.md) . Si no está definida o es cero, el servidor registrará y omitirá los datos incorrectos en el archivo de zona y continuará con la carga. Si es distinto de cero, el servidor registrará los errores de archivos de zona y se producirá un error en ellos.

</dd> <dt>

**UpdateOptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Restringe el tipo de registros que se pueden actualizar dinámicamente en el servidor, que se usan además de los valores de **AllowUpdate** en objetos de servidor y zona.

* * Windows Server 2003: * *

0: sin restricciones.

1: no permitir actualizaciones dinámicas de registros SOA.

2: no permitir actualizaciones dinámicas de registros NS en la raíz de la zona.

4: no permitir actualizaciones dinámicas de registros NS que no se realicen en la raíz de la zona (registros NS de delegación).

Sume estos valores para determinar el valor de configuración.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del servidor DNS.

</dd> <dt>

**WriteAuthorityNS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si el servidor DNS escribe registros NS y SOA en la sección de autoridad en una respuesta correcta.

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tiempo, en segundos, que el servidor DNS espera una conexión TCP correcta con un servidor remoto al intentar una transferencia de zona.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método StartService de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Método StopService de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método StartScavenging de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





