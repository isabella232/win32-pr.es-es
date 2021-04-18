---
description: El servicio de eventos COM+ se utiliza para administrar la entrega de eventos de publicadores a suscriptores.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Usar eventos COM+ con componentes en cola de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714883"
---
# <a name="using-com-events-with-com-queued-components"></a><span data-ttu-id="04b0f-103">Usar eventos COM+ con componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="04b0f-103">Using COM+ Events with COM+ Queued Components</span></span>

<span data-ttu-id="04b0f-104">El servicio de eventos COM+ se utiliza para administrar la entrega de eventos de publicadores a suscriptores.</span><span class="sxs-lookup"><span data-stu-id="04b0f-104">The COM+ events service is used to manage the delivery of events from publishers to subscribers.</span></span> <span data-ttu-id="04b0f-105">El servicio de componentes en cola de COM+ se puede usar para hacer que el publicador y el tiempo de procesamiento del suscriptor sean independientes al poner en cola el mensaje del publicador y, posteriormente, reproducirlo en el suscriptor.</span><span class="sxs-lookup"><span data-stu-id="04b0f-105">The COM+ queued components service can be used to make the publisher and subscriber processing time independent by queuing the publisher's message and later replaying it to the subscriber.</span></span> <span data-ttu-id="04b0f-106">Tanto si necesita usar el servicio de componentes en cola depende de la lógica de negocios subyacente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04b0f-106">Whether or not you need to use the queued components service depends on the underlying business logic of your application.</span></span> <span data-ttu-id="04b0f-107">Si necesita tener eventos independientes del tiempo, puede crearlos mediante el servicio de eventos COM+ con el servicio de componentes en cola de COM+.</span><span class="sxs-lookup"><span data-stu-id="04b0f-107">If you need to have events that are time independent, you can create them by using the COM+ events service with COM+ queued components service.</span></span>

> [!Note]  
> <span data-ttu-id="04b0f-108">Para obtener información adicional acerca del uso del servicio de componentes en cola de COM+, vea [componentes en cola de com+](com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="04b0f-108">For additional information about using the COM+ queued components service, see [COM+ Queued Components](com--queued-components.md).</span></span>

 

<span data-ttu-id="04b0f-109">El servicio de componentes en cola mantiene la invocación de orden de método dentro de un solo mensaje.</span><span class="sxs-lookup"><span data-stu-id="04b0f-109">The queued components service maintains order-of-method invocation within a single message.</span></span> <span data-ttu-id="04b0f-110">La grabadora procesa por lotes todas las invocaciones de método en un mensaje y, a continuación, el reproductor invoca esos métodos en orden cuando se procesa el mensaje.</span><span class="sxs-lookup"><span data-stu-id="04b0f-110">The recorder batches all method invocations into a message, and then the player invokes those methods in order when the message is processed.</span></span>

<span data-ttu-id="04b0f-111">Una grabadora de componentes en cola y un reproductor se pueden colocar en cualquiera de los dos lugares siguientes:</span><span class="sxs-lookup"><span data-stu-id="04b0f-111">A queued components recorder and player can be positioned in either of the following two places:</span></span>

-   <span data-ttu-id="04b0f-112">Entre el publicador y el objeto de evento</span><span class="sxs-lookup"><span data-stu-id="04b0f-112">Between the publisher and event object</span></span>
-   <span data-ttu-id="04b0f-113">Entre el objeto de evento y el suscriptor</span><span class="sxs-lookup"><span data-stu-id="04b0f-113">Between the event object and subscriber</span></span>

<span data-ttu-id="04b0f-114">Si coloca la grabadora y el reproductor entre el publicador y el objeto de evento, hará que el componente de [clase de evento](the-com--event-class-object.md) queuable.</span><span class="sxs-lookup"><span data-stu-id="04b0f-114">If you position the recorder and player between the publisher and event object, you are making the [event class](the-com--event-class-object.md) component queuable.</span></span> <span data-ttu-id="04b0f-115">El componente de la clase de evento debe marcarse para la puesta en cola y ser activado por el reproductor en un proceso independiente del publicador.</span><span class="sxs-lookup"><span data-stu-id="04b0f-115">The event class component must be marked for queuing and be activated by the player in a process that is separate from the publisher.</span></span>

<span data-ttu-id="04b0f-116">Para proporcionar eventos de forma asincrónica, cree la grabadora y el reproductor entre el objeto de evento y el suscriptor, y establezca el atributo en cola del objeto de suscripción.</span><span class="sxs-lookup"><span data-stu-id="04b0f-116">To deliver events asynchronously, compose the recorder and player between the event object and subscriber and set the Queued attribute of the subscription object.</span></span> <span data-ttu-id="04b0f-117">Esto establece SubscriberMoniker como se indica a continuación: "Queue:/New:/ {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="04b0f-117">This sets SubscriberMoniker as follows: "queue:/new:/{12345678-1234-1234-1234-123456789012}".</span></span>

<span data-ttu-id="04b0f-118">Hay un orden de implicación de entrega que se debe tener en cuenta al usar componentes en cola en una situación de evento.</span><span class="sxs-lookup"><span data-stu-id="04b0f-118">There is an order of delivery implication to consider when using queued components in an event situation.</span></span> <span data-ttu-id="04b0f-119">Dado que el servicio de componentes en cola registra y reproduce todas las llamadas dentro de la duración de un solo objeto en un mensaje, todas las llamadas se reproducen en el orden en que se realizaron.</span><span class="sxs-lookup"><span data-stu-id="04b0f-119">Because the queued components service records and plays back all calls within the lifetime of a single object in one message, all calls are replayed in the order in which they were made.</span></span> <span data-ttu-id="04b0f-120">Sin embargo, si hay más de una sesión con más de un objeto, no se puede garantizar el orden.</span><span class="sxs-lookup"><span data-stu-id="04b0f-120">However, if there is more than one session with more than one object, order cannot be guaranteed.</span></span> <span data-ttu-id="04b0f-121">Si el orden es importante, asegúrese de que las llamadas que se deben reproducir en orden residan en la misma instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="04b0f-121">If order is important, make sure that calls that need to be played back in order reside on the same object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04b0f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04b0f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04b0f-123">Filtrado de eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="04b0f-123">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="04b0f-124">Publicar y entregar eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="04b0f-124">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="04b0f-125">Suscripciones</span><span class="sxs-lookup"><span data-stu-id="04b0f-125">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="04b0f-126">Objeto de la clase de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="04b0f-126">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



