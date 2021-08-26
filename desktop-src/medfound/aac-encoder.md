---
description: El codificador Microsoft Media Foundation AAC es una transformación de Media Foundation que codifica el perfil de baja complejidad (LC) de codificación de audio avanzada (AAC), tal como se define en ISO/IEC 13818-7 (MPEG-2 Audio Part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674ad291e1cf6b56f7ffef640fade683265b62a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465642"
---
# <a name="aac-encoder"></a>Codificador AAC

El codificador Microsoft Media Foundation AAC es una transformación [de Media Foundation](media-foundation-transforms.md) que codifica el perfil de baja complejidad (LC) de codificación de audio avanzada (AAC), tal como se define en ISO/IEC 13818-7 (MPEG-2 Audio Part 7).

El codificador AAC no admite la codificación en ningún otro perfil de AAC, como Main, SSR o LTP.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador AAC es **CLSID \_ AACMFTEncoder**, definido en el archivo de encabezado wmcodecdsp.h.

## <a name="media-types"></a>Tipos de medios

El codificador AAC admite los siguientes tipos de medios. Puede establecer primero los tipos en el tipo de entrada de orden o en el tipo de salida.

### <a name="input-types"></a>Tipos de entrada

Establezca los atributos siguientes en el tipo de medio de entrada.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. | Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo. | Debe ser <strong>MFAudioFormat_PCM</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Bits por ejemplo. | Debe ser 16. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Ejemplos por segundo. | Se admiten los valores siguientes:<ul><li>44100 (44,1 KHz)</li><li>48000 (48 KHz)</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canales. | Debe ser 1 (mono) o 2 (estéreo) o 6 (5.1).<blockquote>[!Note]<br />La compatibilidad con 6 canales de audio se introdujo con Windows 10 y no está disponible para versiones anteriores de Windows.</blockquote><br /> | 




 

Una vez establecido el tipo de entrada, el codificador deriva los valores siguientes y los agrega al tipo de medio:

-   [**PROMEDIO \_ DE BYTES PROMEDIO DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO \_ \_ MF MT**](mf-mt-audio-block-alignment-attribute.md)
-   [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>Tipos de salida

Establezca los atributos siguientes en el tipo de medio de salida.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. | Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de audio. | Debe ser <strong>MFAudioFormat_AAC</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Bits por ejemplo. | Debe ser 16. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Ejemplos por segundo. | Debe coincidir con el tipo de entrada. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canales. | Debe coincidir con el tipo de entrada. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Velocidad de bits de la secuencia de AAC codificada, en bytes por segundo. | Se admiten los valores siguientes:<ul><li>12000</li><li>16000</li><li>20000</li><li>24000</li></ul>El valor predeterminado para mono y estéreo es 12000 (96 Kbps).<br /> | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Tipo de carga de AAC. | Opcional. Si se establece, el valor debe ser cero, lo que indica que la secuencia solo raw_data_block elementos.<br /> Opcional. Si no se establece el atributo, el valor predeterminado es cero, lo que indica que la secuencia solo contiene raw_data_block elementos (AAC sin formato). <br /> En Windows 7, si se establece este atributo, el valor debe ser cero.<br /> A partir Windows 8, el valor puede ser 0 (AAC sin procesar) o 1 (AAC de ADTS). <br /> | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Perfil y nivel de audio de AAC. | Opcional. Se admiten los valores siguientes:<ul><li>0x29 (valor predeterminado)</li><li>0x2A</li><li>0x2B</li><li>0x2C</li><li>0x2E</li><li>0x2F</li><li>0x30</li><li>0x31</li><li>0x32</li><li>0x33</li></ul> | 


En la tabla siguiente se enumeran los valores que se pueden usar para el MF_MT_AAC_PROFILE_LEVEL_INDICATION atributo .

| MF_MT_AAC_PROFILE_LEVEL_INDICATION valor | Perfil                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | Perfil de AAC L2                    | 
| 0x2A                                     | Perfil de AAC L4                    | 
| 0x2B                                     | Perfil de AAC L5                    | 
| 0x2C                                     | Perfil de AAC de alta eficacia v1 L2 | 
| 0x2E                                     | Perfil de AAC de alta eficacia v1 L4 | 
| 0x2F                                     | Perfil de AAC de alta eficacia v1 L5 | 
| 0x30                                     | Perfil de AAC de alta eficacia v2 L2 | 
| 0x31                                     | Perfil de AAC de alta eficacia v2 L3 | 
| 0x32                                     | Perfil de AAC de alta eficacia v2 L4 | 
| 0x33                                     | Perfil de AAC de alta eficacia v2 L5 | 

 

Una vez establecido el tipo de salida, el codificador AAC actualiza el tipo agregando el atributo [**MF \_ MT USER \_ \_ DATA.**](mf-mt-user-data-attribute.md) Este atributo contiene la parte de la estructura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece después de la [**estructuraWAVEATEX**](/previous-versions/dd757713(v=vs.85)) (es decir, después del **miembro wfx).** Esto va seguido de los datos AudioSpecificConfig(), tal como se define en ISO/IEC 14496-3.

Cada ejemplo de salida contiene un marco AAC comprimido sin encabezado. Este formato es equivalente al elemento \_ \_ block() de datos sin procesar definido por MPEG-2. El [atributo MF MT \_ \_ AAC PAYLOAD \_ \_ TYPE,](mf-mt-aac-payload-type.md) si está presente en el tipo de salida, debe establecerse en cero para indicar este tipo de carga.

Cada ejemplo de salida contiene un marco AAC comprimido correspondiente a 1024 ejemplos de PCM. Por ejemplo, a una velocidad de muestreo de 48 Khz, la duración de un fotograma comprimido es de 21,33 ms.

Si [MF \_ MT \_ AAC PAYLOAD \_ \_ TYPE](mf-mt-aac-payload-type.md) es cero (el valor predeterminado), cada muestra de salida contiene un elemento bloque de datos sin procesar() tal como se define en \_ \_ ISO/IEC 13818-7.

## <a name="example-media-types"></a>Tipos de medios de ejemplo

Este es un ejemplo de los tipos de medios necesarios para codificar desde audio estéreo de 44,1 kHz y 160 Kbps a AAC sin formato

Tipo de medio de entrada:



| Atributo                                                                                    | Valor                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**TIPO \_ PRINCIPAL DE MF MT \_ \_**](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [**SUBTIPO \_ MT DE MF \_**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [**BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ EJEMPLO**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**CANALES \_ NUM \_ DE AUDIO \_ MF MT \_**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**PROMEDIO \_ DE BYTES PROMEDIO DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (opcional)      |
| [**ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO \_ \_ MF MT**](mf-mt-audio-block-alignment-attribute.md)             | 4 (opcional)           |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md)         | 1 (opcional)           |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (opcional)     |
| [**EJEMPLOS \_ DE TAMAÑO FIJO \_ DE \_ \_ MF MT**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (opcional)           |



 

Tipo de medio de salida:



| Atributo                                                                                      | Valor                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MF MT \_ \_**](mf-mt-major-type-attribute.md)                                      | **MFMediaType \_ Audio**                                                                          |
| [**SUBTIPO \_ MT DE MF \_**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ EJEMPLO**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**CANALES \_ NUM \_ DE AUDIO \_ MF MT \_**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**PROMEDIO \_ DE BYTES PROMEDIO DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [TIPO \_ DE CARGA DE AAC MT \_ \_ MF \_](mf-mt-aac-payload-type.md)                                       | 0 (opcional)                                                                                    |
| [INDICACIÓN \_ DE NIVEL DE PERFIL DE AUDIO MF MT \_ AAC \_ \_ \_ \_](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (opcional)                                                                                 |
| [**ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO \_ \_ MF MT**](mf-mt-audio-block-alignment-attribute.md)               | 1 (opcional)                                                                                    |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md)           | 0 (opcional)                                                                                    |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (opcional)                                                                               |
| [**DATOS \_ DE USUARIO DE MF MT \_ \_**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (opcional) |



 

## <a name="remarks"></a>Comentarios

En la implementación actual, cada ejemplo de entrada debe tener un tiempo y una duración válidos. Para establecer la hora del ejemplo, llame [**a ALEJEMPLO::SetSampleTime.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) Para establecer la duración del ejemplo, llame [**a ALEJEMPLO::SetSampleDuration.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)

Si no se establece el tiempo de ejemplo, el método [**MFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) del codificador devuelve **MF E NO SAMPLE \_ \_ \_ \_ TIMESTAMP**. Si no se establece la duración de la muestra, el **método ProcessInput** devuelve **MF E NO SAMPLE \_ \_ \_ \_ DURATION**.

La duración de la muestra se puede calcular de la siguiente manera:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



donde *nAudioSamplesPerChannel* es el número de muestras de audio pcm por canal en el búfer de entrada y *nSamplesPerSec* es la frecuencia de muestreo, en muestras por segundo.

> [!Note]  
> Debido a un error en la implementación actual, si la duración de la muestra se establece en cero, la llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) se realiza correctamente, pero una llamada posterior a [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) producirá una excepción de división por cero. Para evitar este error, establezca una duración distinta de cero válida en cada ejemplo de entrada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[**Descodificador de AAC**](aac-decoder.md)
</dt> <dt>

[Tipos de medios de AAC](aac-media-types.md)
</dt> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

