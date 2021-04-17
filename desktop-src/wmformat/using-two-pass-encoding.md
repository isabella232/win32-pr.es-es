---
title: Usar la codificación de Two-Pass (Windows Media Format 11 SDK)
description: Uso de la codificación de Two-Pass
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- Advanced Systems Format (ASF), codificación de dos pasos
- ASF (formato de sistemas avanzados), codificación de dos pasos
- codificación de dos pasos, acerca de
- 2-paso de codificación, acerca de
- códecs, codificación de dos pasos
- codificación de dos pasos, interfaz IWMWriterPreprocess
- codificación paso 2, interfaz IWMWriterPreprocess
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3794856f47c1656cc53006268c41a063cdde96
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533723"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Usar la codificación de Two-Pass (Windows Media Format 11 SDK)

Algunos códecs admiten la codificación de dos pasos para determinados formatos. En algunos casos, un códec requiere que un formato especificado se codifique con dos pasos. Cuando se usa la codificación de dos pasos, se envían los ejemplos de la secuencia al códec antes de la fase de codificación. El códec analiza los ejemplos y configura la fase de codificación basada en el análisis. Esto da como resultado un archivo codificado de forma más eficaz.

Para determinar si un códec admite la codificación de un paso, o dos pasos, o ambos, para un formato determinado, llame a [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) con g \_ wszNumPasses y el valor adecuado y, a continuación, enumere los formatos para ver si se devuelve el que desea. Para obtener más información acerca de los códecs de Windows Media que admiten la codificación de dos pasos, consulte [elección de un método de codificación](choosing-an-encoding-method.md).

Puede usar la codificación de dos pasos con el SDK de Windows Media Format llamando a los métodos de la interfaz [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .

En los casos en los que la codificación de dos pasos es necesaria para un formato determinado, pero la aplicación no puede realizar un paso de preprocesamiento, se producirá un error en la primera llamada a [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) con la cantidad de número de llamadas \_ \_ no válidas NS E \_ \_ .

En la función de ejemplo siguiente se muestra cómo realizar la codificación de dos pasos. Se llama a esta función una vez que el escritor se ha establecido con un perfil y se ha iniciado. Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


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

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




