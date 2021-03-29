---
description: Para publicar un evento, simplemente cree una instancia de un objeto de clase de evento e invoque el método deseado; para obtener instrucciones detalladas sobre cómo hacerlo en el código, vea publicar un evento.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Publicar y entregar eventos en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807790"
---
# <a name="publishing-and-delivering-events-in-com"></a><span data-ttu-id="3ef2a-103">Publicar y entregar eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="3ef2a-103">Publishing and Delivering Events in COM+</span></span>

<span data-ttu-id="3ef2a-104">Para publicar un evento, simplemente cree una instancia de un objeto de [clase de evento](the-com--event-class-object.md) e invoque el método deseado; para obtener instrucciones detalladas sobre cómo hacerlo en el código, vea [publicar un evento](publishing-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="3ef2a-104">To publish an event, simply instantiate an [event class](the-com--event-class-object.md) object and invoke the desired method; for detailed instructions on how to do this in code, see [Publishing an Event](publishing-an-event.md).</span></span>

<span data-ttu-id="3ef2a-105">Cuando un publicador desencadena un evento, el servicio de eventos COM+ busca en la base de datos de suscripciones para encontrar todos los suscriptores que han registrado suscripciones a la clase de eventos con instancias.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-105">When a publisher fires an event, the COM+ Events service searches the subscription database to find all the subscribers who have registered subscriptions to the instantiated event class.</span></span> <span data-ttu-id="3ef2a-106">Se conecta a los suscriptores (mediante la creación directa, monikers o componentes en cola) y llama al método.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-106">It connects to those subscribers (by direct creation, monikers, or queued components) and calls the method.</span></span> <span data-ttu-id="3ef2a-107">Para admitir más de una notificación de suscriptor para un evento, los métodos solo pueden contener parámetros in y deben devolver valores **HRESULT** correctos o con errores.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-107">To support more than one subscriber notification for an event, methods can contain only in parameters and must return only success or failure **HRESULT** values.</span></span>

> [!Note]  
> <span data-ttu-id="3ef2a-108">Esta versión de eventos COM+ no es compatible con un almacén de eventos distribuido.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-108">This version of COM+ events does not support a distributed event store.</span></span> <span data-ttu-id="3ef2a-109">Un suscriptor debe suscribirse a un evento en cada equipo desde el que desea recibir la notificación.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-109">A subscriber must subscribe to an event on each computer from which it wants to receive notification.</span></span> <span data-ttu-id="3ef2a-110">Como alternativa, puede registrar el objeto de la clase de evento y las suscripciones en un equipo central y crear una instancia de este objeto de la clase de evento desde los equipos remotos en los que se publican los eventos.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-110">As an alternative, you can register the event class object and subscriptions on a central computer and instantiate this event class object from the remote computers on which you publish events.</span></span> <span data-ttu-id="3ef2a-111">La entrega de eventos se proporciona mediante DCOM o el servicio de componentes en cola de COM+.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-111">Delivery of events is provided either by DCOM or by the COM+ queued components service.</span></span> <span data-ttu-id="3ef2a-112">Para obtener más información acerca del uso del servicio de componentes en cola de COM+, vea [using com+ events with com+ queued Components](using-com--events-with-com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="3ef2a-112">For more information about using the COM+ queued components service, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

 

<span data-ttu-id="3ef2a-113">De forma predeterminada, el servicio de eventos COM+ activa los eventos de uno en uno, sin ningún orden determinado o repetible.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-113">By default, the COM+ events service fires events one at a time, in no determined or repeatable order.</span></span> <span data-ttu-id="3ef2a-114">Los publicadores que necesiten controlar el orden en el que los suscriptores reciben un evento pueden implementar un filtro de publicador.</span><span class="sxs-lookup"><span data-stu-id="3ef2a-114">Publishers that need to control the order in which subscribers receive an event can implement a publisher filter.</span></span> <span data-ttu-id="3ef2a-115">(Para obtener más información, vea [filtrar eventos en com+](filtering-events-in-com-.md)).</span><span class="sxs-lookup"><span data-stu-id="3ef2a-115">(For more information, see [Filtering Events in COM+](filtering-events-in-com-.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ef2a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ef2a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ef2a-117">Filtrado de eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="3ef2a-117">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="3ef2a-118">Suscripciones</span><span class="sxs-lookup"><span data-stu-id="3ef2a-118">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="3ef2a-119">Objeto de la clase de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="3ef2a-119">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="3ef2a-120">Usar eventos COM+ con componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="3ef2a-120">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



