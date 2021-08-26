---
description: 'Este filtro descodifica los siguientes formatos de audio:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Descodificador de audio Microsoft MPEG-1/DD/AAC (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd20bfc2ad8a366b46ac0c0600d8cc7a8bca5abacae621e8ea7d02f5f1cb4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051255"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Descodificador de audio Microsoft MPEG-1/DD/AAC

Este filtro descodifica los siguientes formatos de audio:

-   Capas de audio MPEG-1 I y II.
-   Audio MPEG-2 compatible con versiones anteriores, capas I y II (ISO/IEC 13818-3), solo mono y estéreo.
-   Perfil de baja complejidad (LC) de codificación de audio avanzada (AAC).
-   High-Efficiency AAC (HE-AAC) versión 1 y versión 2.
-   Sistemas de cine digital de paso a través (DTS) para la salida digital.
-   SOLO LPCM, mono y estéreo, con o sin encabezados PES.
-   Dolby Digital.
-   Dolby Digital Plus, incluida la conversión de Dolby Digital Plus a Dolby Digital para la salida digital.

> [!Note]  
> La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby Digital para su uso por parte de las aplicaciones de Microsoft.

 

> [!Note]  
> Este filtro no se admite en plataformas basadas en IA-64.

 

La decodificación de los formatos Dolby Digital Plus, AAC y HE-AAC requiere Windows 7. Lacoding de Dolby Digital o Dolby Digital Plus no se admite en Windows 7 Home Basic ni Windows 7 Starter.

En el Registro, el nombre descriptivo de este filtro es "Descodificador de audio DTV-DVD de Microsoft".



Filtrar información

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipos de medios de pin de entrada

En Windows Vista y versiones posteriores, el filtro admite los siguientes tipos de entrada:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DOLBY \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Payload**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ DOLBY \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ DTS** (vea la nota 2).
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DOLBY \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (vea la nota 2).
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ DOLBY \_ AC3** (vea la nota 1).
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**

A partir Windows 7, el filtro también admite los siguientes tipos de entrada:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DOLBY \_ DDPLUS** (vea la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DTS2** (vea la nota 2).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVM** (vea la nota 1).
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ LOAS**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ RAW \_ AAC1**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ DOLBY \_ DDPLUS** (vea la nota 1).
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ LOAS**

El tipo de entrada puede cambiar dinámicamente durante el streaming.<br/> Para obtener más información sobre estos tipos de medios, vea [**Subtipos de audio**](audio-subtypes.md).<br/>

> [!Note]  
> 1. La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby Digital para su uso por parte de las aplicaciones de Microsoft.

<br/>

> [!Note]  
> 2. En el caso de la entrada de Digital Systems (DTS), solo se admite la salida S/PDIF (DTS a través de S/PDIF). No se admite lacoding de audio.

<br/>

Interfaces de pin de entrada

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de pin de salida

En Windows Vista y versiones posteriores, el filtro admite los siguientes tipos de salida:<br/>

-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DOLBY \_ AC3 \_ SPDIF** (igual que **KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DOLBY \_ DIGITAL)**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**

A partir Windows 7, el filtro también admite los siguientes tipos de salida:<br/>

-   **MEDIATYPE \_ Audio**, **SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTS**
-   **MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ IEEE \_ FLOAT**

Interfaces de pin de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtrar CLSID

**CLSID \_ CMPEG2AudDecoderDS** (declarado en wmcodecdsp.h)

Executable

msmpeg2adec.dll

[Mérito](merit.md)

**LUGAR DE LA CONS \_ NORMAL:** 1

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

> [!Note]  
> Una versión anterior de la documentación indicaba que este filtro puede descodificar "audio MPEG-2". El filtro descodifica solo audio MPEG-2 compatible con versiones anteriores.

 

## <a name="remarks"></a>Comentarios

Las secuencias mono siempre se descodifican en estéreo.

En el caso de las secuencias con una configuración de canal de dos o más altavoces, el descodificador realiza una de las siguientes acciones:

-   Combina hasta seis canales con la configuración común del hablante 5.1.
-   Se desmezcla a estéreo.

Para seleccionar entre estas dos opciones, use la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para establecer la propiedad [**AVDecCommonOutputFormat,**](avdeccommonoutputformat-property.md) antes de conectar los pines. Como alternativa, cuando la aplicación compila el gráfico de filtro, puede establecer el tipo de medio deseado en el pin de salida.

### <a name="aac-decoding"></a>AAC Decoding

Para AAC, el descodificador tiene ciertas restricciones de formato en la entrada AAC comprimida. Estas restricciones de formato son las mismas que Media Foundation descodificador [**de AAC**](../medfound/aac-decoder.md)y se documentan en la sección [**"Restricciones de formato".**](../medfound/aac-decoder.md)

El DirectShow descodificador también acepta tipos de entrada diferentes que el Media Foundation descodificador. El DirectShow descodificador admite los siguientes tipos de entrada de AAC:

-   **MEDIASUBTYPE \_ RAW \_ AAC1:** AAC sin formato, que normalmente se encuentra en AVI o Matroska (. ARCHIVOS DE ARCHIVO).
-   **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC:** AAC en una secuencia de transporte de datos de audio (ADTS) para streaming.
-   **MEDIASUBTYPE \_ MPEG \_ LOAS:** flujo de transporte con una capa de sincronización (LOAS) y una capa multiplex (LATM).

El descodificador Media Foundation admite los siguientes tipos de entrada de AAC:

-   MFAudioFormat \_ AAC (igual que **MEDIASUBTYPE \_ MPEG \_ HEAAC)** para la reproducción de archivos MP4.
-   **MEDIASUBTYPE \_ RAW \_ AAC1**.

### <a name="property-sets"></a>Conjuntos de propiedades

El pin de entrada del descodificador admite los siguientes conjuntos de propiedades a través [**de IKsPropertySet**](ikspropertyset.md):

-   [**Conjunto de propiedades de protección de copia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propiedades Rate-Change**](rate-change-property-set.md).

> [!Note]  
> A partir Windows 7, el descodificador admite el modo de truco a través del conjunto de propiedades rate-change. Admite velocidades de reproducción en el intervalo \[ de 0,501 a 2,0, donde 1,0 es la velocidad de reproducción normal y 2,0 es el doble de la velocidad \] normal.

 

### <a name="codec-properties"></a>Propiedades del códec

El pin de entrada del descodificador admite las siguientes propiedades a través [**de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                          | Requiere                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | Windows Solo Vista; no se admite en Windows 7 o posterior. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

El filtro admite las siguientes propiedades a través [**de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propiedad                                                                          | Requiere      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (vea la nota 3). | Windows Vista |
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. La [**propiedad AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) debe establecerse antes de que se conecte el pin de salida del descodificador. De lo contrario, el cambio no tiene ningún efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[ aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Subtipos de audio**](audio-subtypes.md)
</dt> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de DVD**](dvd-media-types.md)
</dt> </dl>

 

 
