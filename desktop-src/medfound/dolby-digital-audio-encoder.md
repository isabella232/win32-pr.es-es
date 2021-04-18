---
description: El descodificador de audio Dolby es una transformación de Media Foundation (MFT) que codifica audio mono o estéreo en Dolby digital, también denominado Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Codificador Dolby digital audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705413"
---
# <a name="dolby-digital-audio-encoder"></a>Codificador Dolby digital audio

El descodificador de audio Dolby es una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) que codifica audio mono o estéreo en Dolby digital, también denominado Dolby AC-3. El codificador no admite la entrada de varios canales, como la configuración del canal 5,1.

> [!IMPORTANT]
> En el caso de las versiones de Windows anteriores a Windows 8, la implementación de Microsoft de la tecnología Dolby Digital está restringida en lo que respecta al programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.

 

Para obtener más información acerca del audio Dolby digital, consulte el documento sobre el Comité de sistemas de televisión avanzado (ATSC) ( *AC-3, E-AC-3) revisión B*.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador de audio Dolby es **CLSID \_ CMSDolbyDigitalEncMFT**, definido en el archivo de encabezado wmcodecdsp. h.

## <a name="output-types"></a>Tipos de salida

Primero se debe establecer el tipo de salida, antes del tipo de entrada. En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obligatorio. Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de audio.</td>
<td>Obligatorio. Debe ser <strong>MFAudioFormat_Dolby_AC3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Muestras por segundo.</td>
<td>Obligatorio. Se admiten los valores siguientes:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canales.</td>
<td>Obligatorio. Debe ser 1 (mono) o 2 (estéreo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica la asignación de canales de audio a las posiciones del hablante.</td>
<td>Opcional. Si se establece, el valor debe ser 0X3 para los canales estéreo (Front izquierdo y derecho) o 0x4 para mono (canal de centro frontal).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocidad de bits de la secuencia AC-3 codificada, en bytes por segundo.</td>
<td>Opcional. Vea la sección Comentarios para ver los valores válidos. Si no se establece este atributo, el codificador utiliza una velocidad de bits predeterminada, como se describe en la sección Comentarios.</td>
</tr>
</tbody>
</table>



 

Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.

## <a name="input-types"></a>Tipos de entrada

En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de entrada.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obligatorio. Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de audio.</td>
<td>Obligatorio. Debe ser <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Número de bits por muestra de audio.</td>
<td>Obligatorio. El valor debe ser 16 si el subtipo es <strong>MFAudioFormat_PCM</strong>, o 32 si el subtipo es <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Muestras por segundo.</td>
<td>Obligatorio. Debe coincidir con el tipo de salida.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canales.</td>
<td>Obligatorio. Debe coincidir con el tipo de salida.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Alineación de bloque, en bytes.</td>
<td>Obligatorio. Calcule el valor de la siguiente manera:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: número de canales × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: número de canales × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocidad de bits de la secuencia de AC3s codificada, en bytes por segundo.</td>
<td>Obligatorio. Debe ser igual que la alineación de bloque × ejemplos por segundo.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica la asignación de canales de audio a las posiciones del hablante.</td>
<td>Opcional. Si se establece, el valor debe coincidir con el tipo de salida.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Número de bits válidos de datos de audio en cada ejemplo de audio.</td>
<td>Opcional. Si se establece, el valor debe ser idéntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

El codificador no admite la conversión de velocidad de muestra o la conversión estéreo/mono.

## <a name="remarks"></a>Observaciones

Cada fotograma de audio Dolby AC-3 contiene 1536 muestras de audio por canal. Sin embargo, cada búfer de entrada del codificador puede contener cualquier número de muestras de PCM. El tamaño de cada búfer de entrada debe ser un múltiplo de la alineación del bloque. El codificador almacena en caché los ejemplos de entrada hasta que tiene suficiente para 1536 muestras de audio por canal. en ese momento, el codificador genera un fotograma AC-3.

Cada búfer de salida contiene un marco AC-3 sin procesar. La duración es equivalente a la duración de las muestras de 1536 PCM con la frecuencia de muestreo actual (32 ms) a la velocidad de muestra de 48 kHz, 34,83 MS en 44,1 kHz y 48 MS a 32 kHz). El tamaño de cada búfer de salida depende de la velocidad de bits y la velocidad de muestra.

Para especificar la velocidad de bits de codificación, establezca el atributo [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de salida. En la tabla siguiente se muestra la relación entre la velocidad de bits de codificación y los \_ \_ bytes promedio de audio MF MT \_ \_ \_ por \_ segundo.



| Velocidad de bits (kbps) | [\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) | Observaciones                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Solo mono.                                              |
| 80              | 10000                                                                                    | Solo mono.                                              |
| 96              | 12000                                                                                    | Solo mono.                                              |
| 112             | 14000                                                                                    | Solo mono.                                              |
| 128             | 16000                                                                                    | Mono o estéreo.                                         |
| 160             | 20000                                                                                    | Mono o estéreo.                                         |
| 192             | 24000                                                                                    | Mono o estéreo. Esta es la configuración predeterminada de mono.   |
| 224             | 28000                                                                                    | Mono o estéreo.                                         |
| 256             | 32000                                                                                    | Mono o estéreo. Esta es la configuración predeterminada de estéreo. |
| 320             | 40000                                                                                    | Solo estéreo.                                            |
| 384             | 48000                                                                                    | Solo estéreo.                                            |
| 448             | 56 000                                                                                    | Solo estéreo.                                            |



 

La velocidad de bits de codificación predeterminada está establecida en 256 kbps para estéreo y 192 kbps para mono. La configuración predeterminada se refleja en los tipos de medios devueltos por el método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) del codificador.

### <a name="example-media-types"></a>Tipos de medios de ejemplo

A continuación se muestra un ejemplo de los tipos de medios que se necesitan para codificar el PCM de entero de 16 bits, audio estéreo de 48 kHz a la velocidad de bits predeterminada de 256 kbps.

Tipo de medio de salida:

| Atributo                                                                           | Value                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**        |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [\_muestras de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [\_canales de \_ número de audio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Tipo de medio de entrada:

| Atributo                                                                                | Value                  |
|------------------------------------------------------------------------------------------|------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                                    | **\_Audio MFMediaType** |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [MF \_ MT \_ audio \_ bits \_ por \_ muestra](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_muestras de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [\_canales de \_ número de audio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [\_alineación del \_ bloque de audio MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Archivo DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 




