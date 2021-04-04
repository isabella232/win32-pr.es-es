---
description: Recibir y entregar ejemplos
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Recibir y entregar ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906535"
---
# <a name="receiving-and-delivering-samples"></a>Recibir y entregar ejemplos

En el siguiente pseudocódigo se muestra cómo implementar el método **IMemInput:: Receive** :


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



El método **Receive** contiene el bloqueo de streaming, no el bloqueo Filter. Es posible que el filtro tenga que esperar en algún evento antes de que pueda procesar los datos, que se muestran aquí mediante la llamada a **WaitForSingleObject**. No todos los filtros deberán hacerlo. El método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) comprueba algunas condiciones generales de streaming. Devuelve \_ \_ el estado VFW E incorrecto \_ si se detiene el filtro, es \_ false si se está vaciando el filtro, etc. Cualquier código de retorno distinto de S \_ OK indica que el método **Receive** debe volver inmediatamente y no procesar el ejemplo.

Una vez procesado el ejemplo, entréguelo al filtro de bajada llamando a [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md). Este método auxiliar llama a **IMemInputPin:: Receive** en el PIN de entrada de nivel inferior. Un filtro puede proporcionar ejemplos a varios PIN.

 

 



