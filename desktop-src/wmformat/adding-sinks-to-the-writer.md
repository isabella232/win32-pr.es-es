---
title: Agregar receptores al escritor
description: Agregar receptores al escritor
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Advanced Systems Format (ASF), agregar receptores al escritor
- ASF (formato de sistemas avanzados), agregar receptores al escritor
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- Advanced Systems Format (ASF), receptores de escritor
- ASF (formato de sistemas avanzados), receptores de escritor
- receptores, agregar al escritor
- receptores de escritor, agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420275"
---
# <a name="adding-sinks-to-the-writer"></a><span data-ttu-id="70ef5-111">Agregar receptores al escritor</span><span class="sxs-lookup"><span data-stu-id="70ef5-111">Adding Sinks to the Writer</span></span>

<span data-ttu-id="70ef5-112">Los receptores de escritor son objetos independientes del escritor y se deben agregar al escritor que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="70ef5-112">Writer sinks are separate objects from the writer and must be added to the writer to be used.</span></span> <span data-ttu-id="70ef5-113">Si está escribiendo en un archivo, simplemente puede llamar a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), que configurará el receptor de archivos automáticamente.</span><span class="sxs-lookup"><span data-stu-id="70ef5-113">If you are writing to a file, you can simply call [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), which will set up the file sink automatically.</span></span> <span data-ttu-id="70ef5-114">De lo contrario, para agregar un receptor al escritor, llame al método [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) .</span><span class="sxs-lookup"><span data-stu-id="70ef5-114">Otherwise, to add a sink to the writer, call the [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) method.</span></span> <span data-ttu-id="70ef5-115">**AddSink** requiere un puntero a la interfaz [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) del receptor.</span><span class="sxs-lookup"><span data-stu-id="70ef5-115">**AddSink** requires a pointer to the [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) interface of the sink.</span></span>

<span data-ttu-id="70ef5-116">Cuando haya terminado de usar un receptor, debe cerrarlo llamando al método adecuado, en función del tipo de receptor y, a continuación, quitarlo del escritor llamando a [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span><span class="sxs-lookup"><span data-stu-id="70ef5-116">When you are finished using a sink, you should close it by calling the appropriate method, depending on the type of sink, and then remove it from the writer by calling [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span></span>

<span data-ttu-id="70ef5-117">En el ejemplo de código siguiente se muestra cómo crear un receptor de archivo de escritor y agregarlo al escritor.</span><span class="sxs-lookup"><span data-stu-id="70ef5-117">The following example code shows how to create a writer file sink and add it to the writer.</span></span> <span data-ttu-id="70ef5-118">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="70ef5-118">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="70ef5-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70ef5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70ef5-120">**Obtener mensajes de error de un receptor**</span><span class="sxs-lookup"><span data-stu-id="70ef5-120">**Getting Error Messages from a Sink**</span></span>](getting-error-messages-from-a-sink.md)
</dt> <dt>

[<span data-ttu-id="70ef5-121">**Interfaz IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="70ef5-121">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="70ef5-122">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="70ef5-122">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




