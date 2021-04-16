---
description: Los siguientes GUID se usan para el seguimiento de eventos en DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID de seguimiento (PerfStruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671433"
---
# <a name="trace-guids"></a>GUID de seguimiento

Los siguientes GUID se usan para el seguimiento de eventos en DirectShow.



| GUID                                                                                                                                                                   | Descripción                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ AUDIOBREAK**</dt> </dl>    | Evento de interrupción de audio. Los eventos de este tipo usan la estructura [**PERFINFO de \_ DSHOW \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) para los datos de evento.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**CTL del GUID de \_ DSHOW \_**</dt> </dl>      | Proveedor de eventos de DirectShow.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ STREAMTRACE**</dt> </dl> | Evento general de streaming. Los eventos de este tipo usan la estructura [**PERFINFO de \_ DSHOW \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) para los datos de evento.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ VIDEOREND**</dt> </dl>       | Evento de representación de vídeo. Los eventos de este tipo usan la estructura [**PERFINFO de \_ DSHOW \_ AVREND**](perfinfo-dshow-avrend.md) para los datos de evento.<br/>             |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PerfStruct. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Seguimiento de eventos en DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




