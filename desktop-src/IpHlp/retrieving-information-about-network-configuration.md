---
description: La aplicación auxiliar de IP proporciona información acerca de la configuración de red del equipo local.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Recuperación de información acerca de la configuración de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002859"
---
# <a name="retrieving-information-about-network-configuration"></a><span data-ttu-id="95b59-103">Recuperación de información acerca de la configuración de red</span><span class="sxs-lookup"><span data-stu-id="95b59-103">Retrieving Information About Network Configuration</span></span>

<span data-ttu-id="95b59-104">La aplicación auxiliar de IP proporciona información acerca de la configuración de red del equipo local.</span><span class="sxs-lookup"><span data-stu-id="95b59-104">IP Helper provides information about the network configuration of the local computer.</span></span> <span data-ttu-id="95b59-105">Para recuperar la información de configuración general, utilice la función [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="95b59-105">To retrieve general configuration information, use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="95b59-106">Esta función devuelve información que no es específica de un adaptador o una interfaz concretos.</span><span class="sxs-lookup"><span data-stu-id="95b59-106">This function returns information that is not specific to a particular adapter or interface.</span></span> <span data-ttu-id="95b59-107">Por ejemplo, **GetNetworkParams** devuelve una lista de los servidores DNS que usa el equipo local.</span><span class="sxs-lookup"><span data-stu-id="95b59-107">For example, **GetNetworkParams** returns a list of the DNS servers that are used by the local computer.</span></span>

-   <span data-ttu-id="95b59-108">Para obtener ejemplos de código que impliquen a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , vea [recuperar información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span><span class="sxs-lookup"><span data-stu-id="95b59-108">For code samples involving [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) see [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span></span>

 

 



