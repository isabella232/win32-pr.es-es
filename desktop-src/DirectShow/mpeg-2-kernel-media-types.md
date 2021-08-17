---
description: Para varios GUID de tipo multimedia MPEG-2, el Windows DDK define nombres que difieren de los nombres usados en DirectShow. En la tabla siguiente se muestran DirectShow nombres (definidos en Ksuuids.h) y los nombres de modo kernel correspondientes (definidos en Ksmedia.h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Tipos de medios de kernel MPEG-2 (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cfbbd93bfb4d9c21a7ab2b496e69458e2754d95ae4427ad163c4f2a06e4165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952264"
---
# <a name="mpeg-2-kernel-media-types"></a>Tipos de medios de kernel MPEG-2

Para varios GUID de tipo multimedia MPEG-2, el Windows DDK define nombres que difieren de los nombres usados en DirectShow. En la tabla siguiente se muestran DirectShow nombres (definidos en Ksuuids.h) y los nombres de modo kernel correspondientes (definidos en Ksmedia.h).



| Nombre en Ksuuids.h              | Nombre en Ksmedia.h                          |
|--------------------------------|--------------------------------------------|
| FORMAT \_ WaveFormatEx           | KSDATAFORMAT \_ SPECIFIER \_ WAVEFORMATEX      |
| FORMAT \_ MPEG2Video             | KSDATAFORMAT \_ SPECIFIER \_ MPEG2 \_ VIDEO      |
| MEDIASUBTYPE \_ ATSC \_ SI         | KSDATAFORMAT \_ SUBTIPO \_ ATSC \_ SI            |
| MEDIASUBTYPE \_ DOLBY \_ AC3       | KSDATAFORMAT \_ SUBTYPE \_ AC3 \_ AUDIO          |
| MEDIASUBTYPE \_ DVB \_ SI          | KSDATAFORMAT \_ SUBTYPE \_ DVB \_ SI             |
| AUDIO \_ LPCM de DVD DE MEDIASUBTYPE \_ \_ | AUDIO \_ LPCM DE SUBTIPO \_ KSDATAFORMAT \_         |
| MEDIASUBTYPE \_ MPEG2 \_ AUDIO     | KSDATAFORMAT \_ SUBTYPE \_ MPEG2 \_ AUDIO        |
| PROGRAMA \_ MPEG2 DE MEDIASUBTYPE \_   | PROGRAMA MPEG2 DE TIPO \_ KSDATAFORMAT \_ \_ \_ ESTÁTICO |
| TRANSPORTE DE MEDIASUBTYPE \_ MPEG2 \_ | TRANSPORTE \_ \_ MPEG2 DE TIPO KSDATAFORMAT \_       |
| VÍDEO DE MEDIASUBTYPE \_ MPEG2 \_     | VÍDEO \_ MPEG2 DEL SUBTIPO \_ KSDATAFORMAT \_        |
| SECCIONES DE \_ MEDIATYPE MPEG2 \_     | SECCIONES DE TIPO \_ \_ MPEG2 DE KSDATAFORMAT \_        |
| MEDIATYPE \_ Audio               | KSDATAFORMAT \_ TYPE \_ AUDIO                  |
| MEDIATYPE \_ MPEG2 \_ PES          | KSDATAFORMAT \_ TYPE \_ MPEG2 \_ PES             |
| Vídeo \_ DE MEDIATYPE               | VÍDEO DE TIPO KSDATAFORMAT \_ \_                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




