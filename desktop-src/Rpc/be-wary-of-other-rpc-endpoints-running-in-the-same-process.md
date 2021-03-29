---
title: Tenga cuidado con otros puntos de conexión RPC que se ejecuten en el mismo proceso
description: Cuando una aplicación reside en un proceso con otros servidores RPC, todas las aplicaciones escuchan en todos los protocolos.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777107"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a><span data-ttu-id="fc92f-103">Tenga cuidado con otros puntos de conexión RPC que se ejecuten en el mismo proceso</span><span class="sxs-lookup"><span data-stu-id="fc92f-103">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>

<span data-ttu-id="fc92f-104">Cuando una aplicación reside en un proceso con otros servidores RPC, todas las aplicaciones escuchan en todos los protocolos.</span><span class="sxs-lookup"><span data-stu-id="fc92f-104">When an application resides in a process with other RPC servers, all applications listen on all protocols.</span></span> <span data-ttu-id="fc92f-105">Como tal, si un componente llama a [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* solo para lrpc, no es necesariamente accesible a través de lrpc.</span><span class="sxs-lookup"><span data-stu-id="fc92f-105">As such, if a component calls [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* for LRPC only, it is not necessarily accessible over LRPC only.</span></span> <span data-ttu-id="fc92f-106">Puede ser accesible a través de otros protocolos, ya que es posible que otros servidores RPC del proceso estén escuchando en canalizaciones o Sockets (por ejemplo,).</span><span class="sxs-lookup"><span data-stu-id="fc92f-106">It may be accessible over other protocols, since other RPC servers in the process may be listening on pipes or sockets (for example).</span></span>

<span data-ttu-id="fc92f-107">De forma similar a los identificadores de contexto estrictos, no colocar otro extremo en el proceso no significa que no exista otro extremo.</span><span class="sxs-lookup"><span data-stu-id="fc92f-107">Similar to strict context handles, not putting another endpoint in the process does not mean another endpoint does not exist.</span></span> <span data-ttu-id="fc92f-108">Independientemente de cómo registre el servidor, no hay ninguna asociación especial entre la interfaz y el punto de conexión; todas las interfaces son Invocables en todos los puntos de conexión de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="fc92f-108">Regardless of how you register your server, there is no special association between your interface and your endpoint; all interfaces are callable on all endpoints in that process.</span></span> <span data-ttu-id="fc92f-109">Este es otro motivo por el que el modelo de seguridad del extremo es ineficaz. Si un descriptor de seguridad se coloca en un punto de conexión, los atacantes pueden llamar a la interfaz en otro punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="fc92f-109">This is another reason why the endpoint security model is ineffective; if a security descriptor is placed on an endpoint, attackers can call the interface on another endpoint.</span></span>

<span data-ttu-id="fc92f-110">Para asegurarse de que se llame a un proceso solo en una secuencia de protocolo específica, registre una función de devolución de llamada de seguridad y, en esa función, compruebe en qué secuencia de protocolos se realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="fc92f-110">To ensure a process be called only on a specific protocol sequence, register a security callback function, and in that function, check on which protocol sequence the call is made.</span></span>

 

 




