---
title: Tráfico de multidifusión/difusión ALE
description: Todo el tráfico de multidifusión y difusión entrante en las capas de aplicación de nivel de aplicación (ALE) se asigna a un flujo ALE global.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357030"
---
# <a name="ale-multicastbroadcast-traffic"></a><span data-ttu-id="9d6e4-103">Tráfico de multidifusión/difusión ALE</span><span class="sxs-lookup"><span data-stu-id="9d6e4-103">ALE Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="9d6e4-104">Todo el tráfico de multidifusión y difusión entrante en las capas de aplicación de nivel de aplicación (ALE) se asigna a un [flujo ALE](ale-stateful-filtering.md)global.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-104">All inbound multicast and broadcast traffic at the Application Layer Enforcement (ALE) layers is mapped to one global [ALE flow](ale-stateful-filtering.md).</span></span> <span data-ttu-id="9d6e4-105">El tráfico de respuesta para los paquetes de difusión y multidifusión entrantes se clasifica en el nivel de FWPM de la [**\_ autenticación Ale de capa de \_ \_ \_ conexión \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) y se crean flujos de Ale independientes para cada respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-105">Response traffic for inbound multicast and broadcast packets is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and separate ALE flows are created for each response.</span></span>

<span data-ttu-id="9d6e4-106">El tráfico de multidifusión y difusión saliente en los niveles de ALE crea un flujo de ALE de 4 segundos.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-106">Outbound multicast and broadcast traffic at the ALE layers creates a 4-second ALE flow.</span></span> <span data-ttu-id="9d6e4-107">De forma predeterminada, la autorización de un paquete ALE de multidifusión o de difusión de salida permitirá el tráfico entrante, ya sea unidifusión, multidifusión o difusión, desde cualquier dirección remota durante un máximo de 4 segundos.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-107">By default, the authorization of an outbound multicast or broadcast ALE packet will permit inbound traffic, whether unicast, multicast, or broadcast, from any remote address for up to 4 seconds.</span></span> <span data-ttu-id="9d6e4-108">Este tipo de flujo ALE solo se puede actualizar o mantener activo mediante el siguiente tráfico saliente que coincida con el flujo de ALE.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-108">Such an ALE flow can only be refreshed or kept alive by subsequent outbound traffic that matches the ALE flow.</span></span>

> [!Note]  
> <span data-ttu-id="9d6e4-109">La duración de 4 segundos se especifica mediante las opciones del conjunto de [**llamada FWPM de llamada integrada \_ \_ \_ OPTION \_ \_ Connect \_ Layer \_ V {4 \| 6}**](built-in-callout-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="9d6e4-109">The 4-second lifetime is specified by the built-in callout [**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}**](built-in-callout-identifiers.md).</span></span> <span data-ttu-id="9d6e4-110">Para modificar la duración predeterminada de 4 segundos, agregue un filtro que haga referencia a las **\_ Opciones del conjunto de llamadas FWPM \_ \_ \_ auth \_ Connect \_ Layer \_ V {4 \| 6}** CALLOUT.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-110">To alter the 4-second default lifetime, add a filter that references the **FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}** callout.</span></span> <span data-ttu-id="9d6e4-111">Para obtener más información, consulte [Personalización del flujo ALE](ale-flow-customization.md) .</span><span class="sxs-lookup"><span data-stu-id="9d6e4-111">See [ALE Flow Customization](ale-flow-customization.md) for more information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9d6e4-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d6e4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d6e4-113">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="9d6e4-113">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-114">Niveles ALE</span><span class="sxs-lookup"><span data-stu-id="9d6e4-114">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-115">Filtrado con estado ALE</span><span class="sxs-lookup"><span data-stu-id="9d6e4-115">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-116">Reautorización de ALE</span><span class="sxs-lookup"><span data-stu-id="9d6e4-116">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-117">Personalización del flujo ALE</span><span class="sxs-lookup"><span data-stu-id="9d6e4-117">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 




