---
description: El servicio de componentes en cola de COM+ mejora el modelo de programación COM proporcionando un entorno en el que se puede invocar un componente de forma sincrónica (en tiempo real) o de forma asincrónica (en cola).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Arquitectura de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104567621"
---
# <a name="queued-components-architecture"></a><span data-ttu-id="08a56-103">Arquitectura de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="08a56-103">Queued Components Architecture</span></span>

<span data-ttu-id="08a56-104">El servicio de componentes en cola de COM+ mejora el modelo de programación COM proporcionando un entorno en el que se puede invocar un componente de forma sincrónica (en tiempo real) o de forma asincrónica (en cola).</span><span class="sxs-lookup"><span data-stu-id="08a56-104">The COM+ queued components service enhances the COM programming model by providing an environment in which a component can be invoked either synchronously (real-time) or asynchronously (queued).</span></span> <span data-ttu-id="08a56-105">Un componente no necesita tener en cuenta si se emplea en un contexto en tiempo real o en cola.</span><span class="sxs-lookup"><span data-stu-id="08a56-105">A component need not be aware of whether it is employed in a real-time or a queued context.</span></span>

<span data-ttu-id="08a56-106">Las aplicaciones de mensajería son similares a las transacciones por correo electrónico entre programas.</span><span class="sxs-lookup"><span data-stu-id="08a56-106">Messaging applications are like email transactions between programs.</span></span> <span data-ttu-id="08a56-107">El solicitante envía un mensaje al servidor; Cuando el servidor lo recibe, se procesa el mensaje.</span><span class="sxs-lookup"><span data-stu-id="08a56-107">The requester sends a message to the server; when the server gets to it, the message is processed.</span></span> <span data-ttu-id="08a56-108">Como el correo electrónico, un sistema de mensajería debe administrar los detalles de la red y asegurarse de que el mensaje se mueve desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="08a56-108">Like email, a messaging system must handle the network details and ensure that the message moves from the client to the server.</span></span> <span data-ttu-id="08a56-109">En el marco de trabajo de componentes en cola, Message Queue Server es responsable de ello.</span><span class="sxs-lookup"><span data-stu-id="08a56-109">In the queued components framework, Message Queuing is responsible for this.</span></span>

<span data-ttu-id="08a56-110">El servicio de componentes en cola de COM+ consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="08a56-110">The COM+ queued components service consists of the following parts:</span></span>

-   <span data-ttu-id="08a56-111">Grabadora (para el cliente o el lado de envío)</span><span class="sxs-lookup"><span data-stu-id="08a56-111">Recorder (for the client or send side)</span></span>
-   <span data-ttu-id="08a56-112">Agente de escucha (para el servidor o el lado de recepción)</span><span class="sxs-lookup"><span data-stu-id="08a56-112">Listener (for the server or receive side)</span></span>
-   <span data-ttu-id="08a56-113">Reproductor (para el servidor o el lado de recepción)</span><span class="sxs-lookup"><span data-stu-id="08a56-113">Player (for the server or receive side)</span></span>

![Diagrama que muestra la ruta de acceso desde el cliente al servidor: cliente, grabadora, cola, agente de escucha, reproductor, servidor.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a><span data-ttu-id="08a56-115">La grabadora</span><span class="sxs-lookup"><span data-stu-id="08a56-115">The Recorder</span></span>

<span data-ttu-id="08a56-116">En un escenario típico de componentes en cola, el cliente llama a un componente en cola.</span><span class="sxs-lookup"><span data-stu-id="08a56-116">In a typical queued components scenario, the client calls a queued component.</span></span> <span data-ttu-id="08a56-117">La llamada se realiza a la grabadora de componentes en cola, que la empaqueta como parte de un mensaje en el servidor y lo coloca en una cola.</span><span class="sxs-lookup"><span data-stu-id="08a56-117">The call is made to the queued components recorder, which packages it as part of a message to the server and puts it in a queue.</span></span> <span data-ttu-id="08a56-118">La grabadora calcula las referencias del contexto de seguridad del cliente en el mensaje y registra todas las llamadas al método del cliente.</span><span class="sxs-lookup"><span data-stu-id="08a56-118">The recorder marshals the client's security context into the message and records all of the client's method calls.</span></span> <span data-ttu-id="08a56-119">En su rol como proxy para el componente del servidor, la grabadora selecciona interfaces de las interfaces de queuable en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="08a56-119">In its role as proxy for the server component, the recorder selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

<span data-ttu-id="08a56-120">Una representación de la grabación se envía a Message Queue Server como un mensaje que se va a enviar a un servidor.</span><span class="sxs-lookup"><span data-stu-id="08a56-120">A representation of the recording is sent to Message Queuing as a message to be sent to a server.</span></span> <span data-ttu-id="08a56-121">Cuando el componente en cola tiene el valor de atributo de transacción requerido o compatible, Message Queue Server acepta la entrega del mensaje solo si la transacción del cliente se confirma y la cola de Message Queue Server es transaccional, que es el valor predeterminado que se establece normalmente.</span><span class="sxs-lookup"><span data-stu-id="08a56-121">When the queued component has the transaction attribute setting of Required or Supported, Message Queuing accepts delivery of the message only if the client-side transaction commits and the Message Queuing queue is transactional, which is the default normally established.</span></span> <span data-ttu-id="08a56-122">Cuando la configuración del atributo de transacción requiere nuevo, Message Queue Server puede aceptar el mensaje incluso si se anula la transacción del cliente.</span><span class="sxs-lookup"><span data-stu-id="08a56-122">When the transaction attribute setting is Requires New, Message Queuing can accept the message even if the client-side transaction aborts.</span></span> <span data-ttu-id="08a56-123">Para obtener más información sobre las transacciones, vea [Message Queue Server transaccional](transactional-message-queuing.md).</span><span class="sxs-lookup"><span data-stu-id="08a56-123">For more information on transactions, see [Transactional Message Queuing](transactional-message-queuing.md).</span></span>

## <a name="the-listener"></a><span data-ttu-id="08a56-124">El agente de escucha</span><span class="sxs-lookup"><span data-stu-id="08a56-124">The Listener</span></span>

<span data-ttu-id="08a56-125">El agente de escucha de componentes en cola recupera el mensaje de la cola y lo pasa al reproductor de componentes en cola.</span><span class="sxs-lookup"><span data-stu-id="08a56-125">The queued components listener retrieves the message from the queue and passes it to the queued components player.</span></span>

## <a name="the-player"></a><span data-ttu-id="08a56-126">El reproductor</span><span class="sxs-lookup"><span data-stu-id="08a56-126">The Player</span></span>

<span data-ttu-id="08a56-127">El reproductor Anula la serialización del contexto de seguridad del cliente en el lado del servidor y, a continuación, invoca el componente del servidor y realiza las mismas llamadas al método.</span><span class="sxs-lookup"><span data-stu-id="08a56-127">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="08a56-128">El reproductor no reproduce las llamadas al método hasta que el componente de cliente finaliza y la transacción que registra el método llama a las confirmaciones.</span><span class="sxs-lookup"><span data-stu-id="08a56-128">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

## <a name="the-message-mover"></a><span data-ttu-id="08a56-129">El Movedor de mensajes</span><span class="sxs-lookup"><span data-stu-id="08a56-129">The Message Mover</span></span>

<span data-ttu-id="08a56-130">El Movedor de mensajes de componentes en cola es una utilidad que mueve todos los mensajes de Message Queue Server con errores de una cola a otra para que se puedan Reintentar.</span><span class="sxs-lookup"><span data-stu-id="08a56-130">The queued components message mover is a utility that moves all failed Message Queuing messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="08a56-131">La utilidad del Movedor de mensajes es un objeto de automatización que se puede invocar con un VBScript; para obtener más información, vea [control de errores](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="08a56-131">The message mover utility is an Automation object that can be invoked with a VBScript; for more information, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

 

 



