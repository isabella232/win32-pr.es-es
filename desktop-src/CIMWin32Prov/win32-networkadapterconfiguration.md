---
description: Representa los atributos y los comportamientos de un adaptador de red. Esta clase incluye propiedades y métodos adicionales que admiten la administración del protocolo TCP/IP que son independientes del adaptador de red.
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
ms.openlocfilehash: 2bccbe7fc44e75c2448d2eda800fe3c14cd13a9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153422"
---
# <a name="win32_networkadapterconfiguration-class"></a>\_Clase Win32 NetworkAdapterConfiguration

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapterConfiguration de Win32** representa los atributos y los comportamientos de un adaptador de red. Esta clase incluye propiedades y métodos adicionales que admiten la administración del protocolo TCP/IP que son independientes del adaptador de red.

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

La clase **Win32 \_ NetworkAdapterConfiguration** tiene estos métodos.



| Método                                                                                                                       | Descripción                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Deshabilita IPsec en este adaptador de red habilitado para TCP/IP.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Habilita el protocolo de configuración dinámica de host (DHCP) para el servicio con este adaptador de red.<br/>                                              |
| [**Habilitadas**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Habilita el sistema de nombres de dominio (DNS) para el servicio en este adaptador de red enlazado a TCP/IP.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Habilita IPsec globalmente en todos los adaptadores de red enlazados a IP.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Habilita IPsec en este adaptador de red específico habilitado para TCP/IP.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Habilita el direccionamiento TCP/IP estático para el adaptador de red de destino.<br/>                                                                           |
| [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Habilita la configuración de WINS específica de TCP/IP, pero independiente del adaptador de red.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Libera la dirección IP enlazada a un adaptador de red habilitado para DHCP específico.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Libera las direcciones IP enlazadas a todos los adaptadores de red habilitados para DHCP.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Renueva la dirección IP en determinados adaptadores de red habilitados para DHCP.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Renueva las direcciones IP en todos los adaptadores de red habilitados para DHCP.<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Establece la transmisión de consultas ARP por TCP/IP.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Permite a los paquetes Ethernet usar la codificación de ajuste 802,3.<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Establece la ruta de acceso a los archivos de base de datos de Internet estándar (hosts, LMHOSTs, redes y protocolos).<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Habilita la detección de puerta de enlace inactiva.<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Obsoleto. Este método establece el valor predeterminado del tipo de servicio (TOS) en el encabezado de los paquetes IP salientes.<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Establece el valor de período de vida (TTL) predeterminado en el encabezado de los paquetes IP salientes.<br/>                                                            |
| [**Método SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Establece el dominio DNS.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Establece el orden de búsqueda del servidor como una matriz de elementos.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Establece el orden de búsqueda de sufijos como una matriz de elementos.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Indica el registro DNS dinámico de las direcciones IP para este adaptador de enlace de IP.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Especifica la cantidad de memoria IP asignada para almacenar los datos de paquetes en la cola de paquetes del enrutador.<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Especifica una lista de puertas de enlace para enrutar paquetes destinados a una subred diferente a la que está conectada a este adaptador.<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Establece la medida en la que el sistema admite la multidifusión IP y participa en el protocolo de administración de grupos de Internet.<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Establece la métrica de enrutamiento asociada a este adaptador de enlace de IP.<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Establece el uso de difusión IP cero.<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Establece pares de tramas/número de red IPX (intercambio de paquetes de interredes) para este adaptador de red.<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Establece el número de red virtual de intercambio de paquetes de interredes (IPX) en el sistema del equipo de destino.<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Establece el intervalo de separación de las retransmisiones Keep Alive hasta que se reciba una respuesta.<br/>                                                      |
| [**SetKeepAliveTime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Establece la frecuencia con la que TCP intenta comprobar que una conexión inactiva sigue estando disponible mediante el envío de un paquete de mantenimiento de conexión.<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Establece la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red.<br/> No se admite este método.<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Establece el número de encabezados de paquetes IP asignados a la cola de paquetes del enrutador.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Habilita la detección de enrutadores de agujero negro.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Habilita la detección de la unidad de transmisión máxima (MTU).<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Establece la operación predeterminada de NetBIOS a través de TCP/IP.<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Establece el número de intentos que TCP retransmitirá una solicitud de conexión antes de anularse.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Establece el número de veces que TCP retransmitirá un segmento de datos individual antes de anular la conexión.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Establece el número máximo de conexiones que TCP puede haber abierto simultáneamente.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Especifica si TCP usa la especificación RFC 1122 para datos urgentes o el modo utilizado por los sistemas derivados del diseño de software Berkeley (BSD).<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Establece el tamaño máximo de la ventana de recepción de TCP ofrecido por el sistema.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Establece los servidores de Windows Internet Naming Service (WINS) principales y secundarios en este adaptador de red enlazado a TCP/IP.<br/>                        |



 

### <a name="properties"></a>Propiedades

La **clase \_ NetworkAdapterConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ArpAlwaysSourceRoute")
</dt> </dl>

Si **es true**, TCP/IP transmite las consultas del Protocolo de resolución de direcciones (ARP) con enrutamiento de origen habilitado en redes de token ring. De forma predeterminada (FALSE), ARP primero realiza consultas sin enrutamiento de origen y, a continuación, vuelve a intentarlo con el enrutamiento de origen habilitado si no se recibe ninguna respuesta. El enrutamiento de origen permite el enrutamiento de paquetes de red entre diferentes tipos de redes.

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ArpUseEtherSNAP")
</dt> </dl>

Si **es true**, los paquetes Ethernet siguen la codificación de protocolo de acceso Sub-Network (ajuste) IEEE 802,3. Al establecer este parámetro en 1 se fuerza a TCP/IP a transmitir paquetes Ethernet mediante la codificación de ajuste 802,3. De forma predeterminada (FALSE), la pila transmite los paquetes en formato DIX Ethernet.

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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DatabasePath")
</dt> </dl>

Ruta de acceso de archivo de Windows válida a los archivos de base de datos de Internet estándar (hosts, LMHOSTs, redes y protocolos). La interfaz de Windows Sockets usa la ruta de acceso del archivo.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableDeadGWDetect")
</dt> </dl>

Si **es true**, se produce una detección de puerta de enlace inactiva. Con esta característica habilitada, el protocolo de control de transmisión (TCP) solicita al Protocolo de Internet (IP) que cambie a una puerta de enlace de reserva si vuelve a transmitir un segmento varias veces sin recibir una respuesta.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| DefaultGateway")
</dt> </dl>

Matriz de direcciones IP de las puertas de enlace predeterminadas que usa el sistema del equipo.

Ejemplo: "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DefaultTOS")
</dt> </dl>

Valor predeterminado del tipo de servicio (TOS) establecido en el encabezado de los paquetes IP salientes. La solicitud de comentarios (RFC) 791 define los valores. Valor predeterminado: 0 (cero), intervalo válido: 0-255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DefaultTTL")
</dt> </dl>

Valor de período de vida (TTL) predeterminado establecido en el encabezado de los paquetes IP salientes. El TTL especifica el número de enrutadores que puede atravesar un paquete IP para llegar a su destino antes de que se descarte. Cada enrutador disminuye en uno el recuento de TTL de un paquete mientras pasa y descarta los paquetes, si el TTL es 0 (cero). Valor predeterminado: 32, intervalo válido: 1-255.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

Si **es true**, el servidor de protocolo de configuración dinámica de host (DHCP) asigna automáticamente una dirección IP al sistema del equipo al establecer una conexión de red.

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")
</dt> </dl>

Fecha y hora de expiración de una dirección IP concedida asignada al equipo por el servidor de protocolo de configuración dinámica de host (DHCP).

Ejemplo: 20521201000230,000000000

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")
</dt> </dl>

Fecha y hora en que se obtuvo la concesión de la dirección IP asignada al equipo por el servidor de protocolo de configuración dinámica de host (DHCP).

Ejemplo: 19521201000230,000000000

</dd> <dt>

**DHCP**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")
</dt> </dl>

Dirección IP del servidor del Protocolo de configuración dinámica de host (DHCP).

Ejemplo: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| Domain")
</dt> </dl>

Nombre de la organización seguido de un punto y una extensión que indica el tipo de organización, como "microsoft.com". El nombre puede ser cualquier combinación de las letras de la a a la Z, los números del 0 al 9 y el guión (-), más el carácter de punto (.) que se usa como separador.

Ejemplo: "microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| SearchList")
</dt> </dl>

Matriz de sufijos de dominio DNS que se van a anexar al final de los nombres de host durante la resolución de nombres. Al intentar resolver un nombre de dominio completo (FQDN) de un nombre de host único, el sistema anexará primero el nombre de dominio local. Si no se realiza correctamente, el sistema utilizará la lista de sufijos de dominio para crear FQDN adicionales en el orden enumerado y consultar los servidores DNS para cada uno.

Ejemplo: "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableDns")
</dt> </dl>

Si es **true**, el sistema de nombres de dominio (DNS) está habilitado para la resolución de nombres a través de la resolución de Windows Internet Naming Service (WINS). Si el nombre no se puede resolver con DNS, la solicitud de nombre se reenvía a WINS para su resolución.

</dd> <dt>

**ServicePrincipalName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| hostname")
</dt> </dl>

Nombre de host usado para identificar el equipo local para la autenticación por parte de algunas utilidades. Otras utilidades basadas en TCP/IP pueden usar este valor para adquirir el nombre del equipo local. Los nombres de host se almacenan en servidores DNS en una tabla que asigna nombres a direcciones IP para su uso por DNS. El nombre puede ser cualquier combinación de las letras de la a a la Z, los números del 0 al 9 y el guión (-), más el carácter de punto (.) que se usa como separador. De forma predeterminada, este valor es el nombre del equipo de redes de Microsoft, pero el administrador de red puede asignar otro nombre de host sin que ello afecte al nombre del equipo.

Ejemplo: "corpdns"

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| nameserver")
</dt> </dl>

Matriz de direcciones IP de servidor que se va a usar en la consulta de servidores DNS.

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, las direcciones IP de esta conexión se registran en DNS bajo el nombre de dominio de esta conexión, además de registrarse con el nombre DNS completo del equipo. El nombre de dominio de esta conexión se establece mediante el método [**método SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() o se asigna mediante DSCP. El nombre registrado es el nombre de host del equipo con el nombre de dominio anexado.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ForwardBufferMemory"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Memoria asignada por IP para almacenar los datos de paquetes en la cola de paquetes del enrutador. Cuando se rellena este espacio de búfer, el enrutador comienza a descartar los paquetes de forma aleatoria de su cola. Los búferes de datos de cola de paquetes tienen una longitud de 256 bytes, por lo que el valor de este parámetro debe ser un múltiplo de 256. Varios búferes están encadenados juntos para paquetes más grandes. El encabezado IP de un paquete se almacena por separado. Este parámetro se omite y no se asigna ningún búfer si el enrutador IP no está habilitado. El tamaño del búfer puede oscilar entre la MTU de red y un valor menor que 0xFFFFFFFF. Valor predeterminado: 74240 (paquetes de 50 1480 bytes, redondeado a un múltiplo de 256).

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, las direcciones IP de esta conexión se registran en DNS con el nombre DNS completo del equipo. El nombre DNS completo del equipo se muestra en la pestaña **identificación de red** en la aplicación sistema en el panel de control.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de valores de métrica de costo de entero (entre 1 y 9999) que se va a usar para calcular la ruta más rápida, más confiable o que consume menos recursos. Este argumento tiene una correspondencia uno a uno con la propiedad **DefaultIPGateway** .

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| IGMPLevel")
</dt> </dl>

Grado en el que el sistema admite la multidifusión IP y participa en el protocolo de administración de grupos de Internet (IGMP). En el nivel 0 (cero), el sistema no proporciona compatibilidad con multidifusión. En el nivel 1, el sistema solo puede enviar paquetes de multidifusión IP. En el nivel 2, el sistema puede enviar paquetes de multidifusión IP y participar por completo en IGMP para recibir paquetes de multidifusión.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Sin multidifusión** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multidifusión IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & multidifusión IGMP** (2)


</dt> <dd>

IP y multidifusión IGMP (valor predeterminado)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Número de índice de la configuración del adaptador de red de Windows. El número de índice se utiliza cuando hay más de una configuración disponible.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de índice que identifica de forma única una interfaz de red local. El valor de esta propiedad es el mismo que el valor de la propiedad **InterfaceIndex** de la instancia de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa la interfaz de red en la tabla de rutas.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ TCPIP \| IPAddress")
</dt> </dl>

Matriz de todas las direcciones IP asociadas al adaptador de red actual. Esta propiedad puede contener direcciones IPv6 o direcciones IPv4. Para obtener más información, consulte [compatibilidad con IPv6 e IPv4 en WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

Dirección IPv6 de ejemplo: "2010:836B: 4179:: 836B: 4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Costo de usar las rutas configuradas para el adaptador de enlace IP y es el valor ponderado de las rutas de la tabla de enrutamiento IP. Si hay varias rutas a un destino en la tabla de enrutamiento IP, se usa la ruta con la métrica más baja. El valor predeterminado es 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ TCPIP")
</dt> </dl>

Si es **true**, TCP/IP está enlazado y habilitado en este adaptador de red.

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| IPFilterSecurityEnabled")
</dt> </dl>

Si es **true**, la seguridad del puerto IP se habilita globalmente en todos los adaptadores de red enlazados a IP y los valores de seguridad asociados a los adaptadores de red individuales están en vigor. Esta propiedad se usa junto con **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts** y **IPSecPermitIPProtocols**. Si es **false**, la seguridad del filtro IP está deshabilitada en todos los adaptadores de red y permite que todo el tráfico de puertos y protocolos fluya sin filtrar.

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")
</dt> </dl>

Si es **true**, la seguridad del puerto IP está habilitada globalmente en todos los adaptadores de red enlazados a IP. Esta propiedad ha quedado obsoleta. En lugar de esta propiedad, debe utilizar **IPFilterSecurityEnabled**.

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| RawIPAllowedProtocols")
</dt> </dl>

Matriz de los protocolos que se pueden ejecutar a través de la dirección IP. La lista de protocolos se define mediante el método [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . La lista estará vacía o contendrá valores numéricos. Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los protocolos. Una cadena vacía indica que no se permite la ejecución de ningún protocolo cuando **IPFilterSecurityEnabled** es **true**.

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TCPAllowedPorts")
</dt> </dl>

Matriz de los puertos a los que se va a conceder el permiso de acceso para TCP. La lista de protocolos se define mediante el método [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . La lista estará vacía o contendrá valores numéricos. Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos. Una cadena vacía indica que no se concede permiso de acceso a ningún puerto cuando **IPFilterSecurityEnabled** es **true**.

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| UDPAllowedPorts")
</dt> </dl>

Matriz de los puertos a los que se concederá el permiso de acceso UDP (Protocolo de datagramas de usuario). La lista de protocolos se define mediante el método [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . La lista estará vacía o contendrá valores numéricos. Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos. Una cadena vacía indica que no se concede permiso de acceso a ningún puerto cuando **IPFilterSecurityEnabled** es **true**.

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| máscaradesubred")
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

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| UseZeroBroadcast")
</dt> </dl>

Si **es true**, se usan difusiones de ceros IP (0.0.0.0) y el sistema usa difusiones de (255.255.255.255). Normalmente, los sistemas informáticos usan difusiones, pero las que se derivan de las implementaciones de BSD usan difusiones de ceros. Los sistemas que no usan esa misma difusión no interoperarán en la misma red. El valor predeterminado es **false**.

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusado**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Windows Sockets versión 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| \_ Dirección IPX")
</dt> </dl>

Ya no se admite la tecnología de intercambio de paquetes de red (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Ya no se admite la tecnología de intercambio de paquetes de red (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| PktType")
</dt> </dl>

Ya no se admite la tecnología de intercambio de paquetes de red (IPX) y esta propiedad no contiene datos útiles.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ajuste Ethernet** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Auto** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusado**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| mediatype")
</dt> </dl>

Ya no se admite la tecnología de intercambio de paquetes de red (IPX) y esta propiedad no contiene datos útiles.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token ring** (2)


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

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| NetworkNumber")
</dt> </dl>

Ya no se admite la tecnología de intercambio de paquetes de red (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| VirtualNetworkNumber")
</dt> </dl>

Ya no se admite la tecnología de intercambio de paquetes de red (IPX) y esta propiedad no contiene datos útiles.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| KeepAliveInterval"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")
</dt> </dl>

Intervalo que separa las retransmisiones de mantenimiento de conexión hasta que se reciba una respuesta. Después de recibir una respuesta, el retraso hasta la siguiente transmisión de mantenimiento de conexión vuelve a controlarse mediante el valor de **KeepAliveTime**. La conexión se anulará después de que el número de retransmisiones especificado por **TcpMaxDataRetransmissions** haya dejado de responder. Valor predeterminado: 1000, intervalo válido: 1-0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| KeepAliveInterval"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milisegundos")
</dt> </dl>

La propiedad **KeepAliveTime** indica la frecuencia con la que TCP intenta comprobar que una conexión inactiva sigue intacta mediante el envío de un paquete Keep Alive. Un sistema remoto que sea accesible confirmará la transmisión de mantenimiento de conexión. Los paquetes Keep Alive no se envían de forma predeterminada. Esta característica puede estar habilitada en una conexión por parte de una aplicación. Valor predeterminado: 7,2 millones (dos horas).

</dd> <dt>

**Mac**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device INPUT and Output Functions \| DeviceIoControl")
</dt> </dl>

Dirección de Access Control de medios (MAC) del adaptador de red. El fabricante asigna una dirección MAC para identificar de forma única el adaptador de red.

Ejemplo: "00:80: C7:8F: 6C: 96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| MTU"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Invalida la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red. La MTU es el tamaño de paquete máximo (incluido el encabezado de transporte) que el transporte transmitirá a través de la red subyacente. El datagrama IP puede abarcar varios paquetes. El intervalo de este valor abarca el tamaño de paquete mínimo (68) a la MTU compatible con la red subyacente.

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| NumForwardPackets")
</dt> </dl>

Número de encabezados de paquetes IP asignados a la cola de paquetes de enrutadores. Cuando todos los encabezados están en uso, el enrutador comenzará a descartar los paquetes de la cola de forma aleatoria. Este valor debe ser al menos tan grande como el valor de **ForwardBufferMemory** dividido por el tamaño de datos IP máximo de las redes conectadas al enrutador. No debe ser mayor que el valor de **ForwardBufferMemory** dividido por 256, ya que se usan al menos 256 bytes de memoria de búfer de reenvío para cada paquete. El número óptimo de paquetes reenviados para un tamaño de **ForwardBufferMemory** determinado depende del tipo de tráfico de la red. Estará en alguna parte entre estos dos valores. Si el enrutador no está habilitado, este parámetro se omite y no se asigna ningún encabezado. Valor predeterminado: 50, intervalo válido: 1-0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnablePMTUBHDetect")
</dt> </dl>

Si **es true**, la detección de enrutadores de agujeros negros se produce mientras TCP detecta la ruta de acceso de la unidad de transmisión máxima. Un enrutador de agujeros negros no devuelve mensajes de destino ICMP inalcanzables cuando necesita fragmentar un datagrama IP con el bit de no fragmentación establecido. TCP depende de la recepción de estos mensajes para realizar la detección de MTU de ruta de acceso. Con esta característica habilitada, TCP intentará enviar segmentos sin el bit de no fragmentación establecido si varias retransmisiones de un segmento van a no confirmarse. Si el segmento se confirma como resultado, se reducirá el MSS y el bit no fragmentar se establecerá en los paquetes futuros de la conexión. La habilitación de la detección de agujeros negros aumenta el número máximo de retransmisiones realizadas para un segmento determinado. El valor predeterminado de esta propiedad es **false**.

</dd> <dt>

**PMTUDiscoveryEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnablePMTUDiscovery")
</dt> </dl>

Si es **true**, la ruta de acceso de la unidad de transmisión máxima (MTU) se detecta a través de la ruta de acceso a un host remoto. Al detectar la ruta de acceso de MTU y limitar los segmentos TCP a este tamaño, TCP puede eliminar la fragmentación en los enrutadores a lo largo de la ruta de acceso que conecta las redes con diferentes MTU. La fragmentación afecta negativamente al rendimiento TCP y a la congestión de la red. Si se establece este parámetro en **false** , se usará una MTU de 576 bytes para todas las conexiones que no sean equipos de la subred local. El valor predeterminado es **true**.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nombre del servicio del adaptador de red. Este nombre suele ser más corto que el nombre completo del producto.

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

Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mapa de bits de la posible configuración relacionada con NetBIOS a través de TCP/IP. Los valores se identifican en la lista siguiente.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**EnableNetbiosViaDhcp** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**Parámetro enablenetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**TcpMaxConnectRetransmissions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpMaxConnectRetransmissions")
</dt> </dl>

Número de veces que TCP intenta retransmitir una solicitud de conexión antes de finalizar la conexión. El tiempo de espera de la retransmisión inicial es de 3 segundos. El tiempo de espera de retransmisión se duplica para cada intento. Valor predeterminado: 3, intervalo válido: 0-0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpMaxDataRetransmissions")
</dt> </dl>

Número de veces que TCP retransmite un segmento de datos individual (segmento sin conexión) antes de finalizar la conexión. El tiempo de espera de la retransmisión se duplica con cada retransmisión sucesiva en una conexión. Valor predeterminado: 5, intervalo válido: 0-0xFFFFFFFF.

</dd> <dt>

**TcpNumConnections**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpNumConnections")
</dt> </dl>

Número máximo de conexiones que TCP puede tener abiertas simultáneamente. Valor predeterminado: 0xFFFFFE, intervalo válido: 0-0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")
</dt> </dl>

Si **es true**, TCP utiliza la especificación RFC 1122 para datos urgentes. Si **es false** (valor predeterminado), TCP utiliza el modo utilizado por los sistemas derivados del diseño de software Berkeley (BSD). Los dos mecanismos interpretan el puntero urgente de manera diferente y no son interoperables. El valor predeterminado es **FALSE**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpWindowSize"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño máximo de la ventana de recepción de TCP ofrecido por el sistema. La ventana de recepción especifica el número de bytes que un remitente puede transmitir sin recibir una confirmación. En general, las ventanas de recepción más grandes mejorarán el rendimiento en redes de gran retraso y ancho de banda alto. Por motivos de eficacia, la ventana receptora debe ser un múltiplo par del tamaño máximo de segmento (MSS) de TCP. Valor predeterminado: cuatro veces el tamaño máximo de datos TCP o un múltiplo par de tamaño de datos TCP redondeado al múltiplo más próximo de 8192. Las redes Ethernet tienen como valor predeterminado 8760. Intervalo válido: 0-65535.

> [!Note]  
> Windows Vista: esta propiedad tiene acceso a la `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrada del registro, que no se usa en la implementación actual del sistema operativo.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableLMHOSTS")
</dt> </dl>

Si **es true**, se usan los archivos de búsqueda local. Los archivos de búsqueda contendrán un mapa de direcciones IP para los nombres de host. Si existen en el sistema local, se encontrarán en% SystemRoot% \\ system32 \\ drivers, \\ etc.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers, \\ \\ etc. \\ \\ Lmhosts")
</dt> </dl>

Ruta de acceso a un archivo de búsqueda WINS en el sistema local. Este archivo contendrá un mapa de direcciones IP para los nombres de host. Si se encuentra el archivo especificado en esta propiedad, se copiará en la carpeta% SystemRoot% \\ system32 \\ drivers \\ etc del sistema local. Válido solo si la propiedad **WINSEnableLMHostsLookup** es **true**.

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device INPUT and Output Functions \| DeviceIoControl")
</dt> </dl>

Dirección IP del servidor WINS principal.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ScopeID")
</dt> </dl>

Valor anexado al final del nombre NetBIOS que aísla un grupo de sistemas informáticos que se comunican solo entre sí. Se utiliza para todas las transacciones de NetBIOS a través de las comunicaciones TCP/IP de ese equipo. Los equipos configurados con identificadores de ámbito idénticos pueden comunicarse con este equipo. Los clientes TCP/IP con distintos identificadores de ámbito ignoran los paquetes de equipos con este identificador de ámbito. Solo es válido cuando el método [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) se ejecuta correctamente.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device INPUT and Output Functions \| DeviceIoControl")
</dt> </dl>

Dirección IP del servidor WINS secundario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ NetworkAdapterConfiguration de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).

## <a name="examples"></a>Ejemplos

El ejemplo de código VBScript del administrador de [información de WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la galería de TechNet usa la clase **Win32 \_ NetworkAdapterConfiguration** para recuperar información de configuración de red de varios equipos remotos.

El ejemplo de PowerShell [Get-ComputerInfo-Query Computer info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) de PowerShell en la galería de TechNet utiliza varias llamadas a hardware y software, incluido **Win32 \_ NetworkAdapterConfiguration**, para mostrar información acerca de un sistema local o remoto.

El siguiente código de PowerShell recupera los valores de configuración del adaptador de Microsoft ISTAP.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



En el siguiente ejemplo de C se \# recupera la descripción y el número de índice de todas las instancias de configuración del adaptador de red. Tenga en cuenta que este \# ejemplo de C usa el espacio de nombres [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , que generalmente se escala de forma más eficaz que las clases WMI del espacio de nombres [System. Management](/dotnet/api/system.management) .


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



En el siguiente ejemplo de C se \# recupera la descripción y el número de índice de todas las instancias de configuración del adaptador de red. Tenga en cuenta que este \# ejemplo de C usa el espacio de nombres [System. Management](/dotnet/api/system.management) original, que ha sido reemplazado por [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).


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



En el ejemplo siguiente se recupera información de la clase **\_ NetworkAdapterConfiguration de Win32** .


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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Tareas de WMI: redes](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Tareas de WMI: cuentas y dominios](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[Compatibilidad con IPv6 e IPv4 en WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
