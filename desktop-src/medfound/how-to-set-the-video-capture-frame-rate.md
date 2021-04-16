---
description: Un dispositivo de captura de vídeo puede admitir una variedad de velocidades de fotogramas.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Cómo establecer la velocidad de fotogramas de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705843"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a><span data-ttu-id="34a98-103">Cómo establecer la velocidad de fotogramas de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="34a98-103">How to Set the Video Capture Frame Rate</span></span>

<span data-ttu-id="34a98-104">Un dispositivo de captura de vídeo puede admitir una variedad de velocidades de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="34a98-104">A video capture device might support a range of frame rates.</span></span> <span data-ttu-id="34a98-105">Si esta información está disponible, las velocidades de fotogramas mínimo y máximo se almacenan como atributos de tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="34a98-105">If this information is available, the minimum and maximum frame rates are stored as media type attributes:</span></span>



| <span data-ttu-id="34a98-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="34a98-106">Attribute</span></span>                                                         | <span data-ttu-id="34a98-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="34a98-107">Description</span></span>         |
|-------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="34a98-108">\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ máx.</span><span class="sxs-lookup"><span data-stu-id="34a98-108">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md) | <span data-ttu-id="34a98-109">Velocidad de fotogramas máxima.</span><span class="sxs-lookup"><span data-stu-id="34a98-109">Maximum frame rate.</span></span> |
| [<span data-ttu-id="34a98-110">\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ mín.</span><span class="sxs-lookup"><span data-stu-id="34a98-110">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md) | <span data-ttu-id="34a98-111">Velocidad de fotogramas mínima.</span><span class="sxs-lookup"><span data-stu-id="34a98-111">Minimum frame rate.</span></span> |



 

<span data-ttu-id="34a98-112">El intervalo puede variar en función del formato de captura.</span><span class="sxs-lookup"><span data-stu-id="34a98-112">The range can vary depending on the capture format.</span></span> <span data-ttu-id="34a98-113">Por ejemplo, en tamaños de fotogramas mayores, se podría reducir la velocidad máxima de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="34a98-113">For example, at larger frame sizes, the maximum frame rate might be reduced.</span></span>

<span data-ttu-id="34a98-114">Para establecer la velocidad de fotogramas:</span><span class="sxs-lookup"><span data-stu-id="34a98-114">To set the frame rate:</span></span>

1.  <span data-ttu-id="34a98-115">Cree el origen de medios para el dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="34a98-115">Create the media source for the capture device.</span></span> <span data-ttu-id="34a98-116">Consulte [enumeración de dispositivos de captura de vídeo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="34a98-116">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="34a98-117">Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen de medios para obtener el descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="34a98-117">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="34a98-118">Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obtener el descriptor de flujo para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="34a98-118">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="34a98-119">Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="34a98-119">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="34a98-120">Enumerar los formatos de captura, tal y como se describe en [cómo establecer el formato de captura de vídeo](how-to-set-the-video-capture-format.md).</span><span class="sxs-lookup"><span data-stu-id="34a98-120">Enumerate the capture formats, as described in [How to Set the Video Capture Format](how-to-set-the-video-capture-format.md).</span></span>
6.  <span data-ttu-id="34a98-121">Seleccione el formato de salida deseado en la lista.</span><span class="sxs-lookup"><span data-stu-id="34a98-121">Select the desired output format from the list.</span></span>
7.  <span data-ttu-id="34a98-122">Consulte el tipo de medio para los atributos de intervalo de velocidad de fotogramas [MF \_ MT \_ \_ \_ \_ Max](mf-mt-frame-rate-range-max.md) y [MF \_ MT \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="34a98-122">Query the media type for the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) and [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attributes.</span></span> <span data-ttu-id="34a98-123">Estos valores proporcionan el intervalo de velocidades de fotogramas admitidas.</span><span class="sxs-lookup"><span data-stu-id="34a98-123">This values give the range of supported frame rates.</span></span> <span data-ttu-id="34a98-124">Es posible que el dispositivo admita otras velocidades de fotogramas dentro de este intervalo.</span><span class="sxs-lookup"><span data-stu-id="34a98-124">The device might support other frame rates within this range.</span></span>
8.  <span data-ttu-id="34a98-125">Establezca el atributo [**MF \_ MT \_ Frame**](mf-mt-frame-rate-attribute.md) en el tipo de medio para especificar la velocidad de fotogramas deseada.</span><span class="sxs-lookup"><span data-stu-id="34a98-125">Set the [**MF\_MT\_FRAME**](mf-mt-frame-rate-attribute.md) attribute on the media type to specify the desired frame rate.</span></span>
9.  <span data-ttu-id="34a98-126">Llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) con el tipo de medio modificado.</span><span class="sxs-lookup"><span data-stu-id="34a98-126">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) with the modified media type.</span></span>

<span data-ttu-id="34a98-127">En el ejemplo siguiente se establece la velocidad de fotogramas igual a la velocidad de fotogramas máxima que admite el dispositivo:</span><span class="sxs-lookup"><span data-stu-id="34a98-127">The following example sets the frame rate equal to the maximum frame rate that the device supports:</span></span>


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="34a98-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34a98-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34a98-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="34a98-129">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



