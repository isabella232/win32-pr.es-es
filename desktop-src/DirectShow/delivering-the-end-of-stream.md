---
description: Entrega del final de la secuencia
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Entrega del final de la secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906387"
---
# <a name="delivering-the-end-of-stream"></a><span data-ttu-id="0d6cf-103">Entrega del final de la secuencia</span><span class="sxs-lookup"><span data-stu-id="0d6cf-103">Delivering the End of Stream</span></span>

<span data-ttu-id="0d6cf-104">Cuando el PIN de entrada recibe una notificación de final de secuencia, propaga la llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-104">When the input pin receives an end-of-stream notification, it propagates the call downstream.</span></span> <span data-ttu-id="0d6cf-105">Cualquier filtro de nivel inferior que reciba datos de este pin de entrada también debe obtener la notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-105">Any downstream filters that receive data from this input pin should also get the end-of-stream notification.</span></span> <span data-ttu-id="0d6cf-106">De nuevo, realice el bloqueo de streaming y no el bloqueo del filtro.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-106">Again, take the streaming lock and not the filter lock.</span></span> <span data-ttu-id="0d6cf-107">Si el filtro tiene datos pendientes que todavía no se han entregado, el filtro debería entregarlo ahora, antes de enviar la notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-107">If the filter has pending data that was not yet delivered, the filter should deliver it now, before it sends the end-of-stream notification.</span></span> <span data-ttu-id="0d6cf-108">No debe enviar datos después del final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-108">It should not send any data after the end of the stream.</span></span>


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



<span data-ttu-id="0d6cf-109">El método [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) llama a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-109">The [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method calls [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d6cf-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d6cf-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d6cf-111">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="0d6cf-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



