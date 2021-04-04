---
title: Para enumerar los formatos de entrada
description: Para enumerar los formatos de entrada
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Advanced Systems Format (ASF), enumerar formatos de entrada
- ASF (formato de sistemas avanzados), enumerar formatos de entrada
- perfiles, enumerar formatos de entrada
- códecs, enumerar formatos de entrada
- Advanced Systems Format (ASF), enumeraciones de formato de entrada
- ASF (formato de sistemas avanzados), enumeraciones de formato de entrada
- perfiles, enumeraciones de formato de entrada
- códecs, enumeraciones de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077447"
---
# <a name="to-enumerate-input-formats"></a><span data-ttu-id="d84b0-111">Para enumerar los formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="d84b0-111">To Enumerate Input Formats</span></span>

<span data-ttu-id="d84b0-112">Cada uno de los códecs de Windows Media acepta uno o más tipos de medios de entrada para la compresión.</span><span class="sxs-lookup"><span data-stu-id="d84b0-112">Each of the Windows Media codecs accepts one or more types of input media for compression.</span></span> <span data-ttu-id="d84b0-113">El SDK de Windows Media Format permite especificar una mayor variedad de formatos que los que admiten los códecs.</span><span class="sxs-lookup"><span data-stu-id="d84b0-113">The Windows Media Format SDK enables you to input a wider variety of formats than those supported by the codecs.</span></span> <span data-ttu-id="d84b0-114">Para ello, el SDK realiza transformaciones previas al procesamiento en las entradas cuando es necesario, como cambiar el tamaño de los fotogramas de vídeo o volver a muestrear el audio.</span><span class="sxs-lookup"><span data-stu-id="d84b0-114">The SDK does this by performing pre-processing transformations on the inputs when necessary, such as resizing video frames or resampling audio.</span></span> <span data-ttu-id="d84b0-115">En cualquier caso, debe asegurarse de que los formatos de entrada de los archivos que escribe coinciden con los datos que envía al escritor.</span><span class="sxs-lookup"><span data-stu-id="d84b0-115">In any case, you must ensure that the input formats for the files you write match the data you send to the writer.</span></span> <span data-ttu-id="d84b0-116">Cada códec tiene un formato de medio de entrada predeterminado que se establece en el escritor cuando se carga el perfil.</span><span class="sxs-lookup"><span data-stu-id="d84b0-116">Each codec has a default input media format that is set in the writer when the profile is loaded.</span></span> <span data-ttu-id="d84b0-117">Puede examinar el formato de entrada predeterminado llamando a [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="d84b0-117">You can examine the default input format by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>

<span data-ttu-id="d84b0-118">Los códecs de vídeo admiten los formatos siguientes: IYUV, i420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 y RGB 8.</span><span class="sxs-lookup"><span data-stu-id="d84b0-118">The video codecs support the following formats: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555, and RGB 8.</span></span> <span data-ttu-id="d84b0-119">Los códecs de audio admiten audio PCM.</span><span class="sxs-lookup"><span data-stu-id="d84b0-119">The audio codecs support PCM audio.</span></span>

<span data-ttu-id="d84b0-120">Para enumerar los formatos de entrada admitidos por un códec, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d84b0-120">To enumerate the input formats supported by a codec, perform the following steps:</span></span>

1.  <span data-ttu-id="d84b0-121">Cree un objeto de escritor y establezca un perfil para usarlo.</span><span class="sxs-lookup"><span data-stu-id="d84b0-121">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="d84b0-122">Para obtener más información sobre la configuración de perfiles en el escritor, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="d84b0-122">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
2.  <span data-ttu-id="d84b0-123">Identifique el número de entrada para el que desea comprobar los formatos.</span><span class="sxs-lookup"><span data-stu-id="d84b0-123">Identify the input number for which you want to check the formats.</span></span> <span data-ttu-id="d84b0-124">Para obtener más información acerca de la identificación de números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="d84b0-124">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="d84b0-125">Recupere el número total de formatos de entrada admitidos por la entrada deseada llamando a [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span><span class="sxs-lookup"><span data-stu-id="d84b0-125">Retrieve the total number of input formats supported by the desired input by calling [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span></span>
4.  <span data-ttu-id="d84b0-126">Recorra en bucle todos los formatos de entrada admitidos y realice los pasos siguientes para cada uno.</span><span class="sxs-lookup"><span data-stu-id="d84b0-126">Loop through all of the supported input formats, performing the following steps for each.</span></span>
    -   <span data-ttu-id="d84b0-127">Recupere la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para el formato de entrada mediante una llamada a [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span><span class="sxs-lookup"><span data-stu-id="d84b0-127">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input format by calling [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span></span>
    -   <span data-ttu-id="d84b0-128">Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="d84b0-128">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the input format.</span></span> <span data-ttu-id="d84b0-129">Llame a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), pasando **null** para el parámetro *pType* para obtener el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="d84b0-129">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passing **NULL** for the *pType* parameter to get the size of the structure.</span></span> <span data-ttu-id="d84b0-130">A continuación, asigne memoria para que contenga la estructura y llame de nuevo a **GetMediaType** para obtener la estructura.</span><span class="sxs-lookup"><span data-stu-id="d84b0-130">Then allocate memory to hold the structure and call **GetMediaType** again to get the structure.</span></span> <span data-ttu-id="d84b0-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) hereda de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), por lo que puede realizar las llamadas a **GetMediaType** desde la instancia de **IWMInputMediaProps** recuperada en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="d84b0-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) inherits from [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), so you can make the calls to **GetMediaType** from the instance of **IWMInputMediaProps** retrieved in the previous step.</span></span>
    -   <span data-ttu-id="d84b0-132">El formato descrito en la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene toda la información pertinente sobre el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="d84b0-132">The format described in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains all of the pertinent information about the input format.</span></span> <span data-ttu-id="d84b0-133">El formato básico de los medios se identifica mediante el **tipo de medio de WM \_ \_ . SubType**.</span><span class="sxs-lookup"><span data-stu-id="d84b0-133">The basic format of the media is identified by **WM\_MEDIA\_TYPE.subtype**.</span></span> <span data-ttu-id="d84b0-134">En el caso de las secuencias de vídeo, el miembro **pbFormat** apunta a una estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) asignada dinámicamente que contiene más detalles sobre la secuencia, incluido el tamaño del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="d84b0-134">For video streams, the **pbFormat** member points to a dynamically allocated [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure which contains further details about the stream, including rectangle size.</span></span> <span data-ttu-id="d84b0-135">No es necesario que el tamaño de los fotogramas de entrada coincida exactamente con el que admite el códec.</span><span class="sxs-lookup"><span data-stu-id="d84b0-135">The size of the input frames is not required to match exactly a size supported by the codec.</span></span> <span data-ttu-id="d84b0-136">Si no coinciden, los componentes en tiempo de ejecución del SDK, en muchos casos, cambiarán automáticamente el tamaño de los fotogramas de vídeo de entrada a algo que pueda aceptar el códec.</span><span class="sxs-lookup"><span data-stu-id="d84b0-136">If they do not match, the SDK run-time components, in many cases, will automatically resize the input video frames to something the codec can accept.</span></span>

<span data-ttu-id="d84b0-137">En el código de ejemplo siguiente se busca el formato de entrada del subtipo que se pasa como parámetro.</span><span class="sxs-lookup"><span data-stu-id="d84b0-137">The following example code finds the input format of the subtype passed as a parameter.</span></span> <span data-ttu-id="d84b0-138">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="d84b0-138">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d84b0-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d84b0-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d84b0-140">**Interfaz IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="d84b0-140">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="d84b0-141">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="d84b0-141">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




