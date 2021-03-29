---
title: ¿Cuál es el grado de seguridad de mi servidor RPC ahora?
description: Después de la seguridad que se describe en esta sección, que se proporciona en otra parte del SDK de RPC, y que generalmente se aceptan como prácticas de seguridad adecuadas, el resultado será un servidor muy seguro. Estos servidores están protegidos frente a ataques de penetración o infracciones de privacidad.
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994279"
---
# <a name="how-secure-is-my-rpc-server-now"></a><span data-ttu-id="d8603-104">¿Es seguro ahora mi servidor RPC?</span><span class="sxs-lookup"><span data-stu-id="d8603-104">How Secure is My RPC Server Now?</span></span>

<span data-ttu-id="d8603-105">Después de la seguridad que se describe en esta sección, que se proporciona en otra parte del SDK de RPC, y que generalmente se aceptan como prácticas de seguridad adecuadas, el resultado será un servidor muy seguro.</span><span class="sxs-lookup"><span data-stu-id="d8603-105">Following the security outlined in this section, provided elsewhere in the RPC SDK, and generally accepted as proper security practices, will result in a server that is very secure.</span></span> <span data-ttu-id="d8603-106">Estos servidores están protegidos frente a ataques de penetración o infracciones de privacidad.</span><span class="sxs-lookup"><span data-stu-id="d8603-106">Such servers are protected from penetration attacks or privacy breaches.</span></span>

<span data-ttu-id="d8603-107">Si el estado se mantiene entre las llamadas RPC, asegúrese de que un solo cliente no provoque la asignación de recursos excesivos, lo que podría denegar el servicio a otros clientes.</span><span class="sxs-lookup"><span data-stu-id="d8603-107">If state is kept between RPC calls, make sure a single client does not cause the allocation of excessive resources, which could potentially deny service to other clients.</span></span>

 

 




