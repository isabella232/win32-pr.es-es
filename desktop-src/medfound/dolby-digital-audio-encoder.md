---
description: El codificador de audio Dolby es una transformación de Media Foundation (MFT) que codifica audio mono o estéreo en Dolby Digital, también denominado Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Dolby Digital Audio Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d14a434481a94021617f04e4cb9e10329ad20a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483101"
---
# <a name="dolby-digital-audio-encoder"></a>Dolby Digital Audio Encoder

El codificador de [](media-foundation-transforms.md) audio Dolby es una transformación de Media Foundation (MFT) que codifica audio mono o estéreo en Dolby Digital, también denominado Dolby AC-3. El codificador no admite la entrada multicanal, como la configuración del canal 5.1.

> [!IMPORTANT]
> Para las versiones de Windows anteriores a Windows 8, la implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby Digital para que las usen las aplicaciones de Microsoft.

 

Para obtener más información sobre el audio Dolby Digital, consulte el documento del Comité de sistemas de televisión avanzados (ATSC) *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador de audio Dolby es **\_ CLSID CMSDolbyDigitalEncMFT**, definido en el archivo de encabezado wmcodecdsp.h.

## <a name="output-types"></a>Tipos de salida

El tipo de salida debe establecerse primero, antes que el tipo de entrada. En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Necesario. Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de audio. | Necesario. Debe ser <strong>MFAudioFormat_Dolby_AC3</strong>. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Ejemplos por segundo. | Necesario. Se admiten los valores siguientes:<ul><li>32000</li><li>44100</li><li>48000</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canales. | Necesario. Debe ser 1 (mono) o 2 (estéreo). | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica la asignación de canales de audio a las posiciones del hablante. | Opcional. Si se establece, el valor debe ser 0x3 para estéreo (canales delante izquierdo y derecho) o 0x4 para mono (canal front-center). | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Velocidad de bits de la secuencia AC-3 codificada, en bytes por segundo. | Opcional. Vea Comentarios para obtener valores válidos. Si no se establece este atributo, el codificador usa una velocidad de bits predeterminada, como se describe en Comentarios. | 




 

Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.

## <a name="input-types"></a>Tipos de entrada

En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de entrada.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Necesario. Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de audio. | Necesario. Debe ser <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a> | Número de bits por muestra de audio. | Necesario. El valor debe ser 16 si el subtipo <strong>es MFAudioFormat_PCM</strong>o 32 si el subtipo <strong>es MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Ejemplos por segundo. | Necesario. Debe coincidir con el tipo de salida. | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canales. | Necesario. Debe coincidir con el tipo de salida. | 
| <a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> | Alineación de bloques, en bytes. | Necesario. Calcule el valor como se muestra a continuación:<ul><li><strong>MFAudioFormat_PCM:</strong>número de canales × 2.</li><li><strong>MFAudioFormat_Float:</strong>número de canales × 4.</li></ul> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Velocidad de bits de la secuencia AC3 codificada, en bytes por segundo. | Necesario. Debe igualar la alineación de bloques × muestras por segundo. | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica la asignación de canales de audio a las posiciones del hablante. | Opcional. Si se establece, el valor debe coincidir con el tipo de salida. | 
| <a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a> | Número de bits válidos de datos de audio en cada muestra de audio. | Opcional. Si se establece, el valor debe ser idéntico <a href="mf-mt-audio-bits-per-sample-attribute.md">al MF_MT_AUDIO_BITS_PER_SAMPLE</a>. | 




 

El codificador no admite la conversión de frecuencia de muestreo ni la conversión estéreo/mono.

## <a name="remarks"></a>Comentarios

Cada fotograma de audio Dolby AC-3 contiene 1536 muestras de audio por canal. Sin embargo, cada búfer de entrada al codificador puede contener cualquier número de muestras de PCM. El tamaño de cada búfer de entrada debe ser un múltiplo de la alineación del bloque. El codificador almacena en caché ejemplos de entrada hasta que tiene suficiente para 1536 muestras de audio por canal. momento en el que el codificador genera un fotograma AC-3.

Cada búfer de salida contiene un marco AC-3 sin procesar. La duración es equivalente a la duración de 1536 muestras de PCM a la velocidad de muestreo actual (32 mss) a una velocidad de muestreo de 48 kHz, 34,83 ms s a 44,1 kHz y 48 ms a 32 kHz). El tamaño de cada búfer de salida depende de la velocidad de bits y la frecuencia de muestreo.

Para especificar la velocidad de bits de codificación, establezca el atributo [MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de salida. En la tabla siguiente se muestra la relación entre la velocidad de bits de codificación y los BYTES PROMEDIO DE AUDIO MT DE MF \_ \_ POR \_ \_ \_ \_ SEGUNDO.



| Velocidad de bits (kbps) | [PROMEDIO DE BYTES PROMEDIO DE AUDIO DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | Comentarios                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Solo Mono.                                              |
| 80              | 10000                                                                                    | Solo Mono.                                              |
| 96              | 12000                                                                                    | Solo Mono.                                              |
| 112             | 14000                                                                                    | Solo Mono.                                              |
| 128             | 16000                                                                                    | Mono o estéreo.                                         |
| 160             | 20000                                                                                    | Mono o estéreo.                                         |
| 192             | 24000                                                                                    | Mono o estéreo. Esta es la configuración predeterminada para mono.   |
| 224             | 28000                                                                                    | Mono o estéreo.                                         |
| 256             | 32000                                                                                    | Mono o estéreo. Esta es la configuración predeterminada para estéreo. |
| 320             | 40000                                                                                    | Solo estéreo.                                            |
| 384             | 48000                                                                                    | Solo estéreo.                                            |
| 448             | 56 000                                                                                    | Solo estéreo.                                            |



 

La velocidad de bits de codificación predeterminada se establece en 256 kbps para estéreo y 192 kbps para mono. La configuración predeterminada se refleja en los tipos de medios devueltos por el método [**IMFTransform::GetOutputAvailableType del**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) codificador.

### <a name="example-media-types"></a>Tipos de medios de ejemplo

Este es un ejemplo de los tipos de medios necesarios para codificar un PCM entero de 16 bits, audio estéreo de 48 kHz a la velocidad de bits predeterminada de 256 kbps.

Tipo de medio de salida:

| Atributo                                                                           | Valor                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [TIPO \_ PRINCIPAL DE MT \_ DE \_ MF](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**        |
| [\_SUBTIPO DE MT DE MF \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Tipo de medio de entrada:

| Atributo                                                                                | Valor                  |
|------------------------------------------------------------------------------------------|------------------------|
| [TIPO \_ PRINCIPAL DE MT \_ DE \_ MF](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [\_SUBTIPO DE MT DE MF \_](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ MUESTRA](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [PROMEDIO DE BYTES PROMEDIO DE AUDIO DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Archivo DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 




