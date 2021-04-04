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
# <a name="receiving-and-delivering-samples"></a><span data-ttu-id="59be5-103">Recibir y entregar ejemplos</span><span class="sxs-lookup"><span data-stu-id="59be5-103">Receiving and Delivering Samples</span></span>

<span data-ttu-id="59be5-104">En el siguiente pseudocódigo se muestra cómo implementar el método **IMemInput:: Receive** :</span><span class="sxs-lookup"><span data-stu-id="59be5-104">The following pseudocode shows how to implement the **IMemInput::Receive** method:</span></span>


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



<span data-ttu-id="59be5-105">El método **Receive** contiene el bloqueo de streaming, no el bloqueo Filter.</span><span class="sxs-lookup"><span data-stu-id="59be5-105">The **Receive** method holds the streaming lock, not the filter lock.</span></span> <span data-ttu-id="59be5-106">Es posible que el filtro tenga que esperar en algún evento antes de que pueda procesar los datos, que se muestran aquí mediante la llamada a **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="59be5-106">The filter might need to wait on some event before it can process the data, shown here by the call to **WaitForSingleObject**.</span></span> <span data-ttu-id="59be5-107">No todos los filtros deberán hacerlo.</span><span class="sxs-lookup"><span data-stu-id="59be5-107">Not every filter will need to do this.</span></span> <span data-ttu-id="59be5-108">El método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) comprueba algunas condiciones generales de streaming.</span><span class="sxs-lookup"><span data-stu-id="59be5-108">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method verifies some general streaming conditions.</span></span> <span data-ttu-id="59be5-109">Devuelve \_ \_ el estado VFW E incorrecto \_ si se detiene el filtro, es \_ false si se está vaciando el filtro, etc.</span><span class="sxs-lookup"><span data-stu-id="59be5-109">It returns VFW\_E\_WRONG\_STATE if the filter is stopped, S\_FALSE if the filter is flushing, and so forth.</span></span> <span data-ttu-id="59be5-110">Cualquier código de retorno distinto de S \_ OK indica que el método **Receive** debe volver inmediatamente y no procesar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59be5-110">Any return code other than S\_OK indicates that the **Receive** method should return immediately and not process the sample.</span></span>

<span data-ttu-id="59be5-111">Una vez procesado el ejemplo, entréguelo al filtro de bajada llamando a [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md).</span><span class="sxs-lookup"><span data-stu-id="59be5-111">After the sample is processed, deliver it to the downstream filter by calling [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md).</span></span> <span data-ttu-id="59be5-112">Este método auxiliar llama a **IMemInputPin:: Receive** en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="59be5-112">This helper method calls **IMemInputPin::Receive** on the downstream input pin.</span></span> <span data-ttu-id="59be5-113">Un filtro puede proporcionar ejemplos a varios PIN.</span><span class="sxs-lookup"><span data-stu-id="59be5-113">A filter might deliver samples to several pins.</span></span>

 

 



