---
title: MicrosoftDNS_Server clase
description: La clase MicrosoftDNS \_ Server describe un servidor DNS. Cada instancia de esta clase puede asociarse a una instancia de MicrosoftDNS Cache, una instancia de RootHints de MicrosoftDNS y varias instancias de \_ \_ MicrosoftDNS \_ Zone.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- MicrosoftDNS_Server dns de clase
- MicrosoftDNS_Server clase DNS , descrita
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
ms.openlocfilehash: 6c4a42432a11b5cde0df657ba2a9725a68d76a055fce3787bce56c10dfd227ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539275"
---
# <a name="microsoftdns_server-class"></a>Clase de servidor MicrosoftDNS \_

La **clase MicrosoftDNS \_ Server** describe un servidor DNS. Cada instancia de esta clase puede asociarse a una instancia de [**MicrosoftDNS \_ Cache**](microsoftdns-cache.md), una instancia de [**\_ RootHints de MicrosoftDNS**](microsoftdns-roothints.md)y varias instancias de La zona [**MicrosoftDNS \_**](microsoftdns-zone.md).

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase MicrosoftDNS \_ Server** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MicrosoftDNS \_ Server** tiene estos métodos.



| Método                   | Descripción                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **GetDistinguishedName** | Recupera el nombre distintivo dns de la zona.<br/>                        |
| **StartScavenging**      | Inicia la búsqueda de registros obsoletos en las zonas sometidas a scavenging.<br/> |
| **StartService**         | Inicia el servidor DNS.<br/>                                                |
| **StopService**          | Detiene el servidor DNS.<br/>                                                 |



 

### <a name="properties"></a>Propiedades

La **clase MicrosoftDNS \_ Server** tiene estas propiedades.

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Número máximo de registros de host devueltos en respuesta a una solicitud de dirección. Los valores entre 5 y 28 son válidos.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica si el servidor DNS acepta solicitudes de actualización dinámicas. Los valores válidos se muestran en la tabla siguiente.



| Valor                                                                                                | Significado                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Sin restricciones.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | No permite actualizaciones dinámicas de registros SOA.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | No permite actualizaciones dinámicas de registros NS en la raíz de la zona.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | No permite actualizaciones dinámicas de registros NS que no están en la raíz de la zona (registros NS de delegación).<br/> |



 

Sume estos valores para determinar el valor de configuración.

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS intenta actualizar sus entradas de caché mediante datos de servidores raíz. Cuando se inicia un servidor DNS, necesita una lista de NS de "sugerencias" del servidor raíz y registros A para los servidores denominados históricamente el archivo de caché. Los servidores DNS de Microsoft tienen una característica que les permite intentar volver a escribir un nuevo archivo de caché en función de las respuestas de los servidores raíz.

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica qué zonas principales estándar que son autoritativa para el nombre del servidor DNS debe actualizarse cuando cambie el servidor de nombres. Los valores válidos son los siguientes:



| Value                                                                                                | Significado                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Ninguno.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Solo los servidores que permiten actualizaciones dinámicas.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Solo los servidores que no permiten actualizaciones dinámicas.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Todos los servidores.<br/>                                    |



 

El valor predeterminado es 1.

**Windows Server 2003: **

El número 3 representa Todos los servidores.

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Determina el formato de mensaje AXFR al enviar a bases de datos secundarias que no son de Microsoft DNS Server. Cuando se establece en TRUE, el servidor DNS envía transferencias a bases de datos secundarias que no son de Microsoft DNS en formato sin comprimir. Cuando es FALSE, todas las transferencias se envían en el formato rápido.

</dd> <dt>

**BootMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Método de inicialización para el servidor DNS. En la siguiente tabla se muestran los valores válidos.



| Value                                                                                                | Significado                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Sin inicializar.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Arranque desde el archivo.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Arranque desde el Registro.<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Arranque desde el directorio y el registro.<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Valor **predeterminado scavengingInterval** establecido para todas las Active Directory integradas creadas en este servidor DNS. El valor predeterminado es cero, lo que indica que la búsqueda está deshabilitada.

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Intervalo de no actualización, en horas, establecido para todas las Active Directory integradas creadas en este servidor DNS. El valor predeterminado es 168 horas (siete días).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Intervalo de actualización, en horas, establecido para todas las Active Directory integradas creadas en este servidor DNS. El valor predeterminado es 168 horas (siete días).

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS crea automáticamente zonas de búsqueda inversa estándar.

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si se puede invalidar el enlace de puerto predeterminado para un socket usado para enviar consultas a servidores DNS remotos.

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si hay un DS disponible en el servidor DNS.

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Intervalo, en segundos, para sondear las zonas integradas en DS.

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Duración de los registros desenlazados en las zonas integradas del servicio de directorio, expresadas en segundos.

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Duración, en segundos, de la información almacenada en caché que describe la versión de EDNS compatible con otros servidores DNS.

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica si la compatibilidad con las particiones del directorio de la aplicación está habilitada en el servidor DNS.

**Windows Server 2003: **

Este método se denomina EnableDirectoryPartitionSupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica si el servidor DNS incluye RR específicos de DNSSEC, KEY, SIG y NXT en una respuesta, según la tabla siguiente:



| Valor                                                                                                | Significado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | No se incluyen registros DNSSEC en la respuesta a menos que la consulta solicite un conjunto de registros de recursos del tipo de registro DNSSEC.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Los registros DNSSEC se incluyen en la respuesta según RFC 2535.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Los registros DNSSEC se incluyen en una respuesta solo si la consulta de cliente original contenía el registro de recursos OPT según RFC 2671<br/> |



 

Si una consulta solicita un conjunto de registros de recursos del tipo DNSSEC, el servidor DNS siempre responde con dichos registros, si está disponible.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica el comportamiento del servidor DNS. Cuando es TRUE, el servidor DNS siempre responde con registros de recursos OPT según RFC 2671, a menos que el servidor remoto haya indicado que no admite EDNS en un intercambio anterior. Si es FALSE, el servidor DNS responde a las consultas con OTO solo si se envían OPT en la consulta original.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica qué eventos registra el servidor DNS en el Visor de eventos registro del sistema. Se usan los siguientes valores.



| Value                                                                                                | Significado                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Ninguno.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Errores de solo registro.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Registrar solo advertencias y errores.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Registre todos los eventos.<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica si se reenvía las consultas a subádes delegadas.

</dd> <dt>

**Reenviadores**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Enumera la lista de direcciones IP de reenviadores a las que el servidor DNS reenvía las consultas.

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tiempo, en segundos, un servidor DNS que reenvía una consulta esperará la resolución del reenviador antes de intentar resolver la propia consulta. [](f-gly.md)

Este valor no tiene sentido si el servidor de reenvío no está establecido para usar recursividad. Para determinarlo, compruebe la propiedad booleana IsVicee.

</dd> <dt>

**IsVicee**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

**TRUE** si el servidor DNS no usa recursión cuando se produce un error en la resolución de nombres a través de reenviadores.

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Enumera la lista de direcciones IP en las que el servidor DNS puede recibir consultas.

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS da prioridad a la dirección neta local al devolver los registros A.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tamaño del registro de depuración del servidor DNS, en bytes.

</dd> <dt>

**LogFilePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Nombre de archivo y ruta de acceso para el registro de depuración del servidor DNS. El valor predeterminado es %system32% \\ \\ dns dns.log. Las rutas de acceso relativas son relativas a %Systemroot% \\ System32. Se pueden usar rutas de acceso absolutas, pero no se admiten rutas de acceso UNC.

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Lista de direcciones IP usadas para filtrar los eventos DNS escritos en el registro de depuración.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica qué directivas se activan en el registro Visor de eventos sistema.

Debe establecerse en valores específicos basados en el algoritmo siguiente: a cada directiva (que se activará en el registro Visor de eventos sistema) se le asigna un valor específico.



| Valor                                                                                                                  | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Consulta.<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | Notificar.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Actualizar:<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Transacciones no consultadas.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Preguntas.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Respuestas.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Send.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Recibir.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | Udp.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Todos los paquetes.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | Transacción de escritura del servicio de directorio NT.<br/>  |
| <span id="131072"></span><dl> <dt>**131 072**</dt> </dl>         | Transacción de actualización del servicio de directorio NT.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Paquetes completos.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Escribir en .<br/>                           |



 

La suma de los valores correspondientes a todas las directivas que se activarán se indica en esta propiedad.

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS realiza caracteres comodín flexibles. Si no está definido o es cero, el servidor sigue el comportamiento de caracteres comodín especificado en la RFC de DNS. En este caso, se recomienda que un administrador incluya registros MX para todos los hosts que no pueden recibir correo. Si es distinto de cero, el servidor busca el nodo comodín más cercano; En este caso, un administrador debe colocar los registros MX en la raíz de la zona y en un nodo comodín (' \* ') directamente debajo de la raíz de zona. Además, los administradores deben colocar registros MX de referencia propia en los hosts que reciben su propio correo.

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

El tiempo máximo, en segundos, el registro de una consulta de nombre recursiva puede permanecer en la caché del servidor DNS. El servidor DNS elimina registros de la memoria caché cuando expira el valor de esta entrada, incluso si el valor del campo TTL del registro es mayor.

El valor predeterminado de esta propiedad es 86 400 segundos (1 día).

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

El tiempo máximo, en segundos, el resultado de un error de nombre de una consulta recursiva puede permanecer en la caché del servidor DNS. DNS elimina los registros de la memoria caché cuando este temporizador expira, incluso si el campo TTL es mayor. El valor predeterminado es 86 400 (un día).

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

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica el conjunto de caracteres aptos que se usarán en nombres DNS. Se usan los valores siguientes.



| Valor                                                                                                | Significado                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | RFC estricto (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | No RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Multibyte (UTF8)<br/>  |



 

**Windows Server 2003: **

Un valor de "2" indica "Cualquiera".

</dd> <dt>

**NoRecursion**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS realiza búsquedas recursivas. TRUE indica que no se realizan búsquedas recursivas.

</dd> <dt>

**RecursionRetry**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Segundos transcurridos antes de volver a intentar una búsqueda recursiva. Si la propiedad es indefinido o cero, los reintentos se realizan después de tres segundos. No se recomienda a los usuarios modificar esta propiedad. Hay ciertas situaciones en las que se debe cambiar la propiedad; un ejemplo es cuando el servidor DNS se pone en contacto con servidores remotos a través de un vínculo lento y el servidor DNS vuelve a intentarlo antes de recibir la respuesta del DNS remoto. En este caso, aumentar el tiempo de espera para que sea ligeramente mayor que el tiempo de respuesta observado desde el DNS remoto sería razonable.

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Segundos transcurridos antes de que el servidor DNS dé por hecho la consulta recursiva. Si la propiedad es indefinido o cero, el servidor DNS se da por hecho después de 15 segundos. En general, el tiempo de espera de 15 segundos es suficiente para permitir que cualquier respuesta pendiente vuelva al servidor DNS.

No se recomienda a los usuarios modificar esta propiedad. Un escenario en el que se debe cambiar la propiedad es cuando el servidor DNS se pone en contacto con servidores remotos a través de un vínculo lento y se observa que el servidor DNS rechaza las consultas (con ERROR DEL SERVIDOR) antes de recibir \_ respuestas.

Los solucionadores de cliente también reintenten las consultas, por lo que se requiere una investigación cuidadosa para determinar si las respuestas remotas están realmente asociadas a la consulta que se ha quedó el tiempo de espera. En este caso, aumentar el valor de tiempo de espera para que sea ligeramente mayor que el tiempo de respuesta observado desde el DNS remoto sería razonable.

</dd> <dt>

**RoundRobin**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS redondea varios registros A.

</dd> <dt>

**RpcProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Protocolo RPC o protocolos sobre los que se ejecuta RPC administrativo. El algoritmo siguiente se usa para asignar un valor específico:



| Valor                                                                                                | Significado                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Ninguno<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Canalizaciones con nombre<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Lpc<br/>         |



 

La suma de los valores indica los protocolos usados.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Intervalo, en horas, entre dos operaciones de búsqueda consecutivas realizadas por el servidor DNS. Cero indica que la búsqueda está deshabilitada. El valor predeterminado es 168 horas (siete días).

</dd> <dt>

**SecureResponses**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS guarda exclusivamente registros de nombres en el mismo subárbol que el servidor que los proporcionó.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Puerto en el que el servidor DNS envía consultas UDP a otros servidores. De forma predeterminada, el servidor DNS envía consultas en un socket enlazado al puerto DNS.

En determinadas situaciones, esta no es la mejor configuración. Un caso obvio es cuando un administrador bloquea el puerto DNS con un firewall para impedir el acceso externo al servidor DNS, pero quiere que el servidor pueda ponerse en contacto con servidores DNS de Internet para proporcionar resolución de nombres para los clientes internos. Otro caso es cuando el servidor DNS admite redes no unívocas (la propiedad **DisjointNets** establecida en TRUE identifica este escenario). En estos casos, al establecer la propiedad **SendOnNonDnsPort** en un valor distinto de cero, el servidor DNS se enlaza a un puerto arbitrario para enviarlo a servidores DNS remotos.

Si el **valor de SendOnNonDnsPort** es mayor que 1024, el servidor DNS se enlaza explícitamente al valor de puerto especificado. Esta opción de configuración es útil cuando un administrador necesita corregir el puerto de consulta DNS con fines de firewall.

**Windows Server 2003: **

Al establecer la propiedad SendPort en un valor distinto de cero, el servidor DNS se enlaza a un puerto arbitrario para enviarlo a servidores DNS remotos.

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Enumera la lista de direcciones IP del servidor DNS.

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el servidor DNS analiza los archivos de [*zona estrictamente.*](z-gly.md) Si no está definido o es cero, el servidor registrará y omitirá los datos no disponibles en el archivo de zona y seguirá cargando. Si es distinto de cero, el servidor registrará y producirá un error en los errores del archivo de zona.

</dd> <dt>

**UpdateOptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Restringe el tipo de registros que se pueden actualizar dinámicamente en el servidor, que se usa además de la configuración **allowUpdate** en los objetos Server y Zone.

**Windows Server 2003: **

0: Sin restricciones.

1: No permitir actualizaciones dinámicas de registros SOA.

2: No permitir actualizaciones dinámicas de registros NS en la raíz de la zona.

4: No permitir actualizaciones dinámicas de registros NS que no están en la raíz de la zona (registros NS de delegación).

Sume estos valores para determinar el valor de configuración.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Versión del servidor DNS.

</dd> <dt>

**WriteAuthorityNS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica si el servidor DNS escribe registros NS y SOA en la sección de autoridad sobre una respuesta correcta.

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tiempo, en segundos, el servidor DNS espera una conexión TCP correcta a un servidor remoto al intentar una transferencia de zona.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método StartService de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Método StopService de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método StartScavenging de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





