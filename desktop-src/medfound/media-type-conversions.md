---
description: Conversiones de tipos de medios
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversiones de tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5d91844a062d5d4a1aa98af1a2e77c9cabfadb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474351"
---
# <a name="media-type-conversions"></a>Conversiones de tipos de medios

En ocasiones, es necesario convertir entre los tipos Media Foundation multimedia y las estructuras de tipo de medio anteriores de DirectShow o el SDK Windows Media Format.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>De una estructura de formato a un tipo Media Foundation formato

Las siguientes funciones inicializan un tipo Media Foundation medio a partir de una estructura de formato. Estas funciones también son útiles si un flujo de datos o un encabezado de archivo contiene una estructura de formato. Por ejemplo, el encabezado de archivo para los archivos de audio WAVE contiene una [**estructura DESATEX.**](/previous-versions/dd757713(v=vs.85))




| Estructura que se convertirá | Función | 
|----------------------|----------|
| <a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br /><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (objetos multimedia de DirectX) <br /><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (WINDOWS SDK de formato multimedia) <br /><blockquote>[!Note]<br />Estas estructuras son equivalentes.</blockquote><br /><br /> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a> | 
| <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a> | 
| <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a> | 
| <a href="/previous-versions/dd757713(v=vs.85)"><strong>DESENLACE</strong></a> O <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>DESATEXTENSIBLE</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a> | 




 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>De un tipo Media Foundation a una estructura de formato

Las siguientes funciones crean o inicializan una estructura de formato a partir de Media Foundation tipo de medio.



| Función                                                                             | Estructura de destino                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**AM \_ TIPO \_ DE MEDIO,**](/windows/win32/api/strmif/ns-strmif-am_media_type) [**MFVIDEOFORMAT,**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**DESENLACE**](/previous-versions/dd757713(v=vs.85)) O [ **DESATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Asignaciones de formato

En las tablas siguientes se muestran los Media Foundation que corresponden a varias estructuras de formato. No todos estos atributos se pueden traducir directamente. Para realizar conversiones, debe usar las funciones enumeradas en la sección anterior; Estas tablas se proporcionan principalmente como referencia.

### <a name="am_media_type"></a>AM \_ MEDIA \_ TYPE



| Member                   | Atributo                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bComposiciónCompression** | [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**EJEMPLOS \_ DE TAMAÑO FIJO DE MT \_ \_ DE \_ MF**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**TAMAÑO DE \_ MUESTRA DE MT \_ DE MF \_**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>FORMA DE ONDAATEX, FORMA DE ONDAATEXTENSIBLE



| Member                  | Atributo                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)<br/> Si **wFormatTag** es WAVE \_ FORMAT \_ EXTENSIBLE, el subtipo se encuentra en el **miembro SubFormat.**<br/> |
| **nChannels**           | [**CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**PROMEDIO DE BYTES PROMEDIO DE AUDIO DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ MUESTRA**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**\_BITS VÁLIDOS DE AUDIO MF MT \_ \_ POR \_ \_ \_ MUESTRA**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ BLOQUE**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **Subformato**           | [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Datos adicionales              | [**DATOS \_ DE USUARIO DE MF MT \_ \_**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| Member                                         | Atributo                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**TASA \_ DE ERRORES DE BITS PROMEDIO \_ DE MT \_ \_ \_ DE MF**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_ MT \_ FRAME \_ RATE**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate para**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) calcular este valor.                                                                             |
| **dwInterlaceFlags**                           | [**MODO \_ DE \_ INTERLACE MF \_ MT**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | No hay ningún equivalente definido                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**, **dwPictAspectRatioY** | [**MF \_ MT \_ PIXEL \_ ASPECT \_ RATIO**](mf-mt-pixel-aspect-ratio-attribute.md); debe convertir de relación de aspecto de imagen a relación de aspecto de imagen.                                                                                                      |
| **dwControlFlags**                             | [**MF \_ MARCAS \_ DE CONTROL DEL PANEL DE \_ \_ MT**](mf-mt-pad-control-flags-attribute.md). Si la **marca AMCONTROL \_ COLORINFO \_ PRESENT** está presente, establezca los atributos de color extendidos descritos en [Información de color extendida](extended-color-information.md). |
| **bmiHeader.biWidth**, **bmiHeader.biHeight**  | [**TAMAÑO \_ DEL MARCO DE MT \_ \_ DE MF**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | Implícito en el subtipo ([**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiHeader.biCompression**                    | Implícito en el subtipo.                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**TAMAÑO DE \_ MUESTRA DE MT \_ DE MF \_**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Información de la paleta                            | [**PALETA \_ DE MT DE \_ MF**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Los atributos siguientes se pueden inferir de la [**estructura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) pero también requieren cierto conocimiento de los detalles del formato. Por ejemplo, los distintos formatos YUV tienen requisitos de paso diferentes.

-   [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)
-   [**APERTURA \_ DE PANTALLA MÍNIMA DE MF MT \_ \_ \_**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Member                                   | Atributo                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**MF \_ MT \_ MPEG \_ START \_ TIME \_ CODE**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**ENCABEZADO \_ DE SECUENCIA MPEG DE MF MT \_ \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**, **biYPelsPerMeter** | [**RELACIÓN DE \_ ASPECTO \_ DE PÍXELES DE MT \_ DE \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Member               | Atributo                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**MF \_ MT \_ MPEG \_ START \_ TIME \_ CODE**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**ENCABEZADO \_ DE SECUENCIA MPEG DE MF MT \_ \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**MF \_ MT \_ MPEG2 \_ PROFILE**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**MF \_ MT \_ MPEG2 \_ LEVEL**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**MARCAS \_ \_ MPEG2 DE MF MT \_**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Ejemplos

El código siguiente rellena una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de un tipo de medio de vídeo. Tenga en cuenta que estas conversiones pierden parte de la información de formato (entrelazado, velocidad de fotogramas, datos de color extendidos). Sin embargo, puede ser útil al guardar un mapa de bits de un fotograma de vídeo, por ejemplo.


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 
