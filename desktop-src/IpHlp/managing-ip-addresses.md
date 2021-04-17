---
description: La aplicación auxiliar de IP puede ayudar en la administración de las direcciones IP asociadas a las interfaces en el equipo local. Use las funciones descritas en los párrafos siguientes para la administración de direcciones IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Administración de direcciones IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686710"
---
# <a name="managing-ip-addresses"></a><span data-ttu-id="582a3-104">Administración de direcciones IP</span><span class="sxs-lookup"><span data-stu-id="582a3-104">Managing IP Addresses</span></span>

<span data-ttu-id="582a3-105">La aplicación auxiliar de IP puede ayudar en la administración de las direcciones IP asociadas a las interfaces en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="582a3-105">IP Helper can assist in the management of IP addresses associated with interfaces on the local computer.</span></span> <span data-ttu-id="582a3-106">Use las funciones descritas en los párrafos siguientes para la administración de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="582a3-106">Use the functions described in the following paragraphs for IP address management.</span></span>

<span data-ttu-id="582a3-107">La función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera una tabla que contiene la asignación de direcciones IP a las interfaces.</span><span class="sxs-lookup"><span data-stu-id="582a3-107">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function retrieves a table that contains the mapping of IP addresses to interfaces.</span></span> <span data-ttu-id="582a3-108">Se puede asociar más de una dirección IP a la misma interfaz.</span><span class="sxs-lookup"><span data-stu-id="582a3-108">More than one IP address may be associated with the same interface.</span></span>

<span data-ttu-id="582a3-109">Utilice la función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para agregar una dirección IP a una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="582a3-109">Use the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add an IP address to a particular interface.</span></span> <span data-ttu-id="582a3-110">Para quitar las direcciones IP que se agregaron previamente mediante **AddIPAddress**, use la función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .</span><span class="sxs-lookup"><span data-stu-id="582a3-110">To remove IP addresses that were previously added using **AddIPAddress**, use the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function.</span></span>

<span data-ttu-id="582a3-111">Las funciones [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requieren que el equipo local use el protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="582a3-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require the local computer to be using Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="582a3-112">La función **IpReleaseAddress** libera una dirección IP que se obtuvo previamente de DHCP.</span><span class="sxs-lookup"><span data-stu-id="582a3-112">The **IpReleaseAddress** function releases an IP address that was previously obtained from DHCP.</span></span> <span data-ttu-id="582a3-113">La función **IpRenewAddress** renueva una concesión DHCP en una dirección IP determinada.</span><span class="sxs-lookup"><span data-stu-id="582a3-113">The **IpRenewAddress** function renews a DHCP lease on a particular IP address.</span></span> <span data-ttu-id="582a3-114">Una concesión DHCP permite que un equipo use una dirección IP durante un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="582a3-114">A DHCP lease allows a computer to use an IP address for a specified period of time.</span></span>

-   <span data-ttu-id="582a3-115">Para ver ejemplos de código que implican a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , consulte [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="582a3-115">For code samples involving [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) see [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

-   <span data-ttu-id="582a3-116">Para ver ejemplos de código que implican [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) y [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), consulte [Administración de direcciones IP con AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span><span class="sxs-lookup"><span data-stu-id="582a3-116">For code samples involving [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) and [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), see [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span></span>

-   <span data-ttu-id="582a3-117">Para obtener ejemplos de código que impliquen [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , vea [administrar concesiones DHCP mediante IpReleaseAddress y IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span><span class="sxs-lookup"><span data-stu-id="582a3-117">For code samples involving [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) see [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span></span>

 

 



