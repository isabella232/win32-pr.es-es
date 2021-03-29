---
title: Error común suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor
description: Cuando los proveedores de seguridad se registran en el servidor con la función RpcServerRegisterAuthInfo, se agrega una opción, no un requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778876"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a><span data-ttu-id="222fa-103">Error común: suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor</span><span class="sxs-lookup"><span data-stu-id="222fa-103">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>

<span data-ttu-id="222fa-104">Cuando los proveedores de seguridad se registran en el servidor con la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , se agrega una opción, no un requisito.</span><span class="sxs-lookup"><span data-stu-id="222fa-104">When security providers are registered on the server with the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function, an option is added, not a requirement.</span></span> <span data-ttu-id="222fa-105">Esto significa que los registros anteriores con **RpcServerRegisterAuthInfo** no se reemplazan.</span><span class="sxs-lookup"><span data-stu-id="222fa-105">This means previous registrations with **RpcServerRegisterAuthInfo** are not replaced.</span></span> <span data-ttu-id="222fa-106">Esto también significa que los clientes no autenticados todavía pueden conectarse.</span><span class="sxs-lookup"><span data-stu-id="222fa-106">This also means unauthenticated clients still can connect.</span></span> <span data-ttu-id="222fa-107">Al llamar a la función **RpcServerRegisterAuthInfo** , no se impide que los clientes no autenticados se conecten; todavía se pueden conectar, pero se producirá un error en las llamadas de función como [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) .</span><span class="sxs-lookup"><span data-stu-id="222fa-107">By calling the **RpcServerRegisterAuthInfo** function, unauthenticated clients are not disallowed from connecting; they can still connect, but function calls such as [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) will fail.</span></span> <span data-ttu-id="222fa-108">Por tanto, cuando se llama a la función **RpcServerRegisterAuthInfo** , los atacantes potenciales no se han extraído, sino que los clientes que deberían tener acceso tienen la oportunidad de demostrar su identidad.</span><span class="sxs-lookup"><span data-stu-id="222fa-108">So when the **RpcServerRegisterAuthInfo** function is called, potential attackers have not been weeded out—rather, clients that ought to have access are given a chance to prove their identity.</span></span> <span data-ttu-id="222fa-109">Las comprobaciones deben seguir vigentes para determinar si los posibles atacantes intentan conectarse.</span><span class="sxs-lookup"><span data-stu-id="222fa-109">Checks must still be in place to determine whether potential attackers are attempting to connect.</span></span>

 

 




