---
description: Configurar el formato de salida de vídeo
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configurar el formato de salida de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562260"
---
# <a name="configure-the-video-output-format"></a><span data-ttu-id="22e44-103">Configurar el formato de salida de vídeo</span><span class="sxs-lookup"><span data-stu-id="22e44-103">Configure the Video Output Format</span></span>

> [!Note]  
> <span data-ttu-id="22e44-104">La funcionalidad descrita en este tema está en desuso.</span><span class="sxs-lookup"><span data-stu-id="22e44-104">The functionality described in this topic is deprecated.</span></span> <span data-ttu-id="22e44-105">Para configurar el formato de salida de un dispositivo de captura, una aplicación debe usar la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) devuelta por [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) en el parámetro *PMT* .</span><span class="sxs-lookup"><span data-stu-id="22e44-105">To configure a capture device's output format, an application should use the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned by [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in the *pmt* parameter.</span></span>

 

<span data-ttu-id="22e44-106">Un dispositivo de captura puede admitir una variedad de formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="22e44-106">A capture device can support a range of output formats.</span></span> <span data-ttu-id="22e44-107">Por ejemplo, un dispositivo puede admitir RGB de 16 bits, RGB de 32 bits y YUYV.</span><span class="sxs-lookup"><span data-stu-id="22e44-107">For example, a device might support 16-bit RGB, 32-bit RGB, and YUYV.</span></span> <span data-ttu-id="22e44-108">Dentro de cada uno de estos formatos, el dispositivo puede admitir una variedad de tamaños de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="22e44-108">Within each of these formats, the device can support a range of frame sizes.</span></span>

<span data-ttu-id="22e44-109">En un dispositivo WDM, la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) se usa para informar de los formatos que admite el dispositivo y para establecer el formato.</span><span class="sxs-lookup"><span data-stu-id="22e44-109">In a WDM device, the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used to report which formats the device supports, and to set the format.</span></span> <span data-ttu-id="22e44-110">(En el caso de los dispositivos VFW heredados, use el cuadro de diálogo formato de vídeo VFW, como se describe en los [cuadros de diálogo Mostrar captura de VFW](display-vfw-capture-dialog-boxes.md)). La interfaz **IAMStreamConfig** se expone en el PIN de captura del filtro de captura, el PIN de vista previa o ambos.</span><span class="sxs-lookup"><span data-stu-id="22e44-110">(For legacy VFW devices, use the Video Format VFW dialog box, as described in [Display VFW Capture Dialog Boxes](display-vfw-capture-dialog-boxes.md).) The **IAMStreamConfig** interface is exposed on the capture filter's capture pin, preview pin, or both.</span></span> <span data-ttu-id="22e44-111">Use el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para obtener el puntero de interfaz:</span><span class="sxs-lookup"><span data-stu-id="22e44-111">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to get the interface pointer:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



<span data-ttu-id="22e44-112">El dispositivo tiene una lista de tipos de medios que admite.</span><span class="sxs-lookup"><span data-stu-id="22e44-112">The device has a list of media types that it supports.</span></span> <span data-ttu-id="22e44-113">Para cada tipo de medio, el dispositivo también proporciona un conjunto de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="22e44-113">For each media type, the device also provides a set of capabilities.</span></span> <span data-ttu-id="22e44-114">Incluyen el intervalo de tamaños de fotogramas que están disponibles para ese formato, el modo en que el dispositivo puede expandir o reducir la imagen y el intervalo de velocidades de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="22e44-114">These include the range of frame sizes that are available for that format, how well the device can stretch or shrink the image, and the range of frame rates.</span></span>

<span data-ttu-id="22e44-115">Para obtener el número de tipos de medios, llame al método [**IAMStreamConfig:: GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="22e44-115">To get the number of media types, call the [**IAMStreamConfig::GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) method.</span></span> <span data-ttu-id="22e44-116">El método devuelve dos valores:</span><span class="sxs-lookup"><span data-stu-id="22e44-116">The method returns two values:</span></span>

-   <span data-ttu-id="22e44-117">Número de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="22e44-117">The number of media types.</span></span>
-   <span data-ttu-id="22e44-118">Tamaño de la estructura que contiene la información de funciones.</span><span class="sxs-lookup"><span data-stu-id="22e44-118">The size of the structure that holds the capabilities information.</span></span>

<span data-ttu-id="22e44-119">El valor de tamaño es necesario porque la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) se usa para audio y vídeo (y se puede extender a otros tipos de medios).</span><span class="sxs-lookup"><span data-stu-id="22e44-119">The size value is necessary because the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used for both audio and video (and could be extended to other media types).</span></span> <span data-ttu-id="22e44-120">En el caso de los vídeos, las capacidades se describen mediante la estructura de vídeo de configuración de la secuencia, mientras que el audio usa la estructura de los Cap de configuración de la [**secuencia de audio \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) . [**\_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps)</span><span class="sxs-lookup"><span data-stu-id="22e44-120">For video, the capabilities are described using the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure, while audio uses the [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure.</span></span>

<span data-ttu-id="22e44-121">Para enumerar los tipos de medios, llame al método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) con un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="22e44-121">To enumerate the media types, call the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method with a zero-based index.</span></span> <span data-ttu-id="22e44-122">El método **GetStreamCaps** devuelve un tipo de medio y la estructura de funcionalidad correspondiente:</span><span class="sxs-lookup"><span data-stu-id="22e44-122">The **GetStreamCaps** method returns a media type and the corresponding capability structure:</span></span>


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



<span data-ttu-id="22e44-123">Observe cómo se asignan las estructuras para el método [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="22e44-123">Note how the structures are allocated for the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="22e44-124">El método asigna la estructura de tipo de medio, mientras que el llamador asigna la estructura de funciones.</span><span class="sxs-lookup"><span data-stu-id="22e44-124">The method allocates the media type structure, whereas the caller allocates the capabilities structure.</span></span> <span data-ttu-id="22e44-125">Convierte la estructura Capabilities en un puntero de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="22e44-125">Coerce the capabilities structure to a byte array pointer.</span></span> <span data-ttu-id="22e44-126">Cuando haya terminado con el tipo de medio, elimine la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , junto con el bloque de formato del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="22e44-126">After you are done with the media type, delete the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, along with the media type's format block.</span></span>

<span data-ttu-id="22e44-127">Puede configurar el dispositivo para que use un formato devuelto en el método [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="22e44-127">You can configure the device to use a format returned in the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="22e44-128">Simplemente llame a [**IAMStreamConfig:: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) con el tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="22e44-128">Simply call [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) with the media type:</span></span>


```C++
hr = pConfig->SetFormat(pmtConfig);
```



<span data-ttu-id="22e44-129">Si el PIN no está conectado, intentará usar este formato cuando se conecte.</span><span class="sxs-lookup"><span data-stu-id="22e44-129">If the pin is not connected, it will attempt to use this format when it does connect.</span></span> <span data-ttu-id="22e44-130">Si el PIN ya está conectado, intenta volver a conectarse con el nuevo formato.</span><span class="sxs-lookup"><span data-stu-id="22e44-130">If the pin is already connected, it attempts to reconnect using the new format.</span></span> <span data-ttu-id="22e44-131">En cualquier caso, es posible que el filtro de nivel inferior rechace el formato.</span><span class="sxs-lookup"><span data-stu-id="22e44-131">In either case, it is possible that the downstream filter will reject the format.</span></span>

<span data-ttu-id="22e44-132">También puede modificar el tipo de medio antes de pasarlo al método [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) .</span><span class="sxs-lookup"><span data-stu-id="22e44-132">You can also modify the media type before passing it to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method.</span></span> <span data-ttu-id="22e44-133">Aquí es donde entra en juego la estructura de los [**\_ límites de \_ configuración \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="22e44-133">This is where the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure comes in.</span></span> <span data-ttu-id="22e44-134">Describe todas las formas válidas de cambiar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="22e44-134">It describes all of the valid ways to change the media type.</span></span> <span data-ttu-id="22e44-135">Para usar esta información, debe comprender los detalles de ese tipo de medio en particular.</span><span class="sxs-lookup"><span data-stu-id="22e44-135">To use this information, you must understand the details of that particular media type.</span></span>

<span data-ttu-id="22e44-136">Por ejemplo, supongamos que [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) devuelve un formato RGB de 24 bits, con un tamaño de fotograma de 320 x 240 píxeles.</span><span class="sxs-lookup"><span data-stu-id="22e44-136">For example, suppose that [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns a 24-bit RGB format, with a frame size of 320 x 240 pixels.</span></span> <span data-ttu-id="22e44-137">Puede obtener esta información examinando el tipo principal, el subtipo y el bloque de formato del tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="22e44-137">You can get this information by examining the major type, subtype, and format block of the media type:</span></span>


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



<span data-ttu-id="22e44-138">La estructura de los [**\_ límites de \_ configuración \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) de la secuencia de vídeo proporciona el ancho y el alto mínimo y máximo que se pueden usar para este tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="22e44-138">The [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure gives the minimum and maximum width and height that can be used for this media type.</span></span> <span data-ttu-id="22e44-139">También proporciona el tamaño de "paso", que define los incrementos por los que puede ajustar el ancho o el alto.</span><span class="sxs-lookup"><span data-stu-id="22e44-139">It also gives you the "step" size, which defines the increments by which you can adjust the width or height.</span></span> <span data-ttu-id="22e44-140">Por ejemplo, el dispositivo puede devolver lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="22e44-140">For example, the device might return the following:</span></span>

-   <span data-ttu-id="22e44-141">MinOutputSize: 160 x 120</span><span class="sxs-lookup"><span data-stu-id="22e44-141">MinOutputSize: 160 x 120</span></span>
-   <span data-ttu-id="22e44-142">MaxOutputSize: 320 x 240</span><span class="sxs-lookup"><span data-stu-id="22e44-142">MaxOutputSize: 320 x 240</span></span>
-   <span data-ttu-id="22e44-143">OutputGranularityX: 8 píxeles (tamaño de paso horizontal)</span><span class="sxs-lookup"><span data-stu-id="22e44-143">OutputGranularityX: 8 pixels (horizontal step size)</span></span>
-   <span data-ttu-id="22e44-144">OutputGranularityY: 8 píxeles (tamaño de paso vertical)</span><span class="sxs-lookup"><span data-stu-id="22e44-144">OutputGranularityY: 8 pixels (vertical step size)</span></span>

<span data-ttu-id="22e44-145">Dados estos números, podría establecer el ancho en cualquier elemento del intervalo (160, 168, 176,... 304, 312, 320) y el alto en cualquier elemento del intervalo (120, 128, 136,... 104, 112, 120).</span><span class="sxs-lookup"><span data-stu-id="22e44-145">Given these numbers, you could set the width to anything in the range (160, 168, 176, ... 304, 312, 320) and the height to anything in the range (120, 128, 136, ... 104, 112, 120).</span></span> <span data-ttu-id="22e44-146">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="22e44-146">The following diagram illustrates this process.</span></span>

![tamaños de formato de vídeo](images/strmcap3.png)

<span data-ttu-id="22e44-148">Para establecer un nuevo tamaño de marco, modifique directamente la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) devuelta en [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span><span class="sxs-lookup"><span data-stu-id="22e44-148">To set a new frame size, directly modify the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span></span>


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



<span data-ttu-id="22e44-149">Después, pase el tipo de medio al método [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="22e44-149">Then pass the media type to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method, as described previously.</span></span>

<span data-ttu-id="22e44-150">Los miembros **MinFrameInterval** y **MaxFrameInterval** de [**los \_ \_ \_ Cap de configuración de secuencia de vídeo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) son la longitud mínima y máxima de cada fotograma de vídeo, que puede traducir en velocidades de fotogramas de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="22e44-150">The **MinFrameInterval** and **MaxFrameInterval** members of [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) are the minimum and maximum length of each video frame, which you can translate into frame rates as follows:</span></span>

`frames per second = 10,000,000 / frame duration`

<span data-ttu-id="22e44-151">Para solicitar una velocidad de fotogramas determinada, modifique el valor de **AvgTimePerFrame** en la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="22e44-151">To request a particular frame rate, modify the value of **AvgTimePerFrame** in the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure in the media type.</span></span> <span data-ttu-id="22e44-152">Es posible que el dispositivo no admita todos los valores posibles entre el mínimo y el máximo, por lo que el controlador usará el valor más cercano que pueda.</span><span class="sxs-lookup"><span data-stu-id="22e44-152">The device may not support every possible value between the minimum and maximum, so the driver will use the closest value that it can.</span></span> <span data-ttu-id="22e44-153">Para ver el valor que el controlador utilizó realmente, llame a [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) después de llamar a [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span><span class="sxs-lookup"><span data-stu-id="22e44-153">To see what value the driver actually used, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) after you call [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span></span>

<span data-ttu-id="22e44-154">Algunos controladores pueden notificar **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) para el valor de **MaxFrameInterval**, que en efecto significa que no hay una duración máxima.</span><span class="sxs-lookup"><span data-stu-id="22e44-154">Some drivers may report **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) for the value of **MaxFrameInterval**, which in effect means there is no maximum duration.</span></span> <span data-ttu-id="22e44-155">Sin embargo, es posible que desee aplicar una velocidad de fotogramas mínima en la aplicación, como 1 fps.</span><span class="sxs-lookup"><span data-stu-id="22e44-155">However, you might want to enforce a minimum frame rate in your application, such as 1 fps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22e44-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22e44-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e44-157">Acerca de los tipos de medios</span><span class="sxs-lookup"><span data-stu-id="22e44-157">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="22e44-158">Configuración de un dispositivo de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="22e44-158">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



