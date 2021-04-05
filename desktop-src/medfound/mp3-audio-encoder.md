---
description: Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Codificador de audio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082297"
---
# <a name="mp3-audio-encoder"></a>Codificador de audio MP3

El codificador de audio MP3 Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) que codifica audio MPEG-1 capa 3 (MP3).

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador MP3 es **CLSID \_ MP3ACMCodecWrapper**, definido en el archivo de encabezado wmcodecdsp. h.

## <a name="media-types"></a>Tipos de medios

El codificador MP3 admite los siguientes tipos de medios. El tipo de salida debe establecerse antes que el tipo de entrada.

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
<td>Debe ser <strong>MFAudioFormat_MP3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Velocidad de bits de la secuencia MP3 codificada, en bytes por segundo.</td>
<td>El codificador es compatible con todas las velocidades de bits definidas por el estándar (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 o 320 Kbps).<br/> La velocidad de bits predeterminada es 128 kbps para mono y 320 Kbps para estéreo.<br/> Utilice este atributo para especificar la velocidad de bits codificada.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canales.</td>
<td>Se admiten los valores siguientes:
<ul>
<li>1 (mono)</li>
<li>2 (estéreo)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Muestras por segundo.</td>
<td>Se admiten los valores siguientes:
<ul>
<li>48000 (48 KHz)</li>
<li>44100 (44,1 KHz)</li>
<li>32000 (32 KHz)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></td>
<td>Datos de códecs adicionales.</td>
<td>Este atributo contiene los 12 bytes de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> que siguen el miembro de <strong>WFX</strong> de esa estructura.</td>
</tr>
</tbody>
</table>



 

Como alternativa, puede rellenar una estructura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) y llamar a [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) para convertir la estructura en un tipo de medio Media Foundation.

### <a name="input-types"></a>Tipos de entrada

Establezca los siguientes atributos en el tipo de medio de entrada.



| Atributo                                                                               | Descripción         | Observaciones                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                               | Tipo principal.         | Debe ser **MFMediaType \_ audio**. |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                      | Subtipo.            | Debe ser **MFAudioFormat \_ PCM**. |
| [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md)       | Bits por muestra.    | Debe ser 16.                     |
| [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md) | Muestras por segundo. | Debe coincidir con el tipo de salida.     |
| [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)              | Número de canales. | Debe coincidir con el tipo de salida.     |



 

El codificador solo admite datos de entrada de PCM enteros de 16 bits. No admite la entrada de punto flotante de 32 bits.

### <a name="media-formats"></a>Formatos de medios

El estándar MPEG-1 y MPEG-2 define los formatos de audio de nivel 3 de 252. El codificador MP3 admite el estándar con algunas excepciones, así como algunos formatos adicionales, como se describe a continuación. La capa 3 se define como:



| Requisito | Value |
|----------------------------------|---------------------------------------------------------------|
| Canales                         | mono o estéreo                                                |
| Velocidades de muestra MPEG-1 en kHz       | 44,1, 48, 32                                                  |
| Velocidades de bits con codificación MPEG-1 en kbps | 32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 |
| Velocidades de muestra de MPEG-2 en kHz       | 8, 11,025, 12, 16, 22,05, 24                                  |
| Velocidades de bits con codificación MPEG-2 en kbps | 8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160          |



 

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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
