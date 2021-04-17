---
description: La clase CBaseReferenceClock implementa un reloj de referencia.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Clase CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671085"
---
# <a name="cbasereferenceclock-class"></a><span data-ttu-id="b6a47-103">Clase CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="b6a47-103">CBaseReferenceClock class</span></span>

![jerarquía de clases cbasereferenceclock](images/rclock01.png)

<span data-ttu-id="b6a47-105">La `CBaseReferenceClock` clase implementa un reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="b6a47-105">The `CBaseReferenceClock` class implements a reference clock.</span></span>



| <span data-ttu-id="b6a47-106">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="b6a47-106">Protected Member Variables</span></span>                                                         | <span data-ttu-id="b6a47-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a47-107">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6a47-108">**m \_ pSchedule**</span><span class="sxs-lookup"><span data-stu-id="b6a47-108">**m\_pSchedule**</span></span>](cbasereferenceclock-m-pschedule.md)                            | <span data-ttu-id="b6a47-109">Objeto [**CAMSchedule**](camschedule.md) que controla las tareas de programación del reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a47-109">[**CAMSchedule**](camschedule.md) object that handles scheduling tasks for the clock.</span></span> |
| <span data-ttu-id="b6a47-110">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="b6a47-110">Protected Methods</span></span>                                                                  | <span data-ttu-id="b6a47-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a47-111">Description</span></span>                                                                            |
| [<span data-ttu-id="b6a47-112">**~ CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="b6a47-112">**~CBaseReferenceClock**</span></span>](cbasereferenceclock--cbasereferenceclock.md)           | <span data-ttu-id="b6a47-113">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="b6a47-113">Destructor method.</span></span>                                                                     |
| <span data-ttu-id="b6a47-114">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="b6a47-114">Public Methods</span></span>                                                                     | <span data-ttu-id="b6a47-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a47-115">Description</span></span>                                                                            |
| [<span data-ttu-id="b6a47-116">**CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="b6a47-116">**CBaseReferenceClock**</span></span>](cbasereferenceclock-cbasereferenceclock.md)             | <span data-ttu-id="b6a47-117">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="b6a47-117">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="b6a47-118">**GetPrivateTime**</span><span class="sxs-lookup"><span data-stu-id="b6a47-118">**GetPrivateTime**</span></span>](cbasereferenceclock-getprivatetime.md)                       | <span data-ttu-id="b6a47-119">Recupera la hora real del reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a47-119">Retrieves the real time from the clock.</span></span>                                                |
| [<span data-ttu-id="b6a47-120">**SetTimeDelta**</span><span class="sxs-lookup"><span data-stu-id="b6a47-120">**SetTimeDelta**</span></span>](cbasereferenceclock-settimedelta.md)                           | <span data-ttu-id="b6a47-121">Ajusta la hora interna del reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a47-121">Adjusts the internal clock time.</span></span>                                                       |
| [<span data-ttu-id="b6a47-122">**GetSchedule**</span><span class="sxs-lookup"><span data-stu-id="b6a47-122">**GetSchedule**</span></span>](cbasereferenceclock-getschedule.md)                             | <span data-ttu-id="b6a47-123">Recupera un puntero al objeto de programación del reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a47-123">Retrieves a pointer to the clock's scheduling object.</span></span>                                  |
| [<span data-ttu-id="b6a47-124">**TriggerThread**</span><span class="sxs-lookup"><span data-stu-id="b6a47-124">**TriggerThread**</span></span>](cbasereferenceclock-triggerthread.md)                         | <span data-ttu-id="b6a47-125">Reactiva el subproceso de trabajo que controla la programación.</span><span class="sxs-lookup"><span data-stu-id="b6a47-125">Wakes up the worker thread that handles scheduling.</span></span>                                    |
| <span data-ttu-id="b6a47-126">Métodos IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="b6a47-126">IReferenceClock Methods</span></span>                                                            | <span data-ttu-id="b6a47-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a47-127">Description</span></span>                                                                            |
| [<span data-ttu-id="b6a47-128">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="b6a47-128">**GetTime**</span></span>](cbasereferenceclock-gettime.md)                                     | <span data-ttu-id="b6a47-129">Recupera el tiempo de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="b6a47-129">Retrieves the current reference time.</span></span>                                                  |
| [<span data-ttu-id="b6a47-130">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="b6a47-130">**AdviseTime**</span></span>](cbasereferenceclock-advisetime.md)                               | <span data-ttu-id="b6a47-131">Crea una solicitud de notificación de una captura.</span><span class="sxs-lookup"><span data-stu-id="b6a47-131">Creates a one-shot advise request.</span></span>                                                     |
| [<span data-ttu-id="b6a47-132">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="b6a47-132">**AdvisePeriodic**</span></span>](cbasereferenceclock-adviseperiodic.md)                       | <span data-ttu-id="b6a47-133">Crea una solicitud de notificación periódica.</span><span class="sxs-lookup"><span data-stu-id="b6a47-133">Creates a periodic advise request.</span></span>                                                     |
| [<span data-ttu-id="b6a47-134">**No notificar**</span><span class="sxs-lookup"><span data-stu-id="b6a47-134">**Unadvise**</span></span>](cbasereferenceclock-unadvise.md)                                   | <span data-ttu-id="b6a47-135">Quita una solicitud de notificación pendiente.</span><span class="sxs-lookup"><span data-stu-id="b6a47-135">Removes a pending advise request.</span></span>                                                      |
| <span data-ttu-id="b6a47-136">Métodos IReferenceClockTimerControl</span><span class="sxs-lookup"><span data-stu-id="b6a47-136">IReferenceClockTimerControl Methods</span></span>                                                | <span data-ttu-id="b6a47-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a47-137">Description</span></span>                                                                            |
| [<span data-ttu-id="b6a47-138">**GetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="b6a47-138">**GetDefaultTimerResolution**</span></span>](cbasereferenceclock-getdefaulttimerresolution.md) | <span data-ttu-id="b6a47-139">Devuelve la resolución actual del temporizador del reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="b6a47-139">Returns the current resolution of the reference clock's timer.</span></span>                         |
| [<span data-ttu-id="b6a47-140">**SetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="b6a47-140">**SetDefaultTimerResolution**</span></span>](cbasereferenceclock-setdefaulttimerresolution.md) | <span data-ttu-id="b6a47-141">Establece la resolución del temporizador del reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="b6a47-141">Sets the resolution of the reference clock's timer.</span></span>                                    |
| <span data-ttu-id="b6a47-142">Funciones del asistente</span><span class="sxs-lookup"><span data-stu-id="b6a47-142">Helper Functions</span></span>                                                                   | <span data-ttu-id="b6a47-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a47-143">Description</span></span>                                                                            |
| [<span data-ttu-id="b6a47-144">**ConvertToMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="b6a47-144">**ConvertToMilliseconds**</span></span>](converttomilliseconds.md)                             | <span data-ttu-id="b6a47-145">Convierte una hora de referencia en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b6a47-145">Converts a reference time to milliseconds.</span></span>                                             |



 

## <a name="remarks"></a><span data-ttu-id="b6a47-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6a47-146">Remarks</span></span>

<span data-ttu-id="b6a47-147">Esta clase implementa un reloj de referencia que admite las interfaces [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) y [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) .</span><span class="sxs-lookup"><span data-stu-id="b6a47-147">This class implements a reference clock that supports the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) and [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) interfaces.</span></span> <span data-ttu-id="b6a47-148">Si un filtro puede proporcionar un reloj de referencia para el gráfico de filtros, por ejemplo, mediante el acceso a un dispositivo de hardware, puede usar esta clase para implementar el reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a47-148">If a filter can provide a reference clock for the filter graph for example, by accessing a hardware device it can use this class to implement the clock.</span></span>

<span data-ttu-id="b6a47-149">El `CBaseReferenceClock` objeto mantiene dos valores de hora distintos:</span><span class="sxs-lookup"><span data-stu-id="b6a47-149">The `CBaseReferenceClock` object maintains two distinct time values:</span></span>

-   <span data-ttu-id="b6a47-150">Internamente, el método [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) devuelve la hora real que mantiene el reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a47-150">Internally, the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method returns the actual time kept by the clock.</span></span>
-   <span data-ttu-id="b6a47-151">Externamente, el método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) devuelve el tiempo de referencia para el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b6a47-151">Externally, the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method returns the reference time for the filter graph.</span></span>

<span data-ttu-id="b6a47-152">Es válido para que el reloj interno se ejecute hacia atrás en breves períodos.</span><span class="sxs-lookup"><span data-stu-id="b6a47-152">It is valid for the internal clock to run backward over brief periods.</span></span> <span data-ttu-id="b6a47-153">Por ejemplo, si el reloj se desplaza hacia delante, el filtro puede ajustarlo hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="b6a47-153">For example, if the clock drifts forward, the filter can adjust it backward.</span></span> <span data-ttu-id="b6a47-154">(Vea [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md)). El método **getTime** usa los valores de hora que se indican en **GetPrivateTime**.</span><span class="sxs-lookup"><span data-stu-id="b6a47-154">(See [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).) The **GetTime** method uses the time values reported by **GetPrivateTime**.</span></span> <span data-ttu-id="b6a47-155">Sin embargo, el tiempo de referencia aumenta de forma monotónica; en otras palabras, nunca se ejecuta hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="b6a47-155">However, the reference time is monotonically increasing; in other words, it never runs backward.</span></span> <span data-ttu-id="b6a47-156">Por lo tanto, si el reloj interno se ejecuta hacia atrás, **getTime** continúa notificando el tiempo anterior hasta que el reloj interno se pone al día.</span><span class="sxs-lookup"><span data-stu-id="b6a47-156">Therefore, if the internal clock runs backward, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

<span data-ttu-id="b6a47-157">Por ejemplo, los dos métodos podrían devolver las secuencias siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6a47-157">For example, the two methods might return the following sequences:</span></span>

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

<span data-ttu-id="b6a47-158">En el tercer paso del reloj, el reloj interno salta hacia atrás hasta 103.</span><span class="sxs-lookup"><span data-stu-id="b6a47-158">On the third clock tick, the internal clock jumps backward to 103.</span></span> <span data-ttu-id="b6a47-159">El método **getTime** continúa notificando 106 hasta que el reloj interno se pone al día.</span><span class="sxs-lookup"><span data-stu-id="b6a47-159">The **GetTime** method continues to report 106 until the internal clock catches up.</span></span>

<span data-ttu-id="b6a47-160">De forma predeterminada, **GetPrivateTime** devuelve la hora del sistema, a través de una llamada a la función **timeGetTime** .</span><span class="sxs-lookup"><span data-stu-id="b6a47-160">By default, **GetPrivateTime** returns the system time, through a call to the **timeGetTime** function.</span></span> <span data-ttu-id="b6a47-161">Un filtro que proporciona un reloj de referencia desde un dispositivo externo puede realizar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="b6a47-161">A filter that is providing a reference clock from an external device can do one of the following:</span></span>

-   <span data-ttu-id="b6a47-162">Invalide **GetPrivateTime** para devolver la hora del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6a47-162">Override **GetPrivateTime** to return the time from the device.</span></span>
-   <span data-ttu-id="b6a47-163">Supervise la discrepancia entre la hora del dispositivo y la hora del sistema, y llame a **SetTimeDelta** para hacer correcciones.</span><span class="sxs-lookup"><span data-stu-id="b6a47-163">Monitor the discrepancy between the device time and the system time, and call **SetTimeDelta** to make corrections.</span></span>

<span data-ttu-id="b6a47-164">Esta clase utiliza un objeto [**CAMSchedule**](camschedule.md) para controlar la programación de solicitudes de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b6a47-164">This class uses a [**CAMSchedule**](camschedule.md) object to handle scheduling of advise requests.</span></span> <span data-ttu-id="b6a47-165">Para obtener más información, consulte la documentación de la clase **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="b6a47-165">For details, see the documentation for the **CAMSchedule** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a47-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a47-166">Requirements</span></span>



| <span data-ttu-id="b6a47-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a47-167">Requirement</span></span> | <span data-ttu-id="b6a47-168">Value</span><span class="sxs-lookup"><span data-stu-id="b6a47-168">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a47-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6a47-169">Header</span></span><br/>  | <dl> <span data-ttu-id="b6a47-170"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6a47-170"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b6a47-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6a47-171">Library</span></span><br/> | <dl> <span data-ttu-id="b6a47-172"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b6a47-172"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




