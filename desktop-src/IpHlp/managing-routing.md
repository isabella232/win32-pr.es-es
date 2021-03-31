---
description: La aplicación auxiliar de IP proporciona características para administrar el enrutamiento de red. Utilice las siguientes funciones para administrar la tabla de enrutamiento IP y obtener otra información de enrutamiento.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Administrar el enrutamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907884"
---
# <a name="managing-routing"></a><span data-ttu-id="918cf-104">Administrar el enrutamiento</span><span class="sxs-lookup"><span data-stu-id="918cf-104">Managing Routing</span></span>

<span data-ttu-id="918cf-105">La aplicación auxiliar de IP proporciona características para administrar el enrutamiento de red.</span><span class="sxs-lookup"><span data-stu-id="918cf-105">IP Helper provides features to manage network routing.</span></span> <span data-ttu-id="918cf-106">Utilice las siguientes funciones para administrar la tabla de enrutamiento IP y obtener otra información de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="918cf-106">Use the following functions to manage the IP routing table, and to obtain other routing information.</span></span>

<span data-ttu-id="918cf-107">Recupere el contenido de la tabla de enrutamiento IP realizando una llamada a la función [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) .</span><span class="sxs-lookup"><span data-stu-id="918cf-107">Retrieve the contents of the IP routing table by making a call to the [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) function.</span></span> <span data-ttu-id="918cf-108">Manipular entradas específicas en la tabla de enrutamiento IP mediante las funciones [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)y [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) .</span><span class="sxs-lookup"><span data-stu-id="918cf-108">Manipulate specific entries in the IP routing table using the [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry), and [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) functions.</span></span> <span data-ttu-id="918cf-109">Utilice la función **CreateIpForwardEntry** para agregar una nueva entrada de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="918cf-109">Use the **CreateIpForwardEntry** function to add a new routing table entry.</span></span> <span data-ttu-id="918cf-110">Use la función **DeleteIpForwardEntry** para quitar una entrada existente.</span><span class="sxs-lookup"><span data-stu-id="918cf-110">Use the **DeleteIpForwardEntry** function to remove an existing entry.</span></span> <span data-ttu-id="918cf-111">La función **SetIpForwardEntry** modifica una entrada existente.</span><span class="sxs-lookup"><span data-stu-id="918cf-111">The **SetIpForwardEntry** function modifies an existing entry.</span></span>

<span data-ttu-id="918cf-112">Las capacidades de administración del enrutador de la aplicación auxiliar IP se pueden usar para recuperar información acerca de cómo se enrutan los datagramas a través de la red.</span><span class="sxs-lookup"><span data-stu-id="918cf-112">The router management capabilities of IP Helper can be used to retrieve information about how datagrams are routed over the network.</span></span> <span data-ttu-id="918cf-113">La función [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera la mejor ruta a una dirección de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="918cf-113">The [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) function retrieves the best route to a specified destination address.</span></span> <span data-ttu-id="918cf-114">La función [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera el índice de la interfaz utilizada por la mejor ruta a una dirección de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="918cf-114">The [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) function retrieves the index of the interface used by the best route to a specified destination address.</span></span> <span data-ttu-id="918cf-115">Por último, la función [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) recupera el tiempo de ida y vuelta (RTT) y el número de saltos a una dirección de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="918cf-115">Lastly, the [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) function retrieves the round-trip time (RTT) and number of hops to a specified destination address.</span></span>

 

 



