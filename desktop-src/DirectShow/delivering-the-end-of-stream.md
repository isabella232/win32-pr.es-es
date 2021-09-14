---
description: Entrega del final de la secuencia
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Entrega del final de la secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061238"
---
# <a name="delivering-the-end-of-stream"></a>Entrega del final de la secuencia

Cuando el pin de entrada recibe una notificación de fin de flujo, propaga la llamada de nivel inferior. Los filtros de nivel inferior que reciben datos de este pin de entrada también deben obtener la notificación de fin de flujo. De nuevo, tome el bloqueo de streaming y no el bloqueo de filtro. Si el filtro tiene datos pendientes que aún no se entregaron, el filtro debe entregarlo ahora, antes de enviar la notificación de fin de flujo. No debe enviar ningún dato después del final de la secuencia.


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



El [**método CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) llama a [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el pin de entrada de bajada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



