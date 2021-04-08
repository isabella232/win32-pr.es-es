---
description: En este tema se describe cómo especificar el formato de una secuencia de codificación de audio avanzada (AAC) en Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipos de medios AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003311"
---
# <a name="aac-media-types"></a>Tipos de medios AAC

En este tema se describe cómo especificar el formato de una secuencia de codificación de audio avanzada (AAC) en Media Foundation.

Se definen dos subtipos para el audio AAC:



| Subtype                     | Descripción          | Encabezado       |
|-----------------------------|----------------------|--------------|
| **MFAudioFormat \_ AAC**      | AAC sin procesar o ADTS AAC. | mfapi. h      |
| **MEDIASUBTYPE \_ raw \_ AAC1** | AAC sin procesar.             | wmcodecdsp. h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC
</dt> <dd>

Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales antes de la aplicación de las herramientas de replicación de banda espectral (SBR) y de estéreo paramétricos (PS), si está presente. El efecto de la herramienta SBR es duplicar la velocidad de muestra descodificada en relación con la velocidad de muestra de núcleo AAC-LC. El efecto de la herramienta PS es descodificar estéreo de una secuencia de núcleos AAC-LC de canal mono.

Este subtipo es equivalente a **MEDIASUBTYPE \_ MPEG \_ HEAAC**, que se define en wmcodecdsp. h. Vea [GUID de subtipo de audio](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ raw \_ AAC1
</dt> <dd>

Este subtipo se usa para AAC incluido en un archivo AVI con la etiqueta de formato de audio igual al formato de onda \_ \_ raw \_ AAC1 (0x00FF).

Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales después de aplicar las herramientas SBR y PS, si están presentes.

</dd> </dl>

Los siguientes atributos de tipo de medio se aplican al audio AAC.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principal. Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Subtipo de audio. Consulte la descripción anterior para obtener más información.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Nivel y Perfil de audio. <br/> El valor de este atributo es el campo <strong>audioProfileLevelIndication</strong> , tal y como se define en ISO/IEC 14496-3.<br/> Si es desconocido, establezca en cero o 0xFE (no se ha &quot; especificado ningún perfil de audio &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Velocidad de bits de la secuencia AAC codificada, en bytes por segundo.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Tipo de carga.<br/> Solo se aplica a <strong>MFAudioFormat_AAC</strong>.<br/> <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> es opcional. Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que el flujo solo contiene elementos raw_data_block.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Profundidad de bits del audio PCM descodificado.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Asignación de canales de audio a las posiciones del hablante.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.<br/> La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Frecuencia de muestreo, en muestras por segundo.<br/> La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>El valor de este atributo depende del subtipo:<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: contiene la parte de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece después de la estructura <strong>WAVEFORMATEX</strong> (es decir, después del miembro de <strong>WFX</strong> ). A continuación se muestran los datos de AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene los datos de AudioSpecificConfig ().</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

