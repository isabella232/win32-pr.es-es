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
# <a name="flushing-data"></a>Vaciar datos

En el siguiente pseudocódigo se muestra cómo implementar el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :


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



Cuando se inicia el vaciado, el método **BeginFlush** toma el bloqueo de filtro, que serializa el cambio de estado. Todavía no es seguro realizar el bloqueo de streaming, porque el vaciado se produce en el subproceso de la aplicación y el subproceso de streaming puede estar en medio de una llamada de **recepción** . El PIN debe garantizar que la **recepción** no esté bloqueada y que se produzca un error en todas las llamadas posteriores a **Receive** . El método [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) establece una marca interna, [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md). Cuando la marca es **true**, se produce un error en el método **Receive** .

Al entregar la llamada **BeginFlush** downstream, el PIN garantiza que todos los filtros de nivel inferior liberan sus ejemplos y devuelven desde las llamadas de **recepción** . A su vez, garantiza que el PIN de entrada no se bloquea en espera de la acción **getBuffer** o **Receive**. Si el método **Receive** del PIN espera alguna vez en un evento (por ejemplo, para obtener recursos), el método **BeginFlush** debe forzar la espera para finalizar estableciendo el evento. En este momento, se garantiza que el método **Receive** devuelve y la marca **m \_ bFlushing** impide que las nuevas llamadas de **recepción** realicen cualquier trabajo.

En algunos filtros, es necesario que todos los **BeginFlush** . El método **EndFlush** señalará al filtro que puede empezar a recibir muestras de nuevo. Es posible que otros filtros deban usar variables o recursos de **BeginFlush** que también se usan en la **recepción**. En ese caso, el filtro debe mantener el bloqueo de streaming en primer lugar. Asegúrese de no hacerlo antes de ninguno de los pasos anteriores, ya que podría provocar un interbloqueo.

El método **EndFlush** contiene el bloqueo de filtro y propaga la llamada de nivel inferior:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



El método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) restablece la marca **m \_ bFlushing** en **false**, lo que permite que el método **Receive** empiece a recibir ejemplos de nuevo. Este debe ser el último paso de **EndFlush**, porque el PIN no debe recibir ningún ejemplo hasta que se complete el vaciado y se notifiquen todos los filtros de nivel inferior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



