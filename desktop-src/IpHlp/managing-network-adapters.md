---
description: La aplicación auxiliar de IP proporciona funciones para administrar los adaptadores de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Administración de adaptadores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541214"
---
# <a name="managing-network-adapters"></a><span data-ttu-id="12c0a-105">Administración de adaptadores de red</span><span class="sxs-lookup"><span data-stu-id="12c0a-105">Managing Network Adapters</span></span>

<span data-ttu-id="12c0a-106">La aplicación auxiliar de IP proporciona funciones para administrar los adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="12c0a-106">IP Helper provides capabilities for managing network adapters.</span></span> <span data-ttu-id="12c0a-107">Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="12c0a-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="12c0a-108">Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="12c0a-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="12c0a-109">Use las funciones descritas en los párrafos siguientes para recuperar información acerca de los adaptadores de red en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="12c0a-109">Use the functions described in the following paragraphs to retrieve information about the network adapters in the local computer.</span></span>

<span data-ttu-id="12c0a-110">La función [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) devuelve una matriz de estructuras de [**\_ \_ información del adaptador de IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , una para cada adaptador en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="12c0a-110">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns an array of [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structures, one for each adapter in the local computer.</span></span> <span data-ttu-id="12c0a-111">La función [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) devuelve información adicional sobre un adaptador específico.</span><span class="sxs-lookup"><span data-stu-id="12c0a-111">The [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) function returns additional information about a specific adapter.</span></span> <span data-ttu-id="12c0a-112">La función **GetPerAdapterInfo** requiere que el llamador especifique el índice del adaptador.</span><span class="sxs-lookup"><span data-stu-id="12c0a-112">The **GetPerAdapterInfo** function requires the caller to specify the index of the adapter.</span></span> <span data-ttu-id="12c0a-113">Para obtener el índice del adaptador del nombre del adaptador, utilice la función [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .</span><span class="sxs-lookup"><span data-stu-id="12c0a-113">To obtain the adapter index from the adapter name, use the [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) function.</span></span>

<span data-ttu-id="12c0a-114">Algunas aplicaciones usan adaptadores que reciben datagramas, pero no pueden transmitirlos.</span><span class="sxs-lookup"><span data-stu-id="12c0a-114">Some applications use adapters that receive datagrams, but cannot transmit them.</span></span> <span data-ttu-id="12c0a-115">Para obtener información acerca de estos adaptadores, utilice la función [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .</span><span class="sxs-lookup"><span data-stu-id="12c0a-115">To obtain information about these adapters, use the [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) function.</span></span>

<span data-ttu-id="12c0a-116">La función [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) permite recuperar las direcciones IP asociadas a un adaptador determinado.</span><span class="sxs-lookup"><span data-stu-id="12c0a-116">The [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) function enables you to retrieve the IP addresses associated with a particular adapter.</span></span> <span data-ttu-id="12c0a-117">Esta función admite direcciones IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="12c0a-117">This function supports both IPv4 and IPv6 addressing.</span></span>

-   <span data-ttu-id="12c0a-118">Para ver ejemplos de código que implican a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , consulte [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="12c0a-118">For code samples involving [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

 

 



