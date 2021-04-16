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
# <a name="setting-the-group-media-type"></a>Establecer el tipo de medio de grupo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Todos los grupos deben definir un tipo de medio sin comprimir, ya sea audio o vídeo. El tipo de medio sin comprimir es el formato que los visores ven o oyen durante la reproducción. Normalmente, la salida final tendrá un formato comprimido. Para obtener más información, vea [representar un proyecto](rendering-a-project.md).

Para establecer el formato sin comprimir, cree una estructura de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) y rellénelo con el tipo principal, el subtipo y el encabezado de formato adecuados. Para vídeo, asigne una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para el bloque de formato y establezca el ancho, el alto y la profundidad de bits. En el caso de audio, asigne una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) para el bloque de formato y establezca la velocidad de muestra, la profundidad de bits y el número de canales. Si establece solo el tipo principal, DES proporciona valores predeterminados razonables para los demás valores. En la práctica, debe establecer los valores explícitamente para controlar el resultado.

Después de inicializar la estructura de tipo de medio, llame al método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) para establecer el tipo de medio para el grupo.

En el ejemplo siguiente se especifica el vídeo RGB de 16 bits, 320 píxeles de ancho por 240 píxeles de alto:


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



En el ejemplo siguiente se especifica un grupo de audio, estableciendo el tipo de medio de grupo en estéreo de 16 bits, 44100 muestras por segundo:


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



También puede usar la clase [**CMediaType**](cmediatype.md) en las [clases base de DirectShow](directshow-base-classes.md) para administrar los tipos de medios. Contiene algunos métodos auxiliares útiles y libera automáticamente el bloque de formato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los tipos de medios](about-media-types.md)
</dt> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 
