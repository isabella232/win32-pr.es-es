---
description: Establecer el tipo de medio de grupo
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Establecer el tipo de medio de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678635"
---
# <a name="setting-the-group-media-type"></a><span data-ttu-id="9a2f8-103">Establecer el tipo de medio de grupo</span><span class="sxs-lookup"><span data-stu-id="9a2f8-103">Setting the Group Media Type</span></span>

<span data-ttu-id="9a2f8-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9a2f8-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9a2f8-105">Todos los grupos deben definir un tipo de medio sin comprimir, ya sea audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-105">All groups must define an uncompressed media type, either audio or video.</span></span> <span data-ttu-id="9a2f8-106">El tipo de medio sin comprimir es el formato que los visores ven o oyen durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-106">The uncompressed media type is the format that viewers see or hear during playback.</span></span> <span data-ttu-id="9a2f8-107">Normalmente, la salida final tendrá un formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-107">Typically, the final output will be in a compressed format.</span></span> <span data-ttu-id="9a2f8-108">Para obtener más información, vea [representar un proyecto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="9a2f8-108">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="9a2f8-109">Para establecer el formato sin comprimir, cree una estructura de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) y rellénelo con el tipo principal, el subtipo y el encabezado de formato adecuados.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-109">To set the uncompressed format, create an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and fill it with the appropriate major type, subtype, and format header.</span></span> <span data-ttu-id="9a2f8-110">Para vídeo, asigne una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para el bloque de formato y establezca el ancho, el alto y la profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-110">For video, allocate a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure for the format block, and set the width, height, and bit depth.</span></span> <span data-ttu-id="9a2f8-111">En el caso de audio, asigne una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) para el bloque de formato y establezca la velocidad de muestra, la profundidad de bits y el número de canales.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-111">For audio, allocate a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure for the format block, and set the sample rate, bit depth, and number of channels.</span></span> <span data-ttu-id="9a2f8-112">Si establece solo el tipo principal, DES proporciona valores predeterminados razonables para los demás valores.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-112">If you set just the major type, DES provides reasonable defaults for the other values.</span></span> <span data-ttu-id="9a2f8-113">En la práctica, debe establecer los valores explícitamente para controlar el resultado.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-113">In practice, you should set the values explicitly to control the output.</span></span>

<span data-ttu-id="9a2f8-114">Después de inicializar la estructura de tipo de medio, llame al método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) para establecer el tipo de medio para el grupo.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-114">After you initialize the media type structure, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method to set the media type for the group.</span></span>

<span data-ttu-id="9a2f8-115">En el ejemplo siguiente se especifica el vídeo RGB de 16 bits, 320 píxeles de ancho por 240 píxeles de alto:</span><span class="sxs-lookup"><span data-stu-id="9a2f8-115">The following example specifies 16-bit RGB video, 320 pixels wide by 240 pixels high:</span></span>


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



<span data-ttu-id="9a2f8-116">En el ejemplo siguiente se especifica un grupo de audio, estableciendo el tipo de medio de grupo en estéreo de 16 bits, 44100 muestras por segundo:</span><span class="sxs-lookup"><span data-stu-id="9a2f8-116">The next example specifies an audio group, by setting the group media type to 16-bit stereo, 44100 samples per second:</span></span>


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



<span data-ttu-id="9a2f8-117">También puede usar la clase [**CMediaType**](cmediatype.md) en las [clases base de DirectShow](directshow-base-classes.md) para administrar los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-117">You can also use the [**CMediaType**](cmediatype.md) class in the [DirectShow Base Classes](directshow-base-classes.md) to manage media types.</span></span> <span data-ttu-id="9a2f8-118">Contiene algunos métodos auxiliares útiles y libera automáticamente el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="9a2f8-118">It contains some useful helper methods, and automatically releases the format block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a2f8-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a2f8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a2f8-120">Acerca de los tipos de medios</span><span class="sxs-lookup"><span data-stu-id="9a2f8-120">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="9a2f8-121">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="9a2f8-121">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
