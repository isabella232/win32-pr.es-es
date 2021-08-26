---
description: Vaciar datos
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Vaciar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a435bf40ae9f71b35707935812c3a935a95df1904db00a652634b171f20a10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965465"
---
# <a name="flushing-data"></a>Vaciar datos

El pseudocódigo siguiente muestra cómo implementar el [**método IPin::BeginFlush:**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)


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



Cuando se inicia el vaciado, el **método BeginFlush** toma el bloqueo de filtro, que serializa el cambio de estado. Todavía no es seguro tomar el bloqueo de streaming, ya que el vaciado se produce en el subproceso de aplicación y el subproceso de streaming podría estar en medio de una **llamada receive.** El pin debe garantizar que **Receive** no está bloqueado y que se producirá un error en las llamadas posteriores a **Receive.** El [**método CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) establece una marca interna, [**CBaseInputPin::m \_ bFlushing**](cbaseinputpin-m-bflushing.md). Cuando la marca es **TRUE**, se produce un error **en el método Receive.**

Al entregar la **llamada BeginFlush** de bajada, el pin garantiza que todos los filtros de nivel inferior liberen sus muestras y devuelvan de **las llamadas receive.** Esto, a su vez, garantiza que la marca de entrada no se bloquee a la espera de **GetBuffer** o **Receive**. Si el método **Receive** del pin espera algún momento en un evento (por ejemplo, para obtener recursos), el método **BeginFlush** debe forzar la espera para finalizar estableciendo el evento. En este momento, se garantiza la devolución del método **Receive** y la marca **m \_ bFlushing** impide que las nuevas llamadas **Receive** haga cualquier trabajo.

Para algunos filtros, eso es todo lo que debe hacer **BeginFlush.** El **método EndFlush** señalará al filtro que puede empezar a recibir muestras de nuevo. Es posible que otros filtros necesiten usar variables o recursos **en BeginFlush** que también se usan en **Receive**. En ese caso, el filtro debe contener primero el bloqueo de streaming. Asegúrese de no hacerlo antes de ninguno de los pasos anteriores, ya que podría provocar un interbloqueo.

El **método EndFlush** mantiene el bloqueo de filtro y propaga la llamada de nivel inferior:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



El [**método CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) restablece la marca **m \_ bFlushing** a **FALSE,** lo que permite que el **método Receive** empiece a recibir muestras de nuevo. Este debe ser el último paso de **EndFlush,** ya que el pin no debe recibir muestras hasta que se complete el vaciado y se notifiquen todos los filtros de nivel inferior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



