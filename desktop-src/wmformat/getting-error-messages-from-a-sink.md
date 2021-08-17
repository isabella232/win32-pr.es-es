---
title: Obtener mensajes de error de un receptor
description: Obtener mensajes de error de un receptor
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Formato de sistemas avanzados (ASF), mensajes de error de receptores
- ASF (formato de sistemas avanzados), mensajes de error de receptores
- Formato de sistemas avanzados (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- sinks,error messages
- mensajes de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e432f805b5e33de0e830a2f319713bccec328d429f8eb04064d87edc56bf375c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930875"
---
# <a name="getting-error-messages-from-a-sink"></a>Obtener mensajes de error de un receptor

El objeto writer no envía mensajes al método de devolución de llamada [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Sin embargo, puede establecer receptores de escritor para enviar mensajes a OnStatus. Cada receptor debe establecerse para entregar el estado por separado, pero todos los receptores pueden informar a la misma devolución de llamada.

Para establecer un receptor para entregar mensajes de estado a **OnStatus,** llame al [**método IWMRegisterCallback::Advise.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise)

En el código de ejemplo siguiente se muestra cómo establecer todos los receptores para entregar mensajes de estado a una **devolución de llamada OnStatus.** En este ejemplo, el índice de cada receptor se usará como parámetro de contexto para que el **método OnStatus** pueda diferenciar entre los mensajes de los distintos receptores. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


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

[**IWMRegisterCallback (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




