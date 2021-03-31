---
description: El filtro del codificador MPEG-2 de Microsoft codifica el audio y el vídeo MPEG-2 y multiplexa los flujos para generar una secuencia de transporte o flujo de programa MPEG-2.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Codificador MPEG-2 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805624"
---
# <a name="microsoft-mpeg-2-encoder"></a>Codificador MPEG-2 de Microsoft

El filtro del codificador MPEG-2 de Microsoft codifica el audio y el vídeo MPEG-2 y multiplexa los flujos para generar una secuencia de transporte o flujo de programa MPEG-2.

> [!Note]  
> Este filtro no se admite en las plataformas basadas en IA-64.

 



Información de filtro

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de medios de anclaje de entrada

Ver comentarios

Interfaces de PIN de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de anclaje de salida

Ver comentarios

Interfaces de clavija de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Identificador CLSID

**CLSID \_ de CMPEG2EncoderDS** (declarado en wmcodecdsp. h)

Executable

msmpeg2enc.dll

[Fundament](merit.md)

**MÉRITO \_ \_ no se \_ usa**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

Este filtro combina la funcionalidad de codificación de otros dos filtros:

-   [**Codificador de audio MPEG-2 de Microsoft**](microsoft-mpeg-2-audio-encoder.md)
-   [**Codificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-encoder.md)

A menos que se indique lo contrario, este filtro admite las mismas características de codificación que los dos codificadores.

Inicialmente, el filtro tiene un PIN de entrada, que puede aceptar la entrada de audio o vídeo. Cuando el PIN está conectado, el filtro crea un segundo PIN de entrada. Si el primer PIN de entrada recibe audio, el segundo PIN de entrada solo acepta vídeo y viceversa. Cada pin de entrada admite los mismos tipos de medios que el filtro de codificador correspondiente.

Si solo hay un PIN de entrada conectado, el filtro admite los mismos tipos de salida que el codificador de audio o vídeo correspondiente. Si ambos PIN están conectados, el filtro admite los siguientes tipos de resultados:

-   Audio-visual en una secuencia de programa MPEG-2
-   Audio-visual en una secuencia de transporte MPEG-2

Estos se corresponden con los siguientes tipos de salida:

-   **MEDIATYPE \_ Stream**, **\_ \_ programa MEDIASUBTYPE MPEG2**
-   **MEDIATYPE \_ Stream**, **\_ \_ transporte MPEG2 MEDIASUBTYPE**

Este filtro no puede multiplexar flujos previamente codificados. Los flujos de entrada deben ser audio/vídeo sin comprimir, que el filtro codifica antes de multiplexar. La secuencia multiplexada está limitada a un programa que contiene hasta un audio y un flujo de vídeo.

### <a name="codec-properties"></a>Propiedades de códec

El filtro admite las propiedades combinadas del [**codificador de audio MPEG-2**](microsoft-mpeg-2-audio-encoder.md) y los filtros del [**codificador de vídeo MPEG-2**](microsoft-mpeg-2-video-encoder.md) , con la siguiente diferencia:

-   La propiedad [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) establece la velocidad de bits promedio para el flujo de vídeo.
-   La propiedad [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) establece la velocidad de bits promedio para la secuencia de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 
