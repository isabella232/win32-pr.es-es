---
description: Vaciar datos
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Vaciar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805377"
---
# <a name="flushing-data"></a><span data-ttu-id="86710-103">Vaciar datos</span><span class="sxs-lookup"><span data-stu-id="86710-103">Flushing Data</span></span>

<span data-ttu-id="86710-104">En el siguiente pseudocódigo se muestra cómo implementar el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :</span><span class="sxs-lookup"><span data-stu-id="86710-104">The following pseudocode shows how to implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method:</span></span>


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



<span data-ttu-id="86710-105">Cuando se inicia el vaciado, el método **BeginFlush** toma el bloqueo de filtro, que serializa el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="86710-105">When flushing starts, the **BeginFlush** method takes the filter lock, which serializes the state change.</span></span> <span data-ttu-id="86710-106">Todavía no es seguro realizar el bloqueo de streaming, porque el vaciado se produce en el subproceso de la aplicación y el subproceso de streaming puede estar en medio de una llamada de **recepción** .</span><span class="sxs-lookup"><span data-stu-id="86710-106">It is not yet safe to take the streaming lock, because flushing happens on the application thread, and the streaming thread might be in the middle of a **Receive** call.</span></span> <span data-ttu-id="86710-107">El PIN debe garantizar que la **recepción** no esté bloqueada y que se produzca un error en todas las llamadas posteriores a **Receive** .</span><span class="sxs-lookup"><span data-stu-id="86710-107">The pin needs to guarantee that **Receive** is not blocked, and that any subsequent calls to **Receive** will fail.</span></span> <span data-ttu-id="86710-108">El método [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) establece una marca interna, [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md).</span><span class="sxs-lookup"><span data-stu-id="86710-108">The [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method sets an internal flag, [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md).</span></span> <span data-ttu-id="86710-109">Cuando la marca es **true**, se produce un error en el método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="86710-109">When the flag is **TRUE**, the **Receive** method fails.</span></span>

<span data-ttu-id="86710-110">Al entregar la llamada **BeginFlush** downstream, el PIN garantiza que todos los filtros de nivel inferior liberan sus ejemplos y devuelven desde las llamadas de **recepción** .</span><span class="sxs-lookup"><span data-stu-id="86710-110">By delivering the **BeginFlush** call downstream, the pin guarantees that all downstream filters release their samples and return from **Receive** calls.</span></span> <span data-ttu-id="86710-111">A su vez, garantiza que el PIN de entrada no se bloquea en espera de la acción **getBuffer** o **Receive**.</span><span class="sxs-lookup"><span data-stu-id="86710-111">This in turn guarantees that the input pin is not blocked waiting for **GetBuffer** or **Receive**.</span></span> <span data-ttu-id="86710-112">Si el método **Receive** del PIN espera alguna vez en un evento (por ejemplo, para obtener recursos), el método **BeginFlush** debe forzar la espera para finalizar estableciendo el evento.</span><span class="sxs-lookup"><span data-stu-id="86710-112">If your pin's **Receive** method ever waits on an event (for example, to get resources), the **BeginFlush** method should force the wait to terminate by setting the event.</span></span> <span data-ttu-id="86710-113">En este momento, se garantiza que el método **Receive** devuelve y la marca **m \_ bFlushing** impide que las nuevas llamadas de **recepción** realicen cualquier trabajo.</span><span class="sxs-lookup"><span data-stu-id="86710-113">At this point, the **Receive** method is guaranteed to return, and the **m\_bFlushing** flag prevents new **Receive** calls from doing any work.</span></span>

<span data-ttu-id="86710-114">En algunos filtros, es necesario que todos los **BeginFlush** .</span><span class="sxs-lookup"><span data-stu-id="86710-114">For some filters, that is all **BeginFlush** needs to do.</span></span> <span data-ttu-id="86710-115">El método **EndFlush** señalará al filtro que puede empezar a recibir muestras de nuevo.</span><span class="sxs-lookup"><span data-stu-id="86710-115">The **EndFlush** method will signal to the filter that it can start receiving samples again.</span></span> <span data-ttu-id="86710-116">Es posible que otros filtros deban usar variables o recursos de **BeginFlush** que también se usan en la **recepción**.</span><span class="sxs-lookup"><span data-stu-id="86710-116">Other filters may need to use variables or resources in **BeginFlush** that are also used in **Receive**.</span></span> <span data-ttu-id="86710-117">En ese caso, el filtro debe mantener el bloqueo de streaming en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="86710-117">In that case, the filter should hold the streaming lock first.</span></span> <span data-ttu-id="86710-118">Asegúrese de no hacerlo antes de ninguno de los pasos anteriores, ya que podría provocar un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="86710-118">Be sure not to do this before any of the previous steps, because you might cause a deadlock.</span></span>

<span data-ttu-id="86710-119">El método **EndFlush** contiene el bloqueo de filtro y propaga la llamada de nivel inferior:</span><span class="sxs-lookup"><span data-stu-id="86710-119">The **EndFlush** method holds the filter lock and propagates the call downstream:</span></span>


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



<span data-ttu-id="86710-120">El método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) restablece la marca **m \_ bFlushing** en **false**, lo que permite que el método **Receive** empiece a recibir ejemplos de nuevo.</span><span class="sxs-lookup"><span data-stu-id="86710-120">The [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method resets the **m\_bFlushing** flag to **FALSE**, which allows the **Receive** method to start receiving samples again.</span></span> <span data-ttu-id="86710-121">Este debe ser el último paso de **EndFlush**, porque el PIN no debe recibir ningún ejemplo hasta que se complete el vaciado y se notifiquen todos los filtros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="86710-121">This should be the last step in **EndFlush**, because the pin must not receive any samples until flushing is complete and all downstream filters are notified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86710-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86710-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86710-123">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="86710-123">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



