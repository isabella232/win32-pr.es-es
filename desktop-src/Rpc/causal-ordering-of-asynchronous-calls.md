---
title: Ordenación causal de llamadas asincrónicas
description: En una aplicación RPC asincrónica, es posible que un subproceso de cliente realice una segunda llamada asincrónica en un identificador de enlace antes de que se haya completado una llamada anterior realizada en ese controlador.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075643"
---
# <a name="causal-ordering-of-asynchronous-calls"></a><span data-ttu-id="36fb4-103">Ordenación causal de llamadas asincrónicas</span><span class="sxs-lookup"><span data-stu-id="36fb4-103">Causal Ordering of Asynchronous Calls</span></span>

<span data-ttu-id="36fb4-104">En una aplicación RPC asincrónica, es posible que un subproceso de cliente realice una segunda llamada asincrónica en un identificador de enlace antes de que se haya completado una llamada anterior realizada en ese controlador.</span><span class="sxs-lookup"><span data-stu-id="36fb4-104">In an asynchronous RPC application, it is possible for a client thread to make a second asynchronous call on a binding handle before an earlier call made on that handle has completed.</span></span> <span data-ttu-id="36fb4-105">La biblioteca en tiempo de ejecución de RPC controla esta situación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="36fb4-105">The RPC run-time library handles this situation as follows:</span></span>

-   <span data-ttu-id="36fb4-106">El mecanismo RPC asincrónico garantiza que las llamadas asincrónicas realizadas en el mismo identificador de enlace, en el mismo subproceso, en el mismo nivel de seguridad, se envíen en el orden en el que se realizaron.</span><span class="sxs-lookup"><span data-stu-id="36fb4-106">The asynchronous RPC mechanism guarantees that asynchronous calls made on the same binding handle, on the same thread, at the same security level, are dispatched in the order they were made.</span></span> <span data-ttu-id="36fb4-107">La ejecución real de las llamadas puede producirse sin orden.</span><span class="sxs-lookup"><span data-stu-id="36fb4-107">Actual execution of the calls may occur out of order.</span></span>
-   <span data-ttu-id="36fb4-108">Al igual que con las llamadas sincrónicas, las llamadas a procedimientos remotos asincrónicas de diferentes subprocesos de cliente se ejecutan simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="36fb4-108">As with synchronous calls, asynchronous remote procedure calls from different client threads execute simultaneously.</span></span>
-   <span data-ttu-id="36fb4-109">Si una llamada asincrónica desde una aplicación cliente va seguida de una o más llamadas sincrónicas, la llamada asincrónica se puede ejecutar mientras se ejecutan las llamadas sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="36fb4-109">If an asynchronous call from a client application is followed by one or more synchronous calls, the asynchronous call can execute while the synchronous calls are executing.</span></span> <span data-ttu-id="36fb4-110">Independientemente del estado de la llamada asincrónica, las llamadas sincrónicas se ejecutan en el orden en que se reciben en el servidor.</span><span class="sxs-lookup"><span data-stu-id="36fb4-110">Regardless of the status of the asynchronous call, the synchronous calls are executed in the order in which they are received by the server.</span></span>
-   <span data-ttu-id="36fb4-111">Si una aplicación cliente selecciona una ordenación no causal para un identificador de enlace determinado, deshabilita la serialización de ese identificador.</span><span class="sxs-lookup"><span data-stu-id="36fb4-111">If a client application selects noncausal ordering for a particular binding handle, it disables serialization for that handle.</span></span> <span data-ttu-id="36fb4-112">Las aplicaciones habilitan la ordenación no causal mediante una llamada a [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con el parámetro *Option* establecido en el enlace no causal de RPC \_ C \_ \_ \_ y el parámetro *OptionValue* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="36fb4-112">Applications enable noncausal ordering by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) with the *Option* parameter set to RPC\_C\_OPT\_BINDING\_NONCAUSAL and the *OptionValue* parameter set to **TRUE**.</span></span> <span data-ttu-id="36fb4-113">Para obtener más información, consulte [constantes de opciones de enlace](binding-option-constants.md).</span><span class="sxs-lookup"><span data-stu-id="36fb4-113">For details, see [Binding Option Constants](binding-option-constants.md).</span></span>

 

 




