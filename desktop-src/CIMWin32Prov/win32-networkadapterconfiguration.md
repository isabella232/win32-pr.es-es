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
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="9b6d7-104">Clase NetworkAdapterConfiguration de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="9b6d7-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9b6d7-105">La **clase WMI \_ NetworkAdapterConfiguration** [de](../wmisdk/retrieving-a-class.md) Win32 representa los atributos y comportamientos de un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="9b6d7-106">Esta clase incluye propiedades y métodos adicionales que admiten la administración del protocolo TCP/IP que son independientes del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="9b6d7-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9b6d7-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6d7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b6d7-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="9b6d7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b6d7-110">Members</span></span>

<span data-ttu-id="9b6d7-111">La **clase \_ NetworkAdapterConfiguration de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b6d7-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="9b6d7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b6d7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9b6d7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b6d7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9b6d7-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b6d7-114">Methods</span></span>

<span data-ttu-id="9b6d7-115">La **clase \_ NetworkAdapterConfiguration de Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="9b6d7-116">Método</span><span class="sxs-lookup"><span data-stu-id="9b6d7-116">Method</span></span>                                                                                                                       | <span data-ttu-id="9b6d7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b6d7-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b6d7-118">**DisableIPSec**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="9b6d7-119">Deshabilita IPsec en este adaptador de red habilitado para TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="9b6d7-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="9b6d7-121">Habilita el Protocolo de configuración dinámica de host (DHCP) para el servicio con este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="9b6d7-122">**EnableDNS**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="9b6d7-123">Habilita el Sistema de nombres de dominio (DNS) para el servicio en este adaptador de red enlazado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="9b6d7-124">**EnableIPFilterSec**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="9b6d7-125">Habilita IPsec globalmente en todos los adaptadores de red enlazados a IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="9b6d7-126">**EnableIPSec**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="9b6d7-127">Habilita IPsec en este adaptador de red específico habilitado para TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="9b6d7-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="9b6d7-129">Habilita el direccionamiento TCP/IP estático para el adaptador de red de destino.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="9b6d7-130">**EnableWINS**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="9b6d7-131">Habilita la configuración WINS específica de TCP/IP, pero independiente del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="9b6d7-132">**ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="9b6d7-133">Libera la dirección IP enlazada a un adaptador de red específico habilitado para DHCP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="9b6d7-134">**ReleaseDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="9b6d7-135">Libera las direcciones IP enlazadas a todos los adaptadores de red habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="9b6d7-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="9b6d7-137">Renueva la dirección IP en adaptadores de red específicos habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="9b6d7-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="9b6d7-139">Renueva las direcciones IP en todos los adaptadores de red habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="9b6d7-140">**SetArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="9b6d7-141">Establece la transmisión de consultas ARP por TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="9b6d7-142">**SetArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="9b6d7-143">Permite que los paquetes Ethernet usen la codificación SNAP 802.3.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="9b6d7-144">**SetDatabasePath**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="9b6d7-145">Establece la ruta de acceso a los archivos de base de datos de Internet estándar (HOSTS, LMHOSTS, REDES y PROTOCOLOS).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="9b6d7-146">**SetDeadGWDetect**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="9b6d7-147">Habilita la detección de puerta de enlace fallcida.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="9b6d7-148">**SetDefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="9b6d7-149">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-149">Obsolete.</span></span> <span data-ttu-id="9b6d7-150">Este método establece el valor predeterminado de Tipo de servicio (TOS) en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="9b6d7-151">**SetDefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="9b6d7-152">Establece el valor predeterminado De período de vida (TTL) en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="9b6d7-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="9b6d7-154">Establece el dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="9b6d7-155">**SetDNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="9b6d7-156">Establece el orden de búsqueda del servidor como una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="9b6d7-157">**SetDNSSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="9b6d7-158">Establece el orden de búsqueda del sufijo como una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="9b6d7-159">**SetDynamicDNSRegistration**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="9b6d7-160">Indica el registro DNS dinámico de direcciones IP para este adaptador enlazado a IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="9b6d7-161">**SetForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="9b6d7-162">Especifica cuánta dirección IP de memoria asigna para almacenar datos de paquetes en la cola de paquetes del enrutador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="9b6d7-163">**SetGateways**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="9b6d7-164">Especifica una lista de puertas de enlace para enrutar paquetes destinados a una subred diferente de la a la que está conectado este adaptador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="9b6d7-165">**SetIGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="9b6d7-166">Establece la medida en que el sistema admite la multidifusión IP y participa en el Protocolo de administración de grupos de Internet.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="9b6d7-167">**SetIPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="9b6d7-168">Establece la métrica de enrutamiento asociada a este adaptador enlazado a IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="9b6d7-169">**SetIPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="9b6d7-170">Establece el uso de difusión ip cero.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="9b6d7-171">**SetIPXFrameTypeNetworkPairs**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="9b6d7-172">Establece los pares de número de red y trama de intercambio de paquetes de trabajo por Internet (IPX) para este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="9b6d7-173">**SetIPXVirtualNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="9b6d7-174">Establece el número de red virtual de Internetworking Packet Exchange (IPX) en el sistema de equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="9b6d7-175">**SetKeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="9b6d7-176">Establece el intervalo que separa las retransmisiones Keep Alive hasta que se recibe una respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="9b6d7-177">**SetKeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="9b6d7-178">Establece la frecuencia con la que TCP intenta comprobar que una conexión inactiva sigue estando disponible mediante el envío de un paquete Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="9b6d7-179">**SetMTU**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="9b6d7-180">Establece la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="9b6d7-181">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="9b6d7-182">**SetNumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="9b6d7-183">Establece el número de encabezados de paquetes IP asignados para la cola de paquetes del enrutador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="9b6d7-184">**SetPMTUBHDetect**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="9b6d7-185">Habilita la detección de enrutadores black hole.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="9b6d7-186">**SetPMTUDiscovery**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="9b6d7-187">Habilita la detección de unidad de transmisión máxima (MTU).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="9b6d7-188">**SetTcpipNetbios**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="9b6d7-189">Establece la operación predeterminada de NetBIOS a través de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="9b6d7-190">**SetTcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="9b6d7-191">Establece el número de intentos que TCP retransmitirá una solicitud de conexión antes de anularla.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="9b6d7-192">**SetTcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="9b6d7-193">Establece el número de veces que TCP retransmitirá un segmento de datos individual antes de anular la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="9b6d7-194">**SetTcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="9b6d7-195">Establece el número máximo de conexiones que TCP puede tener abiertas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="9b6d7-196">**SetTcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="9b6d7-197">Especifica si TCP usa la especificación RFC 1122 para datos urgentes o el modo que usan los sistemas derivados de Berkeley Software Design (BSD).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="9b6d7-198">**SetTcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="9b6d7-199">Establece el tamaño máximo de ventana de recepción TCP que ofrece el sistema.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="9b6d7-200">**SetWINSServer**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="9b6d7-201">Establece los servidores de Windows Internet Naming Service principal y secundario (WINS) en este adaptador de red enlazado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="9b6d7-202">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b6d7-202">Properties</span></span>

<span data-ttu-id="9b6d7-203">La **clase \_ NetworkAdapterConfiguration de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b6d7-204">**ArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-205">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-207">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ArpAlwaysSourceRoute")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-208">Si **es TRUE,** TCP/IP transmite consultas del Protocolo de resolución de direcciones (ARP) con enrutamiento de origen habilitado en redes de anillo de token.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="9b6d7-209">De forma predeterminada (FALSE), ARP primero consulta sin enrutamiento de origen y, a continuación, vuelve a in reintentos con el enrutamiento de origen habilitado si no se recibe ninguna respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="9b6d7-210">El enrutamiento de origen permite el enrutamiento de paquetes de red entre diferentes tipos de redes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-211">**ArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-212">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-214">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ArpUseEtherSNAP")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-215">Si **es TRUE,** los paquetes Ethernet siguen la codificación IEEE 802.3 Sub-Network Access Protocol (SNAP).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="9b6d7-216">Establecer este parámetro en 1 fuerza a TCP/IP a transmitir paquetes Ethernet mediante la codificación SNAP 802.3.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="9b6d7-217">De forma predeterminada (FALSE), la pila transmite paquetes en formato DIX Ethernet.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-221">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-222">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-222">Short textual description of the current object.</span></span>

<span data-ttu-id="9b6d7-223">Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-224">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-227">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DatabasePath")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-228">Ruta de acceso válida del archivo de Windows a los archivos de base de datos estándar de Internet (HOSTS, LMHOSTS, REDES y PROTOCOLOS).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="9b6d7-229">La interfaz de Windows Sockets usa la ruta de acceso del archivo.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-230">**DeadGWDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-233">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnableDeadGWDetect")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-234">Si **es TRUE,** se produce la detección de puerta de enlace no activa.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="9b6d7-235">Con esta característica habilitada, el Protocolo de control de transmisión (TCP) pide a Protocolo de Internet (IP) que cambie a una puerta de enlace de copia de seguridad si retransmite un segmento varias veces sin recibir una respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-237">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-239">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| DefaultGateway")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-240">Matriz de direcciones IP de puertas de enlace predeterminadas que usa el sistema informático.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="9b6d7-241">Ejemplo: "192.168.12.1 192.168.46.1"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-242">**DefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-243">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-245">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DefaultTOS")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-246">Valor predeterminado del tipo de servicio (TOS) establecido en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="9b6d7-247">Solicitud de comentarios (RFC) 791 define los valores.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="9b6d7-248">Valor predeterminado: 0 (cero), Intervalo válido: 0 - 255.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-250">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-252">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DefaultTTL")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-253">Valor de período de vida (TTL) predeterminado establecido en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="9b6d7-254">El TTL especifica el número de enrutadores que puede pasar un paquete IP para llegar a su destino antes de descartarse.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="9b6d7-255">Cada enrutador disminuye en uno el número de TTL de un paquete a medida que pasa y descarta los paquetes, si el TTL es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="9b6d7-256">Valor predeterminado: 32, intervalo válido: 1 - 255.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-257">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-260">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-260">Textual description of the current object.</span></span>

<span data-ttu-id="9b6d7-261">Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-263">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-265">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-266">Si **es TRUE,** el servidor dhcp (protocolo de configuración dinámica de host) asigna automáticamente una dirección IP al sistema del equipo al establecer una conexión de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-267">**DHCPLeaseExpires**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-268">Tipo de datos: **datetime**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-270">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-271">Fecha y hora de expiración de una dirección IP alquilada asignada al equipo por el servidor del Protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="9b6d7-272">Ejemplo: 20521201000230.000000000</span><span class="sxs-lookup"><span data-stu-id="9b6d7-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-273">**DHCPLeaseObtained**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-274">Tipo de datos: **datetime**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-276">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-277">Fecha y hora en que el servidor dhcp (protocolo de configuración dinámica de host) obtuvo la concesión para la dirección IP asignada al equipo.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="9b6d7-278">Ejemplo: 19521201000230.000000000</span><span class="sxs-lookup"><span data-stu-id="9b6d7-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-279">**DHCPServer**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-282">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-283">Dirección IP del servidor de protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="9b6d7-284">Ejemplo: "10.55.34.2"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-288">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Dominio de parámetros Tcpip de Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ \\ \\ \\ \\ \| Services")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-289">Nombre de la organización seguido de un punto y una extensión que indica el tipo de organización, como "microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="9b6d7-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="9b6d7-290">El nombre puede ser cualquier combinación de las letras A a Z, los números del 0 al 9 y el guion (-), además del carácter de punto (.) usado como separador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="9b6d7-291">Ejemplo: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-292">**DNSDomainSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-293">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-295">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| SearchList")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-296">Matriz de sufijos de dominio DNS que se anexarán al final de los nombres de host durante la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="9b6d7-297">Al intentar resolver un nombre de dominio completo (FQDN) a partir de un nombre de solo host, el sistema anexará primero el nombre de dominio local.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="9b6d7-298">Si esto no se realiza correctamente, el sistema usará la lista de sufijos de dominio para crear FQDN adicionales en el orden indicado y consultar los servidores DNS para cada uno.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="9b6d7-299">Ejemplo: "samples.microsoft.com example.microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-300">**DNSEnabledForWINSResolution**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-301">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-303">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnableDNS")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-304">Si **es TRUE,** el Sistema de nombres de dominio (DNS) está habilitado para la resolución de nombres a través de Windows Internet Naming Service (WINS).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="9b6d7-305">Si el nombre no se puede resolver mediante DNS, la solicitud de nombre se reenvía a WINS para su resolución.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-306">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-309">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| Hostname")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-310">Nombre de host usado para identificar el equipo local para la autenticación por parte de algunas utilidades.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="9b6d7-311">Otras utilidades basadas en TCP/IP pueden usar este valor para adquirir el nombre del equipo local.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="9b6d7-312">Los nombres de host se almacenan en servidores DNS en una tabla que asigna nombres a direcciones IP para su uso por PARTE de DNS.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="9b6d7-313">El nombre puede ser cualquier combinación de las letras A a Z, los números del 0 al 9 y el guion (-), además del carácter de punto (.) utilizado como separador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="9b6d7-314">De forma predeterminada, este valor es el nombre del equipo de red de Microsoft, pero el administrador de red puede asignar otro nombre de host sin que ello afecte al nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="9b6d7-315">Ejemplo: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-316">**DNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-317">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-319">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| NameServer")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-320">Matriz de direcciones IP de servidor que se usará para consultar servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-321">**DomainDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-322">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-324">Si **es TRUE,** las direcciones IP de esta conexión se registran en DNS con el nombre de dominio de esta conexión, además de registrarse con el nombre DNS completo del equipo.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="9b6d7-325">El nombre de dominio de esta conexión se establece mediante el [**método SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() o se asigna mediante DSCP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="9b6d7-326">El nombre registrado es el nombre de host del equipo con el nombre de dominio anexado.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-327">**ForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-328">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-330">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-331">Memoria asignada por IP para almacenar datos de paquetes en la cola de paquetes del enrutador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="9b6d7-332">Cuando se rellena este espacio de búfer, el enrutador comienza a descartar paquetes aleatoriamente de su cola.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="9b6d7-333">Los búferes de datos de cola de paquetes tienen una longitud de 256 bytes, por lo que el valor de este parámetro debe ser un múltiplo de 256.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="9b6d7-334">Varios búferes están encadenados para paquetes más grandes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="9b6d7-335">El encabezado IP de un paquete se almacena por separado.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="9b6d7-336">Este parámetro se omite y no se asignan búferes si el enrutador IP no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="9b6d7-337">El tamaño del búfer puede oscilar entre la MTU de red y un valor menor que 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="9b6d7-338">Valor predeterminado: 74240 (paquetes de 1480 bytes, redondeados a un múltiplo de 256).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-339">**FullDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-340">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-342">Si **es TRUE,** las direcciones IP de esta conexión se registran en DNS con el nombre DNS completo del equipo.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="9b6d7-343">El nombre DNS completo del equipo se muestra en la pestaña **Identificación de** red de la aplicación Sistema en Panel de control.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-344">**GatewayCostMetric**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-345">Tipo de datos: **matriz uint16**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-347">Matriz de valores de métrica de costo entero (comprendidos entre 1 y 9999) que se usarán para calcular las rutas más rápidas, más confiables o con menos recursos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="9b6d7-348">Este argumento tiene una correspondencia uno a uno con la **propiedad DefaultIPGateway.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-349">**IGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-350">Tipo de datos: **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-352">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| IGMPLevel")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-353">Medida en la que el sistema admite la multidifusión IP y participa en el Protocolo de administración de grupos de Internet (IGMP).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="9b6d7-354">En el nivel 0 (cero), el sistema no proporciona compatibilidad con multidifusión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="9b6d7-355">En el nivel 1, el sistema solo puede enviar paquetes de multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="9b6d7-356">En el nivel 2, el sistema puede enviar paquetes de multidifusión IP y participar completamente en IGMP para recibir paquetes de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="9b6d7-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Sin multidifusión** (0)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="9b6d7-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multidifusión IP** (1)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="9b6d7-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**Ip & multidifusión IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9b6d7-360">Multidifusión IP y IGMP (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b6d7-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-362">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-364">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet Control Class \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-365">Número de índice de la configuración del adaptador de red de Windows.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="9b6d7-366">El número de índice se usa cuando hay más de una configuración disponible.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-367">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-368">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-370">Valor de índice que identifica de forma única una interfaz de red local.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="9b6d7-371">El valor de esta propiedad es el mismo que el valor de la propiedad **InterfaceIndex** de la instancia de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa la interfaz de red en la tabla de rutas.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-372">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-373">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-375">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip \| IPAddress")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-376">Matriz de todas las direcciones IP asociadas al adaptador de red actual.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="9b6d7-377">Esta propiedad puede contener direcciones IPv6 o direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="9b6d7-378">Para obtener más información, vea [Compatibilidad con IPv6 e IPv4 en WMI.](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="9b6d7-379">Dirección IPv6 de ejemplo: "2010:836B:4179::836B:4179"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-380">**IPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-381">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-383">Costo de usar las rutas configuradas para el adaptador enlazado a IP y es el valor ponderado de esas rutas en la tabla de enrutamiento IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="9b6d7-384">Si hay varias rutas a un destino en la tabla de enrutamiento IP, se usa la ruta con la métrica más baja.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="9b6d7-385">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-387">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-389">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-390">Si **es TRUE,** TCP/IP está enlazado y habilitado en este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-391">**IPFilterSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-392">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-394">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-395">Si **es TRUE,** la seguridad del puerto IP está habilitada globalmente en todos los adaptadores de red enlazados a IP y los valores de seguridad asociados a adaptadores de red individuales están en vigor.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="9b6d7-396">Esta propiedad se usa junto con **IPSecPermitTCPPorts,** **IPSecPermitUDPPorts** e **IPSecPermitIPProtocols**.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="9b6d7-397">Si **es FALSE,** la seguridad del filtro IP está deshabilitada en todos los adaptadores de red y permite que todo el tráfico de puerto y protocolo fluya sin filtrar.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-398">**IPPortSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-399">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-401">Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-402">Si **es TRUE,** la seguridad del puerto IP está habilitada globalmente en todos los adaptadores de red enlazados a IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="9b6d7-403">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-403">This property is obsolete.</span></span> <span data-ttu-id="9b6d7-404">En lugar de esta propiedad, debe usar **IPFilterSecurityEnabled.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-405">**IPSecPermitIPProtocols**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-406">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-408">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| RawIPAllowedProtocols")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-409">Matriz de los protocolos permitidos para ejecutarse a través de la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="9b6d7-410">La lista de protocolos se define mediante el [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="9b6d7-411">La lista estará vacía o contendrá valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="9b6d7-412">Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los protocolos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="9b6d7-413">Una cadena vacía indica que no se permite ejecutar ningún protocolo **cuando IPFilterSecurityEnabled** es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-414">**IPSecPermitTCPPorts**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-415">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-417">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TCPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-418">Matriz de los puertos a los que se concederá permiso de acceso para TCP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="9b6d7-419">La lista de protocolos se define mediante el [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="9b6d7-420">La lista estará vacía o contendrá valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="9b6d7-421">Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="9b6d7-422">Una cadena vacía indica que no se concede permiso de acceso a ningún puerto **cuando IPFilterSecurityEnabled** es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-423">**IPSecPermitUDPPorts**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-424">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-426">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| UDPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-427">Matriz de los puertos a los que se concederá el permiso de acceso protocolo de datagramas de usuario (UDP).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="9b6d7-428">La lista de protocolos se define mediante el [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="9b6d7-429">La lista estará vacía o contendrá valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="9b6d7-430">Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="9b6d7-431">Una cadena vacía indica que no se concede permiso de acceso a ningún puerto **cuando IPFilterSecurityEnabled** es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-433">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-435">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| SubnetMask")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-436">Matriz de todas las máscaras de subred asociadas al adaptador de red actual.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="9b6d7-437">Ejemplo: "255.255.0.0"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-438">**IPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-439">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-441">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| UseZeroBroadcast")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-442">Si **es TRUE,** se usan difusión de ceros ip (0.0.0.0) y el sistema usa difusión de uno (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="9b6d7-443">Los sistemas informáticos suelen usar difusión ones, pero los derivados de las implementaciones de BSD usan difusión de ceros.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="9b6d7-444">Los sistemas que no usan las mismas difusiones no interoperarán en la misma red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="9b6d7-445">El valor predeterminado es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-446">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-447">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-449">Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-450">Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-451">**IPXEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-452">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-454">Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-455">Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-456">**IPXFrameType**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-457">Tipo de datos: **matriz uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-459">Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| PktType")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-460">Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="9b6d7-461">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="9b6d7-462">**Ethernet 802.3** (1)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="9b6d7-463">**Ethernet 802.2** (2)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="9b6d7-464">**Ethernet SNAP** (3)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="9b6d7-465">**AUTO** (255)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b6d7-466">**IPXMediaType**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-467">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-469">Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| MediaType")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-470">Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="9b6d7-471">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="9b6d7-472">**Anillo de token** (2)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="9b6d7-473">**FDDI** (3)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="9b6d7-474">**ARCNET** (8)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b6d7-475">**IPXNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-476">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="9b6d7-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-478">Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| NetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-479">Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-480">**IPXVirtualNetNumber**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-483">Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| VirtualNetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-484">Ya no se admite la tecnología internetwork Packet Exchange (IPX) y esta propiedad no contiene datos útiles.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-486">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-488">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-489">Intervalo que separa las retransmisiones Keep Alive hasta que se recibe una respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="9b6d7-490">Después de recibir una respuesta, el retraso hasta la siguiente transmisión Keep Alive se controla de nuevo mediante el **valor de KeepAliveTime**.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="9b6d7-491">La conexión se anulará después de que el número de retransmisiones especificadas por **TcpMaxDataRetransmissions** haya quedo sin respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="9b6d7-492">Valor predeterminado: 1000, intervalo válido: 1 - 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-494">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-496">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-497">La **propiedad KeepAliveTime** indica la frecuencia con la que el TCP intenta comprobar que una conexión inactiva sigue intacta mediante el envío de un paquete Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="9b6d7-498">Un sistema remoto al que se pueda acceder confirmará la transmisión keep alive.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="9b6d7-499">Los paquetes Keep Alive no se envían de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="9b6d7-500">Una aplicación puede habilitar esta característica en una conexión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="9b6d7-501">Valor predeterminado: 7 200 000 (dos horas).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-503">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-505">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de entrada y salida del dispositivo Win32API \| \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-506">Dirección Access Control (MAC) del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="9b6d7-507">El fabricante asigna una dirección MAC para identificar de forma única el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="9b6d7-508">Ejemplo: "00:80:C7:8F:6C:96"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-509">**MTU**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-510">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-511">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-512">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-513">Invalida la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="9b6d7-514">La MTU es el tamaño máximo de paquete (incluido el encabezado de transporte) que el transporte transmitirá a través de la red subyacente.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="9b6d7-515">El datagrama IP puede abarcar varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="9b6d7-516">El intervalo de este valor abarca el tamaño mínimo de paquete (68) a la MTU compatible con la red subyacente.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-517">**NumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-518">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-520">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| NumForwardPackets")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-521">Número de encabezados de paquetes IP asignados para la cola de paquetes del enrutador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="9b6d7-522">Cuando todos los encabezados están en uso, el enrutador empezará a descartar paquetes de la cola de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="9b6d7-523">Este valor debe ser al menos tan grande como el valor **ForwardBufferMemory** dividido por el tamaño máximo de datos IP de las redes conectadas al enrutador.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="9b6d7-524">No debe ser mayor que el valor **ForwardBufferMemory** dividido entre 256, ya que se usan al menos 256 bytes de memoria de búfer de reenvío para cada paquete.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="9b6d7-525">El número óptimo de paquetes de reenvío para un tamaño **ForwardBufferMemory** determinado depende del tipo de tráfico en la red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="9b6d7-526">Estará en algún lugar entre estos dos valores.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="9b6d7-527">Si el enrutador no está habilitado, este parámetro se omite y no se asignan encabezados.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="9b6d7-528">Valor predeterminado: 50, intervalo válido: 1 - 0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-529">**PMTUBHDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-530">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-531">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-532">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnablePMTUBHDetect")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-533">Si **es TRUE,** se produce la detección de enrutadores de huecos negros mientras TCP detecta la ruta de acceso de la unidad de transmisión máxima.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="9b6d7-534">Un enrutador de hueco negro no devuelve mensajes de destino icmp inaccesibles cuando necesita fragmentar un datagrama IP con el conjunto de bits No fragmentar.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="9b6d7-535">TCP depende de la recepción de estos mensajes para realizar la detección de MTU de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="9b6d7-536">Con esta característica habilitada, TCP intentará enviar segmentos sin el conjunto de bits No fragmentar si varias retransmisiones de un segmento no se reconocen.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="9b6d7-537">Si el segmento se confirma como resultado, el MSS se disminuirá y el bit No fragmentar se establecerá en paquetes futuros en la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="9b6d7-538">La habilitación de la detección de huecos negros aumenta el número máximo de retransmisiones realizadas para un segmento determinado.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="9b6d7-539">El valor predeterminado de esta propiedad es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-540">**PMTUDiscoveryEnabled**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-541">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-543">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnablePMTUDiscovery")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-544">Si **es TRUE,** la ruta de acceso de la unidad de transmisión máxima (MTU) se detecta a través de la ruta de acceso a un host remoto.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="9b6d7-545">Al detectar la ruta de acceso de MTU y limitar los segmentos TCP a este tamaño, TCP puede eliminar la fragmentación en los enrutadores a lo largo de la ruta de acceso que conectan redes con diferentes MTU.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="9b6d7-546">La fragmentación afecta negativamente al rendimiento tcp y a la congestión de la red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="9b6d7-547">Establecer este parámetro en **FALSE hace** que se utilice un MTU de 576 bytes para todas las conexiones que no están en las máquinas de la subred local.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="9b6d7-548">El valor predeterminado es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-549">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-550">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-551">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-552">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-553">Nombre de servicio del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-553">Service name of the network adapter.</span></span> <span data-ttu-id="9b6d7-554">Este nombre suele ser más corto que el nombre completo del producto.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="9b6d7-555">Ejemplo: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="9b6d7-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-557">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-558">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-559">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-560">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="9b6d7-561">Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-562">**TcpipNetbiosOptions**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-563">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-564">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-565">Mapa de bits de la posible configuración relacionada con NetBIOS a través de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="9b6d7-566">Los valores se identifican en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="9b6d7-567">**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="9b6d7-568">**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="9b6d7-569">**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b6d7-570">**TcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-571">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-572">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-573">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpMaxConnectRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-574">Número de veces que TCP intenta retransmitir una solicitud de conexión antes de finalizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="9b6d7-575">El tiempo de espera de retransmisión inicial es de 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="9b6d7-576">El tiempo de espera de retransmisión se duplica para cada intento.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="9b6d7-577">Valor predeterminado: 3, Intervalo válido: 0 - 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-579">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-580">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-581">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpMaxDataRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-582">Número de veces que TCP retransmite un segmento de datos individual (segmento que no es de conexión) antes de finalizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="9b6d7-583">El tiempo de espera de retransmisión se duplica con cada retransmisión sucesiva en una conexión.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="9b6d7-584">Valor predeterminado: 5, Intervalo válido: 0 - 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-585">**TcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-586">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-587">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-588">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpNumConnections")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-589">Número máximo de conexiones que TCP puede tener abiertas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="9b6d7-590">Valor predeterminado: 0xFFFFFE, Intervalo válido: 0 - 0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-591">**TcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-592">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-593">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-594">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpUseRFC1122UrgentPointer")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-595">Si **es TRUE,** TCP usa la especificación RFC 1122 para los datos urgentes.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="9b6d7-596">Si **es FALSE** (valor predeterminado), TCP usa el modo que usan los sistemas derivados de Berkeley Software Design (BSD).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="9b6d7-597">Los dos mecanismos interpretan el puntero urgente de manera diferente y no son interoperables.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="9b6d7-598">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-600">Tipo de datos: **uint16**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-601">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-602">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-603">Tamaño máximo de ventana de recepción TCP ofrecido por el sistema.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="9b6d7-604">La ventana de recepción especifica el número de bytes que un remitente puede transmitir sin recibir una confirmación.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="9b6d7-605">En general, las ventanas receptoras más grandes mejorarán el rendimiento a través de redes de alto retraso y ancho de banda alto.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="9b6d7-606">Para mejorar la eficacia, la ventana de recepción debe ser un múltiplo par del tamaño máximo de segmento (MSS) de TCP.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="9b6d7-607">Valor predeterminado: cuatro veces el tamaño máximo de los datos TCP o incluso un múltiplo de tamaño de datos TCP redondeado al múltiplo más cercano de 8192.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="9b6d7-608">El valor predeterminado de las redes Ethernet es 8760.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="9b6d7-609">Intervalo válido: 0 - 65535.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="9b6d7-610">Windows Vista: esta propiedad tiene acceso a la entrada `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` del Registro, que no se usa en la implementación actual del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="9b6d7-611">**WINSEnableLMHostsLookup**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-612">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-613">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-614">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnableLMHOSTS")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-615">Si **es TRUE,** se usan archivos de búsqueda local.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="9b6d7-616">Los archivos de búsqueda contendrán una asignación de direcciones IP a nombres de host.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="9b6d7-617">Si existen en el sistema local, se encontrarán en %SystemRoot% \\ system32 \\ drivers \\ etc.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-618">**WINSHostLookupFile**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-619">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-620">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-621">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)drivers etc \| \\ \\ \\ \\ \\ \\ lmhosts")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-622">Ruta de acceso a un archivo de búsqueda WINS en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="9b6d7-623">Este archivo contendrá una asignación de direcciones IP a nombres de host.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="9b6d7-624">Si se encuentra el archivo especificado en esta propiedad, se copiará en la carpeta %SystemRoot% \\ system32 \\ drivers etc del sistema \\ local.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="9b6d7-625">Solo es válido si **la propiedad WINSEnableLMHostsLookup** es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-626">**WINSPrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-627">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-628">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-629">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de entrada y salida del dispositivo Win32API \| \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-630">Dirección IP del servidor WINS principal.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-631">**WINSScopeID**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-632">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-633">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-634">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ScopeID")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-635">Valor anexado al final del nombre NetBIOS que aísla un grupo de sistemas informáticos que se comunican entre sí.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="9b6d7-636">Se usa para todas las transacciones NetBIOS a través de comunicaciones TCP/IP desde ese sistema informático.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="9b6d7-637">Los equipos configurados con identificadores de ámbito idénticos pueden comunicarse con este equipo.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="9b6d7-638">Los clientes TCP/IP con identificadores de ámbito diferentes no tienen en cuenta los paquetes de los equipos con este identificador de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="9b6d7-639">Válido solo cuando [**el método EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d7-640">**WINSSecondaryServer**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d7-641">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-642">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b6d7-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d7-643">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de entrada y salida del dispositivo Win32API \| \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="9b6d7-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d7-644">Dirección IP del servidor WINS secundario.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b6d7-645">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b6d7-645">Remarks</span></span>

<span data-ttu-id="9b6d7-646">La **clase \_ NetworkAdapterConfiguration de Win32** se deriva de [**cim \_ setting**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9b6d7-647">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9b6d7-647">Examples</span></span>

<span data-ttu-id="9b6d7-648">El [ejemplo de](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) código VBScript del recuperador de información de WMI en la Galería de TechNet usa la clase **\_ NetworkAdapterConfiguration de Win32** para recuperar información de configuración de red de varios equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="9b6d7-649">El ejemplo de PowerShell [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) en la Galería de TechNet usa una serie de llamadas a hardware y software, incluido **\_ Win32 NetworkAdapterConfiguration**, para mostrar información sobre un sistema local o remoto.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="9b6d7-650">El siguiente código de PowerShell recupera las opciones de configuración del adaptador de ISTAP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="9b6d7-651">En el ejemplo de C \# siguiente se recupera la descripción y el número de índice de todas las instancias de configuración del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="9b6d7-652">Tenga en cuenta que en este ejemplo de C se usa el espacio de nombres \# [Microsoft.Management.Infrastructure,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) que generalmente se escala de forma más eficaz que las clases WMI del espacio de nombres [System.Management.](/dotnet/api/system.management)</span><span class="sxs-lookup"><span data-stu-id="9b6d7-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


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



<span data-ttu-id="9b6d7-653">En el ejemplo de C \# siguiente se recupera la descripción y el número de índice de todas las instancias de configuración del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b6d7-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="9b6d7-654">Tenga en cuenta que en este ejemplo de C se usa el espacio de nombres \# [System.Management](/dotnet/api/system.management) original, supercedido por [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b6d7-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


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



<span data-ttu-id="9b6d7-655">En el ejemplo siguiente se recupera información de la **clase \_ NetworkAdapterConfiguration de Win32.**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9b6d7-656">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b6d7-656">Requirements</span></span>



| <span data-ttu-id="9b6d7-657">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b6d7-657">Requirement</span></span> | <span data-ttu-id="9b6d7-658">Valor</span><span class="sxs-lookup"><span data-stu-id="9b6d7-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6d7-659">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b6d7-659">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6d7-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b6d7-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b6d7-661">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b6d7-661">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6d7-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b6d7-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b6d7-663">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b6d7-663">Namespace</span></span><br/>                | <span data-ttu-id="9b6d7-664">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="9b6d7-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b6d7-665">MOF</span><span class="sxs-lookup"><span data-stu-id="9b6d7-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b6d7-666"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d7-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b6d7-667">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b6d7-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b6d7-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d7-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b6d7-669">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b6d7-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6d7-670">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9b6d7-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="9b6d7-671">Clases de hardware del sistema de equipo</span><span class="sxs-lookup"><span data-stu-id="9b6d7-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9b6d7-672">Tareas wmi: redes</span><span class="sxs-lookup"><span data-stu-id="9b6d7-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="9b6d7-673">Tareas wmi: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="9b6d7-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="9b6d7-674">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="9b6d7-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
