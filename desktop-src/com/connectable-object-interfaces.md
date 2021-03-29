---
title: Interfaces de objeto conectables
description: Interfaces de objeto conectables
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903856"
---
# <a name="connectable-object-interfaces"></a><span data-ttu-id="a780b-103">Interfaces de objeto conectables</span><span class="sxs-lookup"><span data-stu-id="a780b-103">Connectable Object Interfaces</span></span>

<span data-ttu-id="a780b-104">La compatibilidad con objetos conectables requiere la compatibilidad con cuatro interfaces:</span><span class="sxs-lookup"><span data-stu-id="a780b-104">Support for connectable objects requires support for four interfaces:</span></span>

-   <span data-ttu-id="a780b-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) en el objeto conectable</span><span class="sxs-lookup"><span data-stu-id="a780b-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) on the connectable object</span></span>
-   <span data-ttu-id="a780b-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) en el objeto de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="a780b-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) on the connection point object</span></span>
-   <span data-ttu-id="a780b-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) en un objeto enumerador</span><span class="sxs-lookup"><span data-stu-id="a780b-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) on an enumerator object</span></span>
-   <span data-ttu-id="a780b-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) en un objeto enumerador</span><span class="sxs-lookup"><span data-stu-id="a780b-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) on an enumerator object</span></span>

<span data-ttu-id="a780b-109">Los dos últimos se definen como enumeradores estándar para los tipos **IConnectionPoint \*** y [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span><span class="sxs-lookup"><span data-stu-id="a780b-109">The latter two are defined as standard enumerators for the types **IConnectionPoint \*** and [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span></span>

<span data-ttu-id="a780b-110">Además, el objeto conectable puede admitir opcionalmente [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) y [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para proporcionar suficiente información a un cliente para que el cliente pueda proporcionar compatibilidad con la interfaz de salida en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a780b-110">Additionally, the connectable object can optionally support [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) to provide enough information to a client so that the client can provide support for the outgoing interface at run time.</span></span>

<span data-ttu-id="a780b-111">Por último, el cliente debe proporcionar un objeto de receptor que implementa la interfaz de salida, que es una interfaz COM personalizada definida por el objeto conectable.</span><span class="sxs-lookup"><span data-stu-id="a780b-111">Finally, the client must provide a sink object that implements the outgoing interface, which is a custom COM interface defined by the connectable object.</span></span>

<span data-ttu-id="a780b-112">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a780b-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a780b-113">Usar IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a780b-113">Using IConnectionPointContainer</span></span>](using-iconnectionpointcontainer.md)
-   [<span data-ttu-id="a780b-114">Usar IConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="a780b-114">Using IConnectionPoint</span></span>](using-iconnectionpoint.md)
-   [<span data-ttu-id="a780b-115">Usar IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="a780b-115">Using IProvideClassInfo</span></span>](using-iprovideclassinfo.md)

## <a name="related-topics"></a><span data-ttu-id="a780b-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a780b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a780b-117">Arquitectura de objetos conectables</span><span class="sxs-lookup"><span data-stu-id="a780b-117">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




