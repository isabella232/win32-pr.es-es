---
description: Un dispositivo de captura de vídeo puede admitir varios formatos de captura. Los formatos normalmente se diferencian por el tipo de compresión, el espacio de colores (YUV o RGB), el tamaño de marco o la velocidad de fotogramas.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Cómo establecer el formato de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706213"
---
# <a name="how-to-set-the-video-capture-format"></a><span data-ttu-id="57042-104">Cómo establecer el formato de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="57042-104">How to Set the Video Capture Format</span></span>

<span data-ttu-id="57042-105">Un dispositivo de captura de vídeo puede admitir varios formatos de captura.</span><span class="sxs-lookup"><span data-stu-id="57042-105">A video capture device might support several capture formats.</span></span> <span data-ttu-id="57042-106">Los formatos normalmente se diferencian por el tipo de compresión, el espacio de colores (YUV o RGB), el tamaño de marco o la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="57042-106">Formats typically differ by compression type, color space (YUV or RGB), frame size, or frame rate.</span></span>

<span data-ttu-id="57042-107">La lista de formatos admitidos se encuentra en el *descriptor de presentación*.</span><span class="sxs-lookup"><span data-stu-id="57042-107">The list of supported formats is contained in the *presentation descriptor*.</span></span> <span data-ttu-id="57042-108">Para obtener más información, vea [descriptores de presentación](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="57042-108">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="57042-109">Para enumerar los formatos admitidos:</span><span class="sxs-lookup"><span data-stu-id="57042-109">To enumerate the supported formats:</span></span>

1.  <span data-ttu-id="57042-110">Cree el origen de medios para el dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="57042-110">Create the media source for the capture device.</span></span> <span data-ttu-id="57042-111">Consulte [enumeración de dispositivos de captura de vídeo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="57042-111">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="57042-112">Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen de medios para obtener el descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="57042-112">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="57042-113">Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obtener el descriptor de flujo para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="57042-113">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="57042-114">Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="57042-114">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="57042-115">Llame a [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) para obtener el número de formatos admitidos.</span><span class="sxs-lookup"><span data-stu-id="57042-115">Call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) to get the number of supported formats.</span></span>
6.  <span data-ttu-id="57042-116">En un bucle, llame a [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obtener cada formato.</span><span class="sxs-lookup"><span data-stu-id="57042-116">In a loop, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get each format.</span></span> <span data-ttu-id="57042-117">El formato se representa mediante un *tipo de medio*.</span><span class="sxs-lookup"><span data-stu-id="57042-117">The format is represented by a *media type*.</span></span> <span data-ttu-id="57042-118">Para obtener más información, consulte [tipos de medios de vídeo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="57042-118">For more information, see [Video Media Types](video-media-types.md).</span></span>

<span data-ttu-id="57042-119">En el ejemplo siguiente se enumeran los formatos de captura para un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="57042-119">The following example enumerates the capture formats for a device:</span></span>


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="57042-120">La `LogMediaType` función que se usa en este ejemplo se muestra en el tema [código de depuración de tipo de medio](media-type-debugging-code.md).</span><span class="sxs-lookup"><span data-stu-id="57042-120">The `LogMediaType` function used in this example is listed in the topic [Media Type Debugging Code](media-type-debugging-code.md).</span></span>

<span data-ttu-id="57042-121">Para establecer el formato de captura:</span><span class="sxs-lookup"><span data-stu-id="57042-121">To set the capture format:</span></span>

1.  <span data-ttu-id="57042-122">Obtiene un puntero a la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , tal como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="57042-122">Get a pointer to the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface, as shown in the previous example.</span></span>
2.  <span data-ttu-id="57042-123">Llame a [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obtener el formato deseado, especificado por el índice.</span><span class="sxs-lookup"><span data-stu-id="57042-123">Call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get the desired format, specified by index.</span></span>
3.  <span data-ttu-id="57042-124">Llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para establecer el formato.</span><span class="sxs-lookup"><span data-stu-id="57042-124">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the format.</span></span>

<span data-ttu-id="57042-125">Si no establece el formato de captura, el dispositivo usará su formato predeterminado.</span><span class="sxs-lookup"><span data-stu-id="57042-125">If you do not set the capture format, the device will use its default format.</span></span>

<span data-ttu-id="57042-126">En el ejemplo siguiente se establece el formato de captura:</span><span class="sxs-lookup"><span data-stu-id="57042-126">The following example sets the capture format:</span></span>


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="57042-127">El orden en el que se devuelven los formatos depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57042-127">The order in which formats are returned depends on the device.</span></span> <span data-ttu-id="57042-128">Normalmente, se agrupan primero por tipo de compresión o espacio de colores; y, después, desde el tamaño de fotograma más pequeño hasta el tamaño de fotograma más grande dentro de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="57042-128">Typically, they are grouped first by compression type or color space; and then from smallest frame size to largest frame size within each group.</span></span>

<span data-ttu-id="57042-129">La velocidad de fotogramas se controla de forma ligeramente diferente a los demás atributos de formato.</span><span class="sxs-lookup"><span data-stu-id="57042-129">The frame rate is handled slightly differently than the other format attributes.</span></span> <span data-ttu-id="57042-130">Para obtener más información, vea [cómo establecer la velocidad de fotogramas de captura de vídeo](how-to-set-the-video-capture-frame-rate.md).</span><span class="sxs-lookup"><span data-stu-id="57042-130">For more information, see [How to Set the Video Capture Frame Rate](how-to-set-the-video-capture-frame-rate.md).</span></span>

> [!Note]  
> <span data-ttu-id="57042-131">En algunos dispositivos, la lista de formatos contendrá una entrada duplicada para cada formato.</span><span class="sxs-lookup"><span data-stu-id="57042-131">In some devices, the format list will contain a duplicate entry for each format.</span></span> <span data-ttu-id="57042-132">Por ejemplo, si el dispositivo admite 15 formatos de captura distintos, la lista contendrá 30 entradas.</span><span class="sxs-lookup"><span data-stu-id="57042-132">For example, if the device supports 15 distinct capture formats, the list will contain 30 entries.</span></span> <span data-ttu-id="57042-133">Dentro de cada par, uno de los tipos de medios tendrá el [**atributo \_ MF \_ MT \_ AM format \_ Type**](mf-mt-am-format-type-attribute.md) igual a **format \_ info** y el otro tendrá el **\_ \_ \_ \_ tipo de formato MF MT AM** igual al **formato \_ VideoInfo2**.</span><span class="sxs-lookup"><span data-stu-id="57042-133">Within each pair, one of the media types will have the attribute [**MF\_MT\_AM\_FORMAT\_TYPE**](mf-mt-am-format-type-attribute.md) equal to **FORMAT\_VideoInfo**, and the other will have **MF\_MT\_AM\_FORMAT\_TYPE** equal to **FORMAT\_VideoInfo2**.</span></span> <span data-ttu-id="57042-134">(Estos dos valores se definen en el archivo de encabezado UUID. h). El segundo tipo también puede contener información de color adicional ([información de color ampliada](extended-color-information.md)) o mostrar un valor diferente para el entrelazado ([**\_ \_ \_ modo de entrelazado MF MT**](mf-mt-interlace-mode-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="57042-134">(These two values are defined in the header file uuids.h.) The second type might also contain additional color information ([Extended Color Information](extended-color-information.md)) or show a different value for interlacing ([**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md)).</span></span> <span data-ttu-id="57042-135">Estos tipos duplicados existen para admitir aplicaciones de DirectShow anteriores.</span><span class="sxs-lookup"><span data-stu-id="57042-135">These duplicate types exist to support older DirectShow applications.</span></span> <span data-ttu-id="57042-136">En una aplicación Media Foundation, debe omitir el **formato \_ videoinfo** Type cada vez que se muestre un tipo de **formato \_ VideoInfo2** duplicado.</span><span class="sxs-lookup"><span data-stu-id="57042-136">In a Media Foundation application, you should ignore the **FORMAT\_VideoInfo** type whenever a duplicate **FORMAT\_VideoInfo2** type is listed.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="57042-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57042-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57042-138">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="57042-138">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



