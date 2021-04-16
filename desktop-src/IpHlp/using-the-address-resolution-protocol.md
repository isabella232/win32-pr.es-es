---
description: Puede usar la aplicación auxiliar de IP para realizar operaciones del Protocolo de resolución de direcciones (ARP) para el equipo local. Utilice las siguientes funciones para recuperar y modificar la tabla ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Usar el protocolo de resolución de direcciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678407"
---
# <a name="using-the-address-resolution-protocol"></a><span data-ttu-id="2d417-104">Usar el protocolo de resolución de direcciones</span><span class="sxs-lookup"><span data-stu-id="2d417-104">Using the Address Resolution Protocol</span></span>

<span data-ttu-id="2d417-105">Puede usar la aplicación auxiliar de IP para realizar operaciones del Protocolo de resolución de direcciones (ARP) para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="2d417-105">You can use IP Helper to perform Address Resolution Protocol (ARP) operations for the local computer.</span></span> <span data-ttu-id="2d417-106">Utilice las siguientes funciones para recuperar y modificar la tabla ARP.</span><span class="sxs-lookup"><span data-stu-id="2d417-106">Use the following functions to retrieve and modify the ARP table.</span></span>

<span data-ttu-id="2d417-107">[**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) recupera la tabla ARP.</span><span class="sxs-lookup"><span data-stu-id="2d417-107">The [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) retrieves the ARP table.</span></span> <span data-ttu-id="2d417-108">La tabla ARP contiene la asignación de direcciones IP a direcciones físicas.</span><span class="sxs-lookup"><span data-stu-id="2d417-108">The ARP table contains the mapping of IP addresses to physical addresses.</span></span> <span data-ttu-id="2d417-109">Las direcciones físicas a veces se denominan direcciones de controlador de acceso a medios (MAC).</span><span class="sxs-lookup"><span data-stu-id="2d417-109">Physical addresses are sometimes referred to as Media Access Controller (MAC) addresses.</span></span>

<span data-ttu-id="2d417-110">Use las funciones [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) y [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) para agregar o quitar determinadas entradas ARP de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2d417-110">Use the [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) and [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) functions to add or remove particular ARP entries to or from the table.</span></span> <span data-ttu-id="2d417-111">La función [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) elimina todas las entradas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2d417-111">The [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) function deletes all entries from the table.</span></span>

<span data-ttu-id="2d417-112">Para crear o eliminar entradas ARP de proxy, utilice las funciones [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) y [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .</span><span class="sxs-lookup"><span data-stu-id="2d417-112">To create or delete proxy ARP entries, use the [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) and [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) functions.</span></span>

<span data-ttu-id="2d417-113">La función [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envía una solicitud ARP a la red local.</span><span class="sxs-lookup"><span data-stu-id="2d417-113">The [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) function sends an ARP request to the local network.</span></span>

 

 



