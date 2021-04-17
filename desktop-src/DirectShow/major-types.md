---
description: En la tabla siguiente se describen los principales tipos de medios.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Tipos principales (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5722cbad713f2fb9ae876e58941bde44c2e110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690310"
---
# <a name="major-types"></a>Tipos principales

En la tabla siguiente se describen los principales tipos de medios.



| GUID                                                                                                                                                                                                                                  | Descripción                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**MEDIATYPE \_ AnalogAudio**</dt> </dl>         | Audio analógico.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**MEDIATYPE \_ AnalogVideo**</dt> </dl>         | Vídeo analógico.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**Audio de MEDIATYPE \_**</dt> </dl>                                 | Audio. Vea [subtipos de audio](audio-subtypes.md).<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**MEDIATYPE \_ AUXLine21Data**</dt> </dl> | Datos de la línea 21. Utilizado por subtítulos cerrados. Vea [**tipos de medios de línea 21**](line-21-media-types.md).<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**MEDIATYPE ( \_ archivo)**</dt> </dl>                                     | Archivo: (Obsoleto)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**MEDIATYPE \_ intercalado**</dt> </dl>         | Audio y vídeo intercalados. Se usa para vídeo digital (DV).<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**MEDIATYPE \_ LMRT**</dt> </dl>                                                                      | Obsoleto. No debe usarse.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**\_MIDI MEDIATYPE**</dt> </dl>                                     | Formato MIDI.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**\_PES MPEG2 \_ PE**</dt> </dl>                                                      | Paquetes de PE MPEG-2. Consulte [tipos de medios MPEG-2](mpeg-2-media-types.md).<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**\_Secciones de MPEG2 de MEDIATYPE \_**</dt> </dl>                                       | Datos de sección MPEG-2. Consulte [tipos de medios MPEG-2](mpeg-2-media-types.md).<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**MEDIATYPE \_ comando**</dt> </dl> | Los datos son un comando de script que usan los subtítulos cerrados.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**\_Secuencia MEDIATYPE**</dt> </dl>                             | Secuencia de bytes sin marcas de tiempo. Vea [**subtipos de secuencia**](stream-subtypes.md).<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**\_Texto MEDIATYPE**</dt> </dl>                                     | Texto.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**Código de tiempo de MEDIATYPE \_**</dt> </dl>                     | Datos de código de tiempo. Nota: DirectShow no proporciona ningún filtro que admita este tipo de medio.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**\_secuencia de dirección URL de MEDIATYPE \_**</dt> </dl>                                                   | Obsoleto. No debe usarse.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**MEDIATYPE \_ VBI**</dt> </dl>                                                                         | Datos de intervalo de blanking (VBI) vertical (para televisión). Igual que KSDATAFORMAT \_ Type \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**Vídeo de MEDIATYPE \_**</dt> </dl>                                 | Video. Vea [subtipos de vídeo](video-subtypes.md).<br/>                                               |



## <a name="remarks"></a>Observaciones

El GUID del subtipo define el formato. En algunos formatos, el GUID del subtipo podría ser MEDIASUBTYPE \_ None, lo que significa que el formato no requiere un subtipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




