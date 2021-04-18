---
title: Modo de túnel
description: El escenario de directiva IPsec de modo de túnel se usa para aplicar la protección del modo de túnel IPsec para todo el tráfico coincidente entre dos extremos de túnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357429"
---
# <a name="tunnel-mode"></a><span data-ttu-id="27824-103">Modo de túnel</span><span class="sxs-lookup"><span data-stu-id="27824-103">Tunnel Mode</span></span>

<span data-ttu-id="27824-104">El escenario de directiva IPsec de modo de túnel se usa para aplicar la protección del modo de túnel IPsec para todo el tráfico coincidente entre dos extremos de túnel.</span><span class="sxs-lookup"><span data-stu-id="27824-104">The Tunnel Mode IPsec policy scenario is used to apply IPsec tunnel mode protection for all matching traffic between two tunnel endpoints.</span></span>

<span data-ttu-id="27824-105">Este escenario de Directiva se usa normalmente para proteger el tráfico entre varias subredes de sucursal, cuando se reenvía entre las puertas de enlace correspondientes en Internet.</span><span class="sxs-lookup"><span data-stu-id="27824-105">This policy scenario is typically used to protect traffic between multiple branch-office subnets, when it gets forwarded between the corresponding gateways on the Internet.</span></span> <span data-ttu-id="27824-106">También se puede usar para proteger la comunicación de un extremo a otro entre dos equipos host, también denominados túneles punto a punto.</span><span class="sxs-lookup"><span data-stu-id="27824-106">It can also be used to secure end-to-end communication between two host machines, also referred to as point-to-point tunnels.</span></span>

<span data-ttu-id="27824-107">Para implementar la Directiva de modo de túnel mediante la plataforma de filtrado de Windows (WFP), llame a la función [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) que crea instancias de los filtros de modo de túnel adecuados en las capas adecuadas en nombre del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="27824-107">To implement Tunnel Mode policy using the Windows Filtering Platform (WFP), call the [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) function that instantiates the appropriate tunnel mode filters at the appropriate layers on behalf of the caller.</span></span> <span data-ttu-id="27824-108">El autor de la llamada debe especificar el modo principal, los contextos de proveedor de modo rápido y las condiciones de filtro que describen el tráfico que debe protegerse dentro del túnel.</span><span class="sxs-lookup"><span data-stu-id="27824-108">The caller needs to specify the Main Mode, Quick Mode provider contexts, and the filter conditions describing the traffic that should be secured inside the tunnel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27824-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27824-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27824-110">Código de ejemplo: uso del modo de túnel</span><span class="sxs-lookup"><span data-stu-id="27824-110">Sample code: Using Tunnel Mode</span></span>](using-tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="27824-111">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="27824-111">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




