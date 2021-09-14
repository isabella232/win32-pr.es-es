---
description: Para varios GUID de tipo multimedia MPEG-2, el DDK de Windows define nombres que difieren de los nombres usados en DirectShow. En la tabla siguiente se muestran los DirectShow (definidos en Ksuuids.h) y los nombres de modo kernel correspondientes (definidos en Ksmedia.h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Tipos de medios de kernel MPEG-2 (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061022"
---
# <a name="mpeg-2-kernel-media-types"></a>Tipos de medios de kernel MPEG-2

Para varios GUID de tipo multimedia MPEG-2, el DDK de Windows define nombres que difieren de los nombres usados en DirectShow. En la tabla siguiente se muestran los DirectShow (definidos en Ksuuids.h) y los nombres de modo kernel correspondientes (definidos en Ksmedia.h).



| Nombre en Ksuuids.h              | Nombre en Ksmedia.h                          |
|--------------------------------|--------------------------------------------|
| FORMAT \_ WaveFormatEx           | KSDATAFORMAT \_ SPECIFIER \_ WAVEFORMATEX      |
| FORMAT \_ MPEG2Video             | KSDATAFORMAT \_ SPECIFIER \_ MPEG2 \_ VIDEO      |
| MEDIASUBTYPE \_ ATSC \_ SI         | SUBTIPO \_ \_ ATSC SI \_ DE KSDATAFORMAT            |
| MEDIASUBTYPE \_ DOLBY \_ AC3       | KSDATAFORMAT \_ SUBTYPE \_ AC3 \_ AUDIO          |
| MEDIASUBTYPE \_ VEZ SI \_          | SI DE \_ SUBTIPO \_ DE \_ KSDATAFORMAT             |
| AUDIO \_ LPCM DE DVD DE MEDIASUBTYPE \_ \_ | AUDIO \_ LPCM DE SUBTIPO \_ KSDATAFORMAT \_         |
| MEDIASUBTYPE \_ MPEG2 \_ AUDIO     | KSDATAFORMAT \_ SUBTYPE \_ MPEG2 \_ AUDIO        |
| PROGRAMA MEDIASUBTYPE \_ MPEG2 \_   | PROGRAMA \_ MPEG2 ESTÁTICO DE TIPO KSDATAFORMAT \_ \_ \_ |
| TRANSPORTE DE MEDIASUBTYPE \_ MPEG2 \_ | TRANSPORTE \_ \_ MPEG2 DE TIPO KSDATAFORMAT \_       |
| VÍDEO DE MEDIASUBTYPE \_ MPEG2 \_     | VÍDEO \_ MPEG2 DEL SUBTIPO \_ KSDATAFORMAT \_        |
| SECCIONES DE \_ MEDIATYPE MPEG2 \_     | SECCIONES MPEG2 DE TIPO KSDATAFORMAT \_ \_ \_        |
| MEDIATYPE \_ Audio               | KSDATAFORMAT \_ TYPE \_ AUDIO                  |
| MEDIATYPE \_ MPEG2 \_ PES          | KSDATAFORMAT \_ TYPE \_ MPEG2 \_ PES             |
| VÍDEO \_ MEDIATYPE               | VÍDEO DE TIPO KSDATAFORMAT \_ \_                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




