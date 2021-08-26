---
description: Establecer el tipo de medio de grupo
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Establecer el tipo de medio de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c758e089a4f1240debb14c8159d039380b3473991860fef54470c12c1c00b1e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928185"
---
# <a name="setting-the-group-media-type"></a>Establecer el tipo de medio de grupo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Todos los grupos deben definir un tipo de medio sin comprimir, ya sea audio o vídeo. El tipo de medio sin comprimir es el formato que ven o escuchan los espectadores durante la reproducción. Normalmente, la salida final estará en un formato comprimido. Para obtener más información, vea [Representación de un Project](rendering-a-project.md).

Para establecer el formato sin comprimir, cree una estructura [**\_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) y rellene con el tipo principal, el subtipo y el encabezado de formato adecuados. Para vídeo, asigne una [**estructura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para el bloque de formato y establezca el ancho, el alto y la profundidad de bits. Para el audio, asigne una estructura [**DESATEX para**](/previous-versions/dd757713(v=vs.85)) el bloque de formato y establezca la frecuencia de muestreo, la profundidad de bits y el número de canales. Si establece solo el tipo principal, DES proporciona valores predeterminados razonables para los demás valores. En la práctica, debe establecer los valores explícitamente para controlar la salida.

Después de inicializar la estructura del tipo de medio, llame al método [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) para establecer el tipo de medio para el grupo.

En el ejemplo siguiente se especifica un vídeo RGB de 16 bits, de 320 píxeles de ancho por 240 píxeles de alto:


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



En el ejemplo siguiente se especifica un grupo de audio estableciendo el tipo de medio de grupo en estéreo de 16 bits, 44100 muestras por segundo:


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



También puede usar la clase [**CMediaType**](cmediatype.md) en el DirectShow [base para](directshow-base-classes.md) administrar tipos de medios. Contiene algunos métodos auxiliares útiles y libera automáticamente el bloque de formato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los tipos de medios](about-media-types.md)
</dt> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 
