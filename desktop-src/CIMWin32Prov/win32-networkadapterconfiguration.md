---
description: Representa los atributos y comportamientos de un adaptador de red. Esta clase incluye propiedades y métodos adicionales que admiten la administración del protocolo TCP/IP que son independientes del adaptador de red.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153578"
---
# <a name="win32_networkadapterconfiguration-class"></a>Clase NetworkAdapterConfiguration de Win32 \_

La **clase WMI \_ NetworkAdapterConfiguration** [de](../wmisdk/retrieving-a-class.md) Win32 representa los atributos y comportamientos de un adaptador de red. Esta clase incluye propiedades y métodos adicionales que admiten la administración del protocolo TCP/IP que son independientes del adaptador de red.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a>Miembros

La **clase \_ NetworkAdapterConfiguration de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ NetworkAdapterConfiguration de Win32** tiene estos métodos.



| Método                                                                                                                       | Descripción                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Deshabilita IPsec en este adaptador de red habilitado para TCP/IP.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Habilita el Protocolo de configuración dinámica de host (DHCP) para el servicio con este adaptador de red.<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Habilita el Sistema de nombres de dominio (DNS) para el servicio en este adaptador de red enlazado a TCP/IP.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Habilita IPsec globalmente en todos los adaptadores de red enlazados a IP.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Habilita IPsec en este adaptador de red específico habilitado para TCP/IP.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Habilita el direccionamiento TCP/IP estático para el adaptador de red de destino.<br/>                                                                           |
| [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Habilita la configuración WINS específica de TCP/IP, pero independiente del adaptador de red.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Libera la dirección IP enlazada a un adaptador de red específico habilitado para DHCP.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Libera las direcciones IP enlazadas a todos los adaptadores de red habilitados para DHCP.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Renueva la dirección IP en adaptadores de red específicos habilitados para DHCP.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Renueva las direcciones IP en todos los adaptadores de red habilitados para DHCP.<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Establece la transmisión de consultas ARP por TCP/IP.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Permite que los paquetes Ethernet usen la codificación SNAP 802.3.<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Establece la ruta de acceso a los archivos de base de datos de Internet estándar (HOSTS, LMHOSTS, REDES y PROTOCOLOS).<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Habilita la detección de puerta de enlace fallcida.<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Obsoleto. Este método establece el valor predeterminado de Tipo de servicio (TOS) en el encabezado de los paquetes IP salientes.<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Establece el valor predeterminado De período de vida (TTL) en el encabezado de los paquetes IP salientes.<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Establece el dominio DNS.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Establece el orden de búsqueda del servidor como una matriz de elementos.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Establece el orden de búsqueda del sufijo como una matriz de elementos.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Indica el registro DNS dinámico de direcciones IP para este adaptador enlazado a IP.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Especifica cuánta dirección IP de memoria asigna para almacenar datos de paquetes en la cola de paquetes del enrutador.<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Especifica una lista de puertas de enlace para enrutar paquetes destinados a una subred diferente de la a la que está conectado este adaptador.<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Establece la medida en que el sistema admite la multidifusión IP y participa en el Protocolo de administración de grupos de Internet.<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Establece la métrica de enrutamiento asociada a este adaptador enlazado a IP.<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Establece el uso de difusión ip cero.<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Establece los pares de número de red y trama de intercambio de paquetes de trabajo por Internet (IPX) para este adaptador de red.<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Establece el número de red virtual de Internetworking Packet Exchange (IPX) en el sistema de equipo de destino.<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Establece el intervalo que separa las retransmisiones Keep Alive hasta que se recibe una respuesta.<br/>                                                      |
| [**SetKeepAliveTime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Establece la frecuencia con la que TCP intenta comprobar que una conexión inactiva sigue estando disponible mediante el envío de un paquete Keep Alive.<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Establece la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red.<br/> No se admite este método.<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Establece el número de encabezados de paquetes IP asignados para la cola de paquetes del enrutador.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Habilita la detección de enrutadores black hole.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Habilita la detección de unidad de transmisión máxima (MTU).<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Establece la operación predeterminada de NetBIOS a través de TCP/IP.<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Establece el número de intentos que TCP retransmitirá una solicitud de conexión antes de anularla.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Establece el número de veces que TCP retransmitirá un segmento de datos individual antes de anular la conexión.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Establece el número máximo de conexiones que TCP puede tener abiertas simultáneamente.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Especifica si TCP usa la especificación RFC 1122 para datos urgentes o el modo que usan los sistemas derivados de Berkeley Software Design (BSD).<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Establece el tamaño máximo de ventana de recepción TCP que ofrece el sistema.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Establece los servidores de Windows Internet Naming Service principal y secundario (WINS) en este adaptador de red enlazado a TCP/IP.<br/>                        |



 

### <a name="properties"></a>Propiedades

La **clase \_ NetworkAdapterConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ArpAlwaysSourceRoute")
</dt> </dl>

Si **es TRUE,** TCP/IP transmite consultas del Protocolo de resolución de direcciones (ARP) con enrutamiento de origen habilitado en redes de anillo de token. De forma predeterminada (FALSE), ARP primero consulta sin enrutamiento de origen y, a continuación, vuelve a in reintentos con el enrutamiento de origen habilitado si no se recibe ninguna respuesta. El enrutamiento de origen permite el enrutamiento de paquetes de red entre diferentes tipos de redes.

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ArpUseEtherSNAP")
</dt> </dl>

Si **es TRUE,** los paquetes Ethernet siguen la codificación IEEE 802.3 Sub-Network Access Protocol (SNAP). Establecer este parámetro en 1 fuerza a TCP/IP a transmitir paquetes Ethernet mediante la codificación SNAP 802.3. De forma predeterminada (FALSE), la pila transmite paquetes en formato DIX Ethernet.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DatabasePath")
</dt> </dl>

Ruta de acceso válida del archivo de Windows a los archivos de base de datos estándar de Internet (HOSTS, LMHOSTS, REDES y PROTOCOLOS). La interfaz de Windows Sockets usa la ruta de acceso del archivo.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnableDeadGWDetect")
</dt> </dl>

Si **es TRUE,** se produce la detección de puerta de enlace no activa. Con esta característica habilitada, el Protocolo de control de transmisión (TCP) pide a Protocolo de Internet (IP) que cambie a una puerta de enlace de copia de seguridad si retransmite un segmento varias veces sin recibir una respuesta.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| DefaultGateway")
</dt> </dl>

Matriz de direcciones IP de puertas de enlace predeterminadas que usa el sistema informático.

Ejemplo: "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DefaultTOS")
</dt> </dl>

Valor predeterminado del tipo de servicio (TOS) establecido en el encabezado de los paquetes IP salientes. Solicitud de comentarios (RFC) 791 define los valores. Valor predeterminado: 0 (cero), Intervalo válido: 0 - 255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DefaultTTL")
</dt> </dl>

Valor de período de vida (TTL) predeterminado establecido en el encabezado de los paquetes IP salientes. El TTL especifica el número de enrutadores que puede pasar un paquete IP para llegar a su destino antes de descartarse. Cada enrutador disminuye en uno el número de TTL de un paquete a medida que pasa y descarta los paquetes, si el TTL es 0 (cero). Valor predeterminado: 32, intervalo válido: 1 - 255.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

Si **es TRUE,** el servidor dhcp (protocolo de configuración dinámica de host) asigna automáticamente una dirección IP al sistema del equipo al establecer una conexión de red.

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")
</dt> </dl>

Fecha y hora de expiración de una dirección IP alquilada asignada al equipo por el servidor del Protocolo de configuración dinámica de host (DHCP).

Ejemplo: 20521201000230.000000000

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")
</dt> </dl>

Fecha y hora en que el servidor dhcp (protocolo de configuración dinámica de host) obtuvo la concesión para la dirección IP asignada al equipo.

Ejemplo: 19521201000230.000000000

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")
</dt> </dl>

Dirección IP del servidor de protocolo de configuración dinámica de host (DHCP).

Ejemplo: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Dominio de parámetros Tcpip de Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ \\ \\ \\ \\ \| Services")
</dt> </dl>

Nombre de la organización seguido de un punto y una extensión que indica el tipo de organización, como "microsoft.com". El nombre puede ser cualquier combinación de las letras A a Z, los números del 0 al 9 y el guion (-), además del carácter de punto (.) usado como separador.

Ejemplo: "microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| SearchList")
</dt> </dl>

Matriz de sufijos de dominio DNS que se anexarán al final de los nombres de host durante la resolución de nombres. Al intentar resolver un nombre de dominio completo (FQDN) a partir de un nombre de solo host, el sistema anexará primero el nombre de dominio local. Si esto no se realiza correctamente, el sistema usará la lista de sufijos de dominio para crear FQDN adicionales en el orden indicado y consultar los servidores DNS para cada uno.

Ejemplo: "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnableDNS")
</dt> </dl>

Si **es TRUE,** el Sistema de nombres de dominio (DNS) está habilitado para la resolución de nombres a través de Windows Internet Naming Service (WINS). Si el nombre no se puede resolver mediante DNS, la solicitud de nombre se reenvía a WINS para su resolución.

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| Hostname")
</dt> </dl>

Nombre de host usado para identificar el equipo local para la autenticación por parte de algunas utilidades. Otras utilidades basadas en TCP/IP pueden usar este valor para adquirir el nombre del equipo local. Los nombres de host se almacenan en servidores DNS en una tabla que asigna nombres a direcciones IP para su uso por PARTE de DNS. El nombre puede ser cualquier combinación de las letras A a Z, los números del 0 al 9 y el guion (-), además del carácter de punto (.) utilizado como separador. De forma predeterminada, este valor es el nombre del equipo de red de Microsoft, pero el administrador de red puede asignar otro nombre de host sin que ello afecte al nombre del equipo.

Ejemplo: "corpdns"

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| NameServer")
</dt> </dl>

Matriz de direcciones IP de servidor que se usará para consultar servidores DNS.

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** las direcciones IP de esta conexión se registran en DNS con el nombre de dominio de esta conexión, además de registrarse con el nombre DNS completo del equipo. El nombre de dominio de esta conexión se establece mediante el [**método SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() o se asigna mediante DSCP. El nombre registrado es el nombre de host del equipo con el nombre de dominio anexado.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Memoria asignada por IP para almacenar datos de paquetes en la cola de paquetes del enrutador. Cuando se rellena este espacio de búfer, el enrutador comienza a descartar paquetes aleatoriamente de su cola. Los búferes de datos de cola de paquetes tienen una longitud de 256 bytes, por lo que el valor de este parámetro debe ser un múltiplo de 256. Varios búferes están encadenados para paquetes más grandes. El encabezado IP de un paquete se almacena por separado. Este parámetro se omite y no se asignan búferes si el enrutador IP no está habilitado. El tamaño del búfer puede oscilar entre la MTU de red y un valor menor que 0xFFFFFFFF. Valor predeterminado: 74240 (paquetes de 1480 bytes, redondeados a un múltiplo de 256).

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** las direcciones IP de esta conexión se registran en DNS con el nombre DNS completo del equipo. El nombre DNS completo del equipo se muestra en la pestaña **Identificación de** red de la aplicación Sistema en Panel de control.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de valores de métrica de costo entero (comprendidos entre 1 y 9999) que se usarán para calcular las rutas más rápidas, más confiables o con menos recursos. Este argumento tiene una correspondencia uno a uno con la **propiedad DefaultIPGateway.**

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| IGMPLevel")
</dt> </dl>

Medida en la que el sistema admite la multidifusión IP y participa en el Protocolo de administración de grupos de Internet (IGMP). En el nivel 0 (cero), el sistema no proporciona compatibilidad con multidifusión. En el nivel 1, el sistema solo puede enviar paquetes de multidifusión IP. En el nivel 2, el sistema puede enviar paquetes de multidifusión IP y participar completamente en IGMP para recibir paquetes de multidifusión.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Sin multidifusión** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multidifusión IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**Ip & multidifusión IGMP** (2)


</dt> <dd>

Multidifusión IP y IGMP (valor predeterminado)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet Control Class \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Número de índice de la configuración del adaptador de red de Windows. El número de índice se usa cuando hay más de una configuración disponible.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de índice que identifica de forma única una interfaz de red local. El valor de esta propiedad es el mismo que el valor de la propiedad **InterfaceIndex** de la instancia de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa la interfaz de red en la tabla de rutas.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip \| IPAddress")
</dt> </dl>

Matriz de todas las direcciones IP asociadas al adaptador de red actual. Esta propiedad puede contener direcciones IPv6 o direcciones IPv4. Para obtener más información, vea [Compatibilidad con IPv6 e IPv4 en WMI.](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)

Dirección IPv6 de ejemplo: "2010:836B:4179::836B:4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Costo de usar las rutas configuradas para el adaptador enlazado a IP y es el valor ponderado de esas rutas en la tabla de enrutamiento IP. Si hay varias rutas a un destino en la tabla de enrutamiento IP, se usa la ruta con la métrica más baja. El valor predeterminado es 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip")
</dt> </dl>

Si **es TRUE,** TCP/IP está enlazado y habilitado en este adaptador de red.

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| IPFilterSecurityEnabled")
</dt> </dl>

Si **es TRUE,** la seguridad del puerto IP está habilitada globalmente en todos los adaptadores de red enlazados a IP y los valores de seguridad asociados a adaptadores de red individuales están en vigor. Esta propiedad se usa junto con **IPSecPermitTCPPorts,** **IPSecPermitUDPPorts** e **IPSecPermitIPProtocols**. Si **es FALSE,** la seguridad del filtro IP está deshabilitada en todos los adaptadores de red y permite que todo el tráfico de puerto y protocolo fluya sin filtrar.

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")
</dt> </dl>

Si **es TRUE,** la seguridad del puerto IP está habilitada globalmente en todos los adaptadores de red enlazados a IP. Esta propiedad ha quedado obsoleta. En lugar de esta propiedad, debe usar **IPFilterSecurityEnabled.**

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| RawIPAllowedProtocols")
</dt> </dl>

Matriz de los protocolos permitidos para ejecutarse a través de la dirección IP. La lista de protocolos se define mediante el [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) La lista estará vacía o contendrá valores numéricos. Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los protocolos. Una cadena vacía indica que no se permite ejecutar ningún protocolo **cuando IPFilterSecurityEnabled** es **TRUE.**

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TCPAllowedPorts")
</dt> </dl>

Matriz de los puertos a los que se concederá permiso de acceso para TCP. La lista de protocolos se define mediante el [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) La lista estará vacía o contendrá valores numéricos. Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos. Una cadena vacía indica que no se concede permiso de acceso a ningún puerto **cuando IPFilterSecurityEnabled** es **TRUE.**

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| UDPAllowedPorts")
</dt> </dl>

Matriz de los puertos a los que se concederá el permiso de acceso protocolo de datagramas de usuario (UDP). La lista de protocolos se define mediante el [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) La lista estará vacía o contendrá valores numéricos. Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos. Una cadena vacía indica que no se concede permiso de acceso a ningún puerto **cuando IPFilterSecurityEnabled** es **TRUE.**

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| SubnetMask")
</dt> </dl>

Matriz de todas las máscaras de subred asociadas al adaptador de red actual.

Ejemplo: "255.255.0.0"

</dd> <dt>

**IPUseZeroBroadcast**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| UseZeroBroadcast")
</dt> </dl>

Si **es TRUE,** se usan difusión de ceros ip (0.0.0.0) y el sistema usa difusión de uno (255.255.255.255). Los sistemas informáticos suelen usar difusión ones, pero los derivados de las implementaciones de BSD usan difusión de ceros. Los sistemas que no usan las mismas difusiones no interoperarán en la misma red. El valor predeterminado es **FALSE.**

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS")
</dt> </dl>

Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| PktType")
</dt> </dl>

Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet SNAP** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**AUTO** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| MediaType")
</dt> </dl>

Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Anillo de token** (2)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (3)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXNetworkNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| NetworkNumber")
</dt> </dl>

Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| VirtualNetworkNumber")
</dt> </dl>

Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Intervalo que separa las retransmisiones Keep Alive hasta que se recibe una respuesta. Después de recibir una respuesta, el retraso hasta la siguiente transmisión Keep Alive se controla de nuevo mediante el **valor de KeepAliveTime**. La conexión se anulará después de que el número de retransmisiones especificadas por **TcpMaxDataRetransmissions** haya quedo sin respuesta. Valor predeterminado: 1000, intervalo válido: 1 - 0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

La **propiedad KeepAliveTime** indica la frecuencia con la que el TCP intenta comprobar que una conexión inactiva sigue intacta mediante el envío de un paquete Keep Alive. Un sistema remoto al que se pueda acceder confirmará la transmisión keep alive. Los paquetes Keep Alive no se envían de forma predeterminada. Una aplicación puede habilitar esta característica en una conexión. Valor predeterminado: 7 200 000 (dos horas).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de entrada y salida del dispositivo Win32API \| \| DeviceIoControl")
</dt> </dl>

Dirección Access Control (MAC) del adaptador de red. El fabricante asigna una dirección MAC para identificar de forma única el adaptador de red.

Ejemplo: "00:80:C7:8F:6C:96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Invalida la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red. La MTU es el tamaño máximo de paquete (incluido el encabezado de transporte) que el transporte transmitirá a través de la red subyacente. El datagrama IP puede abarcar varios paquetes. El intervalo de este valor abarca el tamaño mínimo de paquete (68) a la MTU compatible con la red subyacente.

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| NumForwardPackets")
</dt> </dl>

Número de encabezados de paquetes IP asignados para la cola de paquetes del enrutador. Cuando todos los encabezados están en uso, el enrutador empezará a descartar paquetes de la cola de forma aleatoria. Este valor debe ser al menos tan grande como el valor **ForwardBufferMemory** dividido por el tamaño máximo de datos IP de las redes conectadas al enrutador. No debe ser mayor que el valor **ForwardBufferMemory** dividido entre 256, ya que se usan al menos 256 bytes de memoria de búfer de reenvío para cada paquete. El número óptimo de paquetes de reenvío para un tamaño **ForwardBufferMemory** determinado depende del tipo de tráfico en la red. Estará en algún lugar entre estos dos valores. Si el enrutador no está habilitado, este parámetro se omite y no se asignan encabezados. Valor predeterminado: 50, intervalo válido: 1 - 0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnablePMTUBHDetect")
</dt> </dl>

Si **es TRUE,** se produce la detección de enrutadores de huecos negros mientras TCP detecta la ruta de acceso de la unidad de transmisión máxima. Un enrutador de hueco negro no devuelve mensajes de destino icmp inaccesibles cuando necesita fragmentar un datagrama IP con el conjunto de bits No fragmentar. TCP depende de la recepción de estos mensajes para realizar la detección de MTU de ruta de acceso. Con esta característica habilitada, TCP intentará enviar segmentos sin el conjunto de bits No fragmentar si varias retransmisiones de un segmento no se reconocen. Si el segmento se confirma como resultado, el MSS se disminuirá y el bit No fragmentar se establecerá en paquetes futuros en la conexión. La habilitación de la detección de huecos negros aumenta el número máximo de retransmisiones realizadas para un segmento determinado. El valor predeterminado de esta propiedad es **FALSE.**

</dd> <dt>

**PMTUDiscoveryEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnablePMTUDiscovery")
</dt> </dl>

Si **es TRUE,** la ruta de acceso de la unidad de transmisión máxima (MTU) se detecta a través de la ruta de acceso a un host remoto. Al detectar la ruta de acceso de MTU y limitar los segmentos TCP a este tamaño, TCP puede eliminar la fragmentación en los enrutadores a lo largo de la ruta de acceso que conectan redes con diferentes MTU. La fragmentación afecta negativamente al rendimiento tcp y a la congestión de la red. Establecer este parámetro en **FALSE hace** que se utilice un MTU de 576 bytes para todas las conexiones que no están en las máquinas de la subred local. El valor predeterminado es **TRUE.**

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nombre de servicio del adaptador de red. Este nombre suele ser más corto que el nombre completo del producto.

Ejemplo: "Elnkii"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mapa de bits de la posible configuración relacionada con NetBIOS a través de TCP/IP. Los valores se identifican en la lista siguiente.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**EnableNetbiosViaDhcp** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**EnableNetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**TcpMaxConnectRetransmissions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpMaxConnectRetransmissions")
</dt> </dl>

Número de veces que TCP intenta retransmitir una solicitud de conexión antes de finalizar la conexión. El tiempo de espera de retransmisión inicial es de 3 segundos. El tiempo de espera de retransmisión se duplica para cada intento. Valor predeterminado: 3, Intervalo válido: 0 - 0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpMaxDataRetransmissions")
</dt> </dl>

Número de veces que TCP retransmite un segmento de datos individual (segmento que no es de conexión) antes de finalizar la conexión. El tiempo de espera de retransmisión se duplica con cada retransmisión sucesiva en una conexión. Valor predeterminado: 5, Intervalo válido: 0 - 0xFFFFFFFF.

</dd> <dt>

**TcpNumConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpNumConnections")
</dt> </dl>

Número máximo de conexiones que TCP puede tener abiertas simultáneamente. Valor predeterminado: 0xFFFFFE, Intervalo válido: 0 - 0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpUseRFC1122UrgentPointer")
</dt> </dl>

Si **es TRUE,** TCP usa la especificación RFC 1122 para los datos urgentes. Si **es FALSE** (valor predeterminado), TCP usa el modo que usan los sistemas derivados de Berkeley Software Design (BSD). Los dos mecanismos interpretan el puntero urgente de manera diferente y no son interoperables. El valor predeterminado es **FALSE**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño máximo de ventana de recepción TCP ofrecido por el sistema. La ventana de recepción especifica el número de bytes que un remitente puede transmitir sin recibir una confirmación. En general, las ventanas receptoras más grandes mejorarán el rendimiento a través de redes de alto retraso y ancho de banda alto. Para mejorar la eficacia, la ventana de recepción debe ser un múltiplo par del tamaño máximo de segmento (MSS) de TCP. Valor predeterminado: cuatro veces el tamaño máximo de los datos TCP o incluso un múltiplo de tamaño de datos TCP redondeado al múltiplo más cercano de 8192. El valor predeterminado de las redes Ethernet es 8760. Intervalo válido: 0 - 65535.

> [!Note]  
> Windows Vista: esta propiedad tiene acceso a la entrada `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` del Registro, que no se usa en la implementación actual del sistema operativo.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnableLMHOSTS")
</dt> </dl>

Si **es TRUE,** se usan archivos de búsqueda local. Los archivos de búsqueda contendrán una asignación de direcciones IP a nombres de host. Si existen en el sistema local, se encontrarán en %SystemRoot% \\ system32 \\ drivers \\ etc.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)drivers etc \| \\ \\ \\ \\ \\ \\ lmhosts")
</dt> </dl>

Ruta de acceso a un archivo de búsqueda WINS en el sistema local. Este archivo contendrá una asignación de direcciones IP a nombres de host. Si se encuentra el archivo especificado en esta propiedad, se copiará en la carpeta %SystemRoot% \\ system32 \\ drivers etc del sistema \\ local. Solo es válido si **la propiedad WINSEnableLMHostsLookup** es **TRUE.**

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de entrada y salida del dispositivo Win32API \| \| DeviceIoControl")
</dt> </dl>

Dirección IP del servidor WINS principal.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ScopeID")
</dt> </dl>

Valor anexado al final del nombre NetBIOS que aísla un grupo de sistemas informáticos que se comunican entre sí. Se usa para todas las transacciones NetBIOS a través de comunicaciones TCP/IP desde ese sistema informático. Los equipos configurados con identificadores de ámbito idénticos pueden comunicarse con este equipo. Los clientes TCP/IP con identificadores de ámbito diferentes no tienen en cuenta los paquetes de los equipos con este identificador de ámbito. Válido solo cuando [**el método EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) se ejecuta correctamente.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de entrada y salida del dispositivo Win32API \| \| DeviceIoControl")
</dt> </dl>

Dirección IP del servidor WINS secundario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ NetworkAdapterConfiguration de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

## <a name="examples"></a>Ejemplos

El [ejemplo de](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) código VBScript del recuperador de información de WMI en la Galería de TechNet usa la clase **\_ NetworkAdapterConfiguration de Win32** para recuperar información de configuración de red de varios equipos remotos.

El ejemplo de PowerShell [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) en la Galería de TechNet usa una serie de llamadas a hardware y software, incluido **\_ Win32 NetworkAdapterConfiguration**, para mostrar información sobre un sistema local o remoto.

El siguiente código de PowerShell recupera las opciones de configuración del adaptador de ISTAP de Microsoft.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



En el ejemplo de C \# siguiente se recupera la descripción y el número de índice de todas las instancias de configuración del adaptador de red. Tenga en cuenta que en este ejemplo de C se usa el espacio de nombres \# [Microsoft.Management.Infrastructure,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) que generalmente se escala de forma más eficaz que las clases WMI del espacio de nombres [System.Management.](/dotnet/api/system.management)


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



En el ejemplo de C \# siguiente se recupera la descripción y el número de índice de todas las instancias de configuración del adaptador de red. Tenga en cuenta que en este ejemplo de C se usa el espacio de nombres \# [System.Management](/dotnet/api/system.management) original, supercedido por [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



En el ejemplo siguiente se recupera información de la **clase \_ NetworkAdapterConfiguration de Win32.**


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Tareas wmi: redes](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Tareas wmi: cuentas y dominios](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[Compatibilidad con IPv6 e IPv4 en WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
