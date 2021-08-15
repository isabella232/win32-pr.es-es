---
description: Recepción y entrega de ejemplos
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Recepción y entrega de ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e507cb3e20a8fd08c891cca5143f8bbf8c9d4f9a90bad27dc201dd43c43283e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952154"
---
# <a name="receiving-and-delivering-samples"></a>Recepción y entrega de ejemplos

El pseudocódigo siguiente muestra cómo implementar el **método IMemInput::Receive:**


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



El **método Receive** contiene el bloqueo de streaming, no el bloqueo de filtro. Es posible que el filtro tenga que esperar en algún evento para poder procesar los datos, que se muestra aquí mediante la llamada a **WaitForSingleObject**. No todos los filtros tendrán que hacerlo. El [**método CBaseInputPin::Receive**](cbaseinputpin-receive.md) comprueba algunas condiciones generales de streaming. Devuelve VFW E WRONG STATE si se detiene el filtro, S FALSE si el filtro se \_ \_ \_ \_ vacía, etc. Cualquier código de retorno distinto de S \_ OK indica que el método **Receive** debe devolverse inmediatamente y no procesar el ejemplo.

Una vez procesado el ejemplo, puede entregarlo al filtro de bajada mediante una llamada a [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md). Este método auxiliar llama **a IMemInputPin::Receive en** el pin de entrada de bajada. Un filtro podría entregar muestras a varios pines.

 

 



