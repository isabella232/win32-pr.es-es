---
title: RPC y la red
description: En esta sección se describe cómo tratar la no confiabilidad de la red cuando se usa RPC y se explica cómo las API de nivel de RPC se traducen en la actividad de red. La sección solo se refiere a \_ las \_ secuencias de protocolo TCP IP ncacn y ncacn \_ http.
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- RPC (llamada a procedimiento remoto), procedimientos recomendados, RPC y la red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149501"
---
# <a name="rpc-and-the-network"></a><span data-ttu-id="38588-105">RPC y la red</span><span class="sxs-lookup"><span data-stu-id="38588-105">RPC and the Network</span></span>

<span data-ttu-id="38588-106">En esta sección se describe cómo tratar la no confiabilidad de la red cuando se usa RPC y se explica cómo las API de nivel de RPC se traducen en la actividad de red.</span><span class="sxs-lookup"><span data-stu-id="38588-106">This section discusses how to deal with network unreliability when using RPC, and explains how RPC-level APIs translate into network activity.</span></span> <span data-ttu-id="38588-107">La sección solo se refiere a las secuencias de protocolo [**\_ \_ TCP IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) y [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http) .</span><span class="sxs-lookup"><span data-stu-id="38588-107">The section refers only to the [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) and [**ncacn\_http**](/windows/desktop/Midl/ncacn-http) protocol sequences.</span></span>

<span data-ttu-id="38588-108">Esta sección se divide en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="38588-108">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="38588-109">Desarrollo frente a implementación en la red</span><span class="sxs-lookup"><span data-stu-id="38588-109">Development Versus Deployment in the Network</span></span>](development-versus-deployment-in-the-network.md)
-   [<span data-ttu-id="38588-110">Evitar bloqueos Client-Side</span><span class="sxs-lookup"><span data-stu-id="38588-110">Preventing Client-Side Hangs</span></span>](preventing-client-side-hangs.md)
-   [<span data-ttu-id="38588-111">Administración de conjuntos de conexiones de red (asociaciones)</span><span class="sxs-lookup"><span data-stu-id="38588-111">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
-   [<span data-ttu-id="38588-112">Limpieza de conexión inactiva</span><span class="sxs-lookup"><span data-stu-id="38588-112">Idle Connection Cleanup</span></span>](idle-connection-cleanup.md)
-   [<span data-ttu-id="38588-113">Tratamiento de la pérdida de conectividad</span><span class="sxs-lookup"><span data-stu-id="38588-113">Dealing with Loss of Connectivity</span></span>](dealing-with-loss-of-connectivity.md)
-   [<span data-ttu-id="38588-114">Limpieza del lado servidor</span><span class="sxs-lookup"><span data-stu-id="38588-114">Server Side Cleanup</span></span>](server-side-cleanup.md)

 

 