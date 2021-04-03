---
title: Atributos de llamada de función
description: Los programas pueden utilizar estos atributos en funciones individuales dentro de la interfaz y solo afectan a esa función.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- MIDL, atributos, llamada de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779620"
---
# <a name="function-call-attributes"></a><span data-ttu-id="79c8b-104">Atributos de llamada de función</span><span class="sxs-lookup"><span data-stu-id="79c8b-104">Function Call Attributes</span></span>

<span data-ttu-id="79c8b-105">Los programas pueden utilizar estos atributos en funciones individuales dentro de la interfaz y solo afectan a esa función.</span><span class="sxs-lookup"><span data-stu-id="79c8b-105">Programs can use these attributes on individual functions within the interface, and affect only that function.</span></span>



| <span data-ttu-id="79c8b-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="79c8b-106">Attribute</span></span>                        | <span data-ttu-id="79c8b-107">Uso</span><span class="sxs-lookup"><span data-stu-id="79c8b-107">Usage</span></span>                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79c8b-108">**Mensaje**</span><span class="sxs-lookup"><span data-stu-id="79c8b-108">**message**</span></span>](message.md)       | <span data-ttu-id="79c8b-109">La llamada a procedimiento remoto se tratará como un mensaje asíncrono desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="79c8b-109">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="79c8b-110">El cliente realiza la llamada y se devuelve inmediatamente, mientras que la llamada real se controla mediante el transporte de cola de mensajes ([**ncadg \_ MQ**](ncadg-mq.md)).</span><span class="sxs-lookup"><span data-stu-id="79c8b-110">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span> |
| [<span data-ttu-id="79c8b-111">**incluso**</span><span class="sxs-lookup"><span data-stu-id="79c8b-111">**maybe**</span></span>](maybe.md)           | <span data-ttu-id="79c8b-112">El cliente que realiza esta llamada a procedimiento remoto no espera ninguna respuesta que indique la entrega o la finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="79c8b-112">The client making this remote procedure call does not expect any response indicating delivery or completion of the call.</span></span> <span data-ttu-id="79c8b-113">Esto contrasta con las operaciones de [**mensajes**](message.md) en las que no se espera ninguna respuesta, pero se garantiza la entrega.</span><span class="sxs-lookup"><span data-stu-id="79c8b-113">This is in contrast to [**message**](message.md) operations where no response is expected but the delivery is guaranteed.</span></span>        |
| [<span data-ttu-id="79c8b-114">**amplia**</span><span class="sxs-lookup"><span data-stu-id="79c8b-114">**broadcast**</span></span>](broadcast.md)   | <span data-ttu-id="79c8b-115">La llamada a procedimiento remoto se va a enviar a todos los servidores de la red.</span><span class="sxs-lookup"><span data-stu-id="79c8b-115">The remote procedure call is to be sent to all of the servers on the network.</span></span> <span data-ttu-id="79c8b-116">El cliente acepta la primera devolución, las respuestas posteriores de otros servidores se descartan.</span><span class="sxs-lookup"><span data-stu-id="79c8b-116">The client accepts the first return, subsequent replies from other servers are discarded.</span></span>                                                                                    |
| [<span data-ttu-id="79c8b-117">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="79c8b-117">**idempotent**</span></span>](idempotent.md) | <span data-ttu-id="79c8b-118">La llamada no cambia el estado y devuelve la misma información cada vez que se llama con los mismos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="79c8b-118">The call does not change state and returns the same information each time it is called with the same input parameters.</span></span>                                                                                                                                     |
| [<span data-ttu-id="79c8b-119">**devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="79c8b-119">**callback**</span></span>](callback.md)     | <span data-ttu-id="79c8b-120">Designa una función que reside en la aplicación cliente, a la que el servidor puede llamar para obtener información del cliente.</span><span class="sxs-lookup"><span data-stu-id="79c8b-120">Designates a function that resides in the client application, which the server can call to obtain information from the client.</span></span>                                                                                                                             |
| [<span data-ttu-id="79c8b-121">**llamar a \_ como**</span><span class="sxs-lookup"><span data-stu-id="79c8b-121">**call\_as**</span></span>](call-as.md)      | <span data-ttu-id="79c8b-122">Asigna una función no utilizables a una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="79c8b-122">Maps a nonremotable function to a remote procedure call.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="79c8b-123">**localizar**</span><span class="sxs-lookup"><span data-stu-id="79c8b-123">**local**</span></span>](local.md)           | <span data-ttu-id="79c8b-124">Designa un procedimiento local para el que MIDL no genera código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="79c8b-124">Designates a local procedure for which MIDL does not generate stub code.</span></span>                                                                                                                                                                                   |



 

<span data-ttu-id="79c8b-125">En las interfaces que no son de [**objeto**](object.md) , también puede aplicar el atributo de [**\_ identificador de contexto**](context-handle.md) a una función para especificar las características del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="79c8b-125">On non-[**object**](object.md) interfaces, you can also apply the [**context\_handle**](context-handle.md) attribute to a function to specify characteristics of the return value.</span></span>

 

 




