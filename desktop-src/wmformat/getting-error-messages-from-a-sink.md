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
# <a name="getting-error-messages-from-a-sink"></a>Obtener mensajes de error de un receptor

El objeto de escritor no envía mensajes al método de devolución de llamada [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Sin embargo, puede establecer receptores de escritor para enviar mensajes a un estado. Cada receptor debe establecerse para que entregue el estado por separado, pero todos los receptores pueden informar a la misma devolución de llamada.

Para establecer un receptor con el fin de proporcionar mensajes de estado a un **Estado**, llame al método [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) .

En el ejemplo de código siguiente se muestra cómo establecer todos los receptores para proporcionar mensajes de estado a una devolución de llamada de **Estado** . En este ejemplo, se utilizará el índice de cada receptor como parámetro de contexto para que el método de **Estado** pueda diferenciar los mensajes de los distintos receptores. Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




