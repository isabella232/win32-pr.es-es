---
description: El filtro del codificador Microsoft MPEG-2 codifica audio y vídeo MPEG-2 y multiplexa las secuencias para generar una secuencia de programa MPEG-2 o una secuencia de transporte.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Codificador Microsoft MPEG-2 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072154"
---
# <a name="microsoft-mpeg-2-encoder"></a>Codificador Microsoft MPEG-2

El filtro del codificador Microsoft MPEG-2 codifica audio y vídeo MPEG-2 y multiplexa las secuencias para generar una secuencia de programa MPEG-2 o una secuencia de transporte.

> [!Note]  
> Este filtro no se admite en plataformas basadas en IA-64.

 



Filtrar información

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de medios de pin de entrada

Consulte Comentarios.

Interfaces de pin de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de pin de salida

Consulte Comentarios.

Interfaces de pin de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtrar CLSID

**CLSID \_ CMPEG2EncoderDS** (declarado en wmcodecdsp.h)

Executable

msmpeg2enc.dll

[Mérito](merit.md)

**NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

Este filtro combina la funcionalidad de codificación de otros dos filtros:

-   [**Microsoft MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md)
-   [**Codificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-encoder.md)

Excepto como se indicó, este filtro admite las mismas características de codificación que esos dos codificadores.

Inicialmente, el filtro tiene un pin de entrada, que puede aceptar entradas de audio o vídeo. Cuando ese pin está conectado, el filtro crea un segundo pin de entrada. Si el primer pin de entrada recibe audio, el segundo pin de entrada solo acepta vídeo y viceversa. Cada pin de entrada admite los mismos tipos de medios que el filtro de codificador correspondiente.

Si solo hay un pin de entrada conectado, el filtro admite los mismos tipos de salida que el codificador de audio o vídeo correspondiente. Si ambos pines están conectados, el filtro admite los siguientes tipos de salida:

-   Audio-visual en una secuencia de programa MPEG-2
-   Audio-visual en una secuencia de transporte MPEG-2

Se corresponden con los siguientes tipos de salida:

-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**

Este filtro no puede multiplexir secuencias que se codificaron previamente. Los flujos de entrada deben ser de audio o vídeo sin comprimir, que el filtro codifica antes de la multiplexación. La secuencia multiplexada se limita a un programa, que contiene hasta una secuencia de audio y una secuencia de vídeo.

### <a name="codec-properties"></a>Propiedades del códec

El filtro admite las propiedades combinadas de los filtros [**Mpeg-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) y [**MPEG-2 Video Encoder,**](microsoft-mpeg-2-video-encoder.md) con la siguiente diferencia:

-   La [**propiedad AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) establece la velocidad de bits media de la secuencia de vídeo.
-   La [**propiedad AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) establece la velocidad de bits media de la secuencia de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 
