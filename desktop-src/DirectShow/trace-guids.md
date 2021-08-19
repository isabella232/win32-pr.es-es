---
description: Los siguientes GUID se usan para el seguimiento de eventos en DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID de seguimiento (PerfStruct.h)
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
ms.openlocfilehash: 89465996c57e1f1f97f2c101c8dfee99a00219f992a4e68681f76465d21bef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951554"
---
# <a name="trace-guids"></a>GUID de seguimiento

Los siguientes GUID se usan para el seguimiento de eventos en DirectShow.



| GUID                                                                                                                                                                   | Descripción                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ AUDIOBREAK**</dt> </dl>    | Evento de interrupción de audio. Los eventos de este tipo usan la [**estructura PERFINFO \_ DSHOW \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) para los datos de eventos.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**GUID \_ DSHOW \_ CTL**</dt> </dl>      | DirectShow proveedor de eventos.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ STREAMTRACE**</dt> </dl> | Evento de streaming general. Los eventos de este tipo usan la [**estructura PERFINFO \_ DSHOW \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) para los datos de eventos.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ VIDEOREND**</dt> </dl>       | Evento de representación de vídeo. Los eventos de este tipo usan la [**estructura \_ PERFINFO DSHOW \_ AVREND**](perfinfo-dshow-avrend.md) para los datos de eventos.<br/>             |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PerfStruct.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Seguimiento de eventos en DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




