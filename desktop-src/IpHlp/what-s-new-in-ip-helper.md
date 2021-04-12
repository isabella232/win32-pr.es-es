---
description: Novedades de la aplicación auxiliar de IP
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: Novedades de la aplicación auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c1a6eebb3e9e785e8988b822df0b2a80ae6eba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361402"
---
# <a name="whats-new-in-ip-helper"></a>Novedades de la aplicación auxiliar de IP

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 y Windows Server 2012

Se han agregado las siguientes características a las API auxiliares de IP en Windows 8 y Windows Server 2012.

Función que recupera las estimaciones históricas de ancho de banda para una conexión de red. Para más información, consulte:

-   [**GetIpNetworkConnectionBandwidthEstimates**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

Estructura que contiene información sobre las estimaciones de ancho de banda disponibles y la desviación asociada según lo determinado por la pila TCP/IP. Para más información, consulte:

-   [**\_información de ancho de banda nl \_**](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

Se han agregado las siguientes características a las API auxiliares de IP en Windows 7 y Windows Server 2008 R2.

Funciones que convierten una dirección Ethernet entre un formato binario y el formato de cadena de la dirección MAC de Ethernet. Para más información, consulte:

-   [**RtlEthernetAddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [**RtlEthernetStringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 y Windows Vista SP1

Se han agregado las siguientes funciones a las API auxiliares de IP en Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

Función que funciona con IPv4 y el protocolo de mensajes de control de Internet (ICMP). Para más información, consulte:

-   [**IcmpSendEcho2Ex**](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a>Windows Vista

Los siguientes grupos de funciones se han agregado a las API auxiliares de IP en Windows Vista y versiones posteriores.

Funciones que funcionan con IPv6 e IPv4 para la conversión de interfaz. Para más información, consulte:

-   [**ConvertInterfaceAliasToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**ConvertInterfaceGuidToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**ConvertInterfaceIndexToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**ConvertInterfaceLuidToGuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**ConvertInterfaceLuidToIndex**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**ConvertInterfaceLuidToNameA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**ConvertInterfaceLuidToNameW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**ConvertInterfaceNameToLuidA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**ConvertInterfaceNameToLuidW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**Si \_ indextoname**](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [**Si \_ nametoindex**](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

Funciones que funcionan con IPv6 e IPv4 para la administración de interfaces. Para más información, consulte:

-   [**GetIfEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [**GetIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [**GetIfTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**GetInvertedIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**GetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**GetIpInterfaceTable**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**InitializeIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**SetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

Funciones que funcionan con IPv6 e IPv4 para la administración de direcciones IP. Para más información, consulte:

-   [**CreateAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**CreateUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**DeleteAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**DeleteUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**GetAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**GetAnycastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**GetMulticastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**GetMulticastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**GetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**GetUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**InitializeUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**SetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

Función que funciona con IPv6 e IPv4 para la administración de memoria de tablas IP. Para más información, consulte:

-   [**FreeMibTable**](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

Funciones que funcionan con IPv6 e IPv4 para la administración de direcciones de vecino IP. Para más información, consulte:

-   [**CreateIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**ResolveNeighbor**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

Funciones que funcionan con IPv6 e IPv4 para la administración de rutas de acceso IP. Para más información, consulte:

-   [**FlushIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [**GetIpPathEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [**GetIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

Funciones que funcionan con IPv6 e IPv4 para la administración de rutas IP. Para más información, consulte:

-   [**CreateIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**DeleteIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**GetBestRoute2**](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**GetIpForwardTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**InitializeIpForwardEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**SetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**SetIpStatisticsEx**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

Funciones que funcionan con IPv6 e IPv4 para la notificación. Para más información, consulte:

-   [**CancelMibChangeNotify2**](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**NotifyIpInterfaceChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**NotifyRouteChange2**](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**NotifyUnicastIpAddressChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

Funciones de utilidad que funcionan con direcciones IP. Para más información, consulte:

-   [**ConvertIpv4MaskToLength**](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**CreateSortedAddressPairs**](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**ParseNetworkString**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

Funciones que funcionan con el protocolo de control de transmisión (TCP) y el protocolo de datagramas de usuario (UDP) para recuperar la tabla de conexión TCP IPv6 o IPv4 o la tabla de escucha de UDP. Para más información, consulte:

-   [**GetTcp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**GetUdp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

Funciones que funcionan con el protocolo de control de transmisión (TCP) para recuperar estadísticas TCP extendidas en una conexión. Para más información, consulte:

-   [**GetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**GetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**SetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**SetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

Nuevas funciones que funcionan para la administración de clientes IPv6 Teredo. Para más información, consulte:

-   [**GetTeredoPort**](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

Funciones de utilidad que proporcionan conversiones entre las direcciones IP y las representaciones de cadena de direcciones IP. Para más información, consulte:

-   [**RtlIpv4AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

Funciones que proporcionan reservas persistentes para un bloque consecutivo de puertos TCP o UDP en el equipo local. Para más información, consulte:

-   [**CreatePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**CreatePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**DeletePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**DeletePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**LookupPersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**LookupPersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a>Windows Server 2003

Se han agregado las siguientes funciones a las API auxiliares de IP en Windows Server 2003 y versiones posteriores:

-   [**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

## <a name="windows-xp-sp2"></a>Windows XP SP2

Las siguientes funciones se han agregado a las API auxiliares de IP en Windows XP con Service Pack 2 (SP2) y versiones posteriores:

-   [**GetOwnerModuleFromTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**GetOwnerModuleFromUdpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
