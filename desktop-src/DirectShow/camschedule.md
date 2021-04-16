---
description: La clase CAMSchedule implementa un programador para los relojes de referencia.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Clase CAMSchedule (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671292"
---
# <a name="camschedule-class"></a><span data-ttu-id="83997-103">Clase CAMSchedule</span><span class="sxs-lookup"><span data-stu-id="83997-103">CAMSchedule class</span></span>

<span data-ttu-id="83997-104">La `CAMSchedule` clase implementa un programador para los relojes de referencia.</span><span class="sxs-lookup"><span data-stu-id="83997-104">The `CAMSchedule` class implements a scheduler for reference clocks.</span></span>



| <span data-ttu-id="83997-105">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="83997-105">Public Methods</span></span>                                             | <span data-ttu-id="83997-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="83997-106">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="83997-107">**CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="83997-107">**CAMSchedule**</span></span>](camschedule-camschedule.md)             | <span data-ttu-id="83997-108">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="83997-108">Constructor method.</span></span>                                                                  |
| [<span data-ttu-id="83997-109">**~ CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="83997-109">**~CAMSchedule**</span></span>](camschedule--camschedule.md)           | <span data-ttu-id="83997-110">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="83997-110">Destructor method.</span></span> <span data-ttu-id="83997-111">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="83997-111">Virtual.</span></span>                                                          |
| [<span data-ttu-id="83997-112">**GetAdviseCount**</span><span class="sxs-lookup"><span data-stu-id="83997-112">**GetAdviseCount**</span></span>](camschedule-getadvisecount.md)       | <span data-ttu-id="83997-113">Recupera el número de solicitudes de notificación pendientes.</span><span class="sxs-lookup"><span data-stu-id="83997-113">Retrieves the number of pending advise requests.</span></span>                                     |
| [<span data-ttu-id="83997-114">**GetNextAdviseTime**</span><span class="sxs-lookup"><span data-stu-id="83997-114">**GetNextAdviseTime**</span></span>](camschedule-getnextadvisetime.md) | <span data-ttu-id="83997-115">Recupera la hora de la solicitud de notificación siguiente.</span><span class="sxs-lookup"><span data-stu-id="83997-115">Retrieves the time of the next advise request.</span></span>                                       |
| [<span data-ttu-id="83997-116">**AddAdvisePacket**</span><span class="sxs-lookup"><span data-stu-id="83997-116">**AddAdvisePacket**</span></span>](camschedule-addadvisepacket.md)     | <span data-ttu-id="83997-117">Agrega una solicitud de notificación a la lista de solicitudes pendientes.</span><span class="sxs-lookup"><span data-stu-id="83997-117">Adds an advise request to the list of pending requests.</span></span>                              |
| [<span data-ttu-id="83997-118">**No notificar**</span><span class="sxs-lookup"><span data-stu-id="83997-118">**Unadvise**</span></span>](camschedule-unadvise.md)                   | <span data-ttu-id="83997-119">Quita una solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="83997-119">Removes an advise request.</span></span>                                                           |
| [<span data-ttu-id="83997-120">**Informar**</span><span class="sxs-lookup"><span data-stu-id="83997-120">**Advise**</span></span>](camschedule-advise.md)                       | <span data-ttu-id="83997-121">Envía todas las solicitudes programadas durante un tiempo especificado o anterior.</span><span class="sxs-lookup"><span data-stu-id="83997-121">Dispatches all requests that are scheduled for a specified time or earlier.</span></span>          |
| [<span data-ttu-id="83997-122">**GetEvent**</span><span class="sxs-lookup"><span data-stu-id="83997-122">**GetEvent**</span></span>](camschedule-getevent.md)                   | <span data-ttu-id="83997-123">Recupera un identificador de evento, que se usa para indicar un cambio en la hora de notificación siguiente.</span><span class="sxs-lookup"><span data-stu-id="83997-123">Retrieves an event handle, which is used to signal a change in the next advise time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="83997-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83997-124">Remarks</span></span>

<span data-ttu-id="83997-125">Este objeto auxiliar mantiene una lista de solicitudes de notificación para un reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="83997-125">This helper object maintains a list of advise requests for a reference clock.</span></span> <span data-ttu-id="83997-126">La clase [**CBaseReferenceClock**](cbasereferenceclock.md) la usa para ayudar a programar solicitudes de notificación.</span><span class="sxs-lookup"><span data-stu-id="83997-126">The [**CBaseReferenceClock**](cbasereferenceclock.md) class uses it to help schedule advise requests.</span></span> <span data-ttu-id="83997-127">Los relojes usan este objeto de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="83997-127">Clocks use this object in the following manner:</span></span>

1.  <span data-ttu-id="83997-128">El reloj crea un subproceso de trabajo para controlar la programación.</span><span class="sxs-lookup"><span data-stu-id="83997-128">The clock creates a worker thread to handle scheduling.</span></span>
2.  <span data-ttu-id="83997-129">El subproceso de trabajo llama al método [**CAMSchedule:: GetEvent**](camschedule-getevent.md) para recuperar un identificador de evento del programador.</span><span class="sxs-lookup"><span data-stu-id="83997-129">The worker thread calls the [**CAMSchedule::GetEvent**](camschedule-getevent.md) method to retrieve an event handle from the scheduler.</span></span> <span data-ttu-id="83997-130">Espera en este evento, inicialmente con un tiempo de espera infinito.</span><span class="sxs-lookup"><span data-stu-id="83997-130">It waits on this event, initially with an infinite time-out.</span></span>
3.  <span data-ttu-id="83997-131">Para programar una nueva solicitud de notificación, el reloj llama al método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="83997-131">To schedule a new advise request, the clock calls the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span> <span data-ttu-id="83997-132">Una solicitud de notificación puede ser de una sola captura o periódica.</span><span class="sxs-lookup"><span data-stu-id="83997-132">An advise request can be one-shot or periodic.</span></span> <span data-ttu-id="83997-133">Scheduler mantiene la lista de solicitudes en el orden en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="83997-133">The scheduler keeps the list of requests in time order.</span></span>
4.  <span data-ttu-id="83997-134">Si se agrega una solicitud al principio de la lista, el programador indica el evento.</span><span class="sxs-lookup"><span data-stu-id="83997-134">If a request is added to the front of the list, the scheduler signals the event.</span></span> <span data-ttu-id="83997-135">(La lista está vacía al principio, por lo que se garantiza que la primera solicitud señale el evento).</span><span class="sxs-lookup"><span data-stu-id="83997-135">(The list is empty at first, so the first request is guaranteed to signal the event.)</span></span>
5.  <span data-ttu-id="83997-136">Cuando se señala el evento, el subproceso de trabajo llama al método [**CAMSchedule:: Advise**](camschedule-advise.md) , especificando el tiempo de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="83997-136">When the event is signaled, the worker thread calls the [**CAMSchedule::Advise**](camschedule-advise.md) method, specifying the current reference time.</span></span> <span data-ttu-id="83997-137">Si alguna solicitud pendiente ha expirado, el programador las envía.</span><span class="sxs-lookup"><span data-stu-id="83997-137">If any pending requests have expired, the scheduler dispatches them.</span></span>
6.  <span data-ttu-id="83997-138">El método Advise devuelve la hora de la siguiente solicitud.</span><span class="sxs-lookup"><span data-stu-id="83997-138">The Advise method returns the time of the next request.</span></span> <span data-ttu-id="83997-139">El subproceso de trabajo usa este valor para calcular un nuevo valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="83997-139">The worker thread uses this value to calculate a new time-out value.</span></span>
7.  <span data-ttu-id="83997-140">Los pasos 2 6 se repiten indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="83997-140">Steps 2 6 repeat indefinitely.</span></span>
8.  <span data-ttu-id="83997-141">Para terminar el subproceso de trabajo, el reloj establece una marca interna y señala el evento.</span><span class="sxs-lookup"><span data-stu-id="83997-141">To terminate the worker thread, the clock sets an internal flag and signals the event.</span></span>

<span data-ttu-id="83997-142">En el paso 2, se señala el evento o se agota el tiempo de espera. Si el evento se señala, significa que se ha agregado una nueva solicitud al principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="83997-142">In step 2, either the event is signaled, or the wait times out. If the event is signaled, it means that a new request was added to the front of the list.</span></span> <span data-ttu-id="83997-143">El subproceso de trabajo debe calcular un nuevo valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="83997-143">The worker thread must calculate a new time-out value.</span></span> <span data-ttu-id="83997-144">Por otro lado, si se agota el tiempo de espera, significa que una solicitud de notificación ha vencido y se debe enviar.</span><span class="sxs-lookup"><span data-stu-id="83997-144">On the other hand, if the wait times out, it means that an advise request has come due and must be dispatched.</span></span> <span data-ttu-id="83997-145">La llamada a Advise en el paso 5 controla ambos casos.</span><span class="sxs-lookup"><span data-stu-id="83997-145">The call to Advise in step 5 handles both cases.</span></span>

## <a name="requirements"></a><span data-ttu-id="83997-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83997-146">Requirements</span></span>



| <span data-ttu-id="83997-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="83997-147">Requirement</span></span> | <span data-ttu-id="83997-148">Value</span><span class="sxs-lookup"><span data-stu-id="83997-148">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83997-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83997-149">Header</span></span><br/>  | <dl> <span data-ttu-id="83997-150"><dt>Dsschedule. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83997-150"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="83997-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83997-151">Library</span></span><br/> | <dl> <span data-ttu-id="83997-152"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="83997-152"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




