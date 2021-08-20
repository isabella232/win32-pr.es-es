---
description: En la tabla siguiente se describen los tipos de medios principales.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Tipos principales (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3764bffabb85b3b054fc7589d4eae9677adbc8835d0e4aa3029d31834eb887c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153247"
---
# <a name="major-types"></a>Tipos principales

En la tabla siguiente se describen los tipos de medios principales.



| GUID                                                                                                                                                                                                                                  | Descripción                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**MEDIATYPE \_ AnalogAudio**</dt> </dl>         | Audio análogo.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**MEDIATYPE \_ AnalogVideo**</dt> </dl>         | Vídeo análogo.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**MEDIATYPE \_ Audio**</dt> </dl>                                 | Audio. Vea [Subtipos de audio.](audio-subtypes.md)<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**MEDIATYPE \_ AUXLine21Data**</dt> </dl> | Datos de la línea 21. Usado por subtítulos. Vea [**Tipos de medios de línea 21.**](line-21-media-types.md)<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**Archivo \_ MEDIATYPE**</dt> </dl>                                     | Archivo: (Obsoleto)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**MEDIATYPE \_ intercalado**</dt> </dl>         | Audio y vídeo intercalados. Se usa para Digital Video (DV).<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**MEDIATYPE \_ LMRT**</dt> </dl>                                                                      | Obsoleto. No debe usarse.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**MEDIATYPE \_ Midi**</dt> </dl>                                     | Formato MIDI.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**MEDIATYPE \_ MPEG2 \_ PES**</dt> </dl>                                                      | Paquetes PES MPEG-2. Vea [Tipos de medios MPEG-2.](mpeg-2-media-types.md)<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**SECCIONES DE \_ MEDIATYPE MPEG2 \_**</dt> </dl>                                       | Datos de la sección MPEG-2. Vea [Tipos de medios MPEG-2.](mpeg-2-media-types.md)<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**MEDIATYPE \_ ScriptCommand**</dt> </dl> | Los datos son un comando de script que usan los subtítulos.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**Secuencia \_ MEDIATYPE**</dt> </dl>                             | Secuencia de bytes sin marcas de tiempo. Vea [**Stream Subtypes ( Subtipos de secuencia).**](stream-subtypes.md)<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**Texto \_ MEDIATYPE**</dt> </dl>                                     | Texto.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**Código de tiempo \_ DE MEDIATYPE**</dt> </dl>                     | Datos de código de tiempo. Nota: DirectShow no proporciona ningún filtro que admita este tipo de medio.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**SECUENCIA DE \_ DIRECCIÓN URL DE \_ MEDIATYPE**</dt> </dl>                                                   | Obsoleto. No debe usarse.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**MEDIATYPE \_ VBI**</dt> </dl>                                                                         | Datos de intervalo de espacio en blanco vertical (VBI) (para televisión). Igual que KSDATAFORMAT \_ TYPE \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**Vídeo \_ DE MEDIATYPE**</dt> </dl>                                 | Video. Vea [Subtipos de vídeo.](video-subtypes.md)<br/>                                               |



## <a name="remarks"></a>Comentarios

El GUID del subtipo define aún más el formato. Para algunos formatos, el GUID del subtipo podría ser MEDIASUBTYPE None, lo que significa que el formato \_ no requiere un subtipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




