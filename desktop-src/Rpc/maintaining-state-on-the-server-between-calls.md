---
title: Mantener el estado en el servidor entre llamadas
description: A menudo es necesario mantener el estado en el servidor entre llamadas RPC independientes \ 8212; el uso de identificadores de contexto es la mejor manera de hacerlo. Unas cuantas palabras sobre cómo funcionan internamente los identificadores de contexto ayuda a comprender cuándo funcionan mejor los controles de contexto.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC llamada a procedimiento remoto, procedimientos recomendados, mantener el estado entre llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772721"
---
# <a name="maintaining-state-on-the-server-between-calls"></a><span data-ttu-id="8b48d-105">Mantener el estado en el servidor entre llamadas</span><span class="sxs-lookup"><span data-stu-id="8b48d-105">Maintaining State on the Server Between Calls</span></span>

<span data-ttu-id="8b48d-106">A menudo es necesario mantener el estado en el servidor entre llamadas RPC independientes; el uso de identificadores de contexto es la mejor manera de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="8b48d-106">It is often necessary to maintain state on the server between separate RPC calls—using context handles is the best way to do so.</span></span> <span data-ttu-id="8b48d-107">Unas cuantas palabras sobre cómo funcionan internamente los identificadores de contexto ayuda a comprender cuándo funcionan mejor los controles de contexto.</span><span class="sxs-lookup"><span data-stu-id="8b48d-107">A few words about how context handles operate internally helps in understanding when context handles work best.</span></span>

<span data-ttu-id="8b48d-108">El cliente nunca recibe el estado que se mantiene en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8b48d-108">The client never receives the state kept on the server.</span></span> <span data-ttu-id="8b48d-109">Normalmente, el estado del servidor es un puntero a un bloque de memoria y el cliente no tiene información sobre él.</span><span class="sxs-lookup"><span data-stu-id="8b48d-109">Most often the state on the server is a pointer to a memory block, and the client has no information about it.</span></span> <span data-ttu-id="8b48d-110">Todas las recepciones de cliente son un número único grande, con otra información asociada, que el servidor envía al cliente y que representa el identificador de contexto en todas las operaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8b48d-110">All the client receives is a large unique number, with other information associated with it, that the server sends to the client and which represents the context handle in all subsequent operations.</span></span> <span data-ttu-id="8b48d-111">Cada vez que el cliente hace referencia a un identificador abierto, envía el número grande recibido desde el servidor cuando se abre ese identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="8b48d-111">Whenever the client refers to an opened handle, it sends the large number it received from the server when that context handle was opened.</span></span>

<span data-ttu-id="8b48d-112">El servidor realiza un seguimiento de todos los números grandes que envía a un cliente.</span><span class="sxs-lookup"><span data-stu-id="8b48d-112">The server keeps track of all large numbers it sends to a client.</span></span> <span data-ttu-id="8b48d-113">Cuando el servidor recibe un número grande que representa un identificador de contexto, busca el número en la colección de identificadores de contexto vigentes y pendientes para ese cliente, y busca el contexto del servidor correspondiente a un número grande determinado.</span><span class="sxs-lookup"><span data-stu-id="8b48d-113">When the server receives a large number representing a context handle, it looks up the number in the collection of valid, outstanding context handles for that client, and finds the server-side context corresponding to a given large number.</span></span> <span data-ttu-id="8b48d-114">Esto se pasa a la rutina del servidor.</span><span class="sxs-lookup"><span data-stu-id="8b48d-114">This is passed to the server routine.</span></span> <span data-ttu-id="8b48d-115">Si no se encuentra el número grande, se genera una excepción de error de coincidencia de contexto de RPC \_ X \_ SS \_ \_ y se propaga al cliente.</span><span class="sxs-lookup"><span data-stu-id="8b48d-115">If the large number is not found, an RPC\_X\_SS\_CONTEXT\_MISMATCH exception is raised and propagated to the client.</span></span>

<span data-ttu-id="8b48d-116">La corollaries de este diseño es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8b48d-116">The corollaries of this design are as follows:</span></span>

-   <span data-ttu-id="8b48d-117">Un identificador de contexto solo es válido en el contexto de la sesión de cliente/servidor existente.</span><span class="sxs-lookup"><span data-stu-id="8b48d-117">A context handle is valid only in the context of the existing client/server session.</span></span> <span data-ttu-id="8b48d-118">No se puede pasar a otro cliente.</span><span class="sxs-lookup"><span data-stu-id="8b48d-118">It cannot be passed to another client.</span></span>
-   <span data-ttu-id="8b48d-119">Un identificador de contexto deja de ser válido si el servidor se reinicia o se pierde la conexión con el cliente.</span><span class="sxs-lookup"><span data-stu-id="8b48d-119">A context handle becomes invalid if the server is rebooted, or otherwise loses its connection to the client.</span></span>
-   <span data-ttu-id="8b48d-120">El cliente no puede interpretar lo que representa el identificador de contexto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8b48d-120">The client cannot interpret what the context handle represents on the server.</span></span> <span data-ttu-id="8b48d-121">Para un cliente, todos los identificadores de contexto son simplemente números grandes.</span><span class="sxs-lookup"><span data-stu-id="8b48d-121">To a client, all context handles are simply large numbers.</span></span>

<span data-ttu-id="8b48d-122">Si se produce un error en el cliente, el servidor recibirá una notificación y limpiará los identificadores de contexto mediante el mecanismo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="8b48d-122">If the client fails, the server will get a notification and will clean up its context handles using the run-down mechanism.</span></span>

 

 




