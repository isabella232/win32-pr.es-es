---
description: Señala un evento desde un receptor de medios que representa los datos multimedia.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9fc70505033b9d88cd9593d2efa9f3c591f69f5e25bd968b06686c4c6ac911d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061867"
---
# <a name="merendererevent-event"></a>Evento MERendererEvent

Señala un evento desde un receptor de medios que representa los datos multimedia.

El [representador de vídeo](enhanced-video-renderer.md) mejorado (EVR) envía este evento cuando recibe un evento de usuario del presentador de EVR.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE           | Descripción                        |
|-------------------|------------------------------------|
| VT \_ I4<br/> | Código de evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Si el presentador llama al método **IMediaEventSink::Notify** del EVR con un código de evento en el intervalo EC USER o \_ superior, el EVR envía este evento. Los datos de evento son el código de evento que se pasó al **método Notify.**

Los parámetros de evento originales *(EventParam1* y *EventParam2* en el método **IMediaEventSink::Notify)** se omiten, por lo que el presentador debe establecer estos valores en **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




