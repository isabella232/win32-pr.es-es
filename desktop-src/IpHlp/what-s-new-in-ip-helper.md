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
# <a name="whats-new-in-ip-helper"></a><span data-ttu-id="08466-103">Novedades de la aplicación auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="08466-103">What's New in IP Helper</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="08466-104">Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08466-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="08466-105">Se han agregado las siguientes características a las API auxiliares de IP en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="08466-105">The following features have been added to the IP Helper APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="08466-106">Función que recupera las estimaciones históricas de ancho de banda para una conexión de red.</span><span class="sxs-lookup"><span data-stu-id="08466-106">A function that retrieves historical bandwidth estimates for a network connection.</span></span> <span data-ttu-id="08466-107">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-107">For more information, see:</span></span>

-   [<span data-ttu-id="08466-108">**GetIpNetworkConnectionBandwidthEstimates**</span><span class="sxs-lookup"><span data-stu-id="08466-108">**GetIpNetworkConnectionBandwidthEstimates**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

<span data-ttu-id="08466-109">Estructura que contiene información sobre las estimaciones de ancho de banda disponibles y la desviación asociada según lo determinado por la pila TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="08466-109">A structure that contains information on the available bandwidth estimates and associated variance as determined by the TCP/IP stack.</span></span> <span data-ttu-id="08466-110">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-110">For more information, see:</span></span>

-   [<span data-ttu-id="08466-111">**\_información de ancho de banda nl \_**</span><span class="sxs-lookup"><span data-stu-id="08466-111">**NL\_BANDWIDTH\_INFORMATION**</span></span>](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="08466-112">Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08466-112">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="08466-113">Se han agregado las siguientes características a las API auxiliares de IP en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="08466-113">The following features have been added to the IP Helper APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="08466-114">Funciones que convierten una dirección Ethernet entre un formato binario y el formato de cadena de la dirección MAC de Ethernet.</span><span class="sxs-lookup"><span data-stu-id="08466-114">Functions that convert an Ethernet address between a binary format and string format for the Ethernet MAC address.</span></span> <span data-ttu-id="08466-115">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-115">For more information, see:</span></span>

-   [<span data-ttu-id="08466-116">**RtlEthernetAddressToString**</span><span class="sxs-lookup"><span data-stu-id="08466-116">**RtlEthernetAddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [<span data-ttu-id="08466-117">**RtlEthernetStringToAddress**</span><span class="sxs-lookup"><span data-stu-id="08466-117">**RtlEthernetStringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="08466-118">Windows Server 2008 y Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="08466-118">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="08466-119">Se han agregado las siguientes funciones a las API auxiliares de IP en Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="08466-119">The following functions have been added to the IP Helper APIs on Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="08466-120">Función que funciona con IPv4 y el protocolo de mensajes de control de Internet (ICMP).</span><span class="sxs-lookup"><span data-stu-id="08466-120">A function that works with IPv4 and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="08466-121">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-121">For more information, see:</span></span>

-   [<span data-ttu-id="08466-122">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="08466-122">**IcmpSendEcho2Ex**</span></span>](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a><span data-ttu-id="08466-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08466-123">Windows Vista</span></span>

<span data-ttu-id="08466-124">Los siguientes grupos de funciones se han agregado a las API auxiliares de IP en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="08466-124">The following groups of functions have been added to the IP Helper APIs on Windows Vista and later.</span></span>

<span data-ttu-id="08466-125">Funciones que funcionan con IPv6 e IPv4 para la conversión de interfaz.</span><span class="sxs-lookup"><span data-stu-id="08466-125">Functions that work with both IPv6 and IPv4 for interface conversion.</span></span> <span data-ttu-id="08466-126">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-126">For more information, see:</span></span>

-   [<span data-ttu-id="08466-127">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="08466-127">**ConvertInterfaceAliasToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="08466-128">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="08466-128">**ConvertInterfaceGuidToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="08466-129">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="08466-129">**ConvertInterfaceIndexToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="08466-130">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="08466-130">**ConvertInterfaceLuidToGuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="08466-131">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="08466-131">**ConvertInterfaceLuidToIndex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="08466-132">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="08466-132">**ConvertInterfaceLuidToNameA**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="08466-133">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="08466-133">**ConvertInterfaceLuidToNameW**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="08466-134">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="08466-134">**ConvertInterfaceNameToLuidA**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="08466-135">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="08466-135">**ConvertInterfaceNameToLuidW**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="08466-136">**Si \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="08466-136">**if\_indextoname**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="08466-137">**Si \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="08466-137">**if\_nametoindex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

<span data-ttu-id="08466-138">Funciones que funcionan con IPv6 e IPv4 para la administración de interfaces.</span><span class="sxs-lookup"><span data-stu-id="08466-138">Functions that work with both IPv6 and IPv4 for interface management.</span></span> <span data-ttu-id="08466-139">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-139">For more information, see:</span></span>

-   [<span data-ttu-id="08466-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-140">**GetIfEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="08466-141">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="08466-141">**GetIfStackTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="08466-142">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="08466-142">**GetIfTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="08466-143">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="08466-143">**GetIfTable2Ex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="08466-144">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="08466-144">**GetInvertedIfStackTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="08466-145">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-145">**GetIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="08466-146">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="08466-146">**GetIpInterfaceTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="08466-147">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-147">**InitializeIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="08466-148">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-148">**SetIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

<span data-ttu-id="08466-149">Funciones que funcionan con IPv6 e IPv4 para la administración de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="08466-149">Functions that work with both IPv6 and IPv4 for IP address management.</span></span> <span data-ttu-id="08466-150">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-150">For more information, see:</span></span>

-   [<span data-ttu-id="08466-151">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-151">**CreateAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="08466-152">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-152">**CreateUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="08466-153">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-153">**DeleteAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="08466-154">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-154">**DeleteUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="08466-155">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-155">**GetAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="08466-156">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="08466-156">**GetAnycastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="08466-157">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-157">**GetMulticastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="08466-158">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="08466-158">**GetMulticastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="08466-159">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-159">**GetUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="08466-160">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="08466-160">**GetUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="08466-161">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-161">**InitializeUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="08466-162">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="08466-162">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="08466-163">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-163">**SetUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

<span data-ttu-id="08466-164">Función que funciona con IPv6 e IPv4 para la administración de memoria de tablas IP.</span><span class="sxs-lookup"><span data-stu-id="08466-164">A function that works with both IPv6 and IPv4 for IP table memory management.</span></span> <span data-ttu-id="08466-165">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-165">For more information, see:</span></span>

-   [<span data-ttu-id="08466-166">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="08466-166">**FreeMibTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

<span data-ttu-id="08466-167">Funciones que funcionan con IPv6 e IPv4 para la administración de direcciones de vecino IP.</span><span class="sxs-lookup"><span data-stu-id="08466-167">Functions that work with both IPv6 and IPv4 for IP neighbor address management.</span></span> <span data-ttu-id="08466-168">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-168">For more information, see:</span></span>

-   [<span data-ttu-id="08466-169">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-169">**CreateIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="08466-170">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-170">**DeleteIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="08466-171">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="08466-171">**FlushIpNetTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="08466-172">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-172">**GetIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="08466-173">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="08466-173">**GetIpNetTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="08466-174">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-174">**ResolveIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="08466-175">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="08466-175">**ResolveNeighbor**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="08466-176">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-176">**SetIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

<span data-ttu-id="08466-177">Funciones que funcionan con IPv6 e IPv4 para la administración de rutas de acceso IP.</span><span class="sxs-lookup"><span data-stu-id="08466-177">Functions that work with both IPv6 and IPv4 for IP path management.</span></span> <span data-ttu-id="08466-178">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-178">For more information, see:</span></span>

-   [<span data-ttu-id="08466-179">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="08466-179">**FlushIpPathTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="08466-180">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-180">**GetIpPathEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="08466-181">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="08466-181">**GetIpPathTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

<span data-ttu-id="08466-182">Funciones que funcionan con IPv6 e IPv4 para la administración de rutas IP.</span><span class="sxs-lookup"><span data-stu-id="08466-182">Functions that work with both IPv6 and IPv4 for IP route management.</span></span> <span data-ttu-id="08466-183">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-183">For more information, see:</span></span>

-   [<span data-ttu-id="08466-184">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-184">**CreateIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="08466-185">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-185">**DeleteIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="08466-186">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="08466-186">**GetBestRoute2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="08466-187">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-187">**GetIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="08466-188">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="08466-188">**GetIpForwardTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="08466-189">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-189">**InitializeIpForwardEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="08466-190">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="08466-190">**SetIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="08466-191">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="08466-191">**SetIpStatisticsEx**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

<span data-ttu-id="08466-192">Funciones que funcionan con IPv6 e IPv4 para la notificación.</span><span class="sxs-lookup"><span data-stu-id="08466-192">Functions that work with both IPv6 and IPv4 for notification.</span></span> <span data-ttu-id="08466-193">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-193">For more information, see:</span></span>

-   [<span data-ttu-id="08466-194">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="08466-194">**CancelMibChangeNotify2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="08466-195">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="08466-195">**NotifyIpInterfaceChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="08466-196">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="08466-196">**NotifyRouteChange2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="08466-197">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="08466-197">**NotifyUnicastIpAddressChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

<span data-ttu-id="08466-198">Funciones de utilidad que funcionan con direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="08466-198">Utility functions that work with IP addresses.</span></span> <span data-ttu-id="08466-199">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-199">For more information, see:</span></span>

-   [<span data-ttu-id="08466-200">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="08466-200">**ConvertIpv4MaskToLength**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="08466-201">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="08466-201">**ConvertLengthToIpv4Mask**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="08466-202">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="08466-202">**CreateSortedAddressPairs**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="08466-203">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="08466-203">**ParseNetworkString**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

<span data-ttu-id="08466-204">Funciones que funcionan con el protocolo de control de transmisión (TCP) y el protocolo de datagramas de usuario (UDP) para recuperar la tabla de conexión TCP IPv6 o IPv4 o la tabla de escucha de UDP.</span><span class="sxs-lookup"><span data-stu-id="08466-204">Functions that work with Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) to retrieve the IPv6 or IPv4 TCP connection table or UDP listener table.</span></span> <span data-ttu-id="08466-205">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-205">For more information, see:</span></span>

-   [<span data-ttu-id="08466-206">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="08466-206">**GetTcp6Table**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="08466-207">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="08466-207">**GetTcp6Table2**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="08466-208">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="08466-208">**GetTcpTable2**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="08466-209">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="08466-209">**GetUdp6Table**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

<span data-ttu-id="08466-210">Funciones que funcionan con el protocolo de control de transmisión (TCP) para recuperar estadísticas TCP extendidas en una conexión.</span><span class="sxs-lookup"><span data-stu-id="08466-210">Functions that work with Transmission Control Protocol (TCP) to retrieve extended TCP statistics on a connection.</span></span> <span data-ttu-id="08466-211">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-211">For more information, see:</span></span>

-   [<span data-ttu-id="08466-212">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="08466-212">**GetPerTcp6ConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="08466-213">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="08466-213">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="08466-214">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="08466-214">**SetPerTcp6ConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="08466-215">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="08466-215">**SetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

<span data-ttu-id="08466-216">Nuevas funciones que funcionan para la administración de clientes IPv6 Teredo.</span><span class="sxs-lookup"><span data-stu-id="08466-216">New functions that work for Teredo IPv6 client management.</span></span> <span data-ttu-id="08466-217">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-217">For more information, see:</span></span>

-   [<span data-ttu-id="08466-218">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="08466-218">**GetTeredoPort**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="08466-219">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="08466-219">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="08466-220">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="08466-220">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

<span data-ttu-id="08466-221">Funciones de utilidad que proporcionan conversiones entre las direcciones IP y las representaciones de cadena de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="08466-221">Utility functions that provide conversions between IP addresses and string representations of IP addresses.</span></span> <span data-ttu-id="08466-222">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-222">For more information, see:</span></span>

-   [<span data-ttu-id="08466-223">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="08466-223">**RtlIpv4AddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="08466-224">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="08466-224">**RtlIpv4AddressToStringEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="08466-225">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="08466-225">**RtlIpv4StringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="08466-226">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="08466-226">**RtlIpv4StringToAddressEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="08466-227">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="08466-227">**RtlIpv6AddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="08466-228">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="08466-228">**RtlIpv6AddressToStringEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="08466-229">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="08466-229">**RtlIpv6StringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="08466-230">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="08466-230">**RtlIpv6StringToAddressEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

<span data-ttu-id="08466-231">Funciones que proporcionan reservas persistentes para un bloque consecutivo de puertos TCP o UDP en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="08466-231">Functions that provide persistent reservations for a consecutive block of TCP or UDP ports on the local computer.</span></span> <span data-ttu-id="08466-232">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="08466-232">For more information, see:</span></span>

-   [<span data-ttu-id="08466-233">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="08466-233">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="08466-234">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="08466-234">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="08466-235">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="08466-235">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="08466-236">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="08466-236">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="08466-237">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="08466-237">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="08466-238">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="08466-238">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a><span data-ttu-id="08466-239">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08466-239">Windows Server 2003</span></span>

<span data-ttu-id="08466-240">Se han agregado las siguientes funciones a las API auxiliares de IP en Windows Server 2003 y versiones posteriores:</span><span class="sxs-lookup"><span data-stu-id="08466-240">The following functions have been added to the IP Helper APIs on Windows Server 2003 and later:</span></span>

-   <span data-ttu-id="08466-241">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08466-241">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="08466-242">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08466-242">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

## <a name="windows-xp-sp2"></a><span data-ttu-id="08466-243">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="08466-243">Windows XP SP2</span></span>

<span data-ttu-id="08466-244">Las siguientes funciones se han agregado a las API auxiliares de IP en Windows XP con Service Pack 2 (SP2) y versiones posteriores:</span><span class="sxs-lookup"><span data-stu-id="08466-244">The following functions have been added to the IP Helper APIs on Windows XP with Service Pack 2 (SP2) and later:</span></span>

-   [<span data-ttu-id="08466-245">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-245">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="08466-246">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="08466-246">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="08466-247">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="08466-247">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="08466-248">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="08466-248">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
