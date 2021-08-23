---
description: El filtro Microsoft MPEG-2 Audio Encoder codifica las capas de audio MPEG-1 I y II, incluida la compatibilidad con las extensiones de frecuencia de muestreo baja (LSF) MPEG-2.
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Microsoft MPEG-2 Audio Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030821905862a9698ee24c3227f2846cd8c892e20c501d2776cdf2f9bb88f3e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584125"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Microsoft MPEG-2 Audio Encoder

El filtro Microsoft MPEG-2 Audio Encoder codifica las capas de audio MPEG-1 I y II, incluida la compatibilidad con las extensiones de frecuencia de muestreo baja (LSF) MPEG-2.

Para codificar y multiplexar secuencias de audio y vídeo, use el filtro Codificador [**MPEG-2**](microsoft-mpeg-2-encoder.md) de Microsoft, que encapsula las funciones de este filtro y del filtro De codificador de vídeo [**MPEG-2**](microsoft-mpeg-2-video-encoder.md) de Microsoft.

> [!Note]  
> Este filtro no se admite en plataformas basadas en IA-64.

 



Filtrar información

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de medios de pin de entrada

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**

Interfaces de pin de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de pin de salida

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/>

Interfaces de pin de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtrar CLSID

**CLSID \_ CMPEG2EncoderAudioDS** (declarado en wmcodecdsp.h)

Executable

msmpeg2enc.dll

[Mérito](merit.md)

**NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Comentarios

El codificador de audio MPEG-2 puede generar los siguientes tipos de salida:

-   Secuencia elemental de audio
-   Audio en una secuencia de programa MPEG-2
-   Audio en una secuencia de transporte MPEG-2

Admite extensiones de frecuencia de muestreo baja (LSF) de las capas MPEG-1 I y II y MPEG-2.

Las muestras de entrada deben tener 16 bits por muestra, con una velocidad de muestreo de audio de 48, 44,1, 32, 22,05 o 16 KHz. El codificador no puede volver a muestrear la secuencia de audio; El audio codificado tiene la misma frecuencia de muestreo que la entrada.

Los ejemplos de entrada deben ser mono o estéreo. El audio codificado tiene el número de canales como entrada.

### <a name="limitations"></a>Limitaciones

El codificador no admite lo siguiente:

-   Secuencias de bits de audio MPEG layer III.
-   Secuencias de bits de extensión multicanal MPEG-2.
-   Secuencias de bits de AAC MPEG-4.
-   Secuencias de bits MPEG-2 no compatibles con versiones anteriores (MPEG-2).
-   Generación de paquetes de flujo básico en paquetes (PES).
-   Codificación Dolby Digital.

### <a name="codec-properties"></a>Propiedades del códec

El filtro admite las siguientes propiedades a través [**de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

-   [**AVAudioChannelCount**](avaudiochannelcount-property.md)
-   [**AVAudioSampleRate**](avaudiosamplerate-property.md)
-   [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)
-   [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
-   [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
-   [**AVEncMPACodingMode**](avencmpacodingmode-property.md)
-   [**AVEncMPACopyright**](avencmpacopyright-property.md)
-   [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)
-   [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md)
-   [**AVEncMPALayer**](avencmpalayer-property.md)
-   [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)
-   [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)

> [!Note]  
> Una versión anterior de la documentación enumeraba incorrectamente algunas propiedades adicionales que no se admiten.

 

Por compatibilidad con versiones anteriores, el filtro admite la siguiente propiedad a través de la **interfaz IEncoderAPI:**



| Propiedad                 | Descripción                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **VELOCIDAD DE BITS DE ENCAPIPARAM \_** | Equivalente a [**AVEncCommonMeanBitRate.**](avenccommonmeanbitrate-property.md) |



 

Se recomienda establecer las propiedades en el orden siguiente:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

Establezca las propiedades restantes en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de demultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
