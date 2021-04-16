---
description: El filtro del codificador de audio MPEG-2 de Microsoft codifica las capas de audio I y II de MPEG-1, incluida la compatibilidad con las extensiones de la frecuencia de muestreo bajo (LSF) de MPEG-2.
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Codificador de audio MPEG-2 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677113"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Codificador de audio MPEG-2 de Microsoft

El filtro del codificador de audio MPEG-2 de Microsoft codifica las capas de audio I y II de MPEG-1, incluida la compatibilidad con las extensiones de la frecuencia de muestreo bajo (LSF) de MPEG-2.

Para codificar y multiplexar secuencias de audio/vídeo, use el filtro del [**codificador MPEG-2 de Microsoft**](microsoft-mpeg-2-encoder.md) , que encapsula las funciones de este filtro y el filtro del [**codificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-encoder.md) .

> [!Note]  
> Este filtro no se admite en las plataformas basadas en IA-64.

 



Información de filtro

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de medios de anclaje de entrada

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**

Interfaces de PIN de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de anclaje de salida

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**<br/> **MEDIATYPE \_ Streaming**, **MEDIASUBTYPE \_ MPEG2 \_ audio**<br/> **MEDIATYPE \_ Stream**, **\_ \_ programa MEDIASUBTYPE MPEG2**<br/> **MEDIATYPE \_ Stream**, **\_ \_ transporte MPEG2 MEDIASUBTYPE**<br/>

Interfaces de clavija de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Identificador CLSID

**CLSID \_ de CMPEG2EncoderAudioDS** (declarado en wmcodecdsp. h)

Executable

msmpeg2enc.dll

[Fundament](merit.md)

**MÉRITO \_ \_ no se \_ usa**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

El codificador de audio MPEG-2 puede producir los siguientes tipos de resultados:

-   Secuencia de audio elemental
-   Audio en una secuencia de programa MPEG-2
-   Audio en una secuencia de transporte MPEG-2

Admite extensiones MPEG-1 Layers I y II y MPEG-2 Low muestreo Frequency (LSF)

Los ejemplos de entrada deben tener 16 bits por muestra, con una velocidad de muestreo de audio de 48, 44,1, 32, 22,05 o 16 KHz. El codificador no puede volver a muestrear el flujo de audio; el audio codificado tiene la misma velocidad de muestra que la entrada.

Los ejemplos de entrada deben ser mono o estéreo. El audio codificado tiene el número de canales como entrada.

### <a name="limitations"></a>Limitaciones

El codificador no admite lo siguiente:

-   Bitstreams de audio MPEG Layer III.
-   Bitstreams de extensión de varios canales MPEG-2.
-   Bitstreams AAC MPEG-4.
-   Bitstreams compatible con MPEG-2 (NBC).
-   Generación de paquetes de flujo elemental (PES) de paquetes.
-   Codificación Dolby digital.

### <a name="codec-properties"></a>Propiedades de códec

El filtro admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

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

 

Por compatibilidad con versiones anteriores, el filtro admite la siguiente propiedad a través de la interfaz **IEncoderAPI** :



| Propiedad                 | Descripción                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **\_velocidad de bits ENCAPIPARAM** | Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md). |



 

Se recomienda establecer las propiedades en el orden siguiente:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

Establezca las propiedades restantes en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de demultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
