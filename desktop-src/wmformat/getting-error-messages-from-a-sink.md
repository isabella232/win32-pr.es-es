---
title: Obtener mensajes de error de un receptor
description: Obtener mensajes de error de un receptor
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Advanced Systems Format (ASF), mensajes de error de receptores
- ASF (formato de sistemas avanzados), mensajes de error de receptores
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, mensajes de error
- mensajes de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b3fbb43d72107dbffc13eb27425e253bc13839
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149086"
---
# <a name="getting-error-messages-from-a-sink"></a><span data-ttu-id="0ca6f-109">Obtener mensajes de error de un receptor</span><span class="sxs-lookup"><span data-stu-id="0ca6f-109">Getting Error Messages from a Sink</span></span>

<span data-ttu-id="0ca6f-110">El objeto de escritor no envía mensajes al método de devolución de llamada [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="0ca6f-110">The writer object does not send messages to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="0ca6f-111">Sin embargo, puede establecer receptores de escritor para enviar mensajes a un estado.</span><span class="sxs-lookup"><span data-stu-id="0ca6f-111">However, you can set writer sinks to send messages to OnStatus.</span></span> <span data-ttu-id="0ca6f-112">Cada receptor debe establecerse para que entregue el estado por separado, pero todos los receptores pueden informar a la misma devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0ca6f-112">Each sink must be set to deliver status separately, but all sinks can report to the same callback.</span></span>

<span data-ttu-id="0ca6f-113">Para establecer un receptor con el fin de proporcionar mensajes de estado a un **Estado**, llame al método [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) .</span><span class="sxs-lookup"><span data-stu-id="0ca6f-113">To set a sink to deliver status messages to **OnStatus**, call the [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) method.</span></span>

<span data-ttu-id="0ca6f-114">En el ejemplo de código siguiente se muestra cómo establecer todos los receptores para proporcionar mensajes de estado a una devolución de llamada de **Estado** .</span><span class="sxs-lookup"><span data-stu-id="0ca6f-114">The following example code demonstrates how to set all of the sinks to deliver status messages to an **OnStatus** callback.</span></span> <span data-ttu-id="0ca6f-115">En este ejemplo, se utilizará el índice de cada receptor como parámetro de contexto para que el método de **Estado** pueda diferenciar los mensajes de los distintos receptores.</span><span class="sxs-lookup"><span data-stu-id="0ca6f-115">In this example, the index of each sink will be used as the context parameter so that the **OnStatus** method can differentiate between messages from the different sinks.</span></span> <span data-ttu-id="0ca6f-116">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0ca6f-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="0ca6f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ca6f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ca6f-118">**Interfaz IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="0ca6f-118">**IWMRegisterCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[<span data-ttu-id="0ca6f-119">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="0ca6f-119">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




