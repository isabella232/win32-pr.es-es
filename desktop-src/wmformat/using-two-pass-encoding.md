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
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a><span data-ttu-id="1eb05-111">Usar la codificación de Two-Pass (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="1eb05-111">Using Two-Pass Encoding (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="1eb05-112">Algunos códecs admiten la codificación de dos pasos para determinados formatos.</span><span class="sxs-lookup"><span data-stu-id="1eb05-112">Some codecs support two-pass encoding for certain formats.</span></span> <span data-ttu-id="1eb05-113">En algunos casos, un códec requiere que un formato especificado se codifique con dos pasos.</span><span class="sxs-lookup"><span data-stu-id="1eb05-113">In some cases, a codec requires that a specified format be encoded using two passes.</span></span> <span data-ttu-id="1eb05-114">Cuando se usa la codificación de dos pasos, se envían los ejemplos de la secuencia al códec antes de la fase de codificación.</span><span class="sxs-lookup"><span data-stu-id="1eb05-114">When two-pass encoding is used, you send the samples for the stream to the codec before the encoding pass.</span></span> <span data-ttu-id="1eb05-115">El códec analiza los ejemplos y configura la fase de codificación basada en el análisis.</span><span class="sxs-lookup"><span data-stu-id="1eb05-115">The codec analyzes the samples and configures the encoding pass based on the analysis.</span></span> <span data-ttu-id="1eb05-116">Esto da como resultado un archivo codificado de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="1eb05-116">This results in a more efficiently encoded file.</span></span>

<span data-ttu-id="1eb05-117">Para determinar si un códec admite la codificación de un paso, o dos pasos, o ambos, para un formato determinado, llame a [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) con g \_ wszNumPasses y el valor adecuado y, a continuación, enumere los formatos para ver si se devuelve el que desea.</span><span class="sxs-lookup"><span data-stu-id="1eb05-117">To determine whether a codec supports one-pass encoding, or two-pass, or both, for a given format, call [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) with g\_wszNumPasses and the appropriate value, and then enumerate the formats to see if the one you want is returned.</span></span> <span data-ttu-id="1eb05-118">Para obtener más información acerca de los códecs de Windows Media que admiten la codificación de dos pasos, consulte [elección de un método de codificación](choosing-an-encoding-method.md).</span><span class="sxs-lookup"><span data-stu-id="1eb05-118">For more information about the Windows Media codecs that support two-pass encoding, see [Choosing an Encoding Method](choosing-an-encoding-method.md).</span></span>

<span data-ttu-id="1eb05-119">Puede usar la codificación de dos pasos con el SDK de Windows Media Format llamando a los métodos de la interfaz [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="1eb05-119">You can use two-pass encoding with the Windows Media Format SDK by calling methods of the [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) interface.</span></span>

<span data-ttu-id="1eb05-120">En los casos en los que la codificación de dos pasos es necesaria para un formato determinado, pero la aplicación no puede realizar un paso de preprocesamiento, se producirá un error en la primera llamada a [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) con la cantidad de número de llamadas \_ \_ no válidas NS E \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1eb05-120">In cases where two-pass encoding is required for a particular format, but the application fails to perform a preprocessing pass, the first call to [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) will fail with NS\_E\_INVALID\_NUM\_PASSES.</span></span>

<span data-ttu-id="1eb05-121">En la función de ejemplo siguiente se muestra cómo realizar la codificación de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="1eb05-121">The following example function demonstrates how to perform two-pass encoding.</span></span> <span data-ttu-id="1eb05-122">Se llama a esta función una vez que el escritor se ha establecido con un perfil y se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="1eb05-122">This function is called after the writer has been set with a profile and started.</span></span> <span data-ttu-id="1eb05-123">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1eb05-123">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1eb05-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1eb05-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eb05-125">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="1eb05-125">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




