---
description: GUID de subtipo de audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID de subtipo de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26b61dc7c8bb828deb6278b037dd6128afcaf1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361176"
---
# <a name="audio-subtype-guids"></a>GUID de subtipo de audio

Se definen los siguientes GUID de subtipo de audio. Para especificar el subtipo, establezca el atributo [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) en el tipo de medio. Excepto donde se indica, estas constantes se definen en el archivo de encabezado mfapi.h.

Cuando se usen estos subtipos, establezca el atributo [MF \_ MT MAJOR \_ \_ TYPE](mf-mt-major-type-attribute.md) en **MFMediaType \_ Audio**.




| GUID | Descripción | Etiqueta de formato (FOURCC) | 
|------|-------------|---------------------|
| <strong>MEDIASUBTYPE_RAW_AAC1</strong> | Codificación de audio avanzada (AAC).<br /> Este subtipo se usa para AAC incluido en un archivo AVI con una etiqueta de formato de audio igual a 0x00FF. <br /> Para obtener más información, vea <a href="aac-decoder.md"><strong>Descodificador de AAC.</strong></a><br /> Definido en wmcodecdsp.h<br /> | WAVE_FORMAT_RAW_AAC1 (0x00FF) | 
| <strong>MFAudioFormat_AAC</strong> | Codificación de audio avanzada (AAC).<br /><blockquote>[!Note]<br />Equivalente a MEDIASUBTYPE_MPEG_HEAAC, definido en wmcodecdsp.h.</blockquote><br /> La secuencia puede contener datos de AAC sin procesar o datos de AAC en una secuencia de secuencia de transporte de datos de audio (ADTS).<br /> Para más información, consulte:<br /><ul><li><a href="aac-decoder.md"><strong>Descodificador de AAC</strong></a></li><li><a href="mpeg-4-file-source.md">Origen de archivo MPEG-4</a></li></ul> | WAVE_FORMAT_MPEG_HEAAC (0x1610) | 
| <strong>MFAudioFormat_ADTS</strong> | No se utiliza. | WAVE_FORMAT_MPEG_ADTS_AAC (0x1600) | 
| <strong>MFAudioFormat_ALAC</strong> | Códec de audio sin pérdida de Apple<br /> Se admite en Windows 10 y versiones posteriores.<br /> | WAVE_FORMAT_ALAC (0x6C61) | 
| <strong>MFAudioFormat_AMR_NB</strong> | Audio adaptativo de varias velocidades<br /> Se admite en Windows 8.1 y versiones posteriores.<br /> | WAVE_FORMAT_AMR_NB | 
| <strong>MFAudioFormat_AMR_WB</strong> | Audio de banda ancha de velocidad múltiple adaptativa<br /> Se admite en Windows 8.1 y versiones posteriores.<br /> | WAVE_FORMAT_AMR_WB | 
| <strong>MFAudioFormat_AMR_WP</strong> | Se admite en Windows 8.1 y versiones posteriores.<br /> | WAVE_FORMAT_AMR_WP | 
| <strong>MFAudioFormat_Dolby_AC3</strong> | Dolby Digital (AC-3).<br /> El mismo valor GUID <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, que se define en ksuuids.h<br /> | Ninguno. | 
| <strong>MFAudioFormat_Dolby_AC3_SPDIF</strong> | Audio Dolby AC-3 a través de la interfaz digital de Dolby/Dolby (S/PDIF).<br /> Este valor GUID es idéntico a los subtipos siguientes:<br /><ul><li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, definido en ksmedia.h.</li><li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, definido en uuids.h.</li></ul> | WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092) | 
| <strong>MFAudioFormat_Dolby_DDPlus</strong> | Dolby Digital Plus.<br /> El mismo valor GUID <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, que se define en wmcodecdsp.h.<br /> | None | 
| <strong>MFAudioFormat_DRM</strong> | Datos de audio cifrados usados con la ruta de acceso de audio segura. | WAVE_FORMAT_DRM (0x0009) | 
| <strong>MFAudioFormat_DTS</strong> | Audio de Digital Theater Systems (DTS). | WAVE_FORMAT_DTS (0x0008) | 
| <strong>MFAudioFormat_FLAC</strong> | Códec de audio sin pérdida de datos gratuito<br /> Se admite en Windows 10 y versiones posteriores.<br /> | WAVE_FORMAT_FLAC (0xF1AC) | 
| <strong>MFAudioFormat_Float</strong> | Audio de punto flotante IEEE sin comprimir. | WAVE_FORMAT_IEEE_FLOAT (0x0003) | 
| <strong>MFAudioFormat_Float_SpatialObjects</strong> | Audio de punto flotante IEEE sin comprimir. | None | 
| <strong>MFAudioFormat_MP3</strong> | MPEG Audio Layer-3 (MP3). | WAVE_FORMAT_MPEGLAYER3 (0x0055) | 
| <strong>MFAudioFormat_MPEG</strong> | Carga de audio MPEG-1. | WAVE_FORMAT_MPEG (0x0050) | 
| <strong>MFAudioFormat_MSP1</strong> | Windows Códec media Audio 9 Voice. | WAVE_FORMAT_WMAVOICE9 (0x000A) | 
| <strong>MFAudioFormat_Opus</strong> | Opus<br /> Se admite en Windows 10 y versiones posteriores.<br /> | WAVE_FORMAT_OPUS (0x704F) | 
| <strong>MFAudioFormat_PCM</strong> | Audio PCM sin comprimir. | WAVE_FORMAT_PCM (1) | 
| <strong>MFAudioFormat_QCELP</strong> | Audio QCELP (Qualcomm Code Excited Linear Prediction). | None | 
| <strong>MFAudioFormat_WMASPDIF</strong> | Windows Códec de Professional Multimedia Audio 9 a través de S/PDIF. | WAVE_FORMAT_WMASPDIF (0x0164) | 
| <strong>MFAudioFormat_WMAudio_Lossless</strong> | Windows Códec sin pérdida de Media Audio 9 Windows códec Media Audio 9.1. | WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163) | 
| <strong>MFAudioFormat_WMAudioV8</strong> | Windows Códec Media Audio 8, Windows códec Media Audio 9 o Windows códec Media Audio 9.1. | WAVE_FORMAT_WMAUDIO2 (0x0161) | 
| <strong>MFAudioFormat_WMAudioV9</strong> | Windows Códec de Professional o códec Windows Media Audio 9.1 Professional de Media Audio 9.1. | WAVE_FORMAT_WMAUDIO3 (0x0162) | 




 

Las etiquetas de formato enumeradas en la tercera columna de esta tabla se usan en la estructura **DEDATOX** Y se definen en el archivo de encabezado mmreg.h.

Dada una etiqueta de formato de audio, puede crear un GUID de subtipo de audio como se muestra a continuación:

1.  Comience con el valor **MFAudioFormat \_ Base**, que se define en mfaph.i.
2.  Reemplace el primer **DWORD** de este GUID por la etiqueta de formato.

Puede usar la macro [**DEFINE \_ MEDIATYPE \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para definir una nueva constante GUID que siga este patrón.

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

 

 




