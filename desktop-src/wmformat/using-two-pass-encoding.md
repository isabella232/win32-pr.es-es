---
title: Uso de Two-Pass codificación (Windows SDK de formato multimedia 11)
description: Uso de Two-Pass codificación
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- Formato de sistemas avanzados (ASF), codificación de dos pases
- ASF (formato de sistemas avanzados), codificación de dos pases
- codificación de dos pases, acerca de
- Codificación de 2 pases, acerca de
- códecs, codificación de dos pases
- Codificación de dos pases, interfaz IWMWriterPreprocess
- Codificación de 2 pases, interfaz IWMWriterPreprocess
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0683af636197b3f8116fca4dea85ce15609d2c99b0d9e0c11dfe0a2662a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653840"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Uso de Two-Pass codificación (Windows SDK de formato multimedia 11)

Algunos códecs admiten la codificación de dos pases para determinados formatos. En algunos casos, un códec requiere codificar un formato especificado mediante dos pases. Cuando se usa la codificación de dos pases, se envían los ejemplos de la secuencia al códec antes de que pase la codificación. El códec analiza los ejemplos y configura el paso de codificación en función del análisis. Esto da como resultado un archivo codificado de forma más eficaz.

Para determinar si un códec admite la codificación de un paso, o dos pases, o ambos, para un formato determinado, llame a [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) con g wszNumPasses y el valor adecuado y, a continuación, enumere los formatos para ver si se devuelve el que \_ desea. Para obtener más información sobre los códecs Windows media que admiten la codificación de dos pases, vea [Elegir un método de codificación](choosing-an-encoding-method.md).

Puede usar la codificación de dos pases con el SDK Windows Media Format llamando a métodos de la [**interfaz IWMWriterPreprocess.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess)

En los casos en los que se requiere la codificación de dos pases para un formato determinado, pero la aplicación no puede realizar un paso de preprocesamiento, se producirá un error en la primera llamada a [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) con NS \_ E INVALID NUM \_ \_ \_ PASSES.

En la siguiente función de ejemplo se muestra cómo realizar la codificación de dos pasos. Se llama a esta función después de que el escritor se haya establecido con un perfil y se haya iniciado. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


```C++
HRESULT PreProcess(IWMWriter* pWriter, DWORD dwInputNum)
{
    HRESULT hr        = S_OK;
    DWORD   dwMaxPass = 0;

    IWMWriterPreprocess* pPreProc = NULL;

    // Get the writer preprocessor interface.
    hr = pWriter->QueryInterface(IID_IWMWriterPreprocess, 
                                 (void**) &pPreProc);
    GOTO_EXIT_IF_FAILED(hr);

    // Check that the input can be preprocessed.
    hr = pPreProc->GetMaxPreprocessingPasses(dwInputNum,0, &dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    if(dwMaxPass == 0)
    {
        hr = NS_E_INVALID_REQUEST;
        goto Exit;
    }

    // Set the number of preprocessing passes to the maximum.
    hr = pPreProc->SetNumPreprocessingPasses(dwInputNum, 0, dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    // Call BeginWriting before calling BeginPreprocessingPass
    hr = pWriter->BeginWriting();

    // Start preprocessing the first pass.
    hr = pPreProc->BeginPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: Make repeated calls to pPreProc->PreprocessSample to
    // preprocess all the samples in the stream.

    // End preprocessing.
    hr = pPreProc->EndPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: If the maximum number of preprocessing passes is greater
    // than one, repeat the preprocessing steps for each pass.

Exit:
    SAFE_RELEASE(pPreProc);
    Return hr;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




