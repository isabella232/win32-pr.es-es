---
description: La aplicación auxiliar de IP amplía sus capacidades para administrar las interfaces de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Administrar interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276725"
---
# <a name="managing-interfaces"></a><span data-ttu-id="6575c-105">Administrar interfaces</span><span class="sxs-lookup"><span data-stu-id="6575c-105">Managing Interfaces</span></span>

<span data-ttu-id="6575c-106">La aplicación auxiliar de IP amplía sus capacidades para administrar las interfaces de red.</span><span class="sxs-lookup"><span data-stu-id="6575c-106">IP Helper extends your abilities to manage network interfaces.</span></span> <span data-ttu-id="6575c-107">Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="6575c-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="6575c-108">Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="6575c-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="6575c-109">Use las funciones descritas en los párrafos siguientes para administrar interfaces en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6575c-109">Use the functions described in the following paragraphs to manage interfaces on the local computer.</span></span>

<span data-ttu-id="6575c-110">La función [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) devuelve el número de interfaces en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6575c-110">The [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) function returns the number of interfaces on the local computer.</span></span>

<span data-ttu-id="6575c-111">La función [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) devuelve una tabla que contiene los nombres y los índices correspondientes de las interfaces en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6575c-111">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function returns a table that contains the names and corresponding indexes for the interfaces on the local computer.</span></span> <span data-ttu-id="6575c-112">Para ver ejemplos de código que implican a **GetInterfaceInfo** , consulte [Administración de interfaces con GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="6575c-112">For code samples involving **GetInterfaceInfo** see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="6575c-113">La función [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) toma un índice de interfaz y devuelve un índice de interfaz compatible con versiones anteriores, es decir, uno que solo usa los 24 bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="6575c-113">The [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) function takes an interface index and returns a backward-compatible interface index, that is, one that uses only the lower 24 bits.</span></span> <span data-ttu-id="6575c-114">Este tipo de índice se conoce a veces como un índice de interfaz "descriptivo".</span><span class="sxs-lookup"><span data-stu-id="6575c-114">This type of index is sometimes referred to as a "friendly" interface index.</span></span>

<span data-ttu-id="6575c-115">La función [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) devuelve una estructura [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) que contiene información sobre una interfaz determinada en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6575c-115">The [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) function returns a [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) structure that contains information about a particular interface on the local computer.</span></span> <span data-ttu-id="6575c-116">Esta función requiere que el llamador proporcione el índice de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6575c-116">This function requires the caller to supply the index of the interface.</span></span>

<span data-ttu-id="6575c-117">La función [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) devuelve una tabla de entradas [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , una para cada interfaz del equipo.</span><span class="sxs-lookup"><span data-stu-id="6575c-117">The [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) function returns a table of [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) entries, one for each interface on the computer.</span></span>

<span data-ttu-id="6575c-118">Utilice la función [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) para modificar la configuración de una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="6575c-118">Use the [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) function to modify the configuration of a particular interface.</span></span>

 

 
