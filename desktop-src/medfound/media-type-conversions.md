---
description: Conversiones de tipos de medios
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversiones de tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820311"
---
# <a name="media-type-conversions"></a>Conversiones de tipos de medios

En ocasiones, es necesario convertir entre Media Foundation tipos de medios y las estructuras de tipos de medios anteriores de DirectShow o el SDK de Windows Media Format.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>De una estructura de formato a un tipo de Media Foundation

Las siguientes funciones inicializan un tipo de medio Media Foundation a partir de una estructura de formato. Estas funciones también son útiles si un flujo de datos o un encabezado de archivo contiene una estructura de formato. Por ejemplo, el encabezado de archivo de los archivos de audio de WAVE contiene una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Estructura que se va a convertir</th>
<th>Función</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br/> <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (objetos multimedia de DirectX) <br/> <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (SDK de Windows Media Format) <br/>
<blockquote>
[!Note]<br />
Estas estructuras son equivalentes.
</blockquote>
<br/> <br/></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> o <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>Desde un Media Foundation tipo a una estructura de formato

Las siguientes funciones crean o inicializan una estructura de formato a partir de un tipo de medio Media Foundation.



| Función                                                                             | Estructura de destino                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**AM \_ \_Tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**\_tipo de medio am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) o [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**\_tipo de medio am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Asignaciones de formato

En las tablas siguientes se enumeran los atributos de Media Foundation que corresponden a varias estructuras de formato. No todos estos atributos se pueden traducir directamente. Para realizar conversiones, debe utilizar las funciones enumeradas en la sección anterior; Estas tablas se proporcionan principalmente como referencia.

### <a name="am_media_type"></a>\_tipo de medio am \_



| Member                   | Atributo                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bTemporalCompression** | [**MF \_ MT \_ All \_ Samples \_ independiente**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**\_ejemplos de \_ \_ tamaño fijo MF MT \_**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**tamaño de muestra de MF \_ MT \_ \_**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WAVEFORMATEX, WAVEFORMATEXTENSIBLE



| Member                  | Atributo                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)<br/> Si **wFormatTag** es \_ \_ extensible, el subtipo se encuentra en el miembro del **subformato** .<br/> |
| **nChannels**           | [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**\_alineación del \_ bloque de audio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**\_ \_ bits válidos de audio MF MT \_ \_ \_ por \_ muestra**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**\_ejemplos de audio MF MT \_ \_ \_ por \_ bloque**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**\_máscara de \_ canal de audio MF MT \_ \_**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **SubFormat**           | [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Datos adicionales              | [**datos de usuario de MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| Member                                         | Atributo                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**\_velocidad de \_ bits media MF MT \_**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**\_tasa de \_ \_ errores de bit medio MF MT \_ \_**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_ \_ \_ Velocidad de fotogramas de MT**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) para calcular este valor.                                                                             |
| **dwInterlaceFlags**                           | [**\_ \_ modo entrelazado MF MT \_**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | No hay ningún equivalente definido                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**, **dwPictAspectRatioY** | [**MF \_ \_Proporción de \_ aspecto \_ de píxeles de MT**](mf-mt-pixel-aspect-ratio-attribute.md); debe convertirse de la relación de aspecto de imagen en la relación de aspecto de imagen.                                                                                                      |
| **dwControlFlags**                             | [**MF \_ \_marcas de \_ control \_ Pad de MT**](mf-mt-pad-control-flags-attribute.md). Si está presente la marca **AMCONTROL \_ COLORINFO \_ present** , establezca los atributos de color extendido descritos en [información de color ampliada](extended-color-information.md). |
| **bmiHeader. biwidth**, **BmiHeader. biheight**  | [**\_tamaño de \_ marco MF MT \_**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | Implícito en el subtipo ([**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiHeader. bicompression**                    | Implícito en el subtipo.                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**tamaño de muestra de MF \_ MT \_ \_**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Información de la paleta                            | [**\_paleta MF MT \_**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Los siguientes atributos se pueden inferir de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , pero también requieren cierto conocimiento de los detalles del formato. Por ejemplo, los distintos formatos YUV tienen diferentes requisitos de STRIDE.

-   [**\_ \_ intervalo predeterminado de MF MT \_**](mf-mt-default-stride-attribute.md)
-   [**\_ \_ apertura mínima de \_ pantalla MF MT \_**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_apertura de \_ \_ análisis panorámico MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Member                                   | Atributo                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**\_código de \_ \_ hora de inicio de MPEG MT \_ MF \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**\_encabezado de secuencia MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**, **biYPelsPerMeter** | [**\_relación de \_ aspecto de píxeles MF MT \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Member               | Atributo                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**\_código de \_ \_ hora de inicio de MPEG MT \_ MF \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**\_encabezado de secuencia MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**\_Perfil MF MT \_ MPEG2 \_**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**\_Nivel MF MT \_ MPEG2 \_**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**Marcas de MF \_ MT \_ MPEG2 \_**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Ejemplos

En el código siguiente se rellena una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) a partir de un tipo de medio de vídeo. Tenga en cuenta que esta conversión pierde parte de la información de formato (entrelazado, velocidad de fotogramas, datos de color extendido). Sin embargo, podría ser útil al guardar un mapa de bits de un fotograma de vídeo, por ejemplo.


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

 

 
