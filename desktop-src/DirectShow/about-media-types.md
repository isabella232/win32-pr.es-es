---
description: Obtenga información sobre los tipos de medios en DirectShow. El tipo de medio es una manera universal y extensible de describir formatos multimedia digitales.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Acerca de los tipos de medios (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b1489543b33f5eeb2c288add48148b37f31915
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010898"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="32bd4-104">Acerca de los tipos de medios (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="32bd4-104">About Media Types (DirectShow)</span></span>

<span data-ttu-id="32bd4-105">Dado que DirectShow es modular, requiere una manera de describir el formato de los datos en cada punto del gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="32bd4-105">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="32bd4-106">Por ejemplo, considere la posibilidad de reproducir AVI.</span><span class="sxs-lookup"><span data-stu-id="32bd4-106">For example, consider AVI playback.</span></span> <span data-ttu-id="32bd4-107">Los datos entran en el gráfico como una secuencia de fragmentos de RIFF.</span><span class="sxs-lookup"><span data-stu-id="32bd4-107">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="32bd4-108">Se analizan en secuencias de vídeo y audio.</span><span class="sxs-lookup"><span data-stu-id="32bd4-108">These are parsed into video and audio streams.</span></span> <span data-ttu-id="32bd4-109">La secuencia de vídeo consta de fotogramas de vídeo, que probablemente estén comprimidos.</span><span class="sxs-lookup"><span data-stu-id="32bd4-109">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="32bd4-110">Después de la decodificación, la secuencia de vídeo es una serie de mapas de bits sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="32bd4-110">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="32bd4-111">La secuencia de audio pasa por un proceso similar.</span><span class="sxs-lookup"><span data-stu-id="32bd4-111">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="32bd4-112">Tipos de medios: cómo representa DirectShow los formatos</span><span class="sxs-lookup"><span data-stu-id="32bd4-112">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="32bd4-113">El *tipo de medio* es una manera universal y extensible de describir formatos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="32bd4-113">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="32bd4-114">Cuando se conectan dos filtros, se ponen de acuerdo en un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="32bd4-114">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="32bd4-115">El tipo de medio identifica el tipo de datos que el filtro ascendente entregará al filtro de nivel inferior y el diseño físico de los datos.</span><span class="sxs-lookup"><span data-stu-id="32bd4-115">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="32bd4-116">Si dos filtros no pueden coincidir en un tipo de medio, no se conectarán.</span><span class="sxs-lookup"><span data-stu-id="32bd4-116">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="32bd4-117">En algunas aplicaciones, nunca tendrá que preocuparse por los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="32bd4-117">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="32bd4-118">En la reproducción de archivos, por ejemplo, DirectShow controla todos los detalles.</span><span class="sxs-lookup"><span data-stu-id="32bd4-118">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="32bd4-119">Es posible que otros tipos de aplicaciones necesiten trabajar directamente con tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="32bd4-119">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="32bd4-120">Los tipos de medios se definen mediante la [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)</span><span class="sxs-lookup"><span data-stu-id="32bd4-120">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="32bd4-121">Esta estructura contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="32bd4-121">This structure contains the following information:</span></span>

-   <span data-ttu-id="32bd4-122">**Tipo principal:** el tipo principal es un GUID que define la categoría general de los datos.</span><span class="sxs-lookup"><span data-stu-id="32bd4-122">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="32bd4-123">Los tipos principales incluyen vídeo, audio, secuencia de bytes sin análisis, datos DE MIDI, etc.</span><span class="sxs-lookup"><span data-stu-id="32bd4-123">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="32bd4-124">**Subtipo:** el subtipo es otro GUID, que define aún más el formato.</span><span class="sxs-lookup"><span data-stu-id="32bd4-124">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="32bd4-125">Por ejemplo, dentro del tipo principal de vídeo, hay subtipos para RGB-24, RGB-32, UYVY, etc.</span><span class="sxs-lookup"><span data-stu-id="32bd4-125">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="32bd4-126">Dentro del audio, hay audio PCM, carga MPEG-1 y otros.</span><span class="sxs-lookup"><span data-stu-id="32bd4-126">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="32bd4-127">El subtipo proporciona más información que el tipo principal, pero no define todo sobre el formato.</span><span class="sxs-lookup"><span data-stu-id="32bd4-127">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="32bd4-128">Por ejemplo, los subtipos de vídeo no definen el tamaño de la imagen ni la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="32bd4-128">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="32bd4-129">Se definen mediante el bloque de formato, que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="32bd4-129">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="32bd4-130">**Bloque de formato:** el bloque de formato es un bloque de datos que describe el formato en detalle.</span><span class="sxs-lookup"><span data-stu-id="32bd4-130">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="32bd4-131">El bloque de formato se asigna por separado de la [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)</span><span class="sxs-lookup"><span data-stu-id="32bd4-131">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="32bd4-132">El **miembro pbFormat** de la **estructura AM MEDIA \_ \_ TYPE** apunta al bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="32bd4-132">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="32bd4-133">El **miembro pbFormat** tiene el tipo \**void \** _ porque el diseño del bloque de formato cambia en función del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="32bd4-133">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="32bd4-134">Por ejemplo, el audio PCM usa [una estructura _ *FORMADETEATEX.* \*](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32bd4-134">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="32bd4-135">El vídeo usa varias estructuras, como [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="32bd4-135">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="32bd4-136">El **miembro formattype** de la estructura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) es un GUID que especifica qué estructura está contenida en el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="32bd4-136">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="32bd4-137">A cada estructura de formato se le asigna un GUID.</span><span class="sxs-lookup"><span data-stu-id="32bd4-137">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="32bd4-138">El **miembro cbFormat** especifica el tamaño del bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="32bd4-138">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="32bd4-139">Compruebe siempre estos valores antes de desreferenciar el **puntero pbFormat.**</span><span class="sxs-lookup"><span data-stu-id="32bd4-139">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="32bd4-140">Si se rellena el bloque de formato, el tipo principal y el subtipo contienen información redundante.</span><span class="sxs-lookup"><span data-stu-id="32bd4-140">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="32bd4-141">Sin embargo, el tipo principal y el subtipo proporcionan una manera cómoda de identificar formatos sin un bloque de formato completo.</span><span class="sxs-lookup"><span data-stu-id="32bd4-141">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="32bd4-142">Por ejemplo, puede especificar un formato RGB genérico de 24 bits (MEDIASUBTYPE RGB24), sin conocer toda la información requerida por la estructura VIDEOINFOHEADER, como el tamaño de la imagen y la velocidad de \_ fotogramas. [](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)</span><span class="sxs-lookup"><span data-stu-id="32bd4-142">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="32bd4-143">Por ejemplo, un filtro podría usar el código siguiente para comprobar un tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="32bd4-143">For example, a filter might use the following code to check a media type:</span></span>


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



<span data-ttu-id="32bd4-144">La [**estructura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) también contiene algunos campos opcionales.</span><span class="sxs-lookup"><span data-stu-id="32bd4-144">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="32bd4-145">Se pueden usar para proporcionar información adicional, pero no se necesitan filtros para usarlos:</span><span class="sxs-lookup"><span data-stu-id="32bd4-145">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="32bd4-146">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="32bd4-146">**lSampleSize**.</span></span> <span data-ttu-id="32bd4-147">Si este campo es distinto de cero, define el tamaño de cada muestra.</span><span class="sxs-lookup"><span data-stu-id="32bd4-147">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="32bd4-148">Si es cero, indica que el tamaño de la muestra puede cambiar de muestra a muestra.</span><span class="sxs-lookup"><span data-stu-id="32bd4-148">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="32bd4-149">**bFixedSizeSamples**.</span><span class="sxs-lookup"><span data-stu-id="32bd4-149">**bFixedSizeSamples**.</span></span> <span data-ttu-id="32bd4-150">Si esta marca booleana **es TRUE,** significa que el valor de **lSampleSize** es válido.</span><span class="sxs-lookup"><span data-stu-id="32bd4-150">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="32bd4-151">De lo contrario, debe omitir **lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="32bd4-151">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="32bd4-152">**bComposiciónCompression**.</span><span class="sxs-lookup"><span data-stu-id="32bd4-152">**bTemporalCompression**.</span></span> <span data-ttu-id="32bd4-153">Si esta marca booleana **es FALSE,** significa que todos los fotogramas son fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="32bd4-153">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32bd4-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32bd4-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32bd4-155">El gráfico de filtros y sus componentes</span><span class="sxs-lookup"><span data-stu-id="32bd4-155">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
