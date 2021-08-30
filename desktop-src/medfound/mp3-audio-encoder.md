---
description: El Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Codificador de audio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757d070a2cef404780379c6652e6ced0af220dd4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471691"
---
# <a name="mp3-audio-encoder"></a>Codificador de audio MP3

El Microsoft Media Foundation de audio MP3 es un Media Foundation [Transform](media-foundation-transforms.md) (MFT) que codifica audio MPEG-1 capa 3 (MP3).

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador MP3 es **CLSID \_ MP3ACMCodecWrapper,** definido en el archivo de encabezado wmcodecdsp.h.

## <a name="media-types"></a>Tipos de medios

El codificador MP3 admite los siguientes tipos de medios. El tipo de salida debe establecerse antes que el tipo de entrada.

### <a name="output-types"></a>Tipos de salida

Establezca los atributos siguientes en el tipo de medio de salida.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. | Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de audio. | Debe ser <strong>MFAudioFormat_MP3</strong>. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Velocidad de bits de la secuencia MP3 codificada, en bytes por segundo. | El codificador admite todas las velocidades de bits definidas por el estándar (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 o 320 Kbps).<br /> Las velocidades de bits predeterminadas son de 128 Kbps para mono y 320 Kbps para estéreo.<br /> Use este atributo para especificar la velocidad de bits codificada.<br /> | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canales. | Se admiten los valores siguientes:<ul><li>1 (mono)</li><li>2 (estéreo)</li></ul> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Ejemplos por segundo. | Se admiten los valores siguientes:<ul><li>48000 (48 KHz)</li><li>44100 (44,1 KHz)</li><li>32000 (32 KHz)</li></ul> | 
| <a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a> | Datos de códec adicionales. | Este atributo contiene los 12 bytes de la <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>estructura MPEGLAYER3WAVEFORMAT</strong></a> que siguen al <strong>miembro wfx</strong> de esa estructura. | 




 

Como alternativa, puede rellenar una estructura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) y llamar a [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) para convertir la estructura en un tipo Media Foundation multimedia.

### <a name="input-types"></a>Tipos de entrada

Establezca los atributos siguientes en el tipo de medio de entrada.



| Atributo                                                                               | Descripción         | Observaciones                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [**TIPO \_ PRINCIPAL DE MF MT \_ \_**](mf-mt-major-type-attribute.md)                               | Tipo principal.         | Debe ser **MFMediaType \_ Audio**. |
| [**SUBTIPO \_ MT DE MF \_**](mf-mt-subtype-attribute.md)                                      | Subtipo.            | Debe ser **MFAudioFormat \_ PCM.** |
| [**BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ EJEMPLO**](mf-mt-audio-bits-per-sample-attribute.md)       | Bits por ejemplo.    | Debe ser 16.                     |
| [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md) | Ejemplos por segundo. | Debe coincidir con el tipo de salida.     |
| [**CANALES \_ NUM \_ DE AUDIO \_ MF MT \_**](mf-mt-audio-num-channels-attribute.md)              | Número de canales. | Debe coincidir con el tipo de salida.     |



 

El codificador solo admite la entrada PCM de entero de 16 bits. No admite la entrada de punto flotante de 32 bits.

### <a name="media-formats"></a>Formatos multimedia

El estándar MPEG-1 y MPEG-2 define 252 formatos de audio de nivel 3. El codificador MP3 admite el estándar con algunas excepciones, así como algunos formatos adicionales, como se describe a continuación. La capa 3 se define como:



| Requisito | Valor |
|----------------------------------|---------------------------------------------------------------|
| Canales                         | mono o estéreo                                                |
| Velocidades de muestreo MPEG-1 en kHz       | 44.1, 48, 32                                                  |
| Velocidades de bits codificadas mpeg-1 en kbps | 32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 |
| Velocidades de muestreo MPEG-2 en kHz       | 8, 11.025, 12, 16, 22.05, 24                                  |
| Velocidades de bits codificadas mpeg-2 en kbps | 8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160          |



 

El codificador MP3 también admite los siguientes formatos.



| Velocidad de muestreo | Velocidad de bits     | Número de canal |
|-------------|--------------|----------------|
| 8000        | 18000, 20000 | 2              |
| 11025       | 18000, 20000 | 1 o 2         |
| 12000       | 18000, 20000 | 1 o 2         |
| 16000       | 18000, 20000 | 1              |
| 32000       | 144000       | 1 o 2         |
| 44100       | 144000       | 1 o 2         |
| 48000       | 144000       | 1 o 2         |



 

El codificador MP3 no admite los siguientes formatos definidos por el estándar.



| Velocidad de muestreo | Velocidades de bits                                    | Número de canal |
|-------------|----------------------------------------------|----------------|
| 12000       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 o 2         |
| 11025       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 o 2         |
| 8000        | 80000, 96000, 112000, 128000, 144000, 160000 | 1 o 2         |
| 8000        | 8000, 11025, 12000, 16000, 22050, 24000      | 2              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
