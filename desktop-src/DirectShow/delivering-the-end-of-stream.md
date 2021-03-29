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
# <a name="delivering-the-end-of-stream"></a>Entrega del final de la secuencia

Cuando el PIN de entrada recibe una notificación de final de secuencia, propaga la llamada de nivel inferior. Cualquier filtro de nivel inferior que reciba datos de este pin de entrada también debe obtener la notificación de final de secuencia. De nuevo, realice el bloqueo de streaming y no el bloqueo del filtro. Si el filtro tiene datos pendientes que todavía no se han entregado, el filtro debería entregarlo ahora, antes de enviar la notificación de final de secuencia. No debe enviar datos después del final de la secuencia.


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



El método [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) llama a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada de nivel inferior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



