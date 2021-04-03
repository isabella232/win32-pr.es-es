---
description: El codificador AAC Microsoft Media Foundation es una transformación de Media Foundation que codifica el perfil de baja complejidad (LC) de codificación de audio avanzada (AAC), tal y como se define en ISO/IEC 13818-7 (la parte 7 de audio MPEG-2).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908044"
---
# <a name="aac-encoder"></a>Codificador AAC

El codificador AAC Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que codifica el perfil de baja complejidad (LC) de codificación de audio avanzada (AAC), tal y como se define en ISO/IEC 13818-7 (la parte 7 de audio MPEG-2).

El codificador AAC no admite la codificación en ningún otro perfil AAC, como Main, SSR o LTP.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador AAC es **CLSID \_ AACMFTEncoder**, definido en el archivo de encabezado wmcodecdsp. h.

## <a name="media-types"></a>Tipos de medios

El codificador AAC admite los siguientes tipos de medios. En primer lugar, puede establecer los tipos en el tipo de entrada de orden primero o en el tipo de salida.

### <a name="input-types"></a>Tipos de entrada

Establezca los siguientes atributos en el tipo de medio de entrada.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
<th>Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principal.</td>
<td>Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Subtipo.</td>
<td>Debe ser <strong>MFAudioFormat_PCM</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits por muestra.</td>
<td>Debe ser 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Muestras por segundo.</td>
<td>Se admiten los valores siguientes:
<ul>
<li>44100 (44,1 KHz)</li>
<li>48000 (48 KHz)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canales.</td>
<td>Debe ser 1 (mono) o 2 (estéreo) o 6 (5,1).
<blockquote>
[!Note]<br />
La compatibilidad con 6 canales de audio se presentó con Windows 10 y no está disponible para versiones anteriores de Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Una vez establecido el tipo de entrada, el codificador deriva los valores siguientes y los agrega al tipo de medio:

-   [**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_alineación del \_ bloque de audio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_velocidad de \_ bits media MF MT \_**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>Tipos de salida

Establezca los siguientes atributos en el tipo de medio de salida.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
<th>Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principal.</td>
<td>Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Subtipo de audio.</td>
<td>Debe ser <strong>MFAudioFormat_AAC</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits por muestra.</td>
<td>Debe ser 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Muestras por segundo.</td>
<td>Debe coincidir con el tipo de entrada.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canales.</td>
<td>Debe coincidir con el tipo de entrada.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Velocidad de bits de la secuencia AAC codificada, en bytes por segundo.</td>
<td>Se admiten los valores siguientes:
<ul>
<li>12000</li>
<li>16000</li>
<li>20000</li>
<li>24000</li>
</ul>
El valor predeterminado para mono y estéreo es 12000 (96 kbps).<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>El tipo de carga AAC.</td>
<td>Opcional. Si se establece, el valor debe ser cero, lo que indica que el flujo solo contiene elementos raw_data_block.<br/> Opcional. Si no se establece el atributo, el valor predeterminado es cero, lo que indica que el flujo solo contiene elementos raw_data_block (AAC sin formato). <br/> En Windows 7, si se establece este atributo, el valor debe ser cero.<br/> A partir de Windows 8, el valor puede ser 0 (AAC sin formato) o 1 (ADTS AAC). <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>El perfil de audio AAC y el nivel.</td>
<td>Opcional. Se admiten los valores siguientes:
<ul>
<li>0x29 (valor predeterminado)</li>
<li>0x2A</li>
<li>0x2B</li>
<li>0x2C</li>
<li>0x2E</li>
<li>0x2F</li>
<li>0x30</li>
<li>0x31</li>
<li>0x32</li>
<li>0x33</li>
</ul></td>
</tr>
</tbody>
</table>

En la tabla siguiente se enumeran los valores que se pueden usar para el atributo MF_MT_AAC_PROFILE_LEVEL_INDICATION.

| MF_MT_AAC_PROFILE_LEVEL_INDICATION valor | Perfil                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | Perfil de AAC L2                    | 
| 0x2A                                     | Perfil L4 de AAC                    | 
| 0x2B                                     | L5 del perfil AAC                    | 
| 0x2C                                     | Perfil de alta eficacia v1 AAC L2 | 
| 0x2E                                     | Perfil de alta eficacia v1 AAC L4 | 
| 0x2F                                     | Perfil L5 de alta eficacia v1 AAC | 
| 0x30                                     | Perfil del AAC de alta eficacia V2 L2 | 
| 0x31                                     | Perfil de AAC de alta eficacia V2 L3 | 
| 0x32                                     | Perfil de AAC de alta eficacia V2 L4 | 
| 0x33                                     | Perfil L5 de alta eficacia V2 AAC | 

 

Una vez establecido el tipo de salida, el codificador AAC actualiza el tipo agregando el atributo de [**\_ datos de \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) . Este atributo contiene la parte de la estructura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece después de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (es decir, después del miembro de **WFX** ). A continuación se muestran los datos de AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3.

Cada ejemplo de salida contiene un marco AAC comprimido sin encabezado. Este formato es equivalente al elemento de \_ bloque de datos sin formato \_ () definido por MPEG-2. El atributo de [ \_ tipo de carga de módulo MF MT \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) , si está presente en el tipo de salida, debe establecerse en cero para indicar este tipo de carga.

Cada ejemplo de salida contiene un fotograma AAC comprimido correspondiente a los ejemplos 1024 PCM. Por ejemplo, con una frecuencia de muestreo de 48 kHz, la duración de un fotograma comprimido es de 21,33 ms.

Si [el \_ \_ tipo de \_ carga \_ de módulo MF MT AAC](mf-mt-aac-payload-type.md) es cero (el valor predeterminado), cada ejemplo de salida contiene un \_ \_ elemento de bloque de datos sin procesar () tal y como se define en ISO/IEC 13818-7.

## <a name="example-media-types"></a>Tipos de medios de ejemplo

Este es un ejemplo de los tipos de medios necesarios para codificar desde 44,1-kHz, audio estéreo de 160-Kbps a AAC sin formato

Tipo de medio de entrada:



| Atributo                                                                                    | Value                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                                    | **\_Audio MFMediaType** |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (opcional)      |
| [**\_alineación del \_ bloque de audio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)             | 4 (opcional)           |
| [**MF \_ MT \_ All \_ Samples \_ independiente**](mf-mt-all-samples-independent-attribute.md)         | 1 (opcional)           |
| [**\_velocidad de \_ bits media MF MT \_**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (opcional)     |
| [**\_ejemplos de \_ \_ tamaño fijo MF MT \_**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (opcional)           |



 

Tipo de medio de salida:



| Atributo                                                                                      | Value                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                                      | **\_Audio MFMediaType**                                                                          |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [\_tipo de \_ carga del AAC \_ \_ de MF MT](mf-mt-aac-payload-type.md)                                       | 0 (opcional)                                                                                    |
| [\_indicación de \_ \_ nivel de \_ Perfil de audio \_ \_ MF MT AAC](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (opcional)                                                                                 |
| [**\_alineación del \_ bloque de audio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)               | 1 (opcional)                                                                                    |
| [**MF \_ MT \_ All \_ Samples \_ independiente**](mf-mt-all-samples-independent-attribute.md)           | 0 (opcional)                                                                                    |
| [**\_velocidad de \_ bits media MF MT \_**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (opcional)                                                                               |
| [**datos de usuario de MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0X12, 0x10} opta |



 

## <a name="remarks"></a>Observaciones

En la implementación actual, cada muestra de entrada debe tener una hora y una duración válidas. Para establecer la hora de ejemplo, llame a [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Para establecer la duración del ejemplo, llame a [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Si no se establece la hora de ejemplo, el método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) del codificador devuelve **MF \_ E \_ no \_ muestra ninguna \_ marca** de tiempo. Si no se establece la duración del ejemplo, el método **ProcessInput** devuelve **MF \_ E \_ no \_ muestra la \_ duración**.

La duración de la muestra se puede calcular de la manera siguiente:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



donde *nAudioSamplesPerChannel* es el número de muestras de audio PCM por canal en el búfer de entrada, y *nSamplesPerSec* es la frecuencia de muestreo, en muestras por segundo.

> [!Note]  
> Debido a un error en la implementación actual, si la duración de ejemplo está establecida en cero, la llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) se realiza correctamente, pero una llamada subsiguiente a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) producirá una excepción de división por cero. Para evitar este error, establezca una duración válida distinto de cero en cada ejemplo de entrada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[**Descodificador AAC**](aac-decoder.md)
</dt> <dt>

[Tipos de medios AAC](aac-media-types.md)
</dt> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

