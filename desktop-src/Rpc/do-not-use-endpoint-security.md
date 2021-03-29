---
title: No usar seguridad de extremo
description: La seguridad del punto de conexión es un modelo de seguridad en el que se proporciona un descriptor de seguridad cuando se crea un punto de conexión con el grupo de funciones RPC RpcServerUseProtseq \.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775498"
---
# <a name="do-not-use-endpoint-security"></a><span data-ttu-id="15e30-103">No usar seguridad de extremo</span><span class="sxs-lookup"><span data-stu-id="15e30-103">Do Not Use Endpoint Security</span></span>

<span data-ttu-id="15e30-104">La seguridad del punto de conexión es un modelo de seguridad en el que se proporciona un descriptor [](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) de seguridad cuando se crea un punto de conexión con el \* grupo de RPCSERVERUSEPROTSEQ de funciones RPC.</span><span class="sxs-lookup"><span data-stu-id="15e30-104">Endpoint security is a security model in which a security descriptor is given when an endpoint is created with the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* group of RPC functions.</span></span> <span data-ttu-id="15e30-105">No utilice este modelo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="15e30-105">Do not use this security model.</span></span> <span data-ttu-id="15e30-106">No proporcione descriptores de seguridad a esas funciones.</span><span class="sxs-lookup"><span data-stu-id="15e30-106">Do not give security descriptors to those functions.</span></span> <span data-ttu-id="15e30-107">Como es mejor, este método es un desperdicio de recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="15e30-107">At best, this method is a waste of CPU resources.</span></span> <span data-ttu-id="15e30-108">En el peor de los entornos, es posible eludir el descriptor de seguridad, ya que los [puntos de conexión RPC que se ejecutan en la misma](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) sección de proceso ejemplifican.</span><span class="sxs-lookup"><span data-stu-id="15e30-108">At worst, in many environments it is possible to circumvent the security descriptor, as the [Be Wary of Other RPC Endpoints Running In the Same Process](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) section exemplifies.</span></span>

<span data-ttu-id="15e30-109">La seguridad del punto de conexión solo existe para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="15e30-109">Endpoint security exists only for backward compatibility.</span></span>

 

 




