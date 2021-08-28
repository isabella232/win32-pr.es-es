---
description: En este tema se describe cómo especificar el formato de una secuencia de codificación de audio avanzada (AAC) en Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipos de medios de AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70661478ad0d2267c951c80fc4a63d98c15267
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479891"
---
# <a name="aac-media-types"></a>Tipos de medios de AAC

En este tema se describe cómo especificar el formato de una secuencia de codificación de audio avanzada (AAC) en Media Foundation.

Se definen dos subtipos para el audio de AAC:



| Subtype                     | Descripción          | Encabezado       |
|-----------------------------|----------------------|--------------|
| **MFAudioFormat \_ AAC**      | AAC sin procesar o AAC de ADTS. | mfapi.h      |
| **MEDIASUBTYPE \_ RAW \_ AAC1** | AAC sin formato.             | wmcodecdsp.h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC
</dt> <dd>

Para este subtipo, el tipo de medio proporciona la frecuencia de muestreo y el número de canales antes de la aplicación de las herramientas de replicación de banda espectral (SBR) y estéreo paramétrico (PS), si están presentes. El efecto de la herramienta SBR es duplicar la frecuencia de muestreo descodificada en relación con la frecuencia de muestreo de AAC-LC principal. El efecto de la herramienta PS es descodificar estéreo de una secuencia AAC-LC de núcleo monocanal.

Este subtipo es equivalente a **MEDIASUBTYPE \_ MPEG \_ HEAAC,** definido en wmcodecdsp.h. Consulte [GUID de subtipo de audio.](audio-subtype-guids.md)

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ RAW \_ AAC1
</dt> <dd>

Este subtipo se usa para AAC incluido en un archivo AVI con la etiqueta de formato de audio igual a WAVE \_ FORMAT \_ RAW \_ AAC1 (0x00FF).

Para este subtipo, el tipo de medio proporciona la frecuencia de muestreo y el número de canales después de aplicar las herramientas SBR y PS, si están presentes.

</dd> </dl>

Los siguientes atributos de tipo multimedia se aplican al audio de AAC.




| Atributo | Descripción | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de audio. Consulte la descripción anterior para obtener más información. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Perfil y nivel de audio. <br /> El valor de este atributo es el <strong>campo audioProfileLevelIndication,</strong> tal como se define en ISO/IEC 14496-3.<br /> Si es desconocido, establezca en cero o 0xFE ("no se especificó ningún perfil de audio").<br /> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Velocidad de bits de la secuencia de AAC codificada, en bytes por segundo. | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Tipo de carga.<br /> Solo se aplica a <strong>MFAudioFormat_AAC</strong>.<br /><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE es</a> opcional. Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que la secuencia solo raw_data_block elementos.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Profundidad de bits del audio PCM descodificado. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Asignación de canales de audio a posiciones del hablante. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.<br /> La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Frecuencia de muestreo, en muestras por segundo.<br /> La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | El valor de este atributo depende del subtipo:<br /><ul><li><strong>MFAudioFormat_AAC:</strong>contiene la parte de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece después de la estructura <strong>DESACWAVEATEX</strong> (es decir, después del <strong>miembro wfx).</strong> Esto va seguido de los datos AudioSpecificConfig(), tal como se define en ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1:</strong>contiene los datos AudioSpecificConfig().</li></ul> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

