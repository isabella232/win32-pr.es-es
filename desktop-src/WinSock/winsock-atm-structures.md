---
description: En la lista siguiente se proporcionan descripciones concisas de cada estructura de ATM de Winsock. Para obtener información adicional sobre cualquier estructura, haga clic en el nombre de la estructura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Estructuras de ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715469"
---
# <a name="winsock-atm-structures"></a><span data-ttu-id="b4004-104">Estructuras de ATM de Winsock</span><span class="sxs-lookup"><span data-stu-id="b4004-104">Winsock ATM Structures</span></span>

<span data-ttu-id="b4004-105">En la lista siguiente se proporcionan descripciones concisas de cada estructura de ATM de Winsock.</span><span class="sxs-lookup"><span data-stu-id="b4004-105">The following list provides concise descriptions of each Winsock ATM structure.</span></span> <span data-ttu-id="b4004-106">Para obtener información adicional sobre cualquier estructura, haga clic en el nombre de la estructura.</span><span class="sxs-lookup"><span data-stu-id="b4004-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="b4004-107">Estructura ATM</span><span class="sxs-lookup"><span data-stu-id="b4004-107">ATM Structure</span></span>                           | <span data-ttu-id="b4004-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4004-108">Description</span></span>                                                |
|-----------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="b4004-109">**\_dirección ATM**</span><span class="sxs-lookup"><span data-stu-id="b4004-109">**ATM\_ADDRESS**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | <span data-ttu-id="b4004-110">Almacena datos de direcciones ATM para Sockets basados en ATM.</span><span class="sxs-lookup"><span data-stu-id="b4004-110">Stores ATM address data for ATM-based sockets.</span></span>             |
| [<span data-ttu-id="b4004-111">**\_BHLI ATM**</span><span class="sxs-lookup"><span data-stu-id="b4004-111">**ATM\_BHLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | <span data-ttu-id="b4004-112">Identifica la información de B-HLI para un socket ATM asociado.</span><span class="sxs-lookup"><span data-stu-id="b4004-112">Identifies B-HLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="b4004-113">**\_BLLI ATM**</span><span class="sxs-lookup"><span data-stu-id="b4004-113">**ATM\_BLLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | <span data-ttu-id="b4004-114">Identifica la información de B-LLI para un socket de ATM asociado.</span><span class="sxs-lookup"><span data-stu-id="b4004-114">Identifies B-LLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="b4004-115">**\_ATM sockaddr**</span><span class="sxs-lookup"><span data-stu-id="b4004-115">**sockaddr\_atm**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | <span data-ttu-id="b4004-116">Almacena la información de dirección de socket para Sockets ATM.</span><span class="sxs-lookup"><span data-stu-id="b4004-116">Stores socket address information for ATM sockets.</span></span>         |



 

<span data-ttu-id="b4004-117">En el caso de los servicios ATM nativos, use AF \_ ATM para la familia de direcciones y la estructura de direcciones de socket [**\_ ATM sockaddr**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) .</span><span class="sxs-lookup"><span data-stu-id="b4004-117">For native ATM services, use AF\_ATM for address family and the [**sockaddr\_atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) socket address structure.</span></span> <span data-ttu-id="b4004-118">Para abrir un socket ATM nativo, pase AF \_ ATM, sock \_ raw y ATMPROTO \_ AAL5 o ATMPROTO \_ AALUSER a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b4004-118">To open a native ATM socket, pass AF\_ATM, SOCK\_RAW, and ATMPROTO\_AAL5 or ATMPROTO\_AALUSER into the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function, respectively.</span></span>

 

 



