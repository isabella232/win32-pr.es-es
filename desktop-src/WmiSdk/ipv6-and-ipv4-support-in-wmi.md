---
description: Las clases de red y del proveedor de rutas IP de WMI proporcionan datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las capacidades de red IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Compatibilidad con IPv6 e IPv4 en WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687990"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a><span data-ttu-id="801a7-104">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="801a7-104">IPv6 and IPv4 Support in WMI</span></span>

<span data-ttu-id="801a7-105">Las clases de red y del [proveedor de rutas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) de WMI proporcionan datos para las direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="801a7-105">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="801a7-106">A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las capacidades de red IPv6.</span><span class="sxs-lookup"><span data-stu-id="801a7-106">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span>

## <a name="wmi-ip-data"></a><span data-ttu-id="801a7-107">Datos de IP de WMI</span><span class="sxs-lookup"><span data-stu-id="801a7-107">WMI IP Data</span></span>

<span data-ttu-id="801a7-108">Las clases siguientes solo proporcionan datos IPv4:</span><span class="sxs-lookup"><span data-stu-id="801a7-108">The following classes supply only IPv4 data:</span></span>

-   [<span data-ttu-id="801a7-109">**Win32 \_ IP4RouteTable**</span><span class="sxs-lookup"><span data-stu-id="801a7-109">**Win32\_IP4RouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [<span data-ttu-id="801a7-110">**Win32 \_ IP4PersistedRouteTable**</span><span class="sxs-lookup"><span data-stu-id="801a7-110">**Win32\_IP4PersistedRouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [<span data-ttu-id="801a7-111">**Win32 \_ IP4RouteTableEvent**</span><span class="sxs-lookup"><span data-stu-id="801a7-111">**Win32\_IP4RouteTableEvent**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [<span data-ttu-id="801a7-112">**Win32 \_ ActiveRoute**</span><span class="sxs-lookup"><span data-stu-id="801a7-112">**Win32\_ActiveRoute**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [<span data-ttu-id="801a7-113">**Adaptador de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="801a7-113">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)

<span data-ttu-id="801a7-114">Las siguientes clases proporcionan datos tanto para IPv4 como para IPv6.</span><span class="sxs-lookup"><span data-stu-id="801a7-114">The following classes supply data for both IPv4 and IPv6.</span></span>

-   [<span data-ttu-id="801a7-115">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="801a7-115">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    <span data-ttu-id="801a7-116">La propiedad **IpAddess** contiene la dirección IPv6 del equipo en una red IPv6.</span><span class="sxs-lookup"><span data-stu-id="801a7-116">The **IpAddess** property contains the IPv6 address of the computer in an IPv6 network.</span></span>

-   [<span data-ttu-id="801a7-117">**Win32 \_ PingStatus**</span><span class="sxs-lookup"><span data-stu-id="801a7-117">**Win32\_PingStatus**</span></span>](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    <span data-ttu-id="801a7-118">[**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) puede devolver datos para direcciones IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="801a7-118">[**Win32\_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) can return data for either IPv4 or IPv6 addresses.</span></span>

## <a name="ipv4-and-ipv6-connections-to-wmi"></a><span data-ttu-id="801a7-119">Conexiones IPv4 e IPv6 a WMI</span><span class="sxs-lookup"><span data-stu-id="801a7-119">IPv4 and IPv6 Connections to WMI</span></span>

<span data-ttu-id="801a7-120">Al conectarse a un espacio de nombres WMI en un equipo remoto, el equipo de destino debe ejecutar el mismo software IP que el equipo que se conecta.</span><span class="sxs-lookup"><span data-stu-id="801a7-120">When connecting to a WMI namespace on a remote computer, the target computer must be running the same IP software as the connecting computer.</span></span> <span data-ttu-id="801a7-121">Por ejemplo, un equipo que ejecuta IPv4 no puede conectarse a un equipo que ejecuta IPv6, incluso si se intenta la conexión mediante el uso de un nombre de equipo en la llamada a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md)o mediante la `winmgmts` conexión de moniker.</span><span class="sxs-lookup"><span data-stu-id="801a7-121">For example, a computer running IPv4 cannot connect to a computer running IPv6, even if the connection is attempted by using a computer name in the call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), or by using the `winmgmts` moniker connection.</span></span> <span data-ttu-id="801a7-122">Lo contrario también es cierto: un equipo que ejecuta únicamente IPv6 no puede conectarse a un equipo que solo ejecute IPv4.</span><span class="sxs-lookup"><span data-stu-id="801a7-122">The reverse is also true: a computer running only IPv6 cannot connect to a computer running only IPv4.</span></span>

<span data-ttu-id="801a7-123">Si el equipo de destino está ejecutando IPv4 e IPv6, se puede establecer una conexión desde un equipo que ejecute el software IP.</span><span class="sxs-lookup"><span data-stu-id="801a7-123">If the target computer is running both IPv4 and IPv6, then a connection can be made from a computer running either IP software.</span></span> <span data-ttu-id="801a7-124">Se puede proporcionar un nombre de equipo o una dirección IP en formato IPv4 o IPv6 en la conexión a un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="801a7-124">A computer name or an IP address in either IPv4 or IPv6 format can be supplied in the connection to a WMI namespace.</span></span>

<span data-ttu-id="801a7-125">Un equipo que ejecuta IPv4 e IPv6 y se conecta a un equipo de destino que solo ejecuta IPv4 o solo IPv6 debe proporcionar una dirección IP en el formato adecuado para el software de IP del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="801a7-125">A computer that runs both IPv4 and IPv6 and connects to a target computer running only IPv4 or only IPv6 must supply an IP address in the appropriate format for the target computer IP software.</span></span>

## <a name="related-topics"></a><span data-ttu-id="801a7-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="801a7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="801a7-127">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="801a7-127">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
