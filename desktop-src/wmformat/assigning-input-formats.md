---
title: Asignar formatos de entrada
description: Asignar formatos de entrada
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- Advanced Systems Format (ASF), asignar formatos de entrada
- ASF (formato de sistemas avanzados), asignar formatos de entrada
- perfiles, asignar formatos de entrada
- códecs, asignar formatos de entrada
- Formato de sistemas avanzados (ASF), asignaciones de formato de entrada
- ASF (formato de sistemas avanzados), asignaciones de formato de entrada
- perfiles, asignaciones de formato de entrada
- códecs, asignaciones de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c6ad1bcdf161b335d9367d7de4df84b7eb2e6ea
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532956"
---
# <a name="assigning-input-formats"></a><span data-ttu-id="9bf41-111">Asignar formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="9bf41-111">Assigning Input Formats</span></span>

<span data-ttu-id="9bf41-112">Una vez identificado el formato de entrada que coincide con los datos, puede establecerlo para que lo use el escritor llamando a [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).</span><span class="sxs-lookup"><span data-stu-id="9bf41-112">When you have identified the input format that matches your data, you can set it for use by the writer by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).</span></span>

<span data-ttu-id="9bf41-113">En el caso de las secuencias de vídeo, debe establecer el tamaño de los fotogramas en los ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="9bf41-113">For video streams, you must set the size of the frames in the input samples.</span></span> <span data-ttu-id="9bf41-114">En el ejemplo de código siguiente se muestra cómo configurar y establecer una entrada de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9bf41-114">The following example code demonstrates how to configure and set a video input.</span></span> <span data-ttu-id="9bf41-115">Usa la función **FindInputFormat** definida en la sección [para enumerar los formatos de entrada](to-enumerate-input-formats.md) para obtener el formato de entrada para el vídeo RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="9bf41-115">It uses the **FindInputFormat** function defined in the [To Enumerate Input Formats](to-enumerate-input-formats.md) section to get the input format for 24-bit RGB video.</span></span> <span data-ttu-id="9bf41-116">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="9bf41-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT ConfigureVideoInput(IWMWriter* pWriter,
                            DWORD dwInput,
                            GUID guidSubType,
                            LONG lFrameWidth,
                            LONG lFrameHeight)
{
    DWORD   cbSize = 0;
    LONG    lStride = 0;

    IWMInputMediaProps* pProps  = NULL;
    WM_MEDIA_TYPE*      pType   = NULL;
    WMVIDEOINFOHEADER*  pVidHdr = NULL;
    BITMAPINFOHEADER*   pbmi    = NULL;

    // Get the base input format for the required subtype.
    HRESULT hr = FindInputFormat(pWriter, dwInput, guidSubType, &pProps);
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

    // Adjust the format to match your source images.

    // First set pointers to the video structures.
    pVidHdr = (WMVIDEOINFOHEADER*) pType->pbFormat;
    pbmi  = &(pVidHdr->bmiHeader);
        
    pbmi->biWidth  = lFrameWidth;  
    pbmi->biHeight = lFrameHeight;
    
    // Stride = (width * bytes/pixel), rounded to the next DWORD boundary.
    lStride = (lFrameWidth * (pbmi->biBitCount / 8) + 3) & ~3;


    // Image size = stride * height. 
    pbmi->biSizeImage = lFrameHeight * lStride;

    // Apply the adjusted type to the video input. 
    hr = pProps->SetMediaType(pType);
    if (FAILED(hr))
    {
        goto Exit;
    }

    hr = pWriter->SetInputProps(dwInput, pProps);

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="9bf41-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bf41-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf41-118">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="9bf41-118">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




