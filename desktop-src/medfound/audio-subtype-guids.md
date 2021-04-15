---
description: GUID de subtipo de audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID de subtipo de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496852"
---
# <a name="audio-subtype-guids"></a>GUID de subtipo de audio

Se definen los siguientes GUID de subtipo de audio. Para especificar el subtipo, establezca el atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) en el tipo de medio. Excepto donde se indique, estas constantes se definen en el archivo de encabezado mfapi. h.

Cuando se usan estos subtipos, establezca el atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) en **MFMediaType \_ audio**.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descripción</th>
<th>Format (etiqueta) (FOURCC)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MEDIASUBTYPE_RAW_AAC1</strong></td>
<td>Codificación de audio avanzada (AAC).<br/> Este subtipo se usa para AAC incluido en un archivo AVI con una etiqueta de formato de audio igual a 0x00FF. <br/> Para obtener más información, consulte el <a href="aac-decoder.md"><strong>descodificador AAC</strong></a>.<br/> Definido en wmcodecdsp. h<br/></td>
<td>WAVE_FORMAT_RAW_AAC1 (0x00FF)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Codificación de audio avanzada (AAC).<br/>
<blockquote>
[!Note]<br />
Equivalente a MEDIASUBTYPE_MPEG_HEAAC, definido en wmcodecdsp. h.
</blockquote>
<br/> La secuencia puede contener datos AAC sin formato o datos AAC en una secuencia de flujo de transporte de datos (ADTS) de audio.<br/> Para más información, consulte:<br/>
<ul>
<li><a href="aac-decoder.md"><strong>Descodificador AAC</strong></a></li>
<li><a href="mpeg-4-file-source.md">Origen de archivo MPEG-4</a></li>
</ul></td>
<td>WAVE_FORMAT_MPEG_HEAAC (0x1610)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_ADTS</strong></td>
<td>No se utiliza.</td>
<td>WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_ALAC</strong></td>
<td>Códec de audio sin pérdida de Apple<br/> Compatible con Windows 10 y versiones posteriores.<br/></td>
<td>WAVE_FORMAT_ALAC (0x6C61)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_NB</strong></td>
<td>Audio de varias velocidades Adaptative<br/> Se admite en Windows 8.1 y versiones posteriores.<br/></td>
<td>WAVE_FORMAT_AMR_NB</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AMR_WB</strong></td>
<td>Audio de banda ancha multifrecuencia Adaptative<br/> Se admite en Windows 8.1 y versiones posteriores.<br/></td>
<td>WAVE_FORMAT_AMR_WB</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_WP</strong></td>
<td>Se admite en Windows 8.1 y versiones posteriores.<br/></td>
<td>WAVE_FORMAT_AMR_WP</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_AC3</strong></td>
<td>Dolby Digital (AC-3).<br/> El mismo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, que se define en ksuuids. h<br/></td>
<td>Ninguno.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></td>
<td>Audio Dolby AC-3 en una interfaz digital de Sony/Philips (S/PDIF).<br/> Este valor GUID es idéntico a los siguientes subtipos:<br/>
<ul>
<li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, definido en ksmedia. h.</li>
<li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, definido en UUID. h.</li>
</ul></td>
<td>WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_DDPlus</strong></td>
<td>Dolby Digital Plus.<br/> El mismo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, que se define en wmcodecdsp. h.<br/></td>
<td>None</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_DRM</strong></td>
<td>Datos de audio cifrados usados con la ruta de audio segura.</td>
<td>WAVE_FORMAT_DRM (0x0009)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_DTS</strong></td>
<td>Audio de sistemas de Digital Theater (DTS).</td>
<td>WAVE_FORMAT_DTS (0x0008)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_FLAC</strong></td>
<td>Códec de audio sin pérdida de servicio<br/> Compatible con Windows 10 y versiones posteriores.<br/></td>
<td>WAVE_FORMAT_FLAC (0xF1AC)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Audio de punto flotante IEEE sin comprimir.</td>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Float_SpatialObjects</strong></td>
<td>Audio de punto flotante IEEE sin comprimir.</td>
<td>None</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MP3</strong></td>
<td>Capa de audio MPEG-3 (MP3).</td>
<td>WAVE_FORMAT_MPEGLAYER3 (0x0055)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_MPEG</strong></td>
<td>Carga de audio MPEG-1.</td>
<td>WAVE_FORMAT_MPEG (0x0050)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MSP1</strong></td>
<td>Códec de voz de Windows Media Audio 9.</td>
<td>WAVE_FORMAT_WMAVOICE9 (0x000A)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Opus</strong></td>
<td>Opus<br/> Compatible con Windows 10 y versiones posteriores.<br/></td>
<td>WAVE_FORMAT_OPUS (0x704F)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>Audio PCM sin comprimir.</td>
<td>WAVE_FORMAT_PCM (1)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_QCELP</strong></td>
<td>Audio QCELP (predicción lineal entusiasmada de código Qualcomm).</td>
<td>None</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMASPDIF</strong></td>
<td>Windows Media Audio 9 Professional codec a través de S/PDIF.</td>
<td>WAVE_FORMAT_WMASPDIF (0x0164)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudio_Lossless</strong></td>
<td>Códec de Windows Media Audio 9 sin pérdida de Windows Media Audio Códec de 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMAudioV8</strong></td>
<td>Códec Windows Media Audio 8, códec de Windows Media Audio 9 o Windows Media Audio Códec 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO2 (0x0161)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudioV9</strong></td>
<td>Códec Windows Media Audio 9 Professional o Windows Media Audio 9,1 Professional.</td>
<td>WAVE_FORMAT_WMAUDIO3 (0x0162)</td>
</tr>
</tbody>
</table>



 

Las etiquetas de formato enumeradas en la tercera columna de esta tabla se usan en la estructura **WAVEFORMATEX** y se definen en el archivo de encabezado mmreg. h.

Dada una etiqueta de formato de audio, puede crear un GUID de subtipo de audio como se indica a continuación:

1.  Comience con el valor **MFAudioFormat \_ base**, que se define en mfaph. i.
2.  Reemplace el primer **valor DWORD** de este GUID por la etiqueta Format.

Puede usar la macro [**definir \_ \_ GUID de MEDIATYPE**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para definir una nueva constante GUID que siga este patrón.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID de tipo de medio](media-type-guids.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




