---
description: Acerca de los tipos de medios
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Acerca de los tipos de medios (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361845"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="570cd-103">Acerca de los tipos de medios (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="570cd-103">About Media Types (DirectShow)</span></span>

<span data-ttu-id="570cd-104">Dado que DirectShow es modular, requiere una manera de describir el formato de los datos en cada punto del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="570cd-104">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="570cd-105">Por ejemplo, considere la posibilidad de reproducir AVI.</span><span class="sxs-lookup"><span data-stu-id="570cd-105">For example, consider AVI playback.</span></span> <span data-ttu-id="570cd-106">Los datos entran en el gráfico como un flujo de fragmentos RIFF.</span><span class="sxs-lookup"><span data-stu-id="570cd-106">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="570cd-107">Se analizan en secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="570cd-107">These are parsed into video and audio streams.</span></span> <span data-ttu-id="570cd-108">La secuencia de vídeo se compone de fotogramas de vídeo, que probablemente estén comprimidos.</span><span class="sxs-lookup"><span data-stu-id="570cd-108">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="570cd-109">Después de la descodificación, el flujo de vídeo es una serie de mapas de bits sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="570cd-109">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="570cd-110">La secuencia de audio pasa por un proceso similar.</span><span class="sxs-lookup"><span data-stu-id="570cd-110">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="570cd-111">Tipos de medios: Cómo representa DirectShow los formatos</span><span class="sxs-lookup"><span data-stu-id="570cd-111">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="570cd-112">El *tipo de medio* es una manera universal y extensible de describir formatos de medios digitales.</span><span class="sxs-lookup"><span data-stu-id="570cd-112">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="570cd-113">Cuando dos filtros se conectan, coinciden con un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="570cd-113">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="570cd-114">El tipo de medio identifica el tipo de datos que el filtro de nivel superior proporcionará al filtro de bajada y el diseño físico de los datos.</span><span class="sxs-lookup"><span data-stu-id="570cd-114">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="570cd-115">Si dos filtros no pueden estar de acuerdo en un tipo de medio, no se conectarán.</span><span class="sxs-lookup"><span data-stu-id="570cd-115">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="570cd-116">En el caso de algunas aplicaciones, nunca tendrá que preocuparse de los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="570cd-116">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="570cd-117">En la reproducción de archivos, por ejemplo, DirectShow controla todos los detalles.</span><span class="sxs-lookup"><span data-stu-id="570cd-117">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="570cd-118">Otros tipos de aplicaciones pueden necesitar trabajar directamente con los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="570cd-118">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="570cd-119">Los tipos de medios se definen mediante la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="570cd-119">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="570cd-120">Esta estructura contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="570cd-120">This structure contains the following information:</span></span>

-   <span data-ttu-id="570cd-121">**Tipo principal**: el tipo principal es un GUID que define la categoría general de los datos.</span><span class="sxs-lookup"><span data-stu-id="570cd-121">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="570cd-122">Entre los tipos principales se incluyen vídeo, audio, secuencia de bytes sin analizar, datos MIDI, etc.</span><span class="sxs-lookup"><span data-stu-id="570cd-122">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="570cd-123">**SubType**: el subtipo es otro GUID, que define el formato.</span><span class="sxs-lookup"><span data-stu-id="570cd-123">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="570cd-124">Por ejemplo, en el tipo de vídeo principal, hay subtipos para RGB-24, RGB-32, UYVY, etc.</span><span class="sxs-lookup"><span data-stu-id="570cd-124">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="570cd-125">Dentro de audio, hay audio PCM, carga MPEG-1 y otros.</span><span class="sxs-lookup"><span data-stu-id="570cd-125">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="570cd-126">El subtipo proporciona más información que el tipo principal, pero no define todo lo relacionado con el formato.</span><span class="sxs-lookup"><span data-stu-id="570cd-126">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="570cd-127">Por ejemplo, los subtipos de vídeo no definen el tamaño de la imagen ni la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="570cd-127">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="570cd-128">Se definen mediante el bloque de formato, que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="570cd-128">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="570cd-129">**Bloque de formato**: el bloque de formato es un bloque de datos que describe el formato en detalle.</span><span class="sxs-lookup"><span data-stu-id="570cd-129">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="570cd-130">El bloque de formato se asigna por separado de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="570cd-130">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="570cd-131">El miembro **pbFormat** de la estructura de **\_ \_ tipo de medio am** apunta al bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="570cd-131">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="570cd-132">El miembro **pbFormat** tiene tipo \**void \** _ porque el diseño del bloque Format cambia según el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="570cd-132">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="570cd-133">Por ejemplo, PCM audio usa una estructura [_ *WAVEFORMATEX* \*](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="570cd-133">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="570cd-134">El vídeo usa varias estructuras, como [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="570cd-134">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="570cd-135">El miembro **formatType** de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) es un GUID que especifica la estructura que se encuentra en el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="570cd-135">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="570cd-136">A cada estructura de formato se le asigna un GUID.</span><span class="sxs-lookup"><span data-stu-id="570cd-136">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="570cd-137">El miembro **cbFormat** especifica el tamaño del bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="570cd-137">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="570cd-138">Compruebe siempre estos valores antes de desreferenciar el puntero **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="570cd-138">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="570cd-139">Si el bloque de formato se rellena, el tipo y el subtipo principales contienen información redundante.</span><span class="sxs-lookup"><span data-stu-id="570cd-139">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="570cd-140">Sin embargo, el tipo y el subtipo principales proporcionan una manera cómoda de identificar formatos sin un bloque de formato completo.</span><span class="sxs-lookup"><span data-stu-id="570cd-140">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="570cd-141">Por ejemplo, puede especificar un formato RGB de 24 bits genérico (MEDIASUBTYPE \_ RGB24), sin conocer toda la información requerida por la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , como el tamaño de la imagen y la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="570cd-141">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="570cd-142">Por ejemplo, un filtro podría usar el código siguiente para comprobar un tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="570cd-142">For example, a filter might use the following code to check a media type:</span></span>


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



<span data-ttu-id="570cd-143">La estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) también contiene algunos campos opcionales.</span><span class="sxs-lookup"><span data-stu-id="570cd-143">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="570cd-144">Se pueden usar para proporcionar información adicional, pero no es necesario que los filtros los usen:</span><span class="sxs-lookup"><span data-stu-id="570cd-144">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="570cd-145">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="570cd-145">**lSampleSize**.</span></span> <span data-ttu-id="570cd-146">Si este campo es distinto de cero, define el tamaño de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="570cd-146">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="570cd-147">Si es cero, indica que el tamaño de la muestra puede cambiar de sample a sample.</span><span class="sxs-lookup"><span data-stu-id="570cd-147">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="570cd-148">**bFixedSizeSamples**.</span><span class="sxs-lookup"><span data-stu-id="570cd-148">**bFixedSizeSamples**.</span></span> <span data-ttu-id="570cd-149">Si esta marca booleana es **true**, significa que el valor de **lSampleSize** es válido.</span><span class="sxs-lookup"><span data-stu-id="570cd-149">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="570cd-150">De lo contrario, debe omitir **lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="570cd-150">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="570cd-151">**bTemporalCompression**.</span><span class="sxs-lookup"><span data-stu-id="570cd-151">**bTemporalCompression**.</span></span> <span data-ttu-id="570cd-152">Si esta marca booleana es **false**, significa que todos los marcos son fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="570cd-152">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="570cd-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="570cd-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="570cd-154">El gráfico de filtro y sus componentes</span><span class="sxs-lookup"><span data-stu-id="570cd-154">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
