---
title: Escritura de un cliente o servidor RPC seguro
description: En esta sección se proporcionan recomendaciones de procedimientos recomendados para escribir un servidor o cliente RPC seguro.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- RPC llamada a procedimiento remoto, procedimientos recomendados, escribir un cliente o servidor seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078115"
---
# <a name="writing-a-secure-rpc-client-or-server"></a><span data-ttu-id="c03db-104">Escritura de un cliente o servidor RPC seguro</span><span class="sxs-lookup"><span data-stu-id="c03db-104">Writing a Secure RPC Client or Server</span></span>

<span data-ttu-id="c03db-105">En esta sección se proporcionan recomendaciones de procedimientos recomendados para escribir un servidor o cliente RPC seguro.</span><span class="sxs-lookup"><span data-stu-id="c03db-105">This section provides best practice recommendations for writing a secure RPC client or server.</span></span>

<span data-ttu-id="c03db-106">La información de esta sección se aplica a Windows 2000 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c03db-106">The information in this section applies to Windows 2000 and Windows XP.</span></span> <span data-ttu-id="c03db-107">Esta sección se aplica a todas las secuencias de protocolos, incluido [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="c03db-107">This section applies to all protocol sequences, including [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="c03db-108">Los desarrolladores suelen pensar en que **ncalrpc** no es un objetivo probable para un ataque, lo que no es cierto en un servidor de Terminal Server donde puede haber cientos de usuarios que tengan acceso a un servicio y poner en peligro o incluso detener un servicio puede llevar a adquirir acceso adicional.</span><span class="sxs-lookup"><span data-stu-id="c03db-108">Developers tend to think **ncalrpc** is not a probable target for an attack, which is not true on a terminal server where potentially hundreds of users have access to a service, and compromising or even bringing down a service can lead to acquiring extra access.</span></span>

<span data-ttu-id="c03db-109">Esta sección se divide en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c03db-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="c03db-110">Qué proveedor de seguridad usar</span><span class="sxs-lookup"><span data-stu-id="c03db-110">Which Security Provider To Use</span></span>](which-security-provider-to-use.md)
-   [<span data-ttu-id="c03db-111">Controlar la autenticación del cliente</span><span class="sxs-lookup"><span data-stu-id="c03db-111">Controlling Client Authentication</span></span>](controlling-client-authentication.md)
-   [<span data-ttu-id="c03db-112">Elección de un nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="c03db-112">Choosing an Authentication Level</span></span>](choosing-an-authentication-level.md)
-   [<span data-ttu-id="c03db-113">Elegir opciones de QOS de seguridad</span><span class="sxs-lookup"><span data-stu-id="c03db-113">Choosing Security QOS Options</span></span>](choosing-security-qos-options.md)
-   [<span data-ttu-id="c03db-114">Error común: suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor</span><span class="sxs-lookup"><span data-stu-id="c03db-114">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [<span data-ttu-id="c03db-115">Devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="c03db-115">Callbacks</span></span>](callbacks.md)
-   [<span data-ttu-id="c03db-116">Sesiones nulas</span><span class="sxs-lookup"><span data-stu-id="c03db-116">Null Sessions</span></span>](null-sessions.md)
-   [<span data-ttu-id="c03db-117">Usar la marca/Robust</span><span class="sxs-lookup"><span data-stu-id="c03db-117">Use the /robust Flag</span></span>](use-the-robust-flag.md)
-   [<span data-ttu-id="c03db-118">Técnicas de IDL para mejorar el diseño de la interfaz y el método</span><span class="sxs-lookup"><span data-stu-id="c03db-118">IDL Techniques for Better Interface and Method Design</span></span>](idl-techniques-for-better-interface-and-method-design.md)
-   [<span data-ttu-id="c03db-119">Identificadores de contexto STRICT y Type STRICT</span><span class="sxs-lookup"><span data-stu-id="c03db-119">Strict and Type Strict Context Handles</span></span>](strict-and-type-strict-context-handles.md)
-   [<span data-ttu-id="c03db-120">No confíe en su equipo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="c03db-120">Do Not Trust Your Peer</span></span>](do-not-trust-your-peer.md)
-   [<span data-ttu-id="c03db-121">No usar seguridad de extremo</span><span class="sxs-lookup"><span data-stu-id="c03db-121">Do Not Use Endpoint Security</span></span>](do-not-use-endpoint-security.md)
-   [<span data-ttu-id="c03db-122">Tenga cuidado con otros puntos de conexión RPC que se ejecuten en el mismo proceso</span><span class="sxs-lookup"><span data-stu-id="c03db-122">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [<span data-ttu-id="c03db-123">Compruebe que el servidor es quien dice ser</span><span class="sxs-lookup"><span data-stu-id="c03db-123">Verify The Server Is Who It Claims To Be</span></span>](verify-the-server-is-who-it-claims-to-be.md)
-   [<span data-ttu-id="c03db-124">Usar secuencias de protocolo estándar</span><span class="sxs-lookup"><span data-stu-id="c03db-124">Use Mainstream Protocol Sequences</span></span>](use-mainstream-protocol-sequences.md)
-   [<span data-ttu-id="c03db-125">¿Es seguro ahora mi servidor RPC?</span><span class="sxs-lookup"><span data-stu-id="c03db-125">How Secure is my RPC Server Now?</span></span>](how-secure-is-my-rpc-server-now.md)

 

 