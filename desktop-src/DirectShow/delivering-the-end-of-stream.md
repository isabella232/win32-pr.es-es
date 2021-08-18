---
description: Entrega del final de la secuencia
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Entrega del final de la secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebae0fe3238f32f630c0a2ecd0787f6bd9b75a9aed6342e202f187d3fe8dac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831355"
---
# <a name="delivering-the-end-of-stream"></a>Entrega del final de la secuencia

Cuando el pin de entrada recibe una notificación de fin de flujo, propaga la llamada de nivel inferior. Los filtros de nivel inferior que reciban datos de este pin de entrada también deben recibir la notificación de fin de flujo. De nuevo, tome el bloqueo de streaming y no el bloqueo de filtro. Si el filtro tiene datos pendientes que aún no se han entregado, el filtro debe entregarlo ahora, antes de enviar la notificación de fin de flujo. No debe enviar ningún dato después del final de la secuencia.


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

 

 



