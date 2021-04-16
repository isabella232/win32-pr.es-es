---
description: En el caso de varios GUID de tipo de medios MPEG-2, el DDK de Windows define nombres que difieren de los nombres que se usan en DirectShow. En la tabla siguiente se muestran los nombres de DirectShow (definidos en Ksuuids. h) y los nombres de modo kernel correspondientes (definidos en Ksmedia. h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Tipos de medios de kernel MPEG-2 (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690674"
---
# <a name="mpeg-2-kernel-media-types"></a>Tipos de medios de kernel MPEG-2

En el caso de varios GUID de tipo de medios MPEG-2, el DDK de Windows define nombres que difieren de los nombres que se usan en DirectShow. En la tabla siguiente se muestran los nombres de DirectShow (definidos en Ksuuids. h) y los nombres de modo kernel correspondientes (definidos en Ksmedia. h).



| Nombre en Ksuuids. h              | Nombre en Ksmedia. h                          |
|--------------------------------|--------------------------------------------|
| DAR formato a \_ WaveFormatEx           | KSDATAFORMAT ( \_ especificador) \_ WAVEFORMATEX      |
| FORMATO \_ MPEG2Video             | Vídeo de paraKSDATAFORMAT \_ Specifier \_ MPEG2 \_      |
| MEDIASUBTYPE \_ ATSC \_ si         | subtipo de KSDATAFORMAT de \_ \_ ATSC \_ si            |
| MEDIASUBTYPE \_ Dolby \_ AC3       | KSDATAFORMAT \_ SubType \_ AC3 \_ audio          |
| MEDIASUBTYPE \_ DVB \_ si          | subtipo de KSDATAFORMAT \_ \_ DVB \_ si             |
| MEDIASUBTYPE \_ DVD \_ LPCM \_ audio | KSDATAFORMAT \_ SubType \_ LPCM \_ audio         |
| \_Audio MPEG2 de MEDIASUBTYPE \_     | KSDATAFORMAT \_ SubType \_ MPEG2 \_ audio        |
| \_Programa MPEG2 de MEDIASUBTYPE \_   | \_Tipo de KSDATAFORMAT estático \_ \_ \_ programa MPEG2 |
| \_Transporte MPEG2 de MEDIASUBTYPE \_ | KSDATAFORMAT \_ tipo \_ de \_ transporte MPEG2       |
| \_Vídeo MPEG2 de MEDIASUBTYPE \_     | Vídeo de KSDATAFORMAT \_ SubType \_ MPEG2 \_        |
| \_Secciones de MPEG2 de MEDIATYPE \_     | KSDATAFORMAT \_ tipos de texto \_ MPEG2 \_        |
| Audio de MEDIATYPE \_               | KSDATAFORMAT \_ tipo \_ audio                  |
| \_PES MPEG2 \_ PE          | KSDATAFORMAT \_ Type \_ MPEG2 \_ PES             |
| Vídeo de MEDIATYPE \_               | \_vídeo de tipo KSDATAFORMAT \_                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




