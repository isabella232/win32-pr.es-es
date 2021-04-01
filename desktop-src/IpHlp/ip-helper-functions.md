---
description: Las siguientes funciones recuperan y modifican los valores de configuración para el transporte TCP/IP en el equipo local.
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
title: Funciones de aplicación auxiliar IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c8bff21f41c04bb5aecf505b251fbbe2f8bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818995"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="76603-103">Funciones auxiliares de IP</span><span class="sxs-lookup"><span data-stu-id="76603-103">IP Helper functions</span></span>

<span data-ttu-id="76603-104">Las siguientes funciones recuperan y modifican los valores de configuración para el transporte TCP/IP en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="76603-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="76603-105">La siguiente lista de categorías puede ayudar a determinar qué colección de funciones es la más adecuada para una tarea determinada.</span><span class="sxs-lookup"><span data-stu-id="76603-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="76603-106">**GetNetworkConnectivityHint**</span><span class="sxs-lookup"><span data-stu-id="76603-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="76603-107">**GetNetworkConnectivityHintForInterface**</span><span class="sxs-lookup"><span data-stu-id="76603-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="76603-108">**NotifyNetworkConnectivityHintChange**</span><span class="sxs-lookup"><span data-stu-id="76603-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="76603-109">Administración de adaptadores</span><span class="sxs-lookup"><span data-stu-id="76603-109">Adapter management</span></span>

-   [<span data-ttu-id="76603-110">**GetAdapterIndex**</span><span class="sxs-lookup"><span data-stu-id="76603-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="76603-111">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="76603-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="76603-112">**GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="76603-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="76603-113">**GetPerAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="76603-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="76603-114">**GetUniDirectionalAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="76603-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="76603-115">Administración del Protocolo de resolución de direcciones (ARP)</span><span class="sxs-lookup"><span data-stu-id="76603-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="76603-116">**CreateIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="76603-117">**CreateProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="76603-118">**DeleteIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="76603-119">**DeleteProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="76603-120">**FlushIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="76603-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="76603-121">**GetIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="76603-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="76603-122">**SendARP**</span><span class="sxs-lookup"><span data-stu-id="76603-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="76603-123">**SetIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="76603-124">Conversión de interfaz</span><span class="sxs-lookup"><span data-stu-id="76603-124">Interface conversion</span></span>

-   [<span data-ttu-id="76603-125">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="76603-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="76603-126">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="76603-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="76603-127">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="76603-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="76603-128">**ConvertInterfaceLuidToAlias**</span><span class="sxs-lookup"><span data-stu-id="76603-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="76603-129">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="76603-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="76603-130">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="76603-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="76603-131">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="76603-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="76603-132">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="76603-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="76603-133">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="76603-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="76603-134">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="76603-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="76603-135">**Si \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="76603-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="76603-136">**Si \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="76603-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="76603-137">Administración de interfaces</span><span class="sxs-lookup"><span data-stu-id="76603-137">Interface management</span></span>

-   [<span data-ttu-id="76603-138">**GetFriendlyIfIndex**</span><span class="sxs-lookup"><span data-stu-id="76603-138">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="76603-139">**GetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-139">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="76603-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-140">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="76603-141">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="76603-141">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="76603-142">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="76603-142">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="76603-143">**GetIfTable**</span><span class="sxs-lookup"><span data-stu-id="76603-143">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="76603-144">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="76603-144">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="76603-145">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="76603-145">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="76603-146">**GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="76603-146">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="76603-147">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="76603-147">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="76603-148">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-148">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="76603-149">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="76603-149">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="76603-150">**GetNumberOfInterfaces**</span><span class="sxs-lookup"><span data-stu-id="76603-150">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="76603-151">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-151">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="76603-152">**SetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-152">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="76603-153">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-153">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="76603-154">Protocolo de Internet (IP) y Protocolo de mensajes de control de Internet (ICMP)</span><span class="sxs-lookup"><span data-stu-id="76603-154">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="76603-155">**GetIcmpStatistics**</span><span class="sxs-lookup"><span data-stu-id="76603-155">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="76603-156">**GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="76603-156">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="76603-157">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="76603-157">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="76603-158">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="76603-158">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="76603-159">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="76603-159">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="76603-160">**IcmpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="76603-160">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="76603-161">**IcmpCreateFile**</span><span class="sxs-lookup"><span data-stu-id="76603-161">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="76603-162">**IcmpParseReplies**</span><span class="sxs-lookup"><span data-stu-id="76603-162">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="76603-163">**IcmpSendEcho**</span><span class="sxs-lookup"><span data-stu-id="76603-163">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="76603-164">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="76603-164">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="76603-165">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="76603-165">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="76603-166">**SetIpTTL**</span><span class="sxs-lookup"><span data-stu-id="76603-166">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="76603-167">Administración de direcciones IP</span><span class="sxs-lookup"><span data-stu-id="76603-167">IP address management</span></span>

-   [<span data-ttu-id="76603-168">**AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="76603-168">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="76603-169">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-169">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="76603-170">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-170">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="76603-171">**DeleteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="76603-171">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="76603-172">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-172">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="76603-173">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-173">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="76603-174">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-174">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="76603-175">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="76603-175">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="76603-176">**GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="76603-176">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="76603-177">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-177">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="76603-178">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="76603-178">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="76603-179">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-179">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="76603-180">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="76603-180">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="76603-181">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-181">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="76603-182">**IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="76603-182">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="76603-183">**IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="76603-183">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="76603-184">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="76603-184">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="76603-185">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-185">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="76603-186">Conversión de cadena de dirección IP</span><span class="sxs-lookup"><span data-stu-id="76603-186">IP address string conversion</span></span>

-   [<span data-ttu-id="76603-187">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="76603-187">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="76603-188">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="76603-188">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="76603-189">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="76603-189">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="76603-190">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="76603-190">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="76603-191">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="76603-191">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="76603-192">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="76603-192">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="76603-193">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="76603-193">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="76603-194">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="76603-194">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="76603-195">Administración de direcciones de vecino IP</span><span class="sxs-lookup"><span data-stu-id="76603-195">IP neighbor address management</span></span>

-   [<span data-ttu-id="76603-196">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-196">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="76603-197">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-197">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="76603-198">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="76603-198">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="76603-199">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-199">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="76603-200">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="76603-200">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="76603-201">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-201">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="76603-202">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="76603-202">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="76603-203">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-203">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="76603-204">Administración de rutas de acceso IP</span><span class="sxs-lookup"><span data-stu-id="76603-204">IP path management</span></span>

-   [<span data-ttu-id="76603-205">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="76603-205">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="76603-206">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-206">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="76603-207">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="76603-207">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="76603-208">Administración de rutas IP</span><span class="sxs-lookup"><span data-stu-id="76603-208">IP route management</span></span>

-   [<span data-ttu-id="76603-209">**CreateIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-209">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="76603-210">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-210">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="76603-211">**DeleteIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-211">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="76603-212">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-212">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="76603-213">**EnableRouter**</span><span class="sxs-lookup"><span data-stu-id="76603-213">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="76603-214">**GetBestInterface**</span><span class="sxs-lookup"><span data-stu-id="76603-214">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="76603-215">**GetBestInterfaceEx**</span><span class="sxs-lookup"><span data-stu-id="76603-215">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="76603-216">**GetBestRoute**</span><span class="sxs-lookup"><span data-stu-id="76603-216">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="76603-217">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="76603-217">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="76603-218">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-218">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="76603-219">**GetIpForwardTable**</span><span class="sxs-lookup"><span data-stu-id="76603-219">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="76603-220">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="76603-220">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="76603-221">**GetRTTAndHopCount**</span><span class="sxs-lookup"><span data-stu-id="76603-221">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="76603-222">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-222">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="76603-223">**SetIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-223">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="76603-224">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="76603-224">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="76603-225">**SetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="76603-225">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="76603-226">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="76603-226">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="76603-227">**UnenableRouter**</span><span class="sxs-lookup"><span data-stu-id="76603-227">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="76603-228">Administración de memoria de tabla IP</span><span class="sxs-lookup"><span data-stu-id="76603-228">IP table memory management</span></span>

-   [<span data-ttu-id="76603-229">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="76603-229">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="76603-230">Utilidad IP</span><span class="sxs-lookup"><span data-stu-id="76603-230">IP utility</span></span>

-   [<span data-ttu-id="76603-231">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="76603-231">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="76603-232">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="76603-232">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="76603-233">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="76603-233">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="76603-234">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="76603-234">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="76603-235">Configuración de red</span><span class="sxs-lookup"><span data-stu-id="76603-235">Network configuration</span></span>

-   [<span data-ttu-id="76603-236">**GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="76603-236">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="76603-237">notificación</span><span class="sxs-lookup"><span data-stu-id="76603-237">Notification</span></span>

-   [<span data-ttu-id="76603-238">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="76603-238">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="76603-239">**NotifyAddrChange**</span><span class="sxs-lookup"><span data-stu-id="76603-239">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="76603-240">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="76603-240">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="76603-241">**NotifyRouteChange**</span><span class="sxs-lookup"><span data-stu-id="76603-241">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="76603-242">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="76603-242">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="76603-243">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="76603-243">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="76603-244">Reserva de Puerto persistente</span><span class="sxs-lookup"><span data-stu-id="76603-244">Persistent port reservation</span></span>

-   [<span data-ttu-id="76603-245">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="76603-245">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="76603-246">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="76603-246">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="76603-247">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="76603-247">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="76603-248">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="76603-248">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="76603-249">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="76603-249">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="76603-250">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="76603-250">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="76603-251">Estado de la seguridad</span><span class="sxs-lookup"><span data-stu-id="76603-251">Security health</span></span>

-   <span data-ttu-id="76603-252">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76603-252">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="76603-253">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76603-253">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="76603-254">Estas funciones se definen solo en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="76603-254">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="76603-255">Estas funciones no están disponibles en Windows Vista ni en Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="76603-255">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="76603-256">Administración de cliente IPv6 Teredo</span><span class="sxs-lookup"><span data-stu-id="76603-256">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="76603-257">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="76603-257">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="76603-258">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="76603-258">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="76603-259">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="76603-259">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="76603-260">Protocolo de control de transmisión (TCP) y Protocolo de datagramas de usuario (UDP)</span><span class="sxs-lookup"><span data-stu-id="76603-260">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="76603-261">**GetExtendedTcpTable**</span><span class="sxs-lookup"><span data-stu-id="76603-261">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="76603-262">**GetExtendedUdpTable**</span><span class="sxs-lookup"><span data-stu-id="76603-262">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="76603-263">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="76603-263">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="76603-264">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-264">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="76603-265">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="76603-265">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="76603-266">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-266">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="76603-267">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="76603-267">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="76603-268">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="76603-268">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="76603-269">**GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="76603-269">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="76603-270">**GetTcpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="76603-270">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="76603-271">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="76603-271">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="76603-272">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="76603-272">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="76603-273">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="76603-273">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="76603-274">**GetTcpTable**</span><span class="sxs-lookup"><span data-stu-id="76603-274">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="76603-275">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="76603-275">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="76603-276">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="76603-276">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="76603-277">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="76603-277">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="76603-278">**SetTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="76603-278">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="76603-279">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="76603-279">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="76603-280">**GetUdpStatistics**</span><span class="sxs-lookup"><span data-stu-id="76603-280">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="76603-281">**GetUdpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="76603-281">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="76603-282">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="76603-282">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="76603-283">**GetUdpTable**</span><span class="sxs-lookup"><span data-stu-id="76603-283">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="76603-284">Interfaces API desusadas</span><span class="sxs-lookup"><span data-stu-id="76603-284">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="76603-285">Estas funciones están en desuso y no son compatibles con Microsoft.</span><span class="sxs-lookup"><span data-stu-id="76603-285">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="76603-286">**AllocateAndGetTcpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="76603-286">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="76603-287">**AllocateAndGetUdpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="76603-287">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
