---
description: 'Este filtro descodifica los formatos de audio siguientes:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Descodificador de audio MPEG-1/DD/AAC de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686343"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Descodificador de audio MPEG-1/DD/AAC de Microsoft

Este filtro descodifica los formatos de audio siguientes:

-   Capas de audio I y II de MPEG-1.
-   Audio MPEG-2 compatible con versiones anteriores, las capas I y II (ISO/IEC 13818-3), mono y estéreo solamente.
-   Perfil de baja complejidad (LC) de codificación de audio avanzado (AAC).
-   High-Efficiency AAC (HE-AAC) versión 1 y versión 2.
-   Sistemas de cine digital de paso a través (DTS) para la salida digital.
-   LPCM, mono y estéreo únicamente, con o sin encabezados de PES.
-   Dolby digital.
-   Dolby Digital Plus, incluida la conversión de Dolby Digital Plus a Dolby digital para la salida digital.

> [!Note]  
> La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.

 

> [!Note]  
> Este filtro no se admite en las plataformas basadas en IA-64.

 

La descodificación de los formatos Dolby Digital Plus, AAC y HE-AAC requiere Windows 7. No se admite la descodificación de Dolby digital o Dolby Digital Plus en Windows 7 Home Basic o Windows 7 Starter.

En el registro, el nombre descriptivo de este filtro es "Microsoft DTV-DVD audio descodificador".



Información de filtro

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipos de medios de anclaje de entrada

En Windows Vista y versiones posteriores, el filtro admite los siguientes tipos de entrada:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Payload**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**
-   **MEDIATYPE \_ \_ \_ Paquete de DVD cifrado**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ \_ \_ Paquete de DVD cifrado**, **MEDIASUBTYPE \_ DTS** (véase la nota 2).
-   **MEDIATYPE \_ \_ \_ paquete de DVD cifrado**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MEDIATYPE \_ \_ \_ Paquete de DVD cifrado**, **MEDIASUBTYPE \_ MPEG2 \_ audio**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (véase la nota 2).
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **\_ \_ audio MEDIASUBTYPE MPEG2**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Streaming**, **MEDIASUBTYPE \_ MPEG2 \_ audio**

A partir de Windows 7, el filtro también admite los siguientes tipos de entrada:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vea la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DTS2** (véase la nota 2).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ de \_ \_ audio LPCM de DVD**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVM** (véase la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ loa**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ raw \_ AAC1**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vea la nota 1).
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ loa**

El tipo de entrada puede cambiar dinámicamente durante el streaming.<br/> Para obtener más información acerca de estos tipos de medios, consulte [**subtipos de audio**](audio-subtypes.md).<br/>

> [!Note]  
> 1. La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.

<br/>

> [!Note]  
> 2. Para la entrada de sistemas de cine digital (DTS), solo se admite la salida S/PDIF (DTS sobre S/PDIF). No se admite la descodificación de audio.

<br/>

Interfaces de PIN de entrada

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de anclaje de salida

En Windows Vista y versiones posteriores, el filtro admite los siguientes tipos de salida:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (igual que **KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital**)
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**

A partir de Windows 7, el filtro también admite los siguientes tipos de salida:<br/>

-   **MEDIATYPE \_ Audio**, **\_ subtipo de KSDATAFORMAT \_ IEC61937 \_ DTS**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ IEEE \_ float**

Interfaces de clavija de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Identificador CLSID

**CLSID \_ de CMPEG2AudDecoderDS** (declarado en wmcodecdsp. h)

Executable

msmpeg2adec.dll

[Fundament](merit.md)

**Mérito \_ NORMAL** -1

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

> [!Note]  
> Una versión anterior de la documentación indicó que este filtro puede descodificar "audio MPEG-2". El filtro descodifica solo audio MPEG-2 compatible con versiones anteriores.

 

## <a name="remarks"></a>Observaciones

Los flujos mono siempre se descodifican en estéreo.

En el caso de las secuencias con una configuración de canal de dos o más oradores, el descodificador realiza una de las acciones siguientes:

-   Se mezcla hasta seis canales mediante la configuración de altavoz común 5,1.
-   Downmixes a estéreo.

Para seleccionar entre estas dos opciones, use la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para establecer la propiedad [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) antes de conectar los pin. Como alternativa, cuando la aplicación genera el gráfico de filtro, puede establecer el tipo de medio deseado en el terminal de salida.

### <a name="aac-decoding"></a>Descodificación AAC

Para AAC, el descodificador tiene ciertas restricciones de formato en la entrada AAC comprimida. Estas restricciones de formato son las mismas que las del [**descodificador AAC**](../medfound/aac-decoder.md)Media Foundation y se documentan en la sección "[**restricciones de formato**](../medfound/aac-decoder.md)".

El descodificador de DirectShow también acepta distintos tipos de entrada que el descodificador de Media Foundation. El descodificador de DirectShow admite los siguientes tipos de entrada AAC:

-   **MEDIASUBTYPE \_ RAW \_ AAC1**: AAC sin formato, que normalmente se encuentra en AVI o Matroska (. MKV).
-   **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC en una secuencia de transporte de datos de audio (ADTS) para la transmisión por secuencias.
-   **MEDIASUBTYPE \_ MPEG \_ loa**: flujo de transporte con una capa de sincronización (Loa) y una capa de multiplexación (LATM).

El descodificador de Media Foundation admite los siguientes tipos de entrada AAC:

-   MFAudioFormat \_ AAC (igual que **MEDIASUBTYPE \_ MPEG \_ HEAAC**) para la reproducción de archivos MP4.
-   **MEDIASUBTYPE \_ \_AAC1 sin formato**.

### <a name="property-sets"></a>Conjuntos de propiedades

El PIN de entrada del descodificador admite los siguientes conjuntos de propiedades a través de [**IKsPropertySet**](ikspropertyset.md):

-   [**Conjunto de propiedades de protección de copia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propiedades Rate-Change**](rate-change-property-set.md).

> [!Note]  
> A partir de Windows 7, el descodificador admite el modo de truco a través del conjunto de propiedades Rate-Change. Admite velocidades de reproducción en el intervalo de \[ 0,501 \] a 2,0, donde 1,0 es la velocidad de reproducción normal y 2,0 es el doble de la tarifa normal.

 

### <a name="codec-properties"></a>Propiedades de códec

El PIN de entrada del descodificador admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                          | Requiere                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | Solo Windows Vista; no se admite en Windows 7 o posterior. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

El filtro admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                                          | Requiere      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (véase la nota 3). | Windows Vista |
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. La propiedad [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) debe establecerse antes de que se conecte el PIN de salida del descodificador. De lo contrario, el cambio no tiene ningún efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, solo para aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Subtipos de audio**](audio-subtypes.md)
</dt> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de DVD**](dvd-media-types.md)
</dt> </dl>

 

 
