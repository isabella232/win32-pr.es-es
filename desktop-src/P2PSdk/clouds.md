---
description: Las nubes se usan en las infraestructuras de agrupación y gráficos del mismo nivel.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Nubes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156541"
---
# <a name="clouds"></a><span data-ttu-id="be5be-103">Nubes</span><span class="sxs-lookup"><span data-stu-id="be5be-103">Clouds</span></span>

<span data-ttu-id="be5be-104">Las nubes se usan en las infraestructuras de [agrupación](grouping-api.md) y [gráficos](graphing-api.md) del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="be5be-104">Clouds are used by the Peer [Grouping](grouping-api.md) and [Graphing](graphing-api.md) Infrastructures.</span></span> <span data-ttu-id="be5be-105">El [Protocolo de resolución de nombres de mismo nivel (PNRP)](pnrp-namespace-provider-api.md) identifica una nube como un conjunto de elementos del mismo nivel que pueden comunicarse en el mismo ámbito de IPv6.</span><span class="sxs-lookup"><span data-stu-id="be5be-105">The [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifies a cloud as a set of peers that can communicate within the same IPv6 scope.</span></span> <span data-ttu-id="be5be-106">Las nubes están estrechamente relacionadas con los ámbitos IPv6.</span><span class="sxs-lookup"><span data-stu-id="be5be-106">Clouds are closely related to the IPv6 scopes.</span></span> <span data-ttu-id="be5be-107">En la siguiente lista se identifican algunas de las características únicas de la nube:</span><span class="sxs-lookup"><span data-stu-id="be5be-107">The following list identifies some of the unique cloud features:</span></span>

-   <span data-ttu-id="be5be-108">Una nube se identifica mediante un nombre y las nubes disponibles se pueden enumerar mediante [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="be5be-108">A cloud is identified by a name, and available clouds can be enumerated by using [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span></span>
-   <span data-ttu-id="be5be-109">Si un equipo está conectado a Internet, forma parte de una nube global, que se identifica mediante la cadena "global \_ ".</span><span class="sxs-lookup"><span data-stu-id="be5be-109">If a computer is connected to the Internet, it is part of a global cloud, which is identified by the string "Global\_".</span></span>
-   <span data-ttu-id="be5be-110">Si un equipo está conectado a una o más redes de área local (LAN), las nubes individuales estarán disponibles para cada vínculo.</span><span class="sxs-lookup"><span data-stu-id="be5be-110">If a computer is connected to one or more local area networks (LAN), individual clouds are available for each link.</span></span>
-   <span data-ttu-id="be5be-111">Un equipo puede estar conectado a muchas redes con varios adaptadores de red o mediante una red privada virtual (VPN), lo que significa que un equipo con una interfaz puede estar visible en muchas nubes.</span><span class="sxs-lookup"><span data-stu-id="be5be-111">One computer can be connected to many networks by having multiple network adapters or by using a virtual private network (VPN), which means that a computer with one interface can be visible in many clouds.</span></span>
-   <span data-ttu-id="be5be-112">Puede usar PNRP para registrar y resolver nombres de mismo nivel en una nube específica.</span><span class="sxs-lookup"><span data-stu-id="be5be-112">You can use PNRP to register and resolve peer names in a specific cloud.</span></span>

 

 



